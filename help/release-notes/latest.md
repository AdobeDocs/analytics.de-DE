---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
TQID: 'https://experienceleague.adobe.com/yw30Yij2NBaeuWFqxD4-VH1Hysf8dxOpxHUwsFCYEw8'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
  - id: a421fb65-2c82-457a-921c-28c46b697a39
subfeature_v2:
  - id: d89ba969-e026-48bf-927e-e9df2f1e34f3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 6d07329547684e8bee712628a53092eb34e0141a
workflow-type: tm+mt
source-wordcount: 1305
ht-degree: 40%

---

# Aktuelle Versionshinweise zu Adobe Analytics (September 2026)

**Letzte Aktualisierung**: 11. September 2026

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom September 2026. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion und Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ---- |
| **Segmente auf den Berichtsdatumsbereich beschränken**<br/> Daten in einem Workspace-Bericht können über den Berichtsdatumsbereich hinaus erweitert werden, wenn ein Segment Datumsbereichskomponenten enthält.<p>Es ist jetzt eine neue Option verfügbar, mit der Sie die Ergebnisse auf den Datumsbereich des Berichts beschränken können, unabhängig von etwaigen im Segment enthaltenen Datumskomponenten.</p><p>Diese Option ist beim Erstellen oder Ändern eines Segments verfügbar, dessen Container der obersten Ebene „Besucher“ ist.</p><p>Weitere Informationen finden Sie unter [Segmente erstellen](/help/components/segmentation/segmentation-workflow/seg-build.md#components).</p> | &#x200B;26. August 2026 | &#x200B;9. September 2026 |
| **Aktualisierungen der Bot**<br/> Erkennung: Bei Verwendung der Edge-Datenerfassung mit der Web-SDK sind die folgenden Aktualisierungen der Bot-Erkennung verfügbar:<ul><li>Sie können jetzt Regeln für die Bot-Erkennung erstellen, um Ausnahmen im Traffic zu identifizieren, die andernfalls als von Bots generiert behandelt würden. Bestehende und zukünftige Regeln werden weiterhin standardmäßig darauf festgelegt, übereinstimmenden Traffic als Bot-generiert zu markieren.</li><li>Benutzerdefinierte Bot-Regeln werden jetzt vor den IAB-Bot-Erkennungsregeln ausgeführt. Diese Änderung wirkt sich nicht auf die Bot-Scores aus, aber die Namen der Bot-Regeln, die mit einem Ereignis verknüpft sind, können sich ändern.</li></ul><p>Hinweis: Dieses Update gilt nur für Edge-Datenerfassungsimplementierungen, die die Web-SDK verwenden. Dies gilt nicht für ältere Bibliotheken wie AppMeasurement.</p><p>(Link zur Dokumentation folgt.)</p> | | Anfang September 2026 |
| **CX Enterprise Coworker: Analysieren von Adobe Analytics-Daten im**-Chat: Der <br/>Adobe CX Enterprise Coworker-Chat kann jetzt erweiterte Datenanalysen durchführen, die zuvor nur in Analysis Workspace möglich waren. Coworker Chat greift auf Daten aus Ihren Adobe Analytics-Report Suites zu, sodass Sie diese Daten untersuchen und Antworten auf Anfragen in natürlicher Sprache erhalten können.<p>(Link zur Dokumentation folgt.)</p> | | &#x200B;25. September 2026 |
| **CX Enterprise Coworker: Fähigkeit zur Ursachenanalyse** Der <br/>Adobe CX Enterprise Coworker-Chat kann jetzt eine Ursachenanalyse durchführen und erklären, warum sich eine Metrik geändert hat, nicht nur, was sich geändert hat. Im Coworker Chat wird das Datum identifiziert, an dem eine Verschiebung stattgefunden hat, und die Daten vor und nach der Verschiebung verglichen. Anschließend wird die Änderung anhand der zugrunde liegenden Dimensionen und der Größe aufgeschlüsselt, angezeigt sowohl als Prozentsatz als auch als absoluter Wert. Wenn keine bedeutsame Änderung festgestellt wird, informiert der Coworker Chat Sie, anstatt über eine Ursache zu spekulieren.<p>(Link zur Dokumentation folgt.)</p> | | &#x200B;2. Oktober 2026 |
| **CX Enterprise Coworker: Öffnen Sie eine Visualisierung in Analysis Workspace** <br/>Starten Sie eine Datenanalyse im Kollegen-Chat und öffnen Sie dann die Analyse als eine Visualisierung direkt in Analysis Workspace, um mit dem Erstellen, Verfeinern und Entdecken fortzufahren.</p><p>(Link zur Dokumentation folgt.)</p> | | &#x200B;2. Oktober 2026 |
| **Aktualisierungen der Klassifizierungssätze-**<br/>: Die Dokumentation zur Klassifizierungssätze-API enthält jetzt aktualisierte Endpunkt- und Parameterinformationen zum Konfigurieren von Klassifizierungssätze-API-Anfragen.<p>Weitere Informationen finden Sie im [Classifications-Endpunkthandbuch](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/).</p> | &#x200B;5. September 2026 | &#x200B;30. September 2026 |
| **Anleitung zur Kodierung von Datumselementen in den 2.0-API**<br/> BerichtshandbüchernDie Datumstrends-Berichtshandbücher zur Adobe Analytics 2.0-API enthalten jetzt neue Abschnitte, in denen erläutert wird, wie `itemId` und -werte kodiert werden. Dies kann Ihnen bei der Konfiguration und Migration zu 2.0-API-Services aus den jetzt nicht mehr unterstützten 1.4-APIs helfen.<p>Weitere Informationen finden Sie im [KPI-Berichtshandbuch](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/kpi) und im [erweiterten Berichtshandbuch](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/advanced).</p> | &#x200B;5. September 2026 | &#x200B;30. September 2026 |

### Fehlerbehebungen in Adobe Analytics

**Activity Map**: AN-488579, AN-487247, AN-491828
**Analysis Workspace**: AN-487374, AN-487119, AN-468907, AN-468810, AN-468363, AN-468096, AN-467414, AN-466986, AN-466982, AN-465073, AN-463571, AN-462373, AN-492801, AN-488821, AN-488452, AN-486517, AN-478930, AN-468325
**CLASSIFICATIONS**: AN-490825, AN-490802, AN-490549, AN-490472, AN-487782, AN-487286, AN-486531, AN-478859, AN-469929, AN-469033, AN-468592, AN-467115, AN-468944, AN-465636, AN-468827, AN-465616, AN-468326, AN-AN-466995, AN-465380, AN-AN-AN, AN-AN, AN-AN-464911, AN-AN-464338, AN-463677 462729 462577 461040 459316 490072 487100
**Daten-Feeds und Data Warehouse**: AN-487624, AN-487287, AN-479923, AN-479166, AN-479109, AN-468483, AN-493406, AN-492167, AN-333098
**Migration**:
**Exporte**: AN-467131, AN-469034, AN-447252
**Report Builder**: AN-487486, AN-478944, AN-470036, AN-468589, AN-468436, AN-456747, AN-456700, AN-442695, AN-492330, AN-490564, AN-468293, AN-460921
**Reporting**: AN-468621, AN-465383, AN-463924
**Report Suites**: AN-468484, AN-468460, AN-465385, AN-463216
**Terminierte Berichte**: AN-479157
**Segmentierung**: AN-486561, AN-278260
**Sonstige**: AN-488549, AN-467426, AN-465265, AN-464645, AN-459714, AN-459323, AN-454514, AN-487288, AN-470023, AN-469601, AN-320799, AN-316708, AN-309317, AN-266652

### Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Vorgängerversion von Report Builder** | 18. Juni 2025 | Die Vorgängerversion des Report Builder-Add-ins wird im Juni 2026 eingestellt. Alle Benutzenden sollten mit dem Upgrade ihrer Arbeitsmappen der Vorgängerversion auf den [neuen Report Builder](/help/analyze/report-builder/rb-overview.md) beginnen. Der neue Report Builder ist sowohl für Adobe Analytics- als auch für Customer Journey Analytics-Kundschaft verfügbar. Er bietet [nahezu die gleichen Funktionen](/help/analyze/report-builder/convert-workbooks.md#unsupported) sowie viele neue, praktische Funktionen und Verbesserungen der Benutzeroberfläche. Um den Upgrade-Prozess zu vereinfachen, enthält der neue Report Builder eine Funktion zur einfachen Arbeitsmappenkonvertierung. Der neue Report Builder ist nur als Add-in über den Microsoft Store verfügbar. Viele Organisationen benötigen einen internen Genehmigungsprozess, bevor das Add-in Benutzenden zur Verfügung gestellt werden kann. Planen Sie Zeit für diesen Prozess ein und arbeiten Sie jetzt mit Ihrer Organisation, um vor dem Ende der Nutzungsdauer genügend Zeit für ein Upgrade Ihrer Arbeitsmappen zu haben. |
| **Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Am **31. August** haben die folgenden Analytics Legacy-API-Services ihr Ende erreicht und wurden eingestellt, und alle Integrationen, die mit diesen Services erstellt wurden, funktionieren nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics</li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/).</p> |

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).

