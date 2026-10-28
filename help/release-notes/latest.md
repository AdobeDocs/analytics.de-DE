---
title: Aktuelle Adobe Analytics-Versionshinweise
description: Aktuelle Versionshinweise zu Adobe Analytics anzeigen
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
TQID: 'https://experienceleague.adobe.com/yw30Yij2NBaeuWFqxD4-VH1Hysf8dxOpxHUwsFCYEw8'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
    internal-label: Integrations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: d89ba969-e026-48bf-927e-e9df2f1e34f3
    internal-label: Release notes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: db58d6fc510998d56794678c94d8a97f0563beb4
workflow-type: tm+mt
source-wordcount: '1546'
ht-degree: 32%
---
# Aktuelle Adobe Analytics-Versionshinweise (Oktober 2026)

**Letzte Aktualisierung**: 28. Oktober 2026

Diese Versionshinweise beziehen sich auf den Veröffentlichungszeitraum vom Oktober 2026. Die Versionen von Adobe Analytics basieren auf einem [Modell der kontinuierlichen Bereitstellung](releases.md), das einen besser skalierbaren Schritt-für-Schritt-Ansatz für die Implementierung von Funktionen ermöglicht. Dementsprechend werden diese Versionshinweise mehrmals im Monat aktualisiert. Bitte überprüfen Sie sie regelmäßig.

## Neue Funktionen oder Verbesserungen {#features}

