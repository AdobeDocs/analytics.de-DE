---
title: Activity Map-Link nach Region
description: Ein verketteter Wert von Link und Region.
feature: Dimensions
role: User, Admin
exl-id: 33014dc1-da4e-47b7-b73c-3e89e04f3ed6
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# Activity Map-Link nach Region

&quot;Activity Map-Link nach Region“ [Dimension](overview.md) zeigt eine Verkettung von [Activity Map-Link](activity-map-link.md) und [Activity Map-Region](activity-map-link-by-region.md). Diese Dimension ist nützlich, wenn Sie Links haben, die ähnlich benannt sind, sich aber in verschiedenen Regionen Ihrer Site befinden. Wenn Sie beispielsweise über mehrere Links zu Ihrer Startseite verfügen, die alle als „Startseite“ gekennzeichnet sind, können Sie diese Dimension verwenden, um diese Links in den einzelnen Site-Regionen zu unterscheiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus den [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.link` und `c.a.activitymap.region` ab. Diese beiden Werte werden verkettet und durch ein Rohr (`|`) getrennt. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfassen diese Kontextdatenvariablen automatisch Daten, wenn auf Links geklickt wird.

## Dimensionselemente

Dimension-Elemente enthalten Werte aus [Activity Map-Link](activity-map-link.md) und [Activity Map-Region](activity-map-link-by-region.md). Die Site-Struktur und Implementierung Ihres Unternehmens bestimmt die erfassten Werte.
