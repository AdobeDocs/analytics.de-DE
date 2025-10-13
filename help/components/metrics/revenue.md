---
title: Umsatz
description: Der Geldbetrag der bei allen Bestellungen gekauften Produkte.
feature: Metrics
exl-id: a70e4d93-704b-46ac-9cec-31ea20d3dcb5
source-git-commit: a1fbd3f483d3a236fe5dc3246f5e90c1b3f51ba9
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 74%

---

# Umsatz

Die [Metrik „Umsatz“ &#x200B;](overview.md) den Geldbetrag der bei allen Bestellungen gekauften Produkte an. Diese Metrik ist für eCommerce-Sites bei der Konversionsmessung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionselemente zum Umsatz beigetragen haben. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension [Trackingcode](../dimensions/tracking-code.md)) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen.

## Berechnung dieser Metrik

Summieren Sie für jeden Treffer, bei dem `purchase` in der [`events`](/help/implement/vars/page-vars/events/event-purchase.md)-Variable vorhanden ist, das Feld „Preis“ innerhalb der [`products`](/help/implement/vars/page-vars/products.md)-Variable.

Diese Metrik basiert auf der Variablen [currencyCode](/help/implement/vars/config-vars/currencycode.md), wenn die Währung auf der Seite sich von der nativen Währung der Report Suite unterscheidet.
