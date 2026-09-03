---
title: Tage seit letztem Kauf
description: Die Anzahl der Tage zwischen dem aktuellen Treffer und dem letzten Kauf, den er getätigt hat.
feature: Dimensions
exl-id: 6f0d9d79-cf40-4de3-9d9f-9b1bc57f97b6
TQID: https://experienceleague.adobe.com/q86bc1bMRctUBe7dFEJaALsq0GjALFQQtKU9cRpRkoU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
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
source-wordcount: 173
ht-degree: 84%

---

# Tage seit letztem Kauf

Die Dimension „Tage seit dem letzten Kauf[&#x200B; misst &#x200B;](overview.md) Zeitspanne zwischen dem aktuellen Treffer der Besucherin oder des Besuchers und ihrem bzw. seinem letzten Kauf zu diesem Zeitpunkt. Diese Dimension hilft Ihnen, das Verhalten der Besucher nach einem Kauf auf Ihrer Website zu verstehen.

Besucher, die noch nie etwas gekauft haben, werden in dieser Dimension nicht berücksichtigt. Auch Treffer, die vor dem ersten Kauf eines Besuchers erzielt wurden, sind nicht enthalten. Es werden nur Treffer nach dem ersten Kauf des Besuchers berücksichtigt.

## Füllen dieser Dimension mit Daten

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md)-Ereignis in Ihrer Implementierung. Wenn Sie das `purchase`-Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehört die Anzahl der Tage zwischen dem letzten Kauf eines Besuchers und dem aktuellen Treffer. Jede Anzahl von Tagen ist ein eigenes Dimensionselement, wobei „Gleicher Tag“ dann auftritt, wenn der letzte Kauf eines Besuchers und der aktuelle Treffer am selben Tag stattgefunden haben.