| Funktion und Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| ----------- | ---------- | ---- |
| **Schreibgeschützte Berechtigung für den Adobe Analytics MCP-Server**<br/> Administratoren können Benutzenden jetzt schreibgeschützten Zugriff auf den Adobe Analytics MCP-Server gewähren. Das neue [!UICONTROL MCP-]-Berechtigungselement „Nur-Lese-Zugriff“ bietet Benutzern Zugriff auf alle schreibgeschützten Tools, ohne dass sie Projekte, Segmente oder berechnete Metriken erstellen können.<p>Das vorhandene [!UICONTROL MCP-]-Berechtigungselement wird in &quot;[!UICONTROL -Vollzugriff“ &#x200B;]. Benutzende mit dieser Berechtigung behalten Zugriff auf alle Tools, einschließlich Tools zum Erstellen, Ändern oder Löschen von Komponenten.</p><p>Weitere Informationen finden Sie unter [Einrichten von Berechtigungen](https://developer.adobe.com/analytics-mcp/docs/guides/permissions) in der Dokumentation zum Adobe Analytics MCP-Server.</p> | | &#x200B;6. Oktober 2026 |
| **Journey-Arbeitsfläche: Prozentsätze vergleichen**<br/> Beim Vergleichen einer Journey mit einem vorherigen Zeitraum können Sie jetzt die neue Option [!UICONTROL Prozentsätze vergleichen] aktivieren, um die Änderung in Prozentpunkten für jeden Knoten, jeden Pfeil und jeden Fallout anzuzeigen. Dies ist beim Vergleich von Raten nützlich, z. B. bei der Bindung zwischen Knoten oder beim Fallout, da der Vergleich auch dann genau bleibt, wenn die Anzahl der Personen auf dem Journey zwischen Datumsbereichen unterschiedlich ist.<p>Weitere Informationen finden Sie unter „Vergleichen von Prozentsätzen“ in [Konfigurieren einer Journey-Arbeitsflächen-Visualisierung](/help/analyze/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md#configure-visualization-settings).</p> | | &#x200B;19. Oktober 2026 |
| **Komponentenbeschreibungen automatisch generieren** <br/>Sie können jetzt automatisch Beschreibungen für Dimensionen, Metriken, berechnete Metriken, Segmente und Datumsbereiche generieren. Dies hilft Benutzenden von Workspace zu verstehen, welche Komponenten verwendet werden sollen, insbesondere in Organisationen mit großen Komponentenbibliotheken. <p>Sie können für eine einzelne Komponente eine Beschreibung oder für viele Komponenten gleichzeitig Beschreibungen erstellen.</p> <p>(Link zur Dokumentation folgt.)<!--For more information, see [Automatically generate descriptions](/help/components/add-component-descriptions.md#automatically-generate-descriptions).--></p> | | &#x200B;28. Oktober 2026 |
| **Verbesserungen bei Klassifizierungsdaten in Data Warehouse-Berichten**<br/> Klassifizierungsdaten sind jetzt in Data Warehouse-Berichten genauer. Bei diesen Verbesserungen werden Sie möglicherweise die folgenden Unterschiede in Ihren Data Warehouse-Berichten feststellen:<ul><li>**Leere Werte, bei denen Sie zuvor Klassifizierungswerte gesehen haben**: Wenn ein Klassifizierungswert aus einem Klassifizierungssatz gelöscht wird, zeigt Data Warehouse jetzt korrekt ein leeres Feld an. Zuvor konnte ein gelöschter Classification-Wert weiterhin in späteren Berichten angezeigt werden.</li><li>**Vollständigere Klassifizierungswerte**: In einigen Fällen zeigte Data Warehouse zuvor nur einen von mehreren verschiedenen Klassifizierungswerten an. Data Warehouse zeigt jetzt jeden Wert an.</li><li>**Klassifizierungswerte können in Analysis Workspace unterschiedlich dargestellt werden (gelegentlich)**: Data Warehouse kann alle zugehörigen Klassifizierungswerte anzeigen, während Analysis Workspace einen einzigen Wert aufweist. Daher können die Classification-Werte gelegentlich zwischen Data Warehouse und Analysis Workspace abweichen.</li></ul><p>Weitere Informationen finden Sie unter [Klassifizierungsdimensionen in Data Warehouse](/help/export/data-warehouse/component-support.md#classifications).</p> | &#x200B;14. Oktober 2026 | Januar 2027 |
| **Adobe Brand Visibility-Integration**<br/> Verbinden Sie Adobe Brand Visibility mit den Adobe Analytics-Daten Ihres Unternehmens, damit Sie messen können, wie sich die KI-gesteuerte Erkennung in echte Website-Interaktion und Geschäftsergebnisse niederschlägt.<p>(Link zur Dokumentation folgt.)</p> | | TBD <br/> (ursprünglich für Oktober 2026 geplant) |
| **CX Enterprise Coworker: Analysieren von Adobe Analytics-Daten im**-Chat: Der <br/>Adobe CX Enterprise Coworker-Chat kann jetzt erweiterte Datenanalysen durchführen, die zuvor nur in Analysis Workspace möglich waren. Coworker Chat greift auf Daten aus Ihren Adobe Analytics-Report Suites zu, sodass Sie diese Daten untersuchen und Antworten auf Anfragen in natürlicher Sprache erhalten können.<p>Weitere Informationen finden Sie unter [Analysieren von Daten mit dem Coworker Chat](https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/data-insights/analytics-overview) in der Dokumentation zu Adobe CX Enterprise Coworker.</p> | &#x200B;2. Oktober 2026 | &#x200B;29. Oktober 2026<p>(Ursprünglich für den 25. September 2026 geplant)</p> |
| **CX Enterprise Coworker: Die Ursachenanalyse für den Data-**<br/>-Chat in Adobe Analytics kann jetzt untersuchen, warum sich eine Metrik in Ihren Report Suites in Adobe Analytics geändert hat, anstatt nur Änderungen zu melden. Fragen Sie nach einer Änderung an einer bekannten Metrik in einem bekannten Zeitraum, z. B. „Warum ist der Umsatz am Dienstag gestiegen?“, und der Coworker Chat zeigt die Dimensionen und Segmente an, die zu der Änderung beigetragen haben.<p>Weitere Informationen finden Sie unter [Übersicht über die Geschäftsleistung](https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/data-insights/business-performance/business-performance) in der Dokumentation zu Adobe CX Enterprise Coworker.</p> | &#x200B;13. Oktober 2026 | &#x200B;29. Oktober 2026 |
| **CX Enterprise Coworker: Öffnen Sie Visualisierungen in Analysis Workspace**<br/> Wenn Coworker Chat eine Visualisierung aus Ihren Adobe Analytics-Daten erstellt, können Sie diese jetzt in einem neuen Analysis Workspace-Projekt öffnen, um eine tiefergehende Analyse und granulare Kontrolle zu ermöglichen. <p>Weitere Informationen finden Sie unter [Öffnen einer Visualisierung in Analysis Workspace](https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/data-insights/analytics-chat#open-a-visualization-in-analysis-workspace) in der Adobe CX Enterprise Coworker-Dokumentation.</p> | &#x200B;13. Oktober 2026 | &#x200B;29. Oktober 2026 |
| **CX Enterprise Coworker: Projekte nach Customer Journey Analytics migrieren**<br/> Sie können jetzt Coworker verwenden, um Adobe Analytics-Projekte und ihre zugehörigen Komponenten nach Customer Journey Analytics zu migrieren. Der Mitarbeiter prüft, ob die Dimensionen und Metriken in Ihrem Projekt Ihrer Customer Journey Analytics-Datenansicht zugeordnet sind. Er unterstützt Sie beim Zuordnen von Dimensionen und Metriken, die dies nicht sind, und erstellt dann das Projekt in Customer Journey Analytics neu. Benutzer mit der Berechtigung [!UICONTROL Komponentenmigration] können Projekte mit Kollegen migrieren, auch wenn sie keine Administratoren sind. <p>Zuvor konnten Sie Projekte nur über die Adobe Analytics-Benutzeroberfläche oder mit den Adobe Analytics 2.0-APIs migrieren.</p><p>Weitere Informationen finden Sie unter [Migrieren von Adobe Analytics-Projekten zu Customer Journey Analytics mit &#x200B;](https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/data-insights/intelligent-implementation-and-administration/migrate-projects-aa-cja) in der Adobe CX Enterprise Coworker-Dokumentation.</p><!-- FLAG: Confirm rollout and GA dates. --> | &#x200B;26. Oktober 2026 | &#x200B;29. Oktober 2026 |

### Fehlerbehebungen in Adobe Analytics

**Activity Map**: AN-494609, AN-493182
**Analysis Workspace**: AN-495340, AN-494789, AN-493307, AN-468900
**Classifications**: AN-498043, AN-496619, AN-496468, AN-496217, AN-496133, AN-495567, AN-494651, AN-494345, AN-494312, AN-494261, AN-493336, AN-492869, AN-492812, AN-492751, AN-492750, AN-492741, AN-493645, AN-493507, AN-491032, AN-AN-490802 490796 467849
**Daten-Feeds und Data Warehouse**: AN-494937, AN-493065, AN-489796, AN-479109
**Migration**: AN-489850, AN-468014
**Exporte**: AN-494337, AN-486563
**Report Builder**: AN-496602, AN-494224, AN-493737, AN-493508, AN-493505, AN-492806, AN-468981, AN-454376
**Reporting**: AN-493637, AN-461260
**Report Suites**: AN-496773, AN-495227, AN-494981, AN-494372, AN-494370, AN-493629
**Terminierte Berichte**: AN-491103
**Segmentierung**:
**Sonstige**: AN-496398, AN-494453, AN-492494

### Mitteilungen über das Ende der Nutzungsdauer (EOL) {#eol}

| Ende der Nutzungsdauer eines Produkts oder einer Funktion | Datum hinzugefügt oder aktualisiert | Beschreibung |
| --- | --- | --- |
| **Vorgängerversion von Report Builder** | 18. Juni 2025 | Das alte Report Builder-Add-in wurde im Juni 2026 eingestellt. Alle Benutzenden sollten mit dem Upgrade ihrer Arbeitsmappen der Vorgängerversion auf den [neuen Report Builder](/help/analyze/report-builder/rb-overview.md) beginnen. Der neue Report Builder ist sowohl für Adobe Analytics- als auch für Customer Journey Analytics-Kundschaft verfügbar. Er bietet [nahezu die gleichen Funktionen](/help/analyze/report-builder/convert-workbooks.md#unsupported) sowie viele neue, praktische Funktionen und Verbesserungen der Benutzeroberfläche. Um den Upgrade-Prozess zu vereinfachen, enthält der neue Report Builder eine Funktion zur einfachen Arbeitsmappenkonvertierung. Der neue Report Builder ist nur als Add-in über den Microsoft Store verfügbar. Viele Organisationen benötigen einen internen Genehmigungsprozess, bevor das Add-in Benutzenden zur Verfügung gestellt werden kann. Planen Sie Zeit für diesen Prozess ein und arbeiten Sie jetzt mit Ihrer Organisation, um vor dem Ende der Nutzungsdauer genügend Zeit für ein Upgrade Ihrer Arbeitsmappen zu haben. |
| **Adobe Analytics-API (Version 1.4)** | 17. Juli 2024 | Am **31. August** haben die folgenden Analytics Legacy-API-Services ihr Ende erreicht und wurden eingestellt, und alle Integrationen, die mit diesen Services erstellt wurden, funktionieren nicht mehr:<ul><li>Adobe Analytics-API (Version 1.4)</li><li>WSSE-Authentifizierung von Adobe Analytics</li></ul><p>Integrationen, die die Adobe Analytics-API (Version 1.4) verwenden, müssen zur [Adobe Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren, während WSSE-Integrationen zu einem OAuth-basierten Authentifizierungsprotokoll in der [Adobe Developer Console](https://developer.adobe.com/console) migrieren müssen.</p><p>Antworten auf häufig gestellte Fragen und weitere Anleitungen finden Sie in den [häufig gestellten Fragen zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/).</p> |

## AppMeasurement

Die neuesten Aktualisierungen zu AppMeasurement-Versionen finden Sie in den [Versionshinweisen zu AppMeasurement](https://github.com/adobe/appmeasurement/releases).

## Zurückgestellte Funktionen

| Funktion und Beschreibung | [Rollout-Beginn](releases.md) | [Allgemeine Verfügbarkeit](releases.md) |
| -----------|-----------|-----------|
| **Streaming-Mediendienste: Unterstützung von Zeitplandaten** <br/>Sie können jetzt Zeitplandaten von früheren Live-Inhalten von Streaming-Medien hochladen, um Zuschauerzahlen einfacher und genauer zu verfolgen.<p>Im Folgenden finden Sie Beispiele für Live-Content, der mit dem Hochladen von Zeitplandaten unterstützt wird:</p><ul><li>FAST-Plattformen (Free Ad Supported TV)</li><li>Lokale Datenströme</li><li>Live-Sportübertragungen</li></ul><p>Durch das Hochladen von Zeitplandaten können Sie die Zuschauerzahlen für einzelne Programme verfolgen, die in dem von Ihnen in der Upload-Datei angegebenen Zeitraum gelaufen sind. Sie können sogar Zuschauerzahlen für bestimmte Themen oder Programmsegmente erfassen.</p><p>Diese Funktionen sind unabhängig davon verfügbar, wie Sie die Erfassung von Streaming-Medien implementiert haben.</p><p>Zuvor war es bei der Analyse von Live-Inhalten schwierig, eine bestimmte Sitzung genau mit bestimmten Programmen zu verknüpfen, und es war nicht möglich, eine bestimmte Sitzung mit einzelnen Themen oder Programmsegmenten zu verknüpfen.</p><p>Weitere Informationen finden Sie unter [Hochladen von Zeitplandaten zur Verfolgung von Live-Inhalten](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-use-cases/track-schedule-data).</p> | &#x200B;29. Oktober 2025 | TBD<p>(Ursprünglich für den 29. Oktober 2025 geplant)</p> |


>[!MORELIKETHIS]
>
>* [Frühere Versionshinweise für 2026](/help/release-notes/2026.md)
>* [Versionshinweise zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=de)
>* [Versionshinweise zu Streaming-Mediendiensten](https://experienceleague.adobe.com/de/docs/media-analytics/using/release-notes/release-notes)
>* Die neuesten Versions-Updates für [Adobe CX Enterprise-Produkte](https://business.adobe.com/de/products/adobe-experience-cloud-products.html)

