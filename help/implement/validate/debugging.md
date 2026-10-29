---
title: Analytics-Datenerfassung debuggen
description: Vergewissern Sie sich, dass Adobe Analytics die erwarteten Daten von AppMeasurement, der Analytics-Erweiterung, Web SDK, Mobile SDK und der Data Insertion-API erhält.
keywords: Debugging, Validierung, Package Analyzer, Paketmonitor, /b/ss/, Edge Trace, Assurance, hitDebugger, Report Suite
feature: Implementation Basics
role: Admin, Developer
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: e992d880-33bc-4949-a648-aa7d410276cd
    internal-label: Validation
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 049b9b7447c7f91d67eb58fc781898b685bd9d91
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 2%
---
# Analytics-Datenerfassung debuggen

In diesem Artikel wird erläutert, was zu überprüfen ist, wenn Sie Daten debuggen, die an Adobe Analytics gesendet werden. Suchen Sie die Implementierungsmethode in der folgenden Tabelle und befolgen Sie den entsprechenden Abschnitt. Wenn Sie unerwartete Berichtsdaten untersuchen, beginnen Sie mit [Anfragen mit Berichten vergleichen](#reports).

Schritte und Tools, die für alle Adobe-Datenerfassungen gelten, z. B. die Erfassung von Netzwerkanfragen, die Aktivierung der Debugging-Protokollierung und die Untersuchung abgebrochener Anfragen, finden Sie unter [Debugging und Fehlerbehebung bei der Datenerfassung](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/overview).

| Implementierungsmethode | Anzeigen der von Analytics empfangenen Daten | Leitlinien |
| --- | --- | --- |
| AppMeasurement oder die Analytics-Tag-Erweiterung | Anfragen des Browsers direkt an die Datenerfassungs-Server von Analytics | [AppMeasurement](#appmeasurement) |
| Web SDK | Edge Trace, nachdem Edge Network Ihr Ereignis in einen Analytics-Treffer konvertiert hat | [Web SDK](#web-sdk) |
| Mobile SDK | Die Analytics-Ereignisansicht in Assurance. Wenn Sie die Edge Network- oder Edge Bridge-Erweiterung verwenden, aktivieren Sie **[!UICONTROL Analytics Edge View]**. | [Adobe Analytics-Ereignisansicht in Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/adobe-analytics) |
| Dateneinfüge-API | Ausgehende Anfragen Ihres Servers und deren Antworten | [Fehlerbehebung bei Dateneinfüge-API-Anfragen](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/troubleshooting) |

## AppMeasurement und die Analytics-Erweiterung {#appmeasurement}

### Anfrage suchen {#appmeasurement-find}

[Erfassen von Netzwerkanfragen](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/inspect-requests#web) und Filtern nach `/b/ss/`. Tag-Debugger wie Adobe Experience Platform Debugger identifizieren und decodieren diese Anfragen für Sie.

Wenn keine `/b/ss/`-Anfrage angezeigt wird:

* Überprüfen Sie die Browser-Konsole auf JavaScript-Fehler.
* Wenn Sie die Analytics-Tag-Erweiterung verwenden, bestätigen Sie, dass sich der Tag-Einbettungs-Code im `<head>` der Seite befindet und dass Ihre Bibliothek in der Umgebung veröffentlicht wird, die Sie testen. [Tag-Debugging-Modus](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/logging) gibt an, ob die Regel, die den Treffer sendet, ausgelöst wurde.
* Wenn Sie AppMeasurement selbst hosten, öffnen Sie die URL der Bibliothek direkt, um zu bestätigen, dass die Datei geladen wird und Code enthält.
* Deaktivieren Sie Browser-Erweiterungen wie Anzeigenblocker, die das Senden von Anfragen verhindern können.
* Der Debugger erkennt keine Anforderungen, die innerhalb eines IFrame gesendet werden. Verwenden Sie stattdessen Browser-Entwickler-Tools . Siehe [Verwenden von AppMeasurement mit iFrames](../use-cases/iframe.md).

### Überprüfen, was Analytics erhalten hat {#appmeasurement-contents}

* **Report Suites**: Das Pfadsegment nach `/b/ss/` listet die Report Suite-IDs auf, die den Treffer erhalten. Vergewissern Sie sich, dass es sich um die erwarteten Report Suites handelt, z. B. eine Entwicklungs-Report Suite auf Entwicklungsseiten.
* **Variablen**: Raw-Anfragen verwenden Abfrageparameter-Namen anstelle von Variablennamen. Beispielsweise wird eVar1 als `v1` und prop1 als `c1` angezeigt. Siehe die [Variablenreferenz](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference). Wenn eine Anfrage zu lang ist, sendet AppMeasurement sie mit HTTP-`POST`, sodass Variablen im Anfragetext und nicht in der URL angezeigt werden.
* **Treffertyp**: Anfragen, die von [`tl()`](../vars/functions/tl-method.md) gesendet werden, enthalten den `pe` Parameter und erhöhen nicht die Seitenansichten. Von [`t()`](../vars/functions/t-method.md) gesendete Anfragen enthalten keine `pe`.

Wenn Werte vorhanden, aber falsch sind, finden Sie unter [Fehlerbehebung bei der JavaScript](../js/troubleshooting.md) Informationen zu häufigen Ursachen wie Anführungszeichen, Groß-/Kleinschreibung und Leerzeichen.

### Überprüfen der Antwort {#appmeasurement-response}

Eine `2xx` Antwort bestätigt nur, dass der Datenerfassungs-Server die Anfrage empfangen hat, nicht, dass der Treffer aufgezeichnet wurde. Mit dem standardmäßigen Antworttyp kann eine Anfrage auch dann einen Erfolg zurückgeben, wenn der Treffer verworfen wird. Es wird eine `302` Antwort auf die erste Anfrage eines neuen Besuchers erwartet. Siehe [HTTP-Antwort-](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/troubleshooting#http-response-codes).

AppMeasurement sendet Exitlink-Anfragen und alle Anfragen, wenn [`useBeacon`](../vars/config-vars/usebeacon.md) aktiviert ist, mit `navigator.sendBeacon()`. Entwickler-Tools können diese Anfragen auch dann als abgebrochen kennzeichnen, wenn der Browser sie gesendet hat. Siehe [Abgebrochene Anfragen](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/inspect-requests#aborted-requests).

## Web SDK {#web-sdk}

### Anfrage suchen {#web-sdk-find}

Bei Web SDK sendet der Browser Ereignisse an die Edge Network anstatt direkt an Analytics, sodass keine `/b/ss/`-Anfrage angezeigt wird. [Überprüfen Sie die Edge Network-Anfrage](https://experienceleague.adobe.com/en/docs/experience-platform/collection/debugging/inspect-requests#edge-network-requests) und bestätigen Sie Folgendes:

* Der `configId`-Parameter entspricht einem Datenstrom, für den der [Adobe Analytics-Service](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#analytics) mit den erwarteten Report Suites aktiviert ist.
* Die Payload qualifiziert sich als Seitenansicht oder Link-Ereignis. Analytics ignoriert Payloads, die weder Seitendetails noch einen Web-Interaktionstyp enthalten. Siehe [Edge Network-Ereignistypen in Adobe Analytics](../aep-edge/hit-types.md).

### Überprüfen, was Analytics erhalten hat {#web-sdk-contents}

Starten Sie eine [Edge Trace](https://experienceleague.adobe.com/en/docs/experience-platform/debugger/edge-trace) und reproduzieren Sie die Aktion. Suchen Sie die Zeile, die mit **[!UICONTROL Automatisches Analytics-Mapping]** beginnt, erweitern Sie dann `mappedQueryParams` und die Report Suite-ID darunter.

* **Variablen**: Zugeordnete Werte verwenden dieselben Abfrageparameternamen wie AppMeasurement-Anfragen, manchmal in Kurzform, z. B. `gn` für den Seitennamen und `pl` für Produkte. Siehe [XDM-Objektfeldzuordnung](../aep-edge/xdm-var-mapping.md) und [Datenobjektfeldzuordnung](../aep-edge/data-var-mapping.md).
* **Kontextdaten**: XDM-Felder, die keiner Analytics-Variablen zugeordnet sind, werden als Kontextdaten mit dem Präfix `c.a.x.` angezeigt. Verwenden Sie [Verarbeitungsregeln](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md) um sie Variablen zuzuweisen.
* **Report Suites**: Wenn Sie Report Suite-Überschreibungen verwenden, zeigt die Zeile mit der Datenstromkonfiguration in Edge Trace die von Edge Network verwendeten Report Suites an.

### Scheckverarbeitung {#web-sdk-processing}

Suchen Sie in der Assurance-Sitzung, die in Edge Trace geöffnet wird, nach Ereignissen `hitdebugger`. Diese Ereignisse verwenden die `com.adobe.analytics.hitdebugger` des Anbieters, und ihre Payloads zeigen Werte nach der Analytics-Verarbeitung an, z. B. die Experience Cloud-ID (`mcvisId`) und die `pageName`.

Eine Anleitung finden Sie unter [&#x200B; von Adobe Analytics mit Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/platform-learn/implement-web-sdk/applications-setup/setup-analytics).

## Anforderungen mit Berichten vergleichen {#reports}

Ein Treffer, der Analytics erreicht, wird nicht sofort in Berichten angezeigt. Die gemeldeten Werte können von den Werten in der Anfrage abweichen:

* **Latenz**: Vollständige Daten werden in der Regel etwa zwei Stunden nach der Erfassung in Berichten angezeigt. Einige Daten, z. B. Treffer mit Zeitstempel, können länger dauern. Siehe [Datenverfügbarkeit und -latenz](/help/technotes/latency.md).
* **Verarbeitung**: Verarbeitungsregeln, VISTA-Regeln, Bot-Regeln und andere Verarbeitungsschritte können Werte nach der Erfassung ändern oder ausschließen. Siehe [Verarbeitungsreihenfolge für Daten in Adobe Analytics](/help/technotes/processing-order.md). Nachverarbeitete Daten aus Assurance zeigen das Ergebnis der Verarbeitung für einen einzelnen Treffer.
* **Report Suite**: Vergewissern Sie sich, dass Sie dieselbe Report Suite anzeigen, auf die die Anfrage oder der Datenstrom abzielte.
* **Unerwartete Werte**: Zeigt eine Dimension unerwartete Spitzen oder Werte an, siehe [Hash-Kollisionen](hash-collisions.md).

Weitere Informationen zu Traffic-Änderungen finden Sie [Fehlerbehebung bei Datenspitzen und -abfällen](/help/technotes/event/spikes-drops.md).
