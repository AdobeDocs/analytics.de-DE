---
title: Einzelseitenbesuche (Dimensionen)
description: Eine Markierung, die angibt, dass der Besuch nur aus einer einzelnen Seite bestand.
feature: Dimensions
exl-id: f7b58941-add4-4e7b-8645-a64280fd9dcb
TQID: https://experienceleague.adobe.com/mMxxlVpQi7IsSuxSZGijnvWeoqCa-ybf8otPRDf6AyQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
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
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 64%
---
# Einzelseitenbesuche

>[!BEGINSHADEBOX]

*Auf dieser Hilfeseite wird beschrieben, wie „Einzelseitenbesuche“ als [Dimension“ &#x200B;](overview.md). Weitere Informationen finden Sie unter der Metrik [Einzelseitenbesuche](../metrics/single-page-visits.md).*

>[!ENDSHADEBOX]

Die Dimension „Einzelseitenbesuche“ gibt die Anzahl der Besuche an, die aus einem einzigen eindeutigen Dimensionselement für [Seite](page.md) bestanden. Es handelt sich um die Dimension, die der Metrik [Einzelseitenbesuche](../metrics/single-page-visits.md) entspricht.

Diese Dimension wird am häufigsten als Komponente in der [Segmentierung](../segmentation/seg-home.md) verwendet. Sie wird normalerweise nicht als Dimension in Berichten verwendet.

## Füllen dieser Dimension mit Daten

Adobe berechnet diese Dimension Server-seitig, indem es bewertet, ob jeder Besuch eine einzelne eindeutige Seite enthielt. Es gibt keine Variable zum Festlegen. Dies ist bei allen Implementierungen vorkonfiguriert.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (berechnet von Adobe) |
| **Feld Web SDK/XDM** | Keine (berechnet von Adobe) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Das einzige Dimensionselement ist `"Enabled"`. Wenn ein Besuch aus einer einzelnen Seite besteht, wird der Treffer auf diesen Wert festgelegt. Alle anderen Treffer werden in diesem Bericht ausgelassen.
