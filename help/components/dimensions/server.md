---
title: Server
description: Der Name des Servers.
feature: Dimensions
exl-id: c2454c0d-497e-46f8-8569-7d0517097cab
TQID: https://experienceleague.adobe.com/BDVwwy3jCtHrcWLy2nOHVnDRbFiAoR-EeOzp-35XjBs
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
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 61%
---
# Server

Die Dimension [Server](overview.md) listet normalerweise den Host-Namen der Site auf. Bei Report Suites, die mehrere Domänen oder Unterdomänen kombinieren, ist diese Dimension nützlich, um zu sehen, welche Domänen oder Unterdomänen die beste Leistung erbringen.

Diese Dimension hängt mit den Dimensionen [Seite](page.md) und [Website-Bereich](site-section.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Website-Bereich“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

AppMeasurement erfasst diese Daten mithilfe der [`server`](/help/implement/vars/page-vars/server.md)-Variablen, die funktionell mit einer Prop identisch ist.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`server`](/help/implement/vars/page-vars/server.md) |
| **Feld Web SDK/XDM** | [`web.webPageDetails.server`](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/data-types/webpage-details) |
| **Abfrageparameter** | [`server`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<server>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 100 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Die Dimensionselemente umfassen die Server auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Einige Organisationen verwenden `window.location.hostname`, während andere benutzerdefinierte Werte formulieren. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.
