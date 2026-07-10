---
title: Besucher mit Experience Cloud ID
description: Die Anzahl der Unique Visitors, die eine ECID verwenden.
feature: Metrics
exl-id: 16c170d0-3546-4e0a-8f3c-c141b8a0e4fe
TQID: https://experienceleague.adobe.com/CCk7FDZhZ3mFYXtAggcxnAjvJoJp5zMf0NNk5w0tVY8
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
subfeature_v2: id: e6c28e30-8689-4bf4-8fa8-561343d308a9id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 384
ht-degree: 25%

---

# Besucher mit Experience Cloud ID

Die [Metrik[!UICONTROL Besucher mit Experience Cloud-ID] gibt ](overview.md) Anzahl der Unique Visitors an, die von Adobe mit einer ECID identifiziert wurden (mithilfe des [Besucher-ID-](https://experienceleague.adobe.com/de/docs/id-service/using/home) oder [Experience Platform Identity Service](https://experienceleague.adobe.com/de/docs/experience-platform/identity/home)). Sie können diese Metrik mit der Metrik [Unique Visitors](unique-visitors.md) vergleichen, um sicherzustellen, dass die Mehrheit der Besucher Ihrer Site eine ECID verwendet. Wenn ein großer Teil der Besucher diese Kennung nicht verwendet, kann dies auf ein Problem innerhalb Ihrer Implementierung hinweisen.

>[!NOTE]
>
>Diese Metrik ist besonders wichtig für das Debugging, wenn Sie mehrere CX Enterprise-Services verwenden, z. B. Adobe Target oder Adobe Audience Manager. Segmente, die für alle CX Enterprise-Produkte freigegeben sind, enthalten keine Besucher ohne ECID.

## Berechnung dieser Metrik

Diese Metrik basiert auf der Metrik [Unique Visitors](unique-visitors.md), mit der Ausnahme, dass sie nur die mit der `mid`-Abfragezeichenfolge identifizierten Personen enthält (basierend auf dem [`s_ecid`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics)-Cookie).

## Debuggen des ECID-Setups

Die Metrik [!UICONTROL Besucher mit Experience Cloud-ID]&quot; kann bei der Fehlerbehebung bei CX Enterprise-Integrationen oder bei der Identifizierung von Bereichen Ihrer Site nützlich sein, die nicht über den Besucher-ID-Service oder Experience Platform Identity Service verfügen.

Ziehen Sie &quot;[!UICONTROL Besucher mit Experience Cloud ID]&quot; nebeneinander mit „Unique Visitors“, um sie zu vergleichen:

![Vergleich der Unique Visitors](assets/metric-mcvid1.png)

Beachten Sie in diesem Beispiel, dass jede Seite dieselbe Anzahl von &quot;[!UICONTROL Unique Visitors“ ] &quot;[!UICONTROL Visitors with Experience Cloud ID]&quot; aufweist. Die Gesamtzahl der &quot;[!UICONTROL Unique Visitors]&quot; ist jedoch größer als die Gesamtzahl der &quot;[!UICONTROL Visitors mit Experience Cloud ID]&quot;. Sie können eine [berechnete Metrik](../calculated-metrics/cm-overview.md) erstellen, um mithilfe der folgenden Definition herauszufinden, welche Seiten keine ECID verwenden:

![Definition berechneter Metriken](assets/metric-mcvid2.png)

Durch Hinzufügen der berechneten Metrik zum Bericht können Sie den Seitenbericht so sortieren, dass die Seiten mit der höchsten Besucherzahl ohne ECID angezeigt werden:

![Seiten ohne ECID](assets/metric-mcvid3.png)

Beachten Sie, dass das Dimensionselement „Produktschnellansichten“ mit einer ECID nicht ordnungsgemäß implementiert ist. Sie können mit entsprechenden Teams in Ihrem Unternehmen zusammenarbeiten, um diese Seiten so schnell wie möglich zu aktualisieren. Sie können einen ähnlichen Bericht mit einer beliebigen Dimension wie [Browser-Typ](../dimensions/browser-type.md), [Website-Bereich](../dimensions/site-section.md) oder einer beliebigen [eVar](../dimensions/evar.md) erstellen.
