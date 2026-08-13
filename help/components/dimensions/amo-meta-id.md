---
title: AMO Meta Ads Click ID
description: Die Adobe Media Optimizer Meta Ads Click ID , die in Adobe Advertising-Integrationen verwendet wird.
feature: Dimensions
exl-id: c1def73a-51b9-46bf-9dc7-0fbd46fd6e17
TQID: 'https://experienceleague.adobe.com/3J-pLiOz4QwUewRSmEFsJCg0v-PbEmksUzGKOI0hHoA'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 3%

---

# AMO Meta Ads Click ID

Die **[!UICONTROL AMO Meta Ads Click ID]** ist eine Anzeigenklickkennung, die in Adobe Advertising-Integrationen verwendet wird. Die Dimension wird automatisch erstellt, wenn die Integration von [Analytics for Advertising](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview) aktiviert wird. Sie ist in erster Linie als Raw-Tracking-Kennung und nicht als für Menschen lesbare Reporting-Dimension nützlich.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst ihre Werte auf verschiedene Weise:

* Für Clickthrough-Traffic werden Daten aus dem `fbclid` Abfragezeichenfolgenparameter in der [Seiten-URL](page-url.md) erfasst, normalerweise auf der Seite, über die anzeigengesteuerter Traffic auf die Website gelangt.
* Clickthrough-Traffic kann auch erfasst werden, wenn die URL keine Trackingcodes enthält, der Adobe Advertising JavaScript jedoch innerhalb der letzten zwei Minuten einen Klick erkennt.

## Dimensionselemente

Dimension-Elemente enthalten Ad-Click-Kennungen, die von Meta-Werbenetzwerken (Facebook) generiert wurden. Die Längen dieser Hash-Werte können variieren, sind aber in der Regel Hunderte von Zeichen lang. Beispiele für (gekürzte) Werte:

```text
IwY2xjawP0bVtleHRuA2FlbQIxMAB[...]AVp_aem_l5TPw-muraFjBGOq8l1w0g
PAb21jcAQB1LNleHRuA2FlbQIxMQB[...]PoFocE1FH44g_aem_FNMJG5EydJ_59aBwKIf4uA
```
