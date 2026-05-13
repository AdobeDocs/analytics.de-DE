---
title: Warenkörbe
description: Die Anzahl der Treffer, bei denen ein Besucher sein erstes Produkt einem Warenkorb hinzugefügt hat.
feature: Metrics
exl-id: 890bbaba-0140-4995-bbd2-c69aedc801e5
TQID: https://experienceleague.adobe.com/a-qT5Ly8-4mSBGbGTAzbwLIMRFZtqotMPvGFgOrM41Y
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 45%

---

# Warenkörbe

Die [Metrik „Warenkörbe“ &#x200B;](overview.md) die Anzahl der Treffer an, bei denen ein Besucher sein erstes Produkt zu einem Warenkorb hinzugefügt hat.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen `scOpen` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist.

## Unterschied zwischen „Warenkörben“, „Warenkorbansichten“ und „Hinzufügungen zum Warenkorb“

Da es sich bei „Warenkörbe“, „Warenkorbansichten“ und „Hinzufügungen zum Warenkorb“ um Ereignisse handelt, die implementiert werden müssen, entscheidet Ihr Unternehmen über den genauen Unterschied zwischen diesen Metriken. Adobe hat diese Metriken jedoch für die folgende Logik entwickelt:

* „Warenkorb“ wird nur einmal pro Kauf ausgelöst, wenn ein Besucher sein erstes Produkt in den Warenkorb legt.
* „Warenkorbansichten“ zeigen Trigger jedes Mal an, wenn eine Besucherin oder ein Besucher ihren bzw. seinen Warenkorb anzeigt.
* „Zusatz zum Warenkorb“ wird für jedes Produkt ausgelöst, das in den Warenkorb gelegt wird.

Wenn ein Kunde sein erstes Produkt zu einem Warenkorb hinzufügt, ist das beabsichtigte Verhalten, dass sowohl der Trigger „Warenkörbe“ als auch der  „Hinzufügungen zum Warenkorb“ vorhanden ist. Diese Richtlinien sind aber nicht verpflichtend. Ihre Organisation bestimmt die genaue Implementierungslogik.
