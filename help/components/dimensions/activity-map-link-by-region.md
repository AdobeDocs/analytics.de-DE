---
title: Activity Map-Link nach Region
description: Ein verketteter Wert von Link und Region.
feature: Dimensions
role: User, Admin
exl-id: 33014dc1-da4e-47b7-b73c-3e89e04f3ed6
TQID: https://experienceleague.adobe.com/xvYVA064hA0rsBdnLpxXllq3PD0zYAikFRjc6xNErvg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 11%

---

# Activity Map-Link nach Region

&quot;Activity Map-Link nach Region“ [Dimension](overview.md) zeigt eine Verkettung von [Activity Map-Link](activity-map-link.md) und [Activity Map-Region](activity-map-link-by-region.md). Diese Dimension ist nützlich, wenn Sie Links haben, die ähnlich benannt sind, sich aber in verschiedenen Regionen Ihrer Site befinden. Wenn Sie beispielsweise über mehrere Links zu Ihrer Startseite verfügen, die alle als „Startseite“ gekennzeichnet sind, können Sie diese Dimension verwenden, um diese Links in den einzelnen Site-Regionen zu unterscheiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus den [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.link` und `c.a.activitymap.region` ab. Diese beiden Werte werden verkettet und durch ein Rohr (`|`) getrennt. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfassen diese Kontextdatenvariablen automatisch Daten, wenn auf Links geklickt wird.

## Dimensionselemente

Dimension-Elemente enthalten Werte aus [Activity Map Link](activity-map-link.md) und [Activity Map Region](activity-map-link-by-region.md). Die Site-Struktur und Implementierung Ihres Unternehmens bestimmt die erfassten Werte.
