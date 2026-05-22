---
title: Paket-Analyzer
description: Mit Paket-Analyzern können Sie die Daten einsehen, die von Ihrer Implementierung an die Datenerfassungs-Server von Adobe gesendet werden.
keywords: Paket-Sniffer, http-Status, 200, 302, Charles
feature: Implementation Basics
exl-id: db077293-f72c-4933-8a30-f1e1963f332e
role: Admin, Developer, Leader
TQID: 'https://experienceleague.adobe.com/debgxI3FK1fp1Q02GY1-0H40z-L4G2HSmq11Tog97-Y'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
subfeature_v2: id: e992d880-33bc-4949-a648-aa7d410276cd
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 301a0341e725ca15f1700046528ea5f42969add4
workflow-type: tm+mt
source-wordcount: 679
ht-degree: 67%

---

# Paket-Analyzer

Mit Paket-Analyzern können Sie die Daten einsehen, die von Ihrer Implementierung an die Datenerfassungs-Server von Adobe gesendet werden.

Ähnlich wie beim Adobe CX Enterprise-Debugger zeigt ein Paketmonitor an, welche Datenparameter in einer Bildanforderung übergeben werden. Paketmonitore bieten jedoch zusätzliche Funktionen:

* Anzeige von Bildanforderungen aus benutzerspezifischen Linktracking
* Anzeige von Bildanforderungen mit anderen Implementierungsmethoden als JavaScript (wie z. B. fest programmierte Bildanforderungen oder [!DNL Appmeasurement])

Zur Anzeige von Analytics-Anforderungen müssen Sie ausgehende Anforderungen mit „b/ss“ filtern.

In sehr seltenen Fällen meldet der Debugger eine Bildanforderung, obwohl keine solche Anforderung bei den [!DNL Analytics]-Verarbeitungsserver von Adobe einging. Die Verwendung eines Paketmonitors ist eine hervorragende Möglichkeit, um zu 100 % sicher zu sein, dass eine bestimmte Bildanforderung erfolgreich ausgelöst wird.

Adobe bietet zwar keinen offiziellen Paketmonitor an, im Internet gibt es jedoch eine große Auswahl davon. Im Folgenden finden Sie einige Paket-Monitore, die andere für nützlich befunden haben.

>[!TIP]
>
>Die Liste ist nicht vollständig, sondern dient zur Angabe häufig eingesetzter Monitore.

| Firefox | Internet Explorer | Chrome | Eigenständige Programme |
|---|---|---|---|
| [Observe Point](https://www.observepoint.com/product#plugin) (Tag-Viewer) | [HttpWatch](https://www.httpwatch.com/) | [Observe Point](https://www.observepoint.com/product#plugin) (Tag-Viewer) | [Charles](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.thunderbird.net/en-us/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.telerik.com/fiddler) |
| [Daten manipulieren](https://addons.mozilla.org/de-DE/firefox/addon/tamper-data-for-ff-quantum/) |  | [Firebug Lite](https://chromewebstore.google.com/detail/firebug-lite-for-google-c/ehemiojjcpldeipjhjkepfdaohajpbdo) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE]
>
>Adobe bietet WEDER Support NOCH Fehlerbehebung bei Problemen mit diesen Paketmonitoren an. Wenden Sie sich bei Fragen und Problemen an die Website, von der Sie den Paketmonitor heruntergeladen haben.

## Typische HTTP-Antwortstatus-Codes

Wenn AppMeasurement Daten an die Datenerfassungs-Server der Adobe sendet, antworten die Server mit einem Antwortstatus-Code.

* **200 OK**: Die häufigste Antwort von Datenerfassungs-Servern. Die Bildanforderung wurde erfolgreich empfangen und ein transparentes Bild zurückgegeben.
* **302 FOUND**: Es gibt mehrere mögliche Gründe, warum Sie diese Antwort erhalten:
   * Die erste Bildanforderung eines Besuchers: Eine Umleitung tritt auf, wenn ein Benutzer Ihre Site zum ersten Mal besucht. Diese Umleitung dient zum Abrufen eines Besucher-Cookies. Die Datenerfassung wird dadurch nicht beeinflusst.
   * Integration zwischen Comscore und Adobe: Wenn Ihr Unternehmen eine Comscore-/Analytics-Integration verwendet, ergibt jede Bildanforderung immer eine 302-Antwort.
* **404 NOT FOUND**: Diese Antwort bedeutet, dass die Bildanforderung nicht gefunden wurde und keine Daten an die Datenerfassungs-Server von Adobe gesendet werden. Diese Antwort ist auch möglich, wenn fest programmierte Bildanforderungen nicht korrekt formatiert sind. Wenden Sie sich an die Person oder das Team, die/das Analytics implementiert hat, um dieses Problem zu beheben.

## NS_BINDING_ABORTED in Antwortcodes

Der Grund für diese Nachricht liegt darin, dass die zur Linktracking dienende Bildanforderung es dem Browser erlauben soll, zur nächsten Seite zu wechseln, ohne auf eine Antwort von den Datenerfassungs-Servern von Adobe warten zu müssen.

Die Antwort von Adobe ist einfach nur ein leeres transparentes 1x1-Pixel-Bild, das für den Seiteninhalt irrelevant ist. Wenn Ihnen in Ihrem Paketmonitor eine Meldung von Adobe in der Form **[!UICONTROL 200 OK]** oder **[!UICONTROL NS_BINDING_ABORTED]** angezeigt wird, bedeutet dies, dass die Daten bei den Servern von Adobe angekommen sind. Es ist nicht erforderlich, dass die Seite länger wartet.

Paketmonitore, die als Plug-in integriert sind, zeigen nur selten die volle Antwort an. Sie sehen die Anfrage in der Regel als abgebrochen, da keine vollständige Antwort empfangen wurde. Diese Monitore unterscheiden auch selten zwischen der Frage, ob die Anfrage oder die Antwort abgebrochen wurde. Ein eigenständiger Paketmonitor verfügt in der Regel über detailliertere Meldungen und zeigt den Status genauer an. Beispielsweise erhält ein Benutzer möglicherweise eine Nachricht in „Charles *mit der* „Client hat die Verbindung geschlossen, bevor er die gesamte Antwort erhält“. Das bedeutet, dass die Daten unsere Server erreicht haben, nur der Browser ist auf die nächste Seite gegangen, bevor das 1x1 Pixel empfangen wurde.

Wenn ein externer Paketmonitor meldet, dass die Datenerfassungsanforderung abgebrochen wurde (anstatt der Antwort), stellt dies ein Problem dar. Adobe [!DNL Customer Care] kann Ihnen hier bei der Fehlerbehebung helfen.
