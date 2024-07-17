---
title: Activity Map-Link nach Region
description: Ein verketteter Wert von Link und Region.
feature: Dimensions
role: User, Admin
source-git-commit: 65e75a1c2b39823e72abfb0e5b61122c62f1f013
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# Activity Map-Link nach Region

Die Dimension &quot;Activity Map-Link nach Region&quot;[](overview.md) enthält eine Verkettung von [Activity Map-Link](activity-map-link.md) und [Activity Map-Region](activity-map-link-by-region.md). Diese Dimension ist nützlich, wenn Sie Links haben, die auf ähnliche Weise benannt sind, sich aber in verschiedenen Regionen Ihrer Site befinden. Wenn Sie beispielsweise über mehrere Links zu Ihrer Startseite verfügen, die alle die Bezeichnung &quot;Startseite&quot;tragen, können Sie diese Dimension verwenden, um diese Links in den einzelnen Sitebereichen zu unterscheiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus den [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.link` und `c.a.activitymap.region` ab. Diese beiden Werte werden durch einen senkrechten Strich (`|`) verkettet und getrennt. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfassen diese Kontextdatenvariablen automatisch Daten, wenn auf Links geklickt wird.

## Dimensionselemente

Zu den Dimension-Elementen gehören Werte von [Activity Map-Link](activity-map-link.md) und [Activity Map-Region](activity-map-link-by-region.md). Die Site-Struktur und Implementierung Ihres Unternehmens bestimmt die exakten erfassten Werte.
