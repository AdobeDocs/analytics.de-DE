---
title: Vormittag/Nachmittag
description: Bestimmt, ob der Treffer am Vormittag oder am Nachmittag stattgefunden hat.
feature: Dimensions
exl-id: 93fcdb9f-2ba3-402c-a389-b02ed8c990d2
TQID: https://experienceleague.adobe.com/R1syrJ7ylIe2ywH1isX4sjR2O84-8eL-jooYhjUdKhI
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
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 33%
---
# Vormittag/Nachmittag

„AM/PM“ [Dimension](overview.md) gibt insight an, ob der Treffer während der Vormittags- oder Nachmittagszeit stattgefunden hat. Die Uhrzeit des Treffers basierend auf der [Zeitzone der Report Suite](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md).

## Füllen dieser Dimension mit Daten

Diese Dimension wird aus dem Zeitstempel jedes Treffers abgeleitet. Es gibt keine Variable, die festgelegt werden kann. Ihre einzige Abhängigkeit ist die Zeitzone der Report Suite, die bestimmt, welche Stunden AM sind und welche PM.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom Trefferzeitstempel) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom Trefferzeitstempel) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | Treffer |

## Dimensionselemente

Diese Dimension enthält immer genau zwei Dimensionselemente: `"AM"` und `"PM"`. Das Dimensionselement `"AM"` gilt für alle Treffer von 12:00 bis 11:59 Uhr, während das Dimensionselement `"PM"` für alle Treffer von 12:00 bis 23:59 Uhr gilt.
