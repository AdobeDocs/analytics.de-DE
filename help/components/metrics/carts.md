---
title: Warenkörbe
description: Die Anzahl der Treffer, bei denen ein Besucher sein erstes Produkt einem Warenkorb hinzugefügt hat.
feature: Metrics
exl-id: 890bbaba-0140-4995-bbd2-c69aedc801e5
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 45%

---

# Warenkörbe

Die [Metrik „Warenkörbe“ ](overview.md) die Anzahl der Treffer an, bei denen ein Besucher sein erstes Produkt zu einem Warenkorb hinzugefügt hat.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen `scOpen` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist.

## Unterschied zwischen „Warenkörben“, „Warenkorbansichten“ und „Hinzufügungen zum Warenkorb“

Da es sich bei „Warenkörbe“, „Warenkorbansichten“ und „Hinzufügungen zum Warenkorb“ um Ereignisse handelt, die implementiert werden müssen, entscheidet Ihr Unternehmen über den genauen Unterschied zwischen diesen Metriken. Adobe hat diese Metriken jedoch für die folgende Logik entwickelt:

* „Warenkorb“ wird nur einmal pro Kauf ausgelöst, wenn ein Besucher sein erstes Produkt in den Warenkorb legt.
* „Warenkorbansichten“ zeigen Trigger jedes Mal an, wenn eine Besucherin oder ein Besucher ihren bzw. seinen Warenkorb anzeigt.
* „Zusatz zum Warenkorb“ wird für jedes Produkt ausgelöst, das in den Warenkorb gelegt wird.

Wenn ein Kunde sein erstes Produkt zu einem Warenkorb hinzufügt, ist das beabsichtigte Verhalten, dass sowohl der Trigger „Warenkörbe“ als auch der  „Hinzufügungen zum Warenkorb“ vorhanden ist. Diese Richtlinien sind aber nicht verpflichtend. Ihre Organisation bestimmt die genaue Implementierungslogik.
