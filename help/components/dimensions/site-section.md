---
title: Website-Bereich
description: Der Name des Website-Bereichs.
feature: Dimensions
exl-id: 349bace0-4596-4b4c-bf29-6cd8866c246b
TQID: https://experienceleague.adobe.com/fZwN-24--98XULDEgHR-5dcIsiYXspaSOsv1t-M0iys
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
source-wordcount: 139
ht-degree: 90%

---

# Website-Bereich

Die Dimension „Site-Bereich[&#x200B; &#x200B;](overview.md) listet die Namen der Site-Bereiche auf Ihrer Site auf. Bei großen Sites ist es hilfreich, Seiten in Bereiche zu gruppieren. Diese Dimension ist nützlich, um die am meisten angezeigten oder leistungsstärksten Website-Bereiche anzuzeigen.

Diese Dimension hängt mit den Dimensionen [Seite](page.md) und [Server](server.md) zusammen. „Seite“ ist am detailliertesten, „Server“ am wenigsten detailliert und „Website-Bereich“ befindet sich zwischen den beiden.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`ch` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mit der [`channel`](/help/implement/vars/page-vars/channel.md)-Variable.

## Dimensionselemente

Zu den Dimensionselementen gehören die Namen der Website-Bereiche auf Ihrer Site. Ihr Unternehmen legt fest, welche spezifischen Dimensionselemente Sie verwenden möchten. Stellen Sie unabhängig von der verwendeten Methode sicher, dass sie konsistent ist und dass Sie sie in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.
