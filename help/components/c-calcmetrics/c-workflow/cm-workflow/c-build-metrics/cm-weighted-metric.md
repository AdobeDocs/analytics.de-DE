---
description: Enthält Beispiele für gefilterte und gewichtete Metriken.
title: Gefilterte und gewichtete Metriken
feature: Calculated Metrics
exl-id: bea46e03-7d05-44c8-b654-c61b1e32becc
source-git-commit: bf58da2a39e8b9fd298356f23a9bf8f6c394d3de
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 89%

---

# Gefilterte und gewichtete Metriken

Dieser Artikel zeigt Beispiele für gefilterte und gewichtete Metriken.

## Gefilterte Absprungrate

Mit dieser einfachen Metrik wird die Absprungrate nur für die Seiten mit mehr als 100 Besuchen angezeigt:

![Gefilterte Bounce-Rate](assets/filtered-bounce-rate.png){zoomable="yes"}

Denken Sie daran, dass diese Formel von einem konsistenten Zeitraum abhängig ist. Wenn Sie einen Bericht für einen Tag ausführen, lohnt es sich, jede Seite mit mehr als 20 Besuchen zu betrachten. Wenn der Bericht für einen Monat ausgeführt wird, sollte der Filter mehr Besuche umfassen.

## Gefilterte Absprungrate mit Perzentil

Dieser Filter zeigt die Absprungrate für die oberen 30 Prozent der Seiten bei Sortierung nach Besuchen an.

![Gefilterte Absprungrate mit Perzentil](assets/filtered-bounce-rate-with-percentile.png){zoomable="yes"}

## Gewichtete Metrik

Beispiel: Sie möchten nach Absprungrate im Allgemeinen sortieren, aber Seiten mit mehr Besuchen weiter oben in der Liste anzeigen. Dazu könnten Sie eine gewichtete Absprungrate erstellen, die in etwa wie folgt aussieht:

![](assets/weighted-bounce-rate.png)
