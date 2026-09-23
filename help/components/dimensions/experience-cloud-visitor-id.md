---
title: Experience Cloud-Besucher-ID
description: Die Experience Cloud-ID (ECID) des Besuchers, verfügbar in Data Warehouse.
feature: Dimensions
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
source-wordcount: '164'
ht-degree: 18%
---
# Experience Cloud-Besucher-ID

Die Dimension „Experience Cloud-Besucher[ID](overview.md) liefert die ECID für jeden Besucher. Es handelt sich um eine 128-Bit-Zahl, die aus zwei verketteten 64-Bit-Zahlen besteht, die auf 19 Stellen aufgefüllt sind.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar.

## Füllen dieser Dimension mit Daten

Diese Dimension erfordert eine Implementierung, die den Besucher-ID-Dienst (VisitorAPI) oder den Experience Platform Identity Service verwendet. Dies entspricht der `mcvisid` Spalte in Daten-Feeds. Siehe [Datenspaltenreferenz](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) für weitere Informationen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (vom Besucher-ID-Service von Experience Cloud festgelegt) |
| **Feld Web SDK/XDM** | Keine (vom Experience Cloud Identity Service festgelegt) |
| **Abfrageparameter** | [`mid`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<marketingCloudVisitorId>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Dimension-Elemente enthalten die Experience Cloud-ID jedes Besuchers bzw. jeder Besucherin.
