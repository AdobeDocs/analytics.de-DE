---
title: Einheiten
description: Die Gesamtanzahl der bei allen Bestellungen gekauften Produkte.
feature: Metrics
exl-id: c7293445-0760-4237-83ae-812224ca6f4b
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 92%

---

# Einheiten

Die &quot;Einheiten&quot; [Metrik](overview.md) zeigt die Gesamtzahl der bei allen Bestellungen gekauften Produkte an. Diese Metrik ist für eCommerce-Sites bei der Konversionsmessung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionselemente zur Anzahl der gekauften Produkte beigetragen haben. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension [Trackingcode](../dimensions/tracking-code.md)) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen, die zu den gekauften Produkten beigetragen haben.

## Berechnung dieser Metrik

Summieren Sie für jeden Treffer, bei dem `purchase` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md)-Variable vorhanden ist, das Feld „Menge“ innerhalb der [`products`](/help/implement/vars/page-vars/products.md)-Variable.

## Vergleich von Bestellungen und Einheiten

Die Metrik [Bestellungen](orders.md) zeichnet nur die Anzahl der Kaufereignisse auf. Die Metrik „Einheiten“ ist in der Regel höher als die Metrik „Bestellungen“, da Kunden mehr als ein Produkt erwerben können. In diesen Fällen gibt es eine einzige Bestellung mit mehreren Einheiten.

Wenn Sie mehr Bestellungen als Einheiten haben, empfiehlt Adobe, die Integrität Ihrer Implementierung zu überprüfen. Es kann sein, dass Ihre `products`-Variable bei Käufen nicht richtig eingestellt wird, was typischerweise unerwünschtes Verhalten zur Folge hat.
