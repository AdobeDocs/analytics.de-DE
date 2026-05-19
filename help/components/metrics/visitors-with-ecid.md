---
title: Besucher mit Experience Cloud ID
description: Die Anzahl der Unique Visitors, die den Adobe Experience Cloud ID Service verwenden.
feature: Metrics
exl-id: 16c170d0-3546-4e0a-8f3c-c141b8a0e4fe
TQID: https://experienceleague.adobe.com/CCk7FDZhZ3mFYXtAggcxnAjvJoJp5zMf0NNk5w0tVY8
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2:
  - id: e6c28e30-8689-4bf4-8fa8-561343d308a9
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 378
ht-degree: 76%

---

# Besucher mit Experience Cloud ID

Die Metrik „Besucher mit Experience Cloud-ID[&#x200B; &#x200B;](overview.md) gibt die Anzahl der Unique Visitors an, die von Adobe mithilfe des [Experience Cloud ID-Service identifiziert wurden](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de). Sie können diese Metrik mit der Metrik [Unique Visitors](unique-visitors.md) vergleichen, um sicherzustellen, dass die Mehrheit der Besucher Ihrer Site den Identity Service verwendet. Wenn ein Großteil der Besucher die Identity Service-Cookies nicht verwendet, kann dies auf ein Problem in Ihrer Implementierung hindeuten.

>[!NOTE]
>
>Diese Metrik ist besonders wichtig für das Debugging, wenn Sie mehrere CX Enterprise-Services verwenden, z. B. Adobe Target oder Adobe Audience Manager. Segmente, die für alle CX Enterprise-Produkte freigegeben sind, enthalten keine Besucher ohne Experience Cloud ID.

## Berechnung dieser Metrik

Diese Metrik basiert auf der Metrik [Unique Visitors](unique-visitors.md), mit der Ausnahme, dass sie nur die mit der `mid`-Abfragezeichenfolge identifizierten Personen enthält (basierend auf dem [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=de)-Cookie).

## Debuggen Ihres Experience Cloud ID-Setups

Die Metrik „Besucher mit Experience Cloud-ID“ kann bei der Fehlerbehebung bei CX Enterprise-Integrationen oder bei der Identifizierung von Bereichen Ihrer Site nützlich sein, für die der ID-Service nicht bereitgestellt ist.

Ziehen Sie die „Besucher mit Experience Cloud ID“ neben „Unique Visitors“, um sie zu vergleichen:

![Vergleich der Unique Visitors](assets/metric-mcvid1.png)

Beachten Sie Folgendes: In diesem Beispiel weist jede Seite eine identische Anzahl an Unique Visitors und Besuchern mit Experience Cloud ID auf. Die Gesamtanzahl an Unique Visitors ist dabei größer als die Gesamtanzahl an Besuchern mit Experience Cloud ID. Sie können eine [berechnete Metrik](../calculated-metrics/cm-overview.md) erstellen, um herauszufinden, welche Seiten den Identity Service nicht einrichten. Sie können die folgende Definition verwenden:

![Definition berechneter Metriken](assets/metric-mcvid2.png)

Wenn Sie die berechnete Metrik zum Bericht hinzufügen, können Sie den Seitenbericht so sortieren, dass die Seiten mit der größten Anzahl an Besuchern ohne MCID oben angezeigt werden:

![Seiten ohne Identity Service](assets/metric-mcvid3.png)

Beachten Sie, dass das Dimensionselement „Schnellansichten Produkt“ nicht ordnungsgemäß mit dem Identity Service implementiert ist. Sie können mit entsprechenden Teams in Ihrem Unternehmen zusammenarbeiten, um diese Seiten so schnell wie möglich zu aktualisieren. Sie können einen ähnlichen Bericht mit einer beliebigen Dimension wie [Browser-Typ](../dimensions/browser-type.md), [Website-Bereich](../dimensions/site-section.md) oder einer beliebigen [eVar](../dimensions/evar.md) erstellen.
