---
title: Einheiten
description: Die Gesamtanzahl der bei allen Bestellungen gekauften Produkte.
feature: Metrics
exl-id: c7293445-0760-4237-83ae-812224ca6f4b
TQID: https://experienceleague.adobe.com/0v4pF0Iv0IzU9K4CQiTy1-IIYgMCaO37E6QTmAAEPXc
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
source-wordcount: 173
ht-degree: 80%

---

# Einheiten

Die [Metrik „Einheiten“ &#x200B;](overview.md) die Gesamtzahl der bei allen Bestellungen gekauften Produkte an. Diese Metrik ist für eCommerce-Sites bei der Konversionsmessung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionselemente dazu beigetragen haben, wie viele Produkte gekauft wurden. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension [Trackingcode](../dimensions/tracking-code.md)) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen, die zu den gekauften Produkten beigetragen haben.

## Berechnung dieser Metrik

Summieren Sie für jeden Treffer, bei dem `purchase` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist, das Feld „Menge“ innerhalb der [`products`](/help/implement/vars/page-vars/products.md)-Variable.

## Vergleich von Bestellungen und Einheiten

Die Metrik [Bestellungen](orders.md) zeichnet nur die Anzahl der Kaufereignisse auf. Die Metrik „Einheiten“ ist in der Regel höher als die Metrik „Bestellungen“, da Kunden mehr als ein Produkt erwerben können. In diesen Fällen gibt es eine einzige Bestellung mit mehreren Einheiten.

Wenn Sie mehr Bestellungen als Einheiten haben, empfiehlt Adobe, die Integrität Ihrer Implementierung zu überprüfen. Es kann sein, dass Ihre `products`-Variable bei Käufen nicht richtig eingestellt wird, was typischerweise unerwünschtes Verhalten zur Folge hat.
