---
title: Tage bis Erstkauf
description: Die Anzahl der Tage zwischen dem ersten Besuch eines Besuchers und seinem ersten Kauf.
feature: Dimensions
exl-id: 651f9d55-49b9-402a-b7c7-ba4fba62c695
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 83%

---

# Tage bis Erstkauf

Die Dimension „Tage vor dem ersten Kauf[&#x200B; gibt &#x200B;](overview.md) Anzahl der Tage an, die vergehen, bevor eine Besucherin oder ein Besucher zum ersten Mal Ihre Website erreicht, und wann sie bzw. er einen Kauf tätigt. Wenn ein Besucher beispielsweise einen Tag nach dem ersten Besuch einen Kauf tätigt, gehören alle nachfolgenden Besuche und Ereignisse zum Dimensionselement „1 Tag“.

Nachdem ein Besucher den ersten Kauf getätigt hat, gehören sie für die restliche Cookie-Lebensdauer des Besuchers zum selben Dimensionselement.

## Füllen dieser Dimension mit Daten

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md)-Ereignis in Ihrer Implementierung. Wenn Sie das `purchase`-Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehört die Anzahl der Tage zwischen dem ersten Besuch eines Besuchers auf Ihrer Seite und seinem ersten Kauf. Jede Anzahl von Tagen ist ein eigenes Dimensionselement, wobei „Gleicher Tag“ dann auftritt, wenn der erste Besuch imd der erste Kauf eines Besuchers am selben Tag stattgefunden haben.