## Zurückgestellte Funktionen

| Funktion und Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| -----------|-----------|-----------|
| **Streaming-Mediendienste: Unterstützung von Zeitplandaten** <br/>Sie können jetzt Zeitplandaten von früheren Live-Inhalten von Streaming-Medien hochladen, um Zuschauerzahlen einfacher und genauer zu verfolgen.<p>Im Folgenden finden Sie Beispiele für Live-Inhalte, die mit dem Upload von Zeitplandaten unterstützt werden:</p><ul><li>FAST-Plattformen (Free Ad Supported TV)</li><li>Lokale Datenströme</li><li>Live-Sportübertragungen</li></ul><p>Durch das Hochladen von Zeitplandaten können Sie die Zuschauerzahlen für einzelne Programme verfolgen, die in dem von Ihnen in der Upload-Datei angegebenen Zeitraum gelaufen sind. Sie können sogar Zuschauerzahlen für bestimmte Themen oder Programmsegmente erfassen.</p><p>Diese Funktionen sind unabhängig davon verfügbar, wie Sie die Erfassung von Streaming-Medien implementiert haben.</p><p>Zuvor war es bei der Analyse von Live-Inhalten schwierig, eine bestimmte Sitzung genau mit bestimmten Programmen zu verknüpfen, und es war nicht möglich, eine bestimmte Sitzung mit einzelnen Themen oder Programmsegmenten zu verknüpfen.</p><p>Weitere Informationen finden Sie unter [Hochladen von Zeitplandaten zur Verfolgung von Live-Inhalten](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-use-cases/track-schedule-data). | &#x200B;29. Oktober 2025 | TBD<p>(Ursprünglich für den 29. Oktober 2025 geplant)</p> |


>[!MORELIKETHIS]
>
>* [Frühere Versionshinweise für 2026](/help/release-notes/2026.md)
>* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
>* [Versionshinweise zu Streaming-Mediendiensten](https://experienceleague.adobe.com/de/docs/media-analytics/using/release-notes/release-notes)
>* Die neuesten Versions-Updates für [Adobe CX Enterprise-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)

