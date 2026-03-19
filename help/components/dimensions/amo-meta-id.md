---
title: AMO Meta Ads Klick-ID
description: Die Adobe Media Optimizer Meta Ads Click ID , die in Adobe Advertising-Integrationen verwendet wird.
feature: Dimensions
source-git-commit: 408d8db0d1e3c8301a066fe54d611ec7b8e3418a
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 10%

---

# AMO Meta Ads Klick-ID

Die **[!UICONTROL AMO Meta Ads Click ID]** ist eine Anzeigenklickkennung, die in Adobe Advertising-Integrationen verwendet wird. Die Dimension wird automatisch erstellt, wenn die Integration von [Analytics for Advertising](https://experienceleague.adobe.com/de/docs/advertising/integrations/analytics/overview) aktiviert wird. Sie ist in erster Linie als Raw-Tracking-Kennung und nicht als für Menschen lesbare Reporting-Dimension nützlich.

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
