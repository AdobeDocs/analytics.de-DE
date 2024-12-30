---
description: Erfahren Sie, wie Sie in Analysis Workspace Komponenten zu einem Projekt hinzufügen
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

Komponenten bilden die tatsächlichen Daten eines beliebigen Projekts in Analysis Workspace. Komponenten bestehen aus Dimensionen, Metriken, Segmenten und Datumsbereichen. Sie können Komponenten zu einem Projekt hinzufügen, indem Sie sie in Visualisierungen oder Bedienfelder ziehen.

Übersichtsinformationen zu den Komponententypen, die Sie hinzufügen können, finden Sie unter [Komponentenübersicht](/help/analyze/analysis-workspace/components/analysis-workspace-components.md).

>[!TIP]
>
>Informationen zu den einzelnen Komponenten finden Sie über das Infosymbol neben dem Namen einer Komponente in der linken Leiste von Analysis Workspace oder im [Analytics-Komponentenhandbuch](/help/components/home.md).

## Beginnen Sie mit dem Hinzufügen von Komponenten zu einem Projekt

1. [Erstellen Sie ein Projekt in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md) falls noch nicht geschehen.

1. [Bedienfeld hinzufügen](/help/analyze/analysis-workspace/c-panels/panels.md) oder [Visualisierung hinzufügen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel) zum Projekt in Analysis Workspace hinzufügen.

   Wenn Sie einem leeren Projekt eine Komponente hinzufügen, wird automatisch eine Freiformtabellen-Visualisierung erstellt.

1. Wählen Sie in der linken Leiste das Symbol **[!UICONTROL Komponenten]** aus.

   ![](assets/build-components.png)

1. Scrollen Sie zu der Komponente, die Sie hinzufügen möchten, oder suchen Sie sie und ziehen Sie sie anschließend in ein Bedienfeld oder eine Visualisierung innerhalb Ihres Projekts.

