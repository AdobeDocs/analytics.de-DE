---
title: Berechnete Metriken insgesamt
description: Erfahren Sie mehr über berechnete Metriken in Analysis Workspace
feature: Calculated Metrics
exl-id: 3e4429de-3e0c-49a5-b32c-3a4d24a29816
source-git-commit: bf58da2a39e8b9fd298356f23a9bf8f6c394d3de
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 94%

---

# Berechnete Metriken insgesamt

Wenn Sie Daten in Analysis Workspace anzeigen, werden die berechneten Metriken insgesamt in den meisten Fällen angezeigt. In einigen Fällen ist die Bereitstellung einer Gesamtsumme nicht möglich, beispielsweise wenn die Zeilen des Berichts unterschiedliche Formate aufweisen (z. B. Dezimalzahl und Währung).

Wenn Summen angezeigt werden, werden sie häufig serverseitig berechnet, was bedeutet, dass die Summe Metriken wie Besuche oder Besucher dedupliziert. Unter bestimmten Umständen werden berechnete Metriken clientseitig generiert, indem sie über Tabellenzeilen hinweg summiert werden. Das bedeutet, dass die Summe keine Metriken wie Besuche oder Besucher dedupliziert. Dies geschieht:

* Wenn [statische Zeilen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) in Freiform-Tabellen verwendet werden und die Option **[!UICONTROL Als Summe der aktuellen Zeilen anzeigen]** aktiviert ist (Standard).
* In der [Donut-Visualisierung](/help/analyze/analysis-workspace/visualizations/donut.md), sodass die Summe der Zahlen 100 % ergibt.

Weitere Informationen zu den Gesamtsummen in Analysis Workspace finden Sie unter [Gesamtsummen in Workspace](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md#static-row-total).
