---
title: Tage bis Erstkauf
description: Die Anzahl der Tage zwischen dem ersten Besuch eines Besuchers und seinem ersten Kauf.
feature: Dimensions
exl-id: 651f9d55-49b9-402a-b7c7-ba4fba62c695
TQID: https://experienceleague.adobe.com/fA8CgahXKwJfiynK-I8yuD-byaIyFPkaii3FzkrrPoI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 83%

---

# Tage bis Erstkauf

Die Dimension „Tage vor dem ersten Kauf[&#x200B; gibt &#x200B;](overview.md) Anzahl der Tage an, die vergehen, bevor eine Besucherin oder ein Besucher zum ersten Mal Ihre Website erreicht, und wann sie bzw. er einen Kauf tätigt. Wenn ein Besucher beispielsweise einen Tag nach dem ersten Besuch einen Kauf tätigt, gehören alle nachfolgenden Besuche und Ereignisse zum Dimensionselement „1 Tag“.

Nachdem ein Besucher den ersten Kauf getätigt hat, gehören sie für die restliche Cookie-Lebensdauer des Besuchers zum selben Dimensionselement.

## Füllen dieser Dimension mit Daten

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md)-Ereignis in Ihrer Implementierung. Wenn Sie das `purchase`-Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehört die Anzahl der Tage zwischen dem ersten Besuch eines Besuchers auf Ihrer Site und seinem ersten Kauf. Jede Anzahl von Tagen ist ein eigenes Dimensionselement, wobei „Gleicher Tag“ dann auftritt, wenn der erste Besuch imd der erste Kauf eines Besuchers am selben Tag stattgefunden haben.
