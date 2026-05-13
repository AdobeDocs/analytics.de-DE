---
title: Umsatz
description: Der Geldbetrag der bei allen Bestellungen gekauften Produkte.
feature: Metrics
exl-id: a70e4d93-704b-46ac-9cec-31ea20d3dcb5
TQID: https://experienceleague.adobe.com/GJsQWf7h-TihzyNUN6e3VGzOUNyxYD1esuvXet5LM1c
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
source-wordcount: 112
ht-degree: 74%

---

# Umsatz

Die [Metrik „Umsatz“ &#x200B;](overview.md) den Geldbetrag der bei allen Bestellungen gekauften Produkte an. Diese Metrik ist für eCommerce-Sites bei der Konversionsmessung von entscheidender Bedeutung. Sie können diese Metrik mit einer beliebigen Dimension kombinieren, um zu sehen, welche Dimensionselemente zum Umsatz beigetragen haben. Sie könnten beispielsweise die Top-Kampagnen (unter Verwendung der Dimension [Trackingcode](../dimensions/tracking-code.md)) oder die wichtigsten internen Suchbegriffe (unter Verwendung einer [eVar](../dimensions/evar.md)) sehen.

## Berechnung dieser Metrik

Summieren Sie für jeden Treffer, bei dem `purchase` in der [`events`](/help/implement/vars/page-vars/events/event-purchase.md)-Variable vorhanden ist, das Feld „Preis“ innerhalb der [`products`](/help/implement/vars/page-vars/products.md)-Variable.

Diese Metrik basiert auf der Variablen [currencyCode](/help/implement/vars/config-vars/currencycode.md), wenn die Währung auf der Seite sich von der nativen Währung der Report Suite unterscheidet.
