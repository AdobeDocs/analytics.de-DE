---
description: Erläutert die erforderlichen Vorbereitungen zur Vorbereitung der Migration von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics.
title: Vorbereiten der Migration von Komponenten und Projekten von Adobe Analytics nach Customer Journey Analytics
feature: Admin Tools
exl-id: a9ff98dc-6568-428d-a8a8-faca5bc76a29
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 6%

---

# Vorbereiten der Migration von Komponenten und Projekten von Adobe Analytics nach Customer Journey Analytics

Bevor eine Person in Ihrem Unternehmen mit der Migration von Projekten beginnt, wie [Migrieren von Komponenten und Projekten von Adobe Analytics nach Customer Journey Analytics](/help/admin/tools/component-migration/component-migration.md) beschrieben, führen Sie die folgenden Abschnitte aus.

## Voraussetzungen

Bevor Ihre Projekte und die zugehörigen Komponenten für die Migration bereit sind, müssen Sie zunächst die Schritte in [Entwicklung von Adobe Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/aa-to-cja.html?lang=de) im Adobe Customer Journey Analytics-Handbuch befolgen. Zu diesen Schritten gehören:

1. Verwenden Sie eine der folgenden Methoden, um Daten in Adobe Experience Platform aufzunehmen, um Adobe Analytics Report Suite-Daten in Customer Journey Analytics anzuzeigen:

   >[!NOTE]
   >
   >  Wenn Sie das Web SDK verwenden, um Daten aufzunehmen, müssen alle Schemafelder manuell zugeordnet werden. (Weitere Informationen zum Zuordnungsprozess finden Sie unter [Migrieren von Komponenten und Projekten von Adobe Analytics zu Customer Journey Analytics](/help/admin/tools/component-migration/component-migration.md))


   * Um den Adobe Analytics-Quell-Connector zu verwenden, müssen Sie:

      1. [Einrichten von Report Suites für die Aufnahme in Adobe Experience Platform und Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      1. [Aufnehmen und Verwenden der Daten](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/analytics.html?lang=de)

   * Um das WebSDK zu verwenden, müssen Sie:

      1. [Einrichten von Report Suites für die Aufnahme in Adobe Experience Platform und Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

      1. [Aufnehmen von Daten über die Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk.html)

1. Erstellen Sie [Verbindung](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html) und [Datenansicht](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=de) mit den aufgenommenen Daten.

1. Stellen Sie sicher, dass Benutzende in Customer Journey Analytics für die Datenansichten bereitgestellt werden, in denen Daten zugeordnet werden.

   Weitere Informationen finden Sie unter [Customer Journey Analytics-Berechtigungen in der Admin Console](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html#customer-journey-analytics-permissions-in-admin-console) in der [Customer Journey Analytics-Zugriffssteuerung](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html).

   Die Registerkarte Berechtigungen ist Teil jedes Produktprofils in Admin Console. Benutzende können zu bestimmten Produktprofilen hinzugefügt werden. Anschließend weisen Sie bestimmten Datenansichten Rechte zu und geben an, welche Berechtigungen die Benutzer in einem Produktprofil haben.

1. Legen Sie als Organisation fest, wie Sie Komponenten zuordnen.

   Weitere Informationen finden Sie im folgenden Abschnitt [Entscheiden Sie als Organisation, wie Sie Komponenten zuordnen &#x200B;](#decide-as-an-organization-how-you-will-map-components).

## Was in einer Migration enthalten ist

In den folgenden Tabellen ist aufgeführt, welche Elemente eines Projekts und einer Komponente bei einer Migration einbezogen werden:

### Migrierte Komponentenelemente

Dimensionen und Metriken werden im Rahmen des Zuordnungsprozesses migriert, der unter [Migrieren von Adobe Analytics-Projekten zu Customer Journey Analytics&quot; &#x200B;](#migrate-adobe-analytics-projects-to-customer-journey-analytics).

Segmente, Datumsbereiche und berechnete Metriken, die noch nicht in Customer Journey Analytics vorhanden sind, werden dort basierend auf den zugeordneten Dimensionen und Metriken neu erstellt.

|  | Migriert |
|---------|---------|
| **[Inhabende](/help/components/calculated-metrics/workflow/cm-manager.md)** | Dimensionen und Metriken: Nein<p>Segmente und Datumsbereiche: ![Häkchen](assets/Smock_Checkmark_18_N.svg)</p> |
| **[Freigabe](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Dimensionen und Metriken: Nein<p>Segmente und Datumsbereiche: Nein</p> |
| **[Beschreibungen](/help/analyze/analysis-workspace/components/add-component-descriptions.md)** | Dimensionen und Metriken: Nein<p>Segmente und Datumsbereiche: ![Häkchen](assets/Smock_Checkmark_18_N.svg)</p> |
| **[Tags](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)** | Dimensionen und Metriken: Nein<p>Segmente und Datumsbereiche: Nein</p> |
| **[Attribution (auf Dimensionen)](/help/analyze/analysis-workspace/attribution/overview.md)** | Dimensionen und Metriken: Nein<p>Segmente und Datumsbereiche: Nein</p> |

{style="table-layout:auto"}

### Migrierte Projektelemente

|  | Migriert |
|---------|----------|
| **[Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Segmente](/help/components/segmentation/seg-overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Schnellsegmente](/help/analyze/analysis-workspace/components/segments/quick-segments.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Dimensionen](/help/components/dimensions/overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) Automatisch oder manuell zugeordnet |
| **[Metriken](/help/components/metrics/overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) Automatisch oder manuell zugeordnet |
| **[Bedienfelder](/help/analyze/analysis-workspace/c-panels/panels.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Inhabende](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) Wird von der Person definiert, die die Migration durchführt |
| **[Kuratierung](/help/analyze/analysis-workspace/curate-share/curate.md)** | Nein |
| **[Freigabe](/help/analyze/analysis-workspace/curate-share/share-projects.md)** | Nein |
| **[Anmerkungen](/help/analyze/analysis-workspace/components/annotations/overview.md)** | Nein |
| **[Ordnerstruktur](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md)** | Nein |
| **[Beschreibungen](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |
| **[Tags](/help/analyze/landing.md)** | Nein |
| **[Favoriten](/help/analyze/landing.md)** | Nein |
| **[Zeitpläne](/help/components/scheduled-projects-manager.md)** | Nein |
| **[Anomalieerkennung](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md)** | ![Häkchen](assets/Smock_Checkmark_18_N.svg) |

{style="table-layout:auto"}

## Nicht unterstützte Elemente verstehen, die Fehler verursachen

Die folgenden Visualisierungen und Bedienfelder werden in Customer Journey Analytics nicht unterstützt. Wenn diese Elemente vor der Migration in einem Projekt enthalten sind, können sie entweder dazu führen, dass die Migration fehlschlägt, oder sie können zu Fehlern führen, nachdem das Projekt migriert wurde.

Entfernen Sie diese Elemente aus dem Adobe Analytics-Projekt, bevor Sie das Projekt zu Customer Journey Analytics migrieren. Wenn eine Migration fehlschlägt, entfernen Sie diese Elemente, bevor Sie die Migration erneut versuchen.

### Nicht unterstützte Bedienfelder

* [Analytics for Target (A4T)](/help/analyze/analysis-workspace/c-panels/a4t-panel.md)

* [Segmentvergleich](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

* [Medien-Zielgruppendurchschnitt pro Minute](/help/analyze/analysis-workspace/c-panels/average-minute-audience-panel.md)

* [Nächstes oder vorheriges Objekt](/help/analyze/analysis-workspace/c-panels/next-previous.md)

* [Seitenzusammenfassung](/help/analyze/analysis-workspace/c-panels/page-summary.md)

* [Beitragsanalyse](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis)

## Legen Sie als Organisation fest, wie Sie Komponenten zuordnen

>[!NOTE]
>
>Der Migrationsprozess identifiziert Komponenten in Ihrem Adobe Analytics-Projekt, die nicht automatisch Komponenten in Customer Journey Analytics zugeordnet werden können, und ermöglicht Ihnen die manuelle Zuordnung.
>
>**Alle Zuordnungen, die für ein Projekt vorgenommen werden, gelten für alle zukünftigen Projekte in Ihrer gesamten IMS-Organisation, unabhängig davon, welcher Benutzer die Migration durchführt. Diese Zuordnungen können beim Migrieren künftiger Projekte aktualisiert werden.**
>
>Es ist wichtig, dass Ihr Unternehmen entscheidet, wie Dimensionen und Metriken zugeordnet werden, bevor Projekte migriert werden. Dadurch wird vermieden, dass einzelne Administratoren Entscheidungen in einem Silo treffen, wenn nur ein einzelnes Projekt in Betracht gezogen wird.
>
>Im Folgenden finden Sie eine Liste von Dimensionen und Metriken, die Sie manuell zuordnen müssen, wenn sie in Ihrem Projekt vorhanden sind. Es wird empfohlen, diese Liste vor der Migration zu lesen. Wenn eine dieser Komponenten in Ihrem Projekt vorhanden ist, entscheiden Sie jetzt, welchen Customer Journey Analytics-Komponenten Sie sie zuordnen.


### Dimensionen, die manuell zugeordnet werden müssen

* averagePageTime
* pagetimeseconds
* singlePageVisits
* visitnumber
* timePrior
* TimeSpent
* Kategorie
* connectionType
* Kundentreue
* Benutzerspezifischer Link
* Downloadlink
* Exitlink
* Treffertiefe
* HitType
* pathlength
* daysBeforeFirstPurchase
* daysSinceLastPurchase
* daysSinceLastVisit
* Bezeichnerstaat
* Opportunismus
* persistentes Cookie
* Rücklauffrequenz
* searchennaturural
* searchEngineNaturalKeyword
* Mobilnetzbetreiber
* Bildschirmauflösung
* Vermessungsgrundlage
* Zielgruppen
* tntbase
* Zielschleppnetz


### Metriken, die manuell zugeordnet werden müssen

* timespentvisit
* timespentvisitor
* Neuladungen
* Bounces
* zurückprallen
* pageEvents
* pageviewspervisit
* OrdersPerVisit
* averagePageDepth
* averageTimePentOnSite
* exitLinkInstances
* customLinkInstances
* downloadLinkInstances
* DarkVisitors
* singlePageVisits
* singleValueVisits
* VisitorHomepage
* visitorsMCVISID
* pagesNotFound
* Neue Interaktionen
* time_granularity
* concurrent_viewers_visitors
* concurrent_viewers_currences
* Geräte
* estimatedPeople
* player_time_spent_seconds
* player_time_spent_minutes
* average_minute_audience_time_based
* average_minute_audience_media_time
* average_minute_audience_content_time
* video_length
* targetConversion
* targetImpression
