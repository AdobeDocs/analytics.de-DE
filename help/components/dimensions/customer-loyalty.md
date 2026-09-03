---
title: Kundentreue
description: Kategorien, die auf der Anzahl der vorherigen Käufe des Besuchers basieren.
feature: Dimensions
exl-id: 48ac1fdf-9a32-4bcc-8b23-bf58358a3470
TQID: https://experienceleague.adobe.com/Essa0dflFlsqwtTQ4JdaSEOkX6T-zEYrQGhgXBWhfcI
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
source-wordcount: 246
ht-degree: 88%

---

# Kundentreue

Die Dimension „Kundenloyalität[&#x200B; &#x200B;](overview.md) gibt die Anzahl der Besucher auf Ihrer Site an, die 0 frühere Käufe, 1 früheren Kauf, 2 frühere Käufe oder 3+ frühere Käufe getätigt haben. Diese Dimension ist hilfreich, um zu verstehen, wie sich Ihre Website auf das Kaufverhalten auswirkt. Sie können diese Dimension auch in einem Segment verwenden, um sich auf Besucher zu konzentrieren, die zum Kauf zurückkehren, damit Sie ähnliche Verhaltensweisen bei neuen Besuchern fördern können.

## Füllen dieser Dimension mit Daten

Adobe füllt diese Dimension automatisch basierend auf dem [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md)-Ereignis in Ihrer Implementierung. Wenn Sie das `purchase`-Ereignis auf Ihrer Site implementieren, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehören:

* **Kein Kunde**: Zum Zeitpunkt des Treffers hat der Besucher noch nie zuvor einen Kauf getätigt.
* **Neue Kunden**: Zum Zeitpunkt des Treffers hat der Besucher zuvor einen Kauf getätigt.
* **Rückkehrende Kunden**: Zum Zeitpunkt des Treffers hat der Besucher zuvor zwei Käufe getätigt.
* **Loyale Kunden**: Zum Zeitpunkt des Treffers hat der Besucher zuvor drei oder mehr Käufe getätigt.

Wenn ein Besucher einen Kauf tätigt (das `purchase`-Ereignis auslöst), werden dieser Treffer und alle nachfolgenden Treffer in den nächsten „Behälter“ verschoben. Wenn ein Besucher beispielsweise zum ersten Mal ein Produkt von Ihrer Site kauft, wechselt er von „Kein Kunde“ zu „Neuer Kunde“, wobei die Bestellung „Neuer Kunde“ zugeordnet wird. Dem Dimensionselement „Kein Kunde“ können keine Bestellungen zugeordnet werden.
