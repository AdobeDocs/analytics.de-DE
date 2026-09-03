---
title: Server
description: Der Name des Servers.
feature: Dimensions
exl-id: c2454c0d-497e-46f8-8569-7d0517097cab
TQID: https://experienceleague.adobe.com/BDVwwy3jCtHrcWLy2nOHVnDRbFiAoR-EeOzp-35XjBs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 92%

---

# Server

Die Dimension [Server](overview.md) listet normalerweise den Host-Namen der Site auf. Bei Report Suites, die mehrere Domänen oder Unterdomänen kombinieren, ist diese Dimension nützlich, um zu sehen, welche Domänen oder Unterdomänen die beste Leistung erbringen.

Diese Dimension hängt mit den Dimensionen [Seite](page.md) und [Website-Bereich](site-section.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Website-Bereich“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`server` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`server`](/help/implement/vars/page-vars/server.md)-Variable.

## Dimensionselemente

Die Dimensionselemente umfassen die Server auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Einige Organisationen verwenden `window.location.hostname`, während andere benutzerdefinierte Werte formulieren. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.
