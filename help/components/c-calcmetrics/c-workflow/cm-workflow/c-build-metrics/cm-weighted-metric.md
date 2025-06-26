---
description: Enthält Beispiele für gefilterte und gewichtete Metriken.
title: Gefilterte und gewichtete Metriken
feature: Calculated Metrics
exl-id: bea46e03-7d05-44c8-b654-c61b1e32becc
source-git-commit: d85e6990998e3c153ef969d8dc7f3a4835f683bf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 71%

---

# Gefilterte und gewichtete Metriken

Dieser Artikel zeigt Beispiele für gefilterte und gewichtete Metriken.

## Gefilterte Bounce-Rate

Mit dieser einfachen Metrik wird die Absprungrate nur für die Seiten mit mehr als 100 Besuchen angezeigt:

![Gefilterte Bounce-Rate](assets/filtered-bounce-rate.png){zoomable="yes"}

Denken Sie daran, dass diese Formel von einem konsistenten Zeitraum abhängig ist. Wenn Sie einen Bericht für einen Tag ausführen, lohnt es sich, jede Seite mit mehr als 20 Besuchen zu betrachten. Wenn der Bericht für einen Monat ausgeführt wird, sollte der Filter mehr Besuche umfassen.

## Gefilterte Absprungrate mit Perzentil

Dieser Filter zeigt die Absprungrate für die 30 Prozent der häufigsten Seiten an, wenn nach Besuchen sortiert.

![Gefilterte Absprungrate mit Perzentil](assets/filtered-bounce-rate-with-percentile.png){zoomable="yes"}

## Gewichtete Absprungrate

Beispiel: Sie möchten nach Absprungrate im Allgemeinen sortieren, aber Seiten mit mehr Besuchen weiter oben in der Liste anzeigen. Dazu könnten Sie eine gewichtete Absprungrate erstellen, die in etwa wie folgt aussieht:

![](assets/weighted-bounce-rate.png)
