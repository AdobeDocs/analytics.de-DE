---
title: Seite
description: Der Name der Seite.
feature: Dimensions
exl-id: 579963c8-8460-425f-b716-3b30d7a259af
TQID: https://experienceleague.adobe.com/npKfFB-zOPzNGJJ6YZvtz0oA3NDWuQiHYBraH09lc58
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4
    internal-label: Attribution
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
source-wordcount: '226'
ht-degree: 54%
---
# Seite

Die Dimension [Seite](overview.md) listet die Namen von Seiten auf Ihrer Site auf. Sie ist eine der am häufigsten verwendeten Dimensionen in Adobe Analytics, da sie Erkenntnisse darüber liefert, welche Seiten Ihrer Site die beste Leistung erbringen.

Diese Dimension hängt mit den Dimensionen [Website-Bereich](site-section.md) und [Server](server.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Website-Bereich“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

Legen Sie die [`pageName`](/help/implement/vars/page-vars/pagename.md) Variable in [Seitenansichtsaufrufe (`t()`) &#x200B;](/help/implement/vars/functions/t-method.md). Wenn die Variable `pageName` nicht festgelegt ist, wird diese Dimension auf die Verwendung der Variablen [`pageURL`](/help/implement/vars/page-vars/pageurl.md) zurückgesetzt. [Linktracking-Aufrufe (`tl()`)](/help/implement/vars/functions/tl-method.md) entfernen diese Dimension immer, auch wenn der `pageName` vorhanden ist.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`pageName`](/help/implement/vars/page-vars/pagename.md) |
| **Feld Web SDK/XDM** | [`web.webPageDetails.name`](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/data-types/webpage-details) |
| **Abfrageparameter** | [`pageName`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<pageName>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 100 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Seiten auf Ihrer Site. Ihr Unternehmen bestimmt, welche spezifischen Dimensionselemente Sie verwenden möchten. Einige Organisationen verwenden `document.title` direkt, während andere benutzerdefinierte Breadcrumbs formulieren. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.

>[!NOTE]
>
>Analysis Workspace verwendet standardmäßig die letzte Attribution mit der Option, ein beliebiges Attributionsmodell zu verwenden.
