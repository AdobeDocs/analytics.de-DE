---
title: Personen mit Experience Cloud ID
description: Die Anzahl der Personen in der geräteübergreifenden Analyse, die über eine ECID verfügen.
feature: Metrics
exl-id: 072e7d2b-3a08-49c6-a892-4cea2cc10159
TQID: https://experienceleague.adobe.com/w85poHKHnDYQ0iTItr2r26q1aRpN50AsdYzg6v82Jpk
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 0ba418a49e6a226540e0791f0138027566022d6f
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 28%
---
# Personen mit Experience Cloud ID

„Personen mit Experience Cloud-ID“ ist eine Metrik [Geräteübergreifende Analyse](../cda/overview.md) die die Anzahl der [Personen](people.md) anzeigt, die von Adobe mithilfe des [Besucher-ID-Service](https://experienceleague.adobe.com/de/docs/id-service/using/home) oder [Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/identity/overview) wurden.

## Berechnung dieser Metrik

Bei jedem [Personen](people.md) (identifiziert oder nicht identifiziert) erhöht sich diese [Metrik](overview.md), wenn der Treffer die `mid` Abfragezeichenfolge enthält (basierend auf dem [`s_ecid`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics)-Cookie).

Sie können die berechnete Metrik `[People with ECID] ÷ [People]` erstellen, um mithilfe des ID-Service den Prozentsatz der Besucher Ihrer Site festzustellen.

Weitere Informationen zur Bedeutung von ECID und zum Debugging Ihres Setups finden Sie unter [&#x200B; entsprechenden Metrik der nicht-geräteübergreifenden Analyse &#x200B;](visitors-with-ecid.md)Besucher mit Experience Cloud-ID) .
