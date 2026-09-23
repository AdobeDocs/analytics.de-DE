---
title: Kauf-ID
description: Die eindeutige Kennung für einen Kauf, die in Data Warehouse verfügbar ist.
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
source-wordcount: '124'
ht-degree: 18%
---
# Kauf-ID

Die „Kauf-ID[&#x200B; (Dimension](overview.md) stellt die eindeutige Kennung für einen Kauf bereit.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar.

## Füllen dieser Dimension mit Daten

Diese Dimension wird mithilfe der [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) festgelegt. Dies entspricht der `purchaseid` Spalte in Daten-Feeds. Siehe [Datenspaltenreferenz](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) für weitere Informationen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) |
| **Feld Web SDK/XDM** | [`commerce.order.purchaseID`](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/field-groups/event/commerce-details) |
| **Abfrageparameter** | [`purchaseID`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<purchaseId>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 20 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Dimension-Elemente enthalten die Kauf-IDs, die auf Ihrer Site erfasst wurden.
