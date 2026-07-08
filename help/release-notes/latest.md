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
source-git-commit: 13d4b15d7069a52f4953a49aa0f1f5b7cb16ae77
workflow-type: tm+mt
source-wordcount: 890
ht-degree: 63%

---

# Aktuelle Versionshinweise zu Adobe Analytics (Juli 2026)

**Letzte Aktualisierung**: 8. Juli 2026

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom Juli 2026. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion und Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ---- |
| **Analyse von Untertreffern** Mit <br/> Analyse von Untertreffern können Sie Produktdaten auf einer Ebene analysieren, die detaillierter ist als die Trefferebene. Anstatt nach ganzen Treffern zu filtern, können Sie innerhalb von Treffern nach einzelnen Produkten segmentieren. <p>Sie können beispielsweise eine Segmentierung für eine bestimmte Produktkategorie durchführen, ohne alle anderen in derselben Bestellung gekauften Produkte einzubeziehen.</p><p>Weitere Informationen finden Sie [Analyse von Untertreffern](/help/components/segmentation/sub-hit.md).</p> | &#x200B;8. Juli | Ende Juli 2026 |
| **Handbuch zu den API-Suchfunktionen** AA 2.0<br/> Verwenden Sie Suchfunktionen, um [eine Untergruppe von Dimensionselementen in Berichten zurückzugeben](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/search-filters).<p>Weitere Informationen finden Sie unter [Suchfunktionen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/search-filters) im Handbuch zum Reports-Endpunkt in Adobe Developer. | | &#x200B;1. Juli 2026 |
| **Automatisieren von wiederkehrenden Berichten mit AA** APIs<br/> Richten Sie automatische, wiederkehrende Adobe Analytics-Berichte für Ihre Daten-Pipeline mit neuen Metriken in einem Zeitplan mit der Report API ein. <p>Weitere Informationen finden Sie im [Endpunkthandbuch Automatisieren wiederkehrender Analytics-Berichte](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/recurring) auf Adobe Developer.</p> | | &#x200B;1. Juli 2026 |
| **Neue Erweiterungsparameter für AA** <br/>Verwenden Sie neue Dimension-API-Erweiterungsparameter, um eVar-Konfigurationsfelder für Zuordnungstypen, Gültigkeiten, Datentypen und Merchandising abzurufen. <p>Weitere Informationen finden Sie im [API-Verweis](https://developer.adobe.com/analytics-apis/docs/2.0/apis/#operation/dimensions_getDimensions) und [Endpunkthandbuch zu Dimensionen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/dimensions/) auf Adobe Developer.</p> | | &#x200B;1. Juli 2026 |

### Fehlerbehebungen in Adobe Analytics

**Activity Map**:
**Analysis Workspace**: AN-449890, AN-457527, AN-451161, AN-459034, AN-458071, AN-458398
**Klassifizierungen**: AN-453318, AN-456739, AN-455828, AN-455270, AN-460272, AN-459367, AN-459239, AN-458418, AN-458417
**Daten-Feeds und Data Warehouse**: AN-456945, AN-460700
**Migration**:
**Exporte**:
**Report Builder**: AN-457533, AN-453683
**Reporting**: AN-447692, AN-451259, AN-455713
**Report Suites**:
**Terminierte Berichte**: AN-450715
**Segmentierung**:
**Sonstige**: AN-453982, AN-455771

### Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Vorgängerversion von Report Builder** | 18. Juni 2025 | Die Vorgängerversion des Report Builder-Add-ins wird im Juni 2026 eingestellt. Alle Benutzenden sollten mit dem Upgrade ihrer Arbeitsmappen der Vorgängerversion auf den [neuen Report Builder](/help/analyze/report-builder/rb-overview.md) beginnen. Der neue Report Builder ist sowohl für Adobe Analytics- als auch für Customer Journey Analytics-Kundschaft verfügbar. Er bietet [nahezu die gleichen Funktionen](/help/analyze/report-builder/convert-workbooks.md#unsupported) sowie viele neue, praktische Funktionen und Verbesserungen der Benutzeroberfläche. Um den Upgrade-Prozess zu vereinfachen, enthält der neue Report Builder eine Funktion zur einfachen Arbeitsmappenkonvertierung. Der neue Report Builder ist nur als Add-in über den Microsoft Store verfügbar. Viele Organisationen benötigen einen internen Genehmigungsprozess, bevor das Add-in Benutzenden zur Verfügung gestellt werden kann. Planen Sie Zeit für diesen Prozess ein und arbeiten Sie jetzt mit Ihrer Organisation, um vor dem Ende der Nutzungsdauer genügend Zeit für ein Upgrade Ihrer Arbeitsmappen zu haben. |
| **Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Ab **12. August 2026** werden die folgenden veralteten Analytics-API-Dienste nicht mehr unterstützt und beendet. Aktuelle Integrationen, die mit diesen Diensten erstellt wurden, funktionieren dann nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics</li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/).</p> |

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).

## Zurückgestellte Funktionen

| Funktion und Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| -----------|-----------|-----------|
| **Streaming-Mediendienste: Unterstützung von Zeitplandaten** <br/>Sie können jetzt Zeitplandaten von früheren Live-Inhalten von Streaming-Medien hochladen, um Zuschauerzahlen einfacher und genauer zu verfolgen.<p>Im Folgenden finden Sie Beispiele für Live-Inhalte, die mit dem Upload von Zeitplandaten unterstützt werden:</p><ul><li>FAST-Plattformen (Free Ad Supported TV)</li><li>Lokale Datenströme</li><li>Live-Sportübertragungen</li></ul><p>Durch das Hochladen von Zeitplandaten können Sie die Zuschauerzahlen für einzelne Programme verfolgen, die in dem von Ihnen in der Upload-Datei angegebenen Zeitraum gelaufen sind. Sie können sogar Zuschauerzahlen für bestimmte Themen oder Programmsegmente erfassen.</p><p>Diese Funktionen sind unabhängig davon verfügbar, wie Sie die Erfassung von Streaming-Medien implementiert haben.</p><p>Zuvor war es bei der Analyse von Live-Inhalten schwierig, eine bestimmte Sitzung genau mit bestimmten Programmen zu verknüpfen, und es war nicht möglich, eine bestimmte Sitzung mit einzelnen Themen oder Programmsegmenten zu verknüpfen.</p><p>Weitere Informationen finden Sie unter [Hochladen von Zeitplandaten zum Nachverfolgen von Live-Inhalten](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-use-cases/track-schedule-data) | &#x200B;29. Oktober 2025 | TBD<p>(Ursprünglich für den 29. Oktober 2025 geplant)</p> |


>[!MORELIKETHIS]
>
>* [Frühere Versionshinweise für 2026](/help/release-notes/2026.md)
>* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
>* [Versionshinweise zu Streaming-Mediendiensten](https://experienceleague.adobe.com/de/docs/media-analytics/using/release-notes/release-notes)
>* Die neuesten Versions-Updates für [Adobe CX Enterprise-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)

