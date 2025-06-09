---
description: Im Bedienfeld „Seitenzusammenfassung“ werden zusammenfassende Informationen für eine von Ihnen ausgewählte Seite angezeigt.
title: Bedienfeld „Seitenzusammenfassung“
feature: Panels
role: User, Admin
exl-id: f0b7cd92-17b2-452d-9aab-f78629360ab8
source-git-commit: 2aaa8c0d13755b40ec701ca6342ab773103a0422
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 100%

---

# Bedienfeld „Seitenzusammenfassung“ {#page-summary}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_pagesummary_button"
>title="Seitenzusammenfassung"
>abstract="Prüfen Sie schnell einige allgemeine Metriken sowie die Bewegungen zu und von einer bestimmten Seite."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_pagesummary_panel"
>title="Bedienfeld „Seitenzusammenfassung“"
>abstract="Prüfen Sie schnell einige allgemeine Metriken sowie die Bewegungen zu und von einer bestimmten Seite.<br/><br/>**Parameter **<br/>**Dimensionselement „Seite“ hinzufügen**: Öffnen Sie die Komponentenleiste, suchen Sie die Dimension „Seite“ und erweitern Sie sie durch Klicken auf die Karotte, um die Dimensionselemente anzuzeigen. Ziehen Sie dann die Seite, über die Sie etwas erfahren möchten, in den Builder. Danach werden automatisch die wichtigsten Informationen über die Seite in den Bericht übertragen."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_In diesem Artikel wird das Bedienfeld „Seitenzusammenfassung“ in_ ![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics** beschrieben._<br/>_Es gibt kein vergleichbares Bedienfeld in_ ![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**._

>[!ENDSHADEBOX]

Das Bedienfeld **[!UICONTROL Seitenzusammenfassung]** ermöglicht die Untersuchung wichtiger Statistiken zu bestimmten Seiten.

## Verwenden

So verwenden Sie das Bedienfeld **[!UICONTROL Seitenzusammenfassung]**:

1. Erstellen Sie ein Bedienfeld **[!UICONTROL Seitenzusammenfassung]**. Informationen zum Erstellen eines Bedienfelds finden Sie unter [Erstellen eines Bedienfelds](panels.md#create-a-panel).

1. Legen Sie die [Eingabe](#panel-input) für das Bedienfeld fest.

1. Sehen Sie sich die [Ausgabe](#panel-output) für das Bedienfeld an.



Sie können auf das Bedienfeld über [!UICONTROL Berichte] oder [!UICONTROL Workspace ] zugreifen.

| Zugriffspunkt | Beschreibung |
| --- | --- |
| [!UICONTROL Berichte] | <ul><li>Das Bedienfeld ist bereits in einem Projekt abgelegt.</li><li>Die linke Leiste ist reduziert.</li><li>Es wird nur die Seitendimension unterstützt.</li><li>Eine Standardeinstellung wurde bereits angewendet: in diesem Fall die am häufigsten besuchte Seite für die [!UICONTROL Seitendimension]. Sie können diese Einstellung ändern.</li></ul> |
| Workspace | Erstellen Sie ein neues Projekt und wählen Sie in der linken Leiste das Bedienfeldsymbol aus. Ziehen Sie das Bedienfeld [!UICONTROL Seitenzusammenfassung] über die Freiformtabelle. Beachten Sie, dass das Feld mit dem [!UICONTROL Seiten-Dimensionselement] leer gelassen wird. Wählen Sie ein Dimensionselement aus der Dropdown-Liste aus.  |

### Bedienfeldeingabe {#panel-input}

Sie können das Bedienfeld [!UICONTROL Seitenzusammenfassung] mithilfe der folgenden Eingabeeinstellungen konfigurieren:

![Zusammenfassung der Seiteneingabe](assets/page-summary-input.png)

| Eingabe | Beschreibung |
| --- | --- |
| **[!UICONTROL Seite]** | Wählen Sie eine Seitendimension aus, für die wichtige Statistiken untersucht werden sollen. |

{style="table-layout:auto"}


Wählen Sie **[!UICONTROL Erstellen]** aus, um das Bedienfeld zu erstellen.

### Bedienfeldausgabe {#panel-output}

Das Bedienfeld [!UICONTROL Seitenzusammenfassung] gibt eine Vielzahl von Metrikdaten und Visualisierungen zurück, die Ihnen helfen, Statistiken zu bestimmten Seiten besser zu verstehen.

![Bedienfeld „Seitenzusammenfassung“](assets/page-summary-output.png)

| Visualisierung | Beschreibung |
| --- | --- |
| **[!UICONTROL Seitenaufrufe] – aktueller Monat (bis heute)** | Eine [Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)-Visualisierung, die die Anzahl der Seitenansichten für diese Seite im aktuellen Monat anzeigt. |
| **[!UICONTROL Seitenansichten] – 4 Wochen vorher** | Eine [Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)-Visualisierung, die die Anzahl der Seitenansichten für diese Seite im letzten Monat anzeigt. |
| **[!UICONTROL Seitenansichten] – 52 Wochen vorher** | Eine [Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)-Visualisierung, die die Anzahl der Seitenansichten für diese Seite im letzten Jahr anzeigt. |
| **[!UICONTROL Trend]** | Eine [Trend-Linien](/help/analyze/analysis-workspace/visualizations/line.md)-Visualisierung der Seitenansichten für diesen Monat sowie die vorhergehenden 4 Wochen und die vorhergehenden 52 Wochen. |
| **[!UICONTROL Prozentsatz aller Seitenansichten]** | Eine Zusammenfassungszahl für den Prozentsatz aller Seitenansichten, die zu dieser Seite gewechselt sind. |
| **[!UICONTROL Besuchszeit pro Seite]** | Eine [Horizontalbalken](/help/analyze/analysis-workspace/visualizations/horizontal-bar.md)-Visualisierung, die die auf dieser Seite verbrachte Zeit anzeigt. |
| **[!UICONTROL Einzelseitenbesuche]** | Eine [Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md), die die Anzahl der Seitenansichten anzeigt, bei denen nur diese Seite besucht wurde. |
| **[!UICONTROL Neuladungen]** | Eine [Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md), die anzeigt, wie oft ein Dimensionselement während einer Neuladung vorhanden war. Das Aktualisieren des Browsers durch eine Besucherin oder einen Besucher ist die häufigste Art, wie ein erneutes Laden ausgelöst wird. |
| **[!UICONTROL Einträge]** | Eine [Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md), die anzeigt, wie oft ein bestimmtes Dimensionselement als erster Wert bei einem Besuch erfasst wird.  |
| **[!UICONTROL Ausstiege]** | Eine [Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md), die anzeigt, wie oft ein bestimmtes Dimensionselement als letzter Wert bei einem Besuch erfasst wird.  |
| **[!UICONTROL Fluss]** | Eine [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) mit der ausgewählten Seite als Fokus. Wie bei jeder anderen [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md) können Sie sich die Daten genauer ansehen. |

{style="table-layout:auto"}

Verwenden Sie ![Bearbeiten](/help/assets/icons/Edit.svg), um das Bedienfeld neu zu konfigurieren und neu zu erstellen.
