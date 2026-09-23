---
title: Besucher-ID
description: Die eindeutige Kennung für einen Besucher, verfügbar in Data Warehouse.
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
source-wordcount: '133'
ht-degree: 18%
---
# Besucher-ID

Die Dimension „Besucher[ID“ ](overview.md) die eindeutige Kennung für jeden Besucher an.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar.

## Füllen dieser Dimension mit Daten

Adobe generiert automatisch eine Besucher-ID für jeden Besucher. Dieser Wert ist derselbe wie der verkettete Wert der Spalten `visid_high` und `visid_low` in Daten-Feeds. Sie können den automatisch generierten Wert mit der Variablen `visitorID` überschreiben. Siehe [Datenspaltenreferenz](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) für weitere Informationen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`visitorID`](/help/implement/vars/config-vars/visitorid.md) |
| **Feld Web SDK/XDM** | Keine |
| **Abfrageparameter** | [`vid`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<visitorId>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 255 Byte |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Dimension-Elemente enthalten die eindeutige Kennung für jeden Besucher.
