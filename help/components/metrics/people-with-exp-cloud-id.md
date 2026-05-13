---
title: Personen mit Experience Cloud ID
description: Die Anzahl der Personen in der geräteübergreifenden Analyse, die über eine Experience Cloud ID verfügen.
feature: Metrics
exl-id: 072e7d2b-3a08-49c6-a892-4cea2cc10159
TQID: https://experienceleague.adobe.com/w85poHKHnDYQ0iTItr2r26q1aRpN50AsdYzg6v82Jpk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 85%

---

# Personen mit Experience Cloud ID

„Personen mit Experience Cloud-ID“ ist eine Metrik der [geräteübergreifenden Analyse](../cda/overview.md), die die Anzahl der [Personen](people.md) anzeigt, die von Adobe mithilfe des [Experience Cloud ID-Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) identifiziert wurden.

## Berechnung dieser Metrik

Bei jedem [Personen](people.md) (identifiziert oder nicht identifiziert) erhöht sich diese [Metrik](overview.md), wenn der Treffer die `mid` Abfragezeichenfolge enthält (basierend auf dem [`s_ecid`](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-analytics.html?lang=de)-Cookie).

Sie können die berechnete Metrik `[People with ECID] ÷ [People]` erstellen, um mithilfe des ID-Service den Prozentsatz der Besucher Ihrer Site festzustellen.

Weitere Informationen zur Bedeutung der Experience Cloud-ID und zum Debugging Ihres Setups finden Sie unter der entsprechenden Metrik der nicht-geräteübergreifenden Analyse [Besucher mit Experience Cloud ID](visitors-with-ecid.md).
