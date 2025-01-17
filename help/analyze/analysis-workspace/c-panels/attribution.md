---
title: Attributionsbedienfeld
description: Verwendung und Interpretation des Attributionsbedienfelds in Analysis Workspace.
feature: Attribution
role: User, Admin
exl-id: 96ce3cb9-7753-4ec0-b551-e70a1508e3b7
source-git-commit: 7bac64aed46d9d7a83dc61c3f55d33ad56564efe
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 47%

---

# Attributionsbedienfeld {#attribution-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_attribution_button"
>title="Attribution"
>abstract="Vergleichen und visualisieren Sie im Handumdrehen eine beliebige Anzahl von Attributionsmodellen unter Verwendung verschiedener Dimensionen und Konversionskennzahlen"
>additional-url="https://www.youtube.com/watch?v=Yu0hy2klzA0" text="Attribution IQ-Bedienfeld"

>[!CONTEXTUALHELP]
>id="workspace_attribution_panel"
>title="Attributionsbedienfeld"
>abstract="Vergleichen und visualisieren Sie im Handumdrehen eine beliebige Anzahl von Attributionsmodellen unter Verwendung verschiedener Dimensionen und Konversionskennzahlen.<br/><br/>**Parameter **<br/>**Kanal**<br/> Die Dimension, der zugeschrieben werden soll. Bei dieser Dimension kann es sich um Marketing-Kanäle, Kampagnen oder beliebige andere Dimensionen handeln.<br/>**Modelle**<br/> Das Modell bestimmt, wie Credits zu Touchpoints zugewiesen werden.<br/>**Lookback-Fenster**<br/> Diese Einstellung bestimmt das Fenster der Datenattribution, das für jede Konversion gilt."
>additional-url="https://www.youtube.com/watch?v=Yu0hy2klzA0" text="Attribution IQ-Bedienfeld"

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

*In diesem Artikel wird das Attributionsbedienfeld in **Adobe Analytics**.<br/>Siehe [Attributionsbedienfeld](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/attribution) für die **Customer Journey Analytics**-Version dieses Artikels.*

>[!ENDSHADEBOX]

Das **[!UICONTROL Attributionsbedienfeld]** bietet eine einfache Möglichkeit, eine Analyse zu erstellen, mit der verschiedene Attributionsmodelle verglichen werden. Das Bedienfeld bietet Ihnen einen speziellen Arbeitsbereich zum Verwenden und Vergleichen von Attributionsmodellen.

Adobe Analytics erweitert die Attribution und ermöglicht Ihnen Folgendes:

* Definieren Sie die Attribution über bezahlte Medien hinaus: Jede Dimension, Metrik, Kanal oder Ereignis kann auf Modelle (z. B. interne Suche) angewendet werden, nicht nur auf Marketing-Kampagnen.
* Unbegrenzten Attributionsmodellvergleich verwenden: Dynamisches Vergleichen beliebig vieler Modelle.
* Vermeiden Sie Implementierungsänderungen: Bei Berichtszeitverarbeitung und kontextabhängigen Sitzungen kann der Kunden-Journey-Kontext zur Laufzeit integriert und angewendet werden.
* Die Sitzung erstellen, die Ihrem Attributionsszenario am ehesten entspricht.
* Die Attribution nach Segmenten aufschlüsseln: Vergleichen Sie problemlos die Leistung Ihrer Marketing-Kanäle über alle wichtigen Segmente hinweg (z. B. Neu- mit Bestandskunden, Produkt X vs. Produkt Y, Treuestufe oder CLV).
* Wechsel zwischen Kanälen und Multi-Touch-Analyse beachten: Verwenden Sie Venn-Diagramme und Histogramme und erstellen Sie Trends anhand von Attributionsergebnissen.
* Wichtige Marketing-Sequenzen visuell analysieren: Erkunden Sie zur Konversion führende Pfade visuell mithilfe von mehrknotigen Fluss- und Fallout-Visualisierungen.
* Berechnete Metriken erstellen: Verwenden Sie eine beliebige Anzahl an Attributionszuordnungsmethoden.

## Verwenden

So verwenden Sie ein **[!UICONTROL Attributions]** Bedienfeld:

