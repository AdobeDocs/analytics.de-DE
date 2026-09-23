---
title: Rangansicht aller Suchseiten
description: Bestimmen Sie, welche Seite in einer Suchmaschine ein Besucher zu Ihrer Site durchgeklickt hat.
feature: Dimensions
exl-id: 58ce54c3-cc45-4e84-a14d-5fec0b70f50f
TQID: https://experienceleague.adobe.com/U7WgtQDXInyD1gXeBntncC9Fao1Rdc9W4AHFgx07T4A
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
source-wordcount: '201'
ht-degree: 62%
---
# Rangansicht aller Suchseiten

Der „Rang aller Suchseiten“ [Dimension](overview.md) liefert insight, auf welcher Suchergebnisseite ein Besucher auf Ihre Site geklickt hat. Wenn Ihre Site beispielsweise auf der zweiten Seite der Suchergebnisse einer Suchmaschine erscheint, ist das Dimensionselement für diese Variable „Suchseite 2“.

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension von der Suchmaschine (Referrer[ jedes Treffers ](referrer.md) und bestimmt, durch welche Seite mit Suchergebnissen der Besucher klickte. Es gibt keine Variable zum Festlegen. Damit diese Dimension funktioniert, müssen die [internen URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) in Ihrer Report Suite korrekt eingerichtet sein.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom Suchmaschinen-Referrer) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom Suchmaschinen-Referrer) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Wenn ein Besucher von einer Suchmaschine zu Ihrer Site durchklickt, lautet der Wert dieser Dimension „Suchseite“, gefolgt von der Seitenzahl, auf der er durchgeklickt hat. Wenn ein Treffer nicht von einer Suchmaschine stammt, lautet der Wert dieser Dimension „Nicht angegeben“.