1. (Optional) Ziehen Sie eine Komponente in den Ablegebereich für Segmente in einer Bedienfeldkopfzeile.

   Segmente gelten für alle Inhalte im Bedienfeld.

   Informationen dazu, wie Sie den Segment-Ablagebereich in einem Bedienfeld zum Filtern Ihres Bedienfelds verwenden können, finden Sie unter [Ablagebereich](/help/analyze/analysis-workspace/c-panels/panels.md#drop-zone) in [Bedienfelder - Übersicht](/help/analyze/analysis-workspace/c-panels/panels.md).

   ![Segment im Ablegebereich ablegen](assets/segment-dropzone.png)

1. Weitere Informationen finden Sie in einem der folgenden Abschnitte, je nach dem Komponententyp, den Sie hinzufügen:

   * [Hinzufügen von Dimensionen zu einem Projekt](#add-dimensions-to-a-project)

   * [Hinzufügen von Metriken zu einem Projekt](#add-metrics-to-a-project)

   * [Segmente zu einem Projekt hinzufügen](#add-segments-to-a-project)

   * [Hinzufügen von Datumsbereichen zu einem Projekt](#add-date-ranges-to-a-project)

## Hinzufügen von Dimensionen zu einem Projekt

[Dimensionen ](/help/components/dimensions/overview.md) sind Variablen in Adobe Analytics, die normalerweise Zeichenfolgenwerte enthalten. Zu den gebräuchlichen Dimensionen gehören [Seite](/help/components/dimensions/page.md), [Referrer-Domäne](/help/components/dimensions/referring-domain.md) oder eine [eVar](/help/components/dimensions/evar.md). Im Gegensatz dazu enthalten [Metriken](/help/components/metrics/overview.md) numerische Werte, die mit einer Dimension verknüpft sind. Ein Basisbericht zeigt Zeilen mit Zeichenfolgenwerten (Dimension) gegen eine Spalte mit numerischen Werten (Metrik) an.

1. Beginnen Sie mit dem Hinzufügen einer Dimension zu Ihrem Projekt in Analysis Workspace, wie unter [Beginnen Sie mit dem Hinzufügen von Komponenten zu einem Projekt](#begin-adding-components-to-a-project) beschrieben.

1. Wählen Sie eine der folgenden Methoden, um Dimensionen hinzuzufügen, und bestimmen Sie den Datentyp, den Sie analysieren möchten:

   * Ziehen einer Dimension in eine Visualisierung (z. B. eine Freiformtabelle) in Analysis Workspace.

     ![Hinzufügen von Dimensionen zu einem Projekt](assets/add-dimensions.png)

   * Ziehen Sie eine oder mehrere Dimensionen aus der linken Leiste in den Ablegebereich für Segmente, um ein Ad-hoc-Segment zu erstellen, wie in [Hinzufügen von Segmenten zu einem Projekt](#add-segments-to-a-project) beschrieben.

     ![Segment im Ablegebereich ablegen](assets/segment-dropzone.png)

1. (Optional) Sie können Dimensionen und Dimensionselemente in Analysis Workspace mit anderen Komponenten aufschlüsseln.

   Weitere Informationen finden Sie unter [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md).

Weitere Informationen zur Verwendung von Dimensionen in Analysis Workspace finden Sie unter [Vorschau von Dimensionen](/help/analyze/analysis-workspace/components/dimensions/view-dimensions.md), [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md) und [Dimensionen für die Zeitunterteilung](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md).

## Hinzufügen von Metriken zu einem Projekt

[Metriken](/help/analyze/analysis-workspace/components/apply-create-metrics.md) ermöglichen es Ihnen, Datenpunkte in Analysis Workspace zu quantifizieren. Sie werden meist als Spalten in einer Visualisierung verwendet und sind an Dimensionen gebunden.

So fügen Sie einem Projekt in Analysis Workspace eine Metrik hinzu:

1. Beginnen Sie mit dem Hinzufügen einer Metrik zu Ihrem Projekt in Analysis Workspace, wie beschrieben [Beginnen Sie mit dem Hinzufügen von Komponenten zu einem Projekt](#begin-adding-components-to-a-project).

1. Wählen Sie eine der folgenden Methoden, um eine Metrik in Analysis Workspace hinzuzufügen:

   * Ziehen Sie eine Metrik in die Metrik-Ablagezone in einer leeren Freiformtabelle, um die Entwicklung dieser Metrik über den Datumsbereich des Projekts anzuzeigen.

     ![Hinzufügen einer Metrik zu einem Projekt](assets/add-metrics.png)

   * Ziehen Sie eine Metrik, wenn eine Dimension vorhanden ist, um diese Metrik mit jedem Dimensionselement zu vergleichen.

   * Ziehen Sie eine Metrik auf eine vorhandene Metrik-Kopfzeile, um sie zu ersetzen.

   * Ziehen Sie eine Metrik neben eine Kopfzeile, um beide Metriken nebeneinander anzuzeigen.

Weitere Informationen zur Verwendung von Metriken in Analysis Workspace finden Sie unter [Metriken](/help/analyze/analysis-workspace/components/apply-create-metrics.md).

## Segmente zu einem Projekt hinzufügen

[Segmente](/help/components/segmentation/seg-overview.md) ermöglichen es Ihnen, Untergruppen von Besuchern anhand von Merkmalen oder bestimmten Interaktionen zu identifizieren.

Sie können Segmente in Analysis Workspace auf eine der folgenden Arten verwenden:

### Segmente zu einem Bedienfeld hinzufügen

Wenn Sie Segmente zu einem Bedienfeld hinzufügen, gelten die Segmente für alle Inhalte im Bedienfeld.

Informationen dazu, wie Sie den Segment-Ablagebereich in einem Bedienfeld zum Filtern Ihres Bedienfelds verwenden können, finden Sie unter [Ablagebereich](/help/analyze/analysis-workspace/c-panels/panels.md#drop-zone) in [Bedienfelder - Übersicht](/help/analyze/analysis-workspace/c-panels/panels.md).

### Hinzufügen von Segmenten zu einer Spalte in einer Freiformtabelle

Wenn Sie einer Spalte in einer Freiformtabelle Segmente hinzufügen, werden die Segmente auf alle Inhalte in der Tabellenspalte angewendet.

### Segmente beim Erstellen berechneter Metriken verwenden

Im Generator für berechnete Metriken können Sie Segmente innerhalb Ihrer Metrikdefinition anwenden.

Weitere Informationen finden Sie unter [Segmentierte Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md).

## Hinzufügen von Datumsbereichen zu einem Projekt

[Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md) bestimmen den Berichtszeitrahmen in Analysis Workspace und können auf ein oder mehrere Bedienfelder innerhalb eines Projekts angewendet werden.

Jedes Bedienfeld enthält standardmäßig einen Datumsbereich. Es gibt mehrere Möglichkeiten, einen Datumsbereich für ein Bedienfeld zu aktualisieren. Eine Möglichkeit, einen Datumsbereich für ein Bedienfeld in Analysis Workspace zu aktualisieren, besteht darin, eine Datumsbereichskomponente aus der linken Leiste zu ziehen:

1. Beginnen Sie mit dem Hinzufügen eines Datumsbereichs zu Ihrem Projekt in Analysis Workspace, wie unter [Beginnen Sie mit dem Hinzufügen von Komponenten zu einem Projekt](#begin-adding-components-to-a-project) beschrieben.

1. Ziehen Sie einen Datumsbereich aus der linken Leiste auf den aktuellen Datumsbereich im oberen rechten Bereich des Bedienfelds.

   ![Einen Datumsbereich ablegen](assets/daterange-drop.png)

Weitere Informationen zur Verwendung von Kalendern und Datumsbereichen in Analysis Workspace finden Sie unter [Übersicht über Kalender und Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md).
