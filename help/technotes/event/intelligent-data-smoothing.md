---
title: Intelligente Datenausgleichung
description: Erfahren Sie, wie die intelligente Datenausgleichung historische Trends analysiert, um den Wert einer Metrik innerhalb eines betroffenen Zeitraums vorherzusagen.
feature: AI Tools
role: User, Admin
exl-id: b7a2e5d5-99d4-408d-84e6-67abff9e8727
source-git-commit: e0a4caec9bc58a0846cd46871aad3bed99d218a3
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 3%

---

# Intelligente Datenausgleichung

In seltenen Fällen können einige Faktoren die Datenqualität beeinträchtigen. Sowohl Traffic als auch Implementierungsänderungen oder Service-Unterbrechungen können sich auf die Integrität der erfassten Daten auswirken. Sie erschweren auch die Analyse, inwiefern das Ereignis die Vollständigkeit der Daten beeinflusst haben könnte.

Intelligente Datenausgleichung ist ein Prototyp in [Analytics Labs](/help/analyze/labs.md) der dabei helfen kann, diese Ansicht abzuschließen, indem historische Trends analysiert werden, um den Wert einer beliebigen Metrik innerhalb des betroffenen Zeitraums vorherzusagen. Der Prototyp wendet erweiterte Algorithmen des maschinellen Lernens an, um die erwarteten Werte für Metriken über den analysierten Zeitraum darzustellen.

## Intelligente Datenausgleichung ausführen

1. Navigieren Sie zu Adobe Analytics Labs:
   ![Labs](assets/labs.png)
1. Starten Sie den Prototyp Intelligente Datenausgleichung .
   ![Prototyp starten](assets/intelligent-ds.png)
1. Fügen Sie die Metrik, die analysiert werden muss, zur Freiformtabelle hinzu. Der Prototyp funktioniert nur mit einer täglichen Granularität. Stellen Sie daher sicher, dass die Dimension in der Tabelle Tag lautet.
   ![Metrik hinzufügen](assets/add-metric.png)
1. Wählen Sie einen Datumsbereich aus, der breiter ist als das Fenster des Ereignisses, stellen Sie jedoch sicher, dass er das Ereignis enthält.
   ![Datumsbereich](assets/date-range.png)
1. Klicken Sie in der Freiformtabelle auf das Zahnradsymbol für die Metrik.
   ![Zahnradsymbol](assets/gear-icon.png)
1. Wählen [!UICONTROL  unter ] die Option [!UICONTROL Datenausgleichung] aus.
   ![Datenglättung](assets/column-setting.png)
1. Wählen Sie das Datum/den Datumsbereich für das Ereignis aus und klicken Sie auf [!UICONTROL Anwenden].
Stellen Sie sicher, dass der Datenbereich für die Datenausgleichung eine Teilmenge des für das Bedienfeld ausgewählten Datumsbereichs ist. Die Metriken in der Tabelle und im Diagramm werden durch die prognostizierten Werte ersetzt.
   ![Prognostizierte Werte](assets/predictive-values.png)
