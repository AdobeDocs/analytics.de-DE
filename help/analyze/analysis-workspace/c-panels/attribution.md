---
title: Attributionsbedienfeld
description: Verwendung und Interpretation des Attributionsbedienfelds in Analysis Workspace.
translation-type: tm+mt
source-git-commit: e1cfaea079f69daeec639c6d43ef4fa442cfaa97
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 72%

---


# Attributionsbedienfeld

Das Attributionsbedienfeld bietet eine einfache Möglichkeit, eine Analyse zu erstellen, mit der verschiedene Attributionsmodelle verglichen werden. Dabei handelt es sich um eine Funktion in [Attribution IQ](../attribution/overview.md), die Ihnen einen eigenen Arbeitsbereich bietet, um Attributionsmodelle zu verwenden und zu vergleichen.

## Erstellen eines Attributionsbedienfeldes

1. Klicken Sie links auf das Bedienfeldsymbol.
1. Ziehen Sie das Attributionsbedienfeld in Ihr Analysis Workspace-Projekt.

   ![Neues Attributionsbedienfeld](assets/Attribution_Panel_1.png)

1. Fügen Sie eine Metrik hinzu, die Sie zuordnen möchten, und fügen Sie eine beliebige Dimension hinzu, gegen die Sie zuordnen möchten. Beispiele sind Marketing-Kanäle oder benutzerdefinierte Dimensionen wie interne Promotions.

   ![Dimension und Metrik auswählen](assets/attribution_panel2.png)

1. Wählen Sie die [Attributionsmodelle und das Lookback-Fenster](../attribution/models.md) aus, die Sie vergleichen möchten.

1. Das Attributionsbedienfeld gibt einen umfangreichen Satz an Daten und Visualisierungen zurück, die die Attribution für die ausgewählte Dimension und Metrik vergleichen.

   ![Visualisierungen der Attribution](assets/attr_panel_vizs.png)

## Visualisierungen der Attribution

* **Gesamtmetrik**: Die Gesamtanzahl der im Berichtszeitfenster aufgetretenen Konversionen. Hierbei handelt es sich um die Konversionen, die über die von Ihnen ausgewählte Dimension hinweg mit Attributen versehen werden.
* **Vergleichsleiste**: Vergleicht visuell die zugeordneten Konvertierungen über die einzelnen Dimensionselemente Ihrer ausgewählten Dimension hinweg. Jede Balkenfarbe stellt ein bestimmtes Attributionsmodell dar.
* **Zuteilungstabelle**: Zeigt dieselben Daten wie das Balkendiagramm an, das als Tabelle dargestellt wird. Durch die Auswahl verschiedener Spalten oder Zeilen in dieser Tabelle werden das Balkendiagramm sowie mehrere andere Visualisierungen im Bedienfeld gefiltert. Diese Tabelle verhält sich ähnlich wie jede andere Freiformtabelle in Workspace. So können Sie Komponenten wie Metriken, Segmente oder Aufschlüsselungen hinzufügen.
* **Überschneidungsdiagramm**: Ein Venn-Diagramm, das die drei wichtigsten Dimensionselemente und deren gemeinsame Teilnahme an einer Konversion anzeigt. Beispielsweise gibt die Größe der Blasenüberlagerung an, wie oft Konversionen auftraten, wenn ein Besucher beiden Dimensionselementen ausgesetzt war. Durch die Auswahl anderer Zeilen in der angrenzenden Freiformtabelle wird die Visualisierung entsprechend Ihrer Auswahl aktualisiert.
* **Leistungsdetails**: Ermöglicht den visuellen Vergleich von bis zu drei Zuordnungsmodellen mithilfe eines Streudiagramms.
* **Trendleistung**: Zeigt den Trend der zugeordneten Konvertierungen für das Element der obersten Dimension. Durch die Auswahl anderer Zeilen in der angrenzenden Freiformtabelle wird die Visualisierung entsprechend Ihrer Auswahl aktualisiert.
* **Fluss**: Hier können Sie sehen, mit welchen Kanälen am häufigsten und in welcher Reihenfolge während der Reise eines Besuchers interagiert wird.
