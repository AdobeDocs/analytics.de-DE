---
description: Erfahren Sie, wie Sie einem Projekt in Analysis Workspace Komponenten hinzufügen.
title: Verwenden von Komponenten in Analysis Workspace
feature: Workspace Basics
role: User, Admin
exl-id: fb56e794-67e3-4f85-960e-b90684300fa0
source-git-commit: 9fcebd7a8fb3a3d98eebef53a748c8ac585cbcd1
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 16%

---

# Verwenden von Komponenten in Analysis Workspace

Komponenten bilden die tatsächlichen Daten eines Projekts in Analysis Workspace. Komponenten bestehen aus Dimensionen, Metriken, Segmenten und Datumsbereichen. Sie können einem Projekt Komponenten hinzufügen, indem Sie sie in Visualisierungen oder Bedienfelder ziehen.

Eine Übersicht über die Komponententypen, die Sie hinzufügen können, finden Sie unter [Komponentenübersicht](/help/analyze/analysis-workspace/components/analysis-workspace-components.md).

>[!TIP]
>
>Informationen zu den einzelnen Komponenten erhalten Sie, wenn Sie in der linken Leiste von Analysis Workspace auf das Infosymbol neben dem Namen einer Komponente klicken oder in der [Komponentenleitfaden für Analytics](/help/components/home.md).

## Hinzufügen von Komponenten zu einem Projekt beginnen

1. [Erstellen eines Projekts in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md) wenn Sie es noch nicht getan haben.

1. [Bedienfeld hinzufügen](/help/analyze/analysis-workspace/c-panels/panels.md) oder [Visualisierung hinzufügen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel) zum Projekt in Analysis Workspace.

   Wenn Sie eine Komponente zu einem leeren Projekt hinzufügen, wird automatisch eine Freiformtabellenvisualisierung erstellt.

1. Wählen Sie in der linken Leiste das Symbol **[!UICONTROL Komponenten]** aus.

   ![](assets/build-components.png)

1. Scrollen Sie zu der Komponente, die Sie hinzufügen möchten, oder suchen Sie sie und ziehen Sie sie anschließend in ein Bedienfeld oder eine Visualisierung innerhalb Ihres Projekts.

