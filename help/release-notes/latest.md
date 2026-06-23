---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
TQID: 'https://experienceleague.adobe.com/yw30Yij2NBaeuWFqxD4-VH1Hysf8dxOpxHUwsFCYEw8'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85eid: a421fb65-2c82-457a-921c-28c46b697a39
subfeature_v2: id: d89ba969-e026-48bf-927e-e9df2f1e34f3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 6adcad3efbe3c7f38ba8b15f835d700861fd2209
workflow-type: tm+mt
source-wordcount: 573
ht-degree: 90%

---

# Aktuelle Versionshinweise zu Adobe Analytics (Juni 2026)

**Letzte Aktualisierung**: 22. Juni 2026

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom Juni 2026. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion und Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ---- |
| **Journey-Arbeitsfläche in Adobe Analytics** <br/>Die Journey-Arbeitsfläche ist eine Visualisierung in Analysis Workspace, mit der Sie umfassendere Erkenntnisse zu einer definierten Benutzer-Journey gewinnen können, indem Sie analysieren, wie Benutzende eine Journey durchlaufen oder aus dieser aussteigen. Damit können Sie ein flexibles Diagramm von Knoten und Pfeilen erstellen, die eine beliebige Kombination von Ereignissen, Dimensionselementen und Segmenten darstellen, die in der Journey enthalten sind. Daten werden aktualisiert, wenn Sie Knoten auf die Arbeitsfläche ziehen oder Ereignisse und Bedingungen einer Journey neu anordnen.<p>Die Journey-Arbeitsfläche war bisher nur für Customer Journey Analytics verfügbar.</p><p>Weitere Informationen zur Journey-Arbeitsfläche finden Sie unter [Journey-Arbeitsfläche – Überblick](/help/analyze/analysis-workspace/visualizations/journey-canvas/journey-canvas.md). </p><p>Weitere Informationen zum Erstellen einer Journey-Arbeitsflächen-Visualisierung in Adobe Analytics finden Sie unter [Konfigurieren einer Journey-Arbeitsfläche](/help/analyze/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md).</p> | 18. Mai 2026 | 5. Juni 2026 |

### Fehlerbehebungen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-452009, AN-450375, AN-449870, AN-450814, AN-450698
**Klassifizierungen**:
**Daten-Feeds und Data Warehouse**:
**Migration**:
**Exporte**:
**Report Builder**: AN-440912
**Reporting**: AN-423516
**Report Suites**: AN-455684
**Geplante Berichte**:
**Segmentierung**:
**Sonstige**:


### Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Vorgängerversion von Report Builder** | 18. Juni 2025 | Die Vorgängerversion des Report Builder-Add-ins wird im Juni 2026 eingestellt. Alle Benutzenden sollten mit dem Upgrade ihrer Arbeitsmappen der Vorgängerversion auf den [neuen Report Builder](/help/analyze/report-builder/rb-overview.md) beginnen. Der neue Report Builder ist sowohl für Adobe Analytics- als auch für Customer Journey Analytics-Kundschaft verfügbar. Er bietet [nahezu die gleichen Funktionen](/help/analyze/report-builder/convert-workbooks.md#unsupported) sowie viele neue, praktische Funktionen und Verbesserungen der Benutzeroberfläche. Um den Upgrade-Prozess zu vereinfachen, enthält der neue Report Builder eine Funktion zur einfachen Arbeitsmappenkonvertierung. Der neue Report Builder ist nur als Add-in über den Microsoft Store verfügbar. Viele Organisationen benötigen einen internen Genehmigungsprozess, bevor das Add-in Benutzenden zur Verfügung gestellt werden kann. Planen Sie Zeit für diesen Prozess ein und arbeiten Sie jetzt mit Ihrer Organisation, um vor dem Ende der Nutzungsdauer genügend Zeit für ein Upgrade Ihrer Arbeitsmappen zu haben. |
| **Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics</li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/).</p> |


## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).


>[!MORELIKETHIS]
>
>* [Frühere Versionshinweise für 2026](/help/release-notes/2026.md)
>* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
>* [Versionshinweise zu Streaming-Mediendiensten](https://experienceleague.adobe.com/de/docs/media-analytics/using/release-notes/release-notes)
>* Die neuesten Versions-Updates für [Adobe CX Enterprise-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)
