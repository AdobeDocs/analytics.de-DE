---
title: Experience Cloud-Besucher-ID
description: Die Experience Cloud-ID (ECID) des Besuchers, verfügbar in Data Warehouse.
feature: Dimensions
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 21%

---

# Experience Cloud-Besucher-ID

Die Dimension „Experience Cloud-Besucher[ID](overview.md) liefert die ECID für jeden Besucher. Es handelt sich um eine 128-Bit-Zahl, die aus zwei verketteten 64-Bit-Zahlen besteht, die auf 19 Stellen aufgefüllt sind.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar.

## Füllen dieser Dimension mit Daten

Diese Dimension erfordert eine Implementierung, die den Besucher-ID-Dienst (VisitorAPI) oder den Experience Platform Identity Service verwendet. Dies entspricht der `mcvisid` Spalte in Daten-Feeds. Siehe [Datenspaltenreferenz](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) für weitere Informationen.

## Dimensionselemente

Dimension-Elemente enthalten die Experience Cloud-ID jedes Besuchers bzw. jeder Besucherin.