1. (Optional) Ziehen Sie eine Komponente in die Segment-Dropzone in einer Bedienfeldüberschrift.

   Segmente gelten für alle Inhalte im Bereich.

   Informationen dazu, wie Sie die Segment-Dropzone in einem Bedienfeld zum Filtern Ihres Bedienfelds verwenden können, finden Sie unter [Dropzone](/help/analyze/analysis-workspace/c-panels/panels.md#drop-zone) in [Bedienfelder - Übersicht](/help/analyze/analysis-workspace/c-panels/panels.md).

   ![Segment im Ablegebereich ablegen](assets/segment-dropzone.png)

1. Weitere Informationen erhalten Sie in den folgenden Abschnitten, je nach Typ der Komponente, die Sie hinzufügen:

   * [Dimensionen zu einem Projekt hinzufügen](#add-dimensions-to-a-project)

   * [Hinzufügen von Metriken zu einem Projekt](#add-metrics-to-a-project)

   * [Segmente zu einem Projekt hinzufügen](#add-segments-to-a-project)

   * [Hinzufügen von Datumsbereichen zu einem Projekt](#add-date-ranges-to-a-project)

## Dimensionen zu einem Projekt hinzufügen

[Dimensionen](/help/components/dimensions/overview.md) sind Variablen in Adobe Analytics, die normalerweise Zeichenfolgenwerte enthalten. Zu den gebräuchlichen Dimensionen gehören [Seite](/help/components/dimensions/page.md), [Referrer-Domäne](/help/components/dimensions/referring-domain.md) oder eine [eVar](/help/components/dimensions/evar.md). Im Gegensatz dazu enthalten [Metriken](/help/components/metrics/overview.md) numerische Werte, die mit einer Dimension verknüpft sind. Ein Basisbericht zeigt Zeilen mit Zeichenfolgenwerten (Dimension) gegen eine Spalte mit numerischen Werten (Metrik) an.

1. Beginnen Sie mit dem Hinzufügen einer Dimension zu Ihrem Projekt in Analysis Workspace, wie beschrieben in [Hinzufügen von Komponenten zu einem Projekt beginnen](#begin-adding-components-to-a-project).

1. Wählen Sie eine der folgenden Methoden, um Dimensionen hinzuzufügen und den Datentyp zu bestimmen, den Sie analysieren möchten:

   * Ziehen Sie eine Dimension in eine Visualisierung (z. B. eine Freiformtabelle) in Analysis Workspace.

     ![Dimensionen zu einem Projekt hinzufügen](assets/add-dimensions.png)

   * Ziehen Sie eine oder mehrere Dimensionen aus der linken Leiste in den Segment-Ablagebereich, um ein Ad-hoc-Segment zu erstellen, wie unter [Segmente zu einem Projekt hinzufügen](#add-segments-to-a-project).

     ![Segment im Ablegebereich ablegen](assets/segment-dropzone.png)

1. (Optional) Sie können Dimensionen und Dimensionselemente in Analysis Workspace mit anderen Komponenten aufschlüsseln.

   Weitere Informationen finden Sie unter [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md).

Weitere Informationen zur Verwendung von Dimensionen in Analysis Workspace finden Sie unter [Dimensionen in der Vorschau anzeigen](/help/analyze/analysis-workspace/components/dimensions/view-dimensions.md), [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md), und [Dimensionen für die Zeitunterteilung](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md).

## Hinzufügen von Metriken zu einem Projekt

[Metriken](/help/analyze/analysis-workspace/components/apply-create-metrics.md) können Sie Datenpunkte in Analysis Workspace quantifizieren. Sie werden meist als Spalten in einer Visualisierung verwendet und sind an Dimensionen gebunden.

So fügen Sie einem Projekt in Analysis Workspace eine Metrik hinzu:

1. Beginnen Sie mit dem Hinzufügen einer Metrik zu Ihrem Projekt in Analysis Workspace, wie unter [Hinzufügen von Komponenten zu einem Projekt beginnen](#begin-adding-components-to-a-project).

1. Wählen Sie eine der folgenden Methoden, um eine Metrik in Analysis Workspace hinzuzufügen:

   * Ziehen Sie eine Metrik in den Ablagebereich der Metrik in einer leeren Freiformtabelle, um die Trendansicht dieser Metrik über den Datumsbereich des Projekts anzuzeigen.

     ![Hinzufügen einer Metrik zu einem Projekt](assets/add-metrics.png)

   * Ziehen Sie eine Metrik, wenn eine Dimension vorhanden ist, um diese Metrik mit jedem Dimensionselement zu vergleichen.

   * Ziehen Sie eine Metrik auf eine vorhandene Metrik-Kopfzeile, um sie zu ersetzen.

   * Ziehen Sie eine Metrik neben eine Kopfzeile, um beide Metriken nebeneinander anzuzeigen.

Weitere Informationen zur Verwendung von Metriken in Analysis Workspace finden Sie unter [Metriken](/help/analyze/analysis-workspace/components/apply-create-metrics.md).

## Segmente zu einem Projekt hinzufügen

[Segmente](/help/components/segmentation/seg-overview.md) ermöglichen es Ihnen, Besucheruntergruppen anhand von Merkmalen oder spezifischen Interaktionen zu identifizieren.

Sie können Segmente in Analysis Workspace auf eine der folgenden Arten verwenden:

### Segmente zu einem Bereich hinzufügen

Wenn Sie einem Bedienfeld Segmente hinzufügen, gelten die Segmente für alle Inhalte im Bedienfeld.

Informationen dazu, wie Sie die Segment-Dropzone in einem Bedienfeld zum Filtern Ihres Bedienfelds verwenden können, finden Sie unter [Dropzone](/help/analyze/analysis-workspace/c-panels/panels.md#drop-zone) in [Bedienfelder - Übersicht](/help/analyze/analysis-workspace/c-panels/panels.md).

### Segmente zu einer Spalte in einer Freiformtabelle hinzufügen

Wenn Sie einer Spalte in einer Freiformtabelle Segmente hinzufügen, gelten die Segmente für alle Inhalte in der Tabellenspalte.

### Segmente beim Erstellen berechneter Metriken verwenden

Im Generator für berechnete Metriken können Sie Segmente innerhalb Ihrer Metrikdefinition anwenden.

Weitere Informationen finden Sie unter [Segmentierte Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md).

## Hinzufügen von Datumsbereichen zu einem Projekt

[Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md) den Berichtszeitrahmen in Analysis Workspace bestimmen und auf einen oder mehrere Bereiche innerhalb eines Projekts angewendet werden können.

Jedes Bedienfeld enthält standardmäßig einen Datumsbereich. Es gibt mehrere Möglichkeiten, einen Datumsbereich für ein Bedienfeld zu aktualisieren. Eine Möglichkeit, einen Datumsbereich für ein Bedienfeld in Analysis Workspace zu aktualisieren, besteht darin, eine Datumsbereichskomponente aus der linken Leiste zu ziehen:

1. Beginnen Sie mit dem Hinzufügen eines Datumsbereichs zu Ihrem Projekt in Analysis Workspace, wie beschrieben in [Hinzufügen von Komponenten zu einem Projekt beginnen](#begin-adding-components-to-a-project).

1. Ziehen Sie einen Datumsbereich aus der linken Leiste in den aktuellen Datumsbereich oben rechts im Bedienfeld.

   ![Datumsbereich ablegen](assets/daterange-drop.png)

Weitere Informationen zur Verwendung von Kalendern und Datumsbereichen in Analysis Workspace finden Sie unter [Übersicht über Kalender und Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md).
