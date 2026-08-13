---
description: Erfahren Sie mehr über Beispiele für gefilterte und gewichtete Metriken.
title: Gefilterte und gewichtete Metriken
feature: Calculated Metrics
exl-id: bea46e03-7d05-44c8-b654-c61b1e32becc
TQID: https://experienceleague.adobe.com/Euk3sI0-AYtfmpEbL-8gfWU4HcFE6kGO6QGgctZbvig
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 9%

---

# Gefilterte und gewichtete Metriken

Dieser Artikel zeigt Beispiele für gefilterte und gewichtete Metriken.

## Gefilterte Bounce-Rate

Diese einfache gefilterte Metrik zeigt die Absprungrate nur für Seiten mit mehr als 100 Besuchen an:

![Gefilterte Bounce-Rate](assets/filtered-bounce-rate.png){zoomable="yes"}

Beachten Sie, dass diese Formel von einem konsistenten Zeitraum abhängt. Wenn Sie einen Bericht für einen einzelnen Tag ausführen, lohnt es sich, jede Seite mit mehr als 20 Besuchen anzusehen. Wenn der Filter einen Monat lang ausgeführt wird, sollte er möglicherweise weitere Besuche enthalten.

## Gefilterte Absprungrate mit Perzentil

Dieser Filter zeigt die Absprungrate für die 30 Prozent der häufigsten Seiten an, wenn nach Besuchen sortiert.

![Gefilterte Absprungrate mit Perzentil](assets/filtered-bounce-rate-with-percentile.png){zoomable="yes"}

## Gewichtete Absprungrate

Angenommen, Sie möchten die Seite nach der Absprungrate im Allgemeinen sortieren, Seiten mit höheren Besuchen sollten jedoch höher auf der Liste stehen. Dazu könnten Sie eine gewichtete Absprungrate erstellen, die in etwa wie folgt aussieht:

![](assets/weighted-bounce-rate.png)
