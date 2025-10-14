---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 732e625131723d38f839aa5651cccd76122fe66b
workflow-type: tm+mt
source-wordcount: '1249'
ht-degree: 84%

---

# Aktuelle Adobe Analytics-Versionshinweise (Version Oktober 2025)

**Letztes Update**: Mittwoch, 14. Oktober 2025

Diese Versionshinweise decken den Veröffentlichungszeitraum von Oktober bis Anfang November 2025 ab. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion | Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Filterkriterien enthalten in Linienvisualisierungen und Sparklines** | Alle Suchfilterkriterien, die Sie auf einen Freiformtabellen-Filter anwenden, sind jetzt immer in Sparklines enthalten. Darüber hinaus können Sie Suchfilterkriterien in jede verbundene Linienvisualisierung einbeziehen.<p>Sie können Linienvisualisierungen so konfigurieren, dass Suchfilterkriterien einbezogen werden, indem Sie die Wortgrafik in der Metrik-Spaltenüberschrift der verbundenen Tabelle auswählen.</p><p>Zuvor waren Suchfilterkriterien nicht in Sparklines oder Visualisierungen von verbundenen Zeilen enthalten.</p><p>(Link zur Dokumentation folgt.) | | &#x200B;15. Oktober 2025 |
| **Analysieren von KI-Traffic mit einem neuen Dimensionselement vom Referrer-Typ** | Ein neues Dimensionselement vom Referrer-Typ wird zur Verfügung stehen, um den von KI-Tools stammenden Traffic zu analysieren. <p>Dieses neue Dimensionselement vom Referrer-Typ namens Conversational AI-Tools gruppiert verweisende Domains der wichtigsten KI-Tools und ermöglicht es Ihnen, Trends für die Gruppe als Ganzes zu betrachten. Die anfängliche Liste der verweisenden Domains in dieser neuen Kategorie umfasst (ist jedoch nicht auf beschränkt auf):</p><ul><li>chatgpt.com</li><li>claude.ai</li><li>m365.cloud.microsoft</li><li>grok.com</li><li>gemini.google.com</li><li>perplexity.ai</li></ul><p>Das neue Dimensionselement ist in allen Adobe Analytics-bezogenen Tools verfügbar, einschließlich Analysis Workspace, Report Builder, Data Warehouse, Daten-Feeds usw.</p><p>Beachten Sie bei der Verwendung dieses neuen Dimensionselements Folgendes:</p><ul><li>Es ist nicht immer möglich, den Referrer-Traffic, der aus den Ergebnissen im „KI-Modus” einer Suchmaschine stammt, von dem Traffic zu unterscheiden, der aus Klicks auf herkömmliche Suchergebnisse stammt.</li><li>Das neue Dimensionselement der Conversational AI-Tools konzentriert sich auf die wichtigsten Anbieter mit dem meisten Traffic. Ein neuer Trend zeigt eine steigende Anzahl von imitierenden Sites mit Domains, die denen großer Anbieter von KI-Tools ähneln. Das liegt wahrscheinlich daran, dass einzelne Personen oder Gruppen sehr einfach eigene KI-Tools erstellen und im Internet hosten können. Da sich dieser Bereich schnell weiterentwickelt, wenden Sie sich an das Adobe-Support-Team, wenn Ihnen auffällt, dass eine beliebte Website nicht enthalten ist.</li><li>Die Dimension vom Referrer-Typ, einschließlich des neuen Dimensionselements „Conversational AI-Tools“, ist nur bei Daten verfügbar, die von Adobe Analytics verarbeitet werden. </li></ul><p>(Link zur Dokumentation folgt.)</p> |   | &#x200B;15. Oktober 2025 |
| **Streaming-Mediendienste: Unterstützung von Zeitplandaten** | Sie können jetzt Zeitplandaten von früheren Live-Inhalten von Streaming-Medien hochladen, um die Zuschauerzahlen einfacher und genauer zu verfolgen.<p>Im Folgenden finden Sie Beispiele für Live-Inhalte, die mit dem Upload von Zeitplandaten unterstützt werden:</p><ul><li>FAST-Plattformen (Free Ad Supported TV)</li><li>Lokale Datenströme</li><li>Live-Sportübertragungen</li></ul><p>Durch das Hochladen von Zeitplandaten können Sie die Zuschauerzahlen für einzelne Programme verfolgen, die in dem von Ihnen in der Upload-Datei angegebenen Zeitraum gelaufen sind. Sie können sogar Zuschauerzahlen für bestimmte Themen oder Programmsegmente erfassen.</p><p>Diese Funktionen sind unabhängig davon verfügbar, wie Sie die Erfassung von Streaming-Medien implementiert haben.</p><p>Zuvor war es bei der Analyse von Live-Inhalten schwierig, eine bestimmte Sitzung genau mit bestimmten Programmen zu verknüpfen, und es war nicht möglich, eine bestimmte Sitzung mit einzelnen Themen oder Programmsegmenten zu verknüpfen.</p><p>(Link zur Dokumentation folgt.)<!--For more information, see [Upload schedule data to track live content](https://experienceleague.adobe.com/en/docs/media-analytics/using/media-use-cases/track-schedule-data)--></p> |  | &#x200B;29. Oktober 2025 |
| **Streaming-Mediendienste: XDM-Felder zum Erfassen von Streaming-Mediendaten in Adobe Experience Platform wurden aktualisiert** | Beim Erfassen von Streaming-Mediendaten in Adobe Experience Platform sollten die XDM-Feldpfade unter der Überschrift „XDM-Feldpfad“ in der Dokumentation zu den Streaming-Medienparametern nicht mehr verwendet werden. Stattdessen müssen Kundinnen und Kunden, die den Analytics-Quell-Connector vor dem 9. Mai 2025 implementiert haben, zum Erfassen von Streaming-Mediendaten in Platform ihre vorhandenen Konfigurationen in die mediaReporting-Feldpfade migrieren, wie unter der Überschrift „XDM-Feldpfad für Berichterstellung“ der Dokumentation zu Streaming-Medienparametern gezeigt.<p> Diese Feldpfade befinden sich auf den folgenden Seiten und sind als „veraltet“ gekennzeichnet: [Audio- und Videoparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/audio-video-parameters), [Anzeigenparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/ad-parameters), [Kapitelparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/chapter-parameters), [Player-Statusparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/player-state-parameters) und [Qualitätsparameter](https://experienceleague.adobe.com/de/docs/media-analytics/using/implementation/variables/quality-parameters). (Bei Kundinnen und Kunden, die den Analytics-Quell-Connector nach dem 9. Mai 2025 implementiert haben und bereits nur XDM-Pfade für mediaReporting verwenden, ist keine Aktion erforderlich.)</p><p>Die Datenaufnahme über die veralteten XDM-Feldpfade wird noch bis Ende Oktober 2025 fortgesetzt. Danach werden die veralteten Felder vollständig entfernt und nicht mehr in der Schema-Benutzeroberfläche von Adobe Experience Platform angezeigt. Daten werden nur mithilfe der mediaReporting-Feldpfade gesendet.</p><p>Weitere Informationen finden Sie unter [Migrieren einer Analytics-Quell-Connector-Implementierung zu aktualisierten XDM-Streaming-Medien-Feldern](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-use-cases/xdm-updates/updated-xdm-fields).</p><p>Wenden Sie sich an Ihren Adobe Consulting-Dienst oder Ihr Konto-Team, um Unterstützung bei der Migration zu erhalten.  </p> |  | Oktober 2025 |
| Erstellung von Report Suites mit der **Adobe Analytics 2.0-API** | Erstellen von Report Suites in Adobe Analytics mit den 2.0-APIs. Die neue POST-Methode ersetzt die Erstellung der Report Suite 1.4-API in Vorbereitung auf die bevorstehende Einstellung der APIs 1.4. | | &#x200B;15. Oktober 2025 |

## Fehlerbehebungen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-399209, AN-397146, AN-394992, AN-390795
**Klassifizierungen**: AN-400583, AN-399205, AN-398580, AN-398257, AN-395921, AN-394973
**Datenerfassung**:
**Daten-Feeds und Data Warehouse**: AN-400938, AN-399075, AN-398924, AN-398573, AN-396574, AN-393946
**Datenschutz**:
**Report Builder**: AN-401127, AN-400618, AN-392971, AN-391692
**Reporting**:
**Terminierte Berichte**:
**Segmentvergleich**:
**Sonstige**: AN-396084


## Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Vorgängerversion von Report Builder** | 18. Juni 2025 | Die Vorgängerversion des Report Builder-Add-ins wird im Juni 2026 eingestellt. Alle Benutzenden sollten mit dem Upgrade ihrer Arbeitsmappen der Vorgängerversion auf den [neuen Report Builder](/help/analyze/report-builder/rb-overview.md) beginnen. Der neue Report Builder ist sowohl für Adobe Analytics- als auch für Customer Journey Analytics-Kundschaft verfügbar. Er bietet [nahezu die gleichen Funktionen](/help/analyze/report-builder/convert-workbooks.md#unsupported) sowie viele neue, praktische Funktionen und Verbesserungen der Benutzeroberfläche. Um den Upgrade-Prozess zu vereinfachen, enthält der neue Report Builder eine Funktion zur einfachen Arbeitsmappenkonvertierung. Der neue Report Builder ist nur als Add-in über den Microsoft Store verfügbar. Viele Organisationen benötigen einen internen Genehmigungsprozess, bevor das Add-in Benutzenden zur Verfügung gestellt werden kann. Planen Sie Zeit für diesen Prozess ein und arbeiten Sie jetzt mit Ihrer Organisation, um vor dem Ende der Nutzungsdauer genügend Zeit für ein Upgrade Ihrer Arbeitsmappen zu haben. |
| **Zugriff über Legacy-Domains oder Legacy-SSO** | 10. April 2025 | Adobe plant, die Art und Weise zu aktualisieren, wie Benutzende auf Adobe Analytics zugreifen, um die Sicherheit zu erhöhen und das Anmeldeerlebnis zu optimieren. Im Rahmen dieser Bemühungen wird der Zugriff über Legacy-Domains oder Legacy-SSO, einschließlich `my.omniture.com`, am **2. Januar 2026** dauerhaft eingestellt. Nach diesem Datum funktionieren die alten Anmeldedaten bzw. die alte SSO-Methode nicht mehr. Alle Benutzenden müssen sich über `experience.adobe.com` mit ihren Adobe Experience Cloud-IDs anmelden. Wenn Sie Hilfe im Zusammenhang mit Ihrer Experience Cloud-ID benötigen, wenden Sie sich an das Adobe Analytics-Admin-Team Ihrer Organisation oder an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/contact.html). |
| **Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics </li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/).</p> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).


## Verwandte Ressourcen

* [Frühere Versionshinweise für 2025](/help/release-notes/2025.md)
* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
* [Versionshinweise zu Streaming-Mediendiensten](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=de)
* Die neuesten Versions-Updates für [Adobe Experience Cloud-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
