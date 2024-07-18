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

Die Metrik &quot;Warenkorb&quot;[zeigt die Anzahl der Treffer an, bei denen ein Besucher sein erstes Produkt zu einem Warenkorb hinzugefügt hat.](overview.md)

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen `scOpen` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist.

## Unterschied zwischen &quot;Warenkorb&quot;, &quot;Warenkorbansicht&quot;und &quot;Zusatz zum Warenkorb&quot;

Da &quot;Warenkorb&quot;, &quot;Warenkorbansichten&quot;und &quot;Zusatz zum Warenkorb&quot;Ereignisse sind, die implementiert werden müssen, entscheidet Ihr Unternehmen über den genauen Unterschied zwischen diesen Metriken. Adobe hat diese Metriken jedoch für die folgende Logik entwickelt:

* „Warenkorb“ wird nur einmal pro Kauf ausgelöst, wenn ein Besucher sein erstes Produkt in den Warenkorb legt.
* &quot;Warenkorb&quot;Trigger jedes Mal anzeigen, wenn ein Besucher seinen Warenkorb anzeigt.
* „Zusatz zum Warenkorb“ wird für jedes Produkt ausgelöst, das in den Warenkorb gelegt wird.

Wenn ein Kunde sein erstes Produkt einem Warenkorb hinzufügt, soll sowohl der Trigger &quot;Warenkorb&quot;als auch der Zusatz zum Warenkorb verwendet werden. Diese Richtlinien sind aber nicht verpflichtend. Ihre Organisation bestimmt die genaue Implementierungslogik.
