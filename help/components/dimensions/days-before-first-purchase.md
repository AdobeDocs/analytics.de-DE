---
title: Tage bis Erstkauf
description: Die Anzahl der Tage zwischen dem ersten Besuch eines Besuchers und seinem ersten Kauf.
feature: Dimensions
exl-id: 651f9d55-49b9-402a-b7c7-ba4fba62c695
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '173'
ht-degree: 100%

---

# Tage bis Erstkauf

Die Dimension „Tage bis Erstkauf“ gibt die Anzahl der Tage an, die zwischen dem ersten Sitebesuch eines Besuchers und dem ersten Kauf durch diesen Besucher verstrichen sind. Wenn ein Besucher beispielsweise einen Tag nach dem ersten Besuch einen Kauf tätigt, gehören alle nachfolgenden Besuche und Ereignisse zum Dimensionselement „1 Tag“.

Nachdem ein Besucher den ersten Kauf getätigt hat, gehören sie für die restliche Cookie-Lebensdauer des Besuchers zum selben Dimensionselement.

## Füllen dieser Dimension mit Daten

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md)-Ereignis in Ihrer Implementierung. Wenn Sie das `purchase`-Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehört die Anzahl der Tage zwischen dem ersten Besuch eines Besuchers auf Ihrer Seite und seinem ersten Kauf. Jede Anzahl von Tagen ist ein eigenes Dimensionselement, wobei „Gleicher Tag“ dann auftritt, wenn der erste Besuch imd der erste Kauf eines Besuchers am selben Tag stattgefunden haben.