1. Erstellen Sie **[!UICONTROL Bedienfeld]** Attribution“. Informationen zum Erstellen eines Bedienfelds finden Sie unter [Erstellen eines Bedienfelds](panels.md#create-a-panel).

1. Legen Sie die [Eingabe](#panel-input) für das Bedienfeld fest.

1. Sehen Sie sich die [Ausgabe](#panel-output) für das Bedienfeld an.

### Bedienfeldeingabe

Sie können das Attributionsbedienfeld mithilfe der folgenden Eingabeeinstellungen konfigurieren:

1. Fügen Sie eine **[!UICONTROL Erfolgsmetrik]** und eine Dimension aus dem **[!UICONTROL Kanal]** hinzu, für den Sie ein Attribut erstellen möchten. Beispiele sind Marketing-Kanäle oder benutzerdefinierte Dimensionen wie interne Promotions.

   ![Das Fenster des Attributionsbedienfelds zeigt mehrere ausgewählte Dimensionen und Metriken.](assets/attribution-panel.png)

1. Wählen Sie ein oder [ (](#attribution-models)) aus **[!UICONTROL Einbezogene Modelle]** und ein [Lookback-Fenster](#lookback-window) aus dem **[!UICONTROL Lookback-Fenster]**, die Sie für den Vergleich verwenden möchten.

1. Wählen **[!UICONTROL Erstellen]**, um die Visualisierungen im Bedienfeld zu erstellen.

### Bedienfeldausgabe

Das Bedienfeld **[!UICONTROL Attribution]** gibt eine Vielzahl von Daten und Visualisierungen zurück, die die Attribution für die ausgewählte Dimension und Metrik vergleichen.

![Die Visualisierungen des Attributionsbedienfelds, die ausgewählte Metriken und Dimensionen vergleichen.](assets/attr_panel_vizs.png)

### Visualisierungen der Attribution

Die folgende Visualisierung ist Teil der Bedienfeldausgabe.

* **Gesamtmetrik**: Die Gesamtzahl der Konversionen, die im Berichtszeitfenster stattgefunden haben und der ausgewählten Dimension zugeordnet wurden.
* **Balkendiagramm für den Vergleich der Metrik-Attribution**: Vergleicht visuell die zugeordneten Konversionen über die einzelnen Dimensionselemente der von Ihren ausgewählten Dimension hinweg. Jede Balkenfarbe stellt ein bestimmtes Attributionsmodell dar.
* **Attributionsvergleichstabelle**: Zeigt dieselben Daten wie das Balkendiagramm in Tabellenform an. Durch die Auswahl verschiedener Spalten oder Zeilen in dieser Tabelle werden das Balkendiagramm sowie mehrere andere Visualisierungen im Bedienfeld gefiltert. Diese Tabelle verhält sich ähnlich wie jede andere Freiformtabelle in Workspace - sodass Sie Komponenten wie Metriken, Segmente oder Aufschlüsselungen hinzufügen können.
* **Überlagerungsdiagramm**: Eine Venn-Visualisierung, die die drei wichtigsten Dimensionselemente zeigt und wie oft sie gemeinsam an einer Konversion beteiligt sind. Beispielsweise gibt die Größe der Blasenüberschneidung an, wie oft Konversionen aufgetreten sind, wenn eine Person beiden Dimensionselementen ausgesetzt war. Durch die Auswahl anderer Zeilen in der angrenzenden Freiformtabelle wird die Visualisierung entsprechend Ihrer Auswahl aktualisiert.
* **Leistungsdetails**: Eine Streuvisualisierung zum visuellen Vergleich von bis zu drei Attributionsmodellen.
* **Trendleistung**: Zeigt den Trend der zugeordneten Konvertierungen für das Element der obersten Dimension. Durch die Auswahl anderer Zeilen in der angrenzenden Freiformtabelle wird die Visualisierung entsprechend Ihrer Auswahl aktualisiert.
* **Fluss**: Hiermit können Sie anzeigen, mit welchen Kanälen am häufigsten interagiert wird und wie sich die Reihenfolge auf dem Journey einer Person darstellt.

## Attributionsmodelle

{{attribution-models-details}}

## Lookback-Fenster

{{attribution-lookback-window}}

>[!MORELIKETHIS]
>
> [Erstellen eines Bedienfelds](/help/analyze/analysis-workspace/c-panels/panels.md#create-a-panel)
>

<!--
# Attribution panel

The [!UICONTROL Attribution] panel is an easy way to build an analysis comparing various attribution models. It is a feature in [Attribution](/help/analyze/analysis-workspace/attribution/overview.md) that gives you a dedicated workspace to use and compare attribution models.

>[!VIDEO](https://video.tv.adobe.com/v/23139/?quality=12)

## Create an attribution panel

1. Click the panel icon on the left.
1. Drag the [!UICONTROL Attribution] panel into your Analysis Workspace Project.

   ![New attribution panel](assets/Attribution_Panel_1.png)

1. Add a metric that you want to attribute and add any dimension to attribute against. Examples include Marketing Channels or custom dimensions, such as internal promotions.

   ![Select dimension and metric](assets/attribution_panel2.png)

1. Select the [attribution models and lookback window](../attribution/models.md) you want to compare.

1. The Attribution panel returns a rich set of data and visualizations that compare attribution for the selected dimension and metric.

   ![Attribution visualizations](assets/attr_panel_vizs.png)

## Attribution visualizations

* **Total metric**: The total number of conversions that occurred over the reporting time window. These are the conversions that are attributed across the dimension that you selected.
* **Attribution Comparison Bar**: Visually compares the attributed conversions across each of the dimension items from your selected dimension. Each bar color represents a distinct attribution model.
* **Attribution Comparison Table**: Shows the same data as the bar chart, represented as a table. Selecting different columns or rows in this table filters the bar chart as well as several of the other visualizations in the panel. This table acts similar to any other Freeform Table in Workspace - allowing you to add components such as metrics, segments, or breakdowns.
* **Overlap Diagram**: A Venn Diagram showing the top three dimension items and how often they participate jointly in a conversion. For example, the size of the bubble overlap indicates how often conversions occurred when a visitor was exposed to both dimension items. Selecting other rows in the adjacent Freeform table updates the visualization to reflect your selection.
* **Performance Detail**: Lets you to compare up to three attribution models visually using a scatter plot.
* **Trended Performance**: By default, shows the conversion performance trend by attribution model for the first dimension listed in the adjacent Freeform table. You can select different dimension rows in the Freeform table to show the trend for the selected dimensions (such as Total Revenue for each attribution model for Social Campaigns and Paid Search). Alternately, you can select cells in the columns for any metric and attribution type combinations in the Freeform table to see the trended performance by dimension value for the specified attribution models (such as Total Revenue by Marketing Channel using Last Touch and First Touch attribution).
* **Flow**: Lets you see which channels are interacted with most commonly, and in what order across a visitor's journey.

-->