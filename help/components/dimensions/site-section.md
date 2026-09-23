---
title: Website-Bereich
description: Der Name des Site-Abschnitts.
feature: Dimensions
exl-id: 349bace0-4596-4b4c-bf29-6cd8866c246b
TQID: https://experienceleague.adobe.com/fZwN-24--98XULDEgHR-5dcIsiYXspaSOsv1t-M0iys
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
source-wordcount: '179'
ht-degree: 66%
---
# Website-Bereich

Die Dimension „Site-Bereich[&#x200B; &#x200B;](overview.md) listet die Namen der Site-Bereiche auf Ihrer Site auf. Bei großen Sites ist es hilfreich, Seiten in Abschnitte zu gruppieren. Diese Dimension ist nützlich, um die am meisten angezeigten oder leistungsstärksten Site-Abschnitte anzuzeigen.

Diese Dimension hängt mit den Dimensionen [Seite](page.md) und [Server](server.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Site-Abschnitt“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

AppMeasurement erfasst diese Daten mit der [`channel`](/help/implement/vars/page-vars/channel.md)-Variable.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`channel`](/help/implement/vars/page-vars/channel.md) |
| **Feld Web SDK/XDM** | [`web.webPageDetails.siteSection`](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/data-types/webpage-details) |
| **Abfrageparameter** | [`ch`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<channel>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 100 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Site-Abschnitte auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.
