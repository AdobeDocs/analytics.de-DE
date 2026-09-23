---
title: Wochentag
description: Der Wochentag, unabhängig vom Datumsbereich.
feature: Dimensions
exl-id: 01aa6b5f-49e6-4f86-97c7-8d0ff431e15b
TQID: https://experienceleague.adobe.com/9nudTrYTDMEFXSo81uUuw9KFT3mRPhZer3cX81AwoPM
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
source-wordcount: '167'
ht-degree: 62%
---
# Wochentag

Die Dimension „Wochentag“ [Dimension](overview.md) gibt den Wochentag an, an dem der Treffer aufgetreten ist. Dieser Bericht ist nützlich, wenn Sie einen Bericht nach Woche aufschlüsseln möchten, aber keine statischen Tage als Dimensionswerte wünschen. Er ist besonders nützlich als Dimension in terminierten Berichten, da diese Dimension mit jedem beliebigen Datumsbereich funktioniert.

## Füllen dieser Dimension mit Daten

Diese Dimension wird aus dem Zeitstempel jedes Treffers abgeleitet. Es gibt keine Variable zum Festlegen. Dies ist bei jeder Implementierung vorkonfiguriert.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom Trefferzeitstempel) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom Trefferzeitstempel) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | Treffer |

## Dimensionselemente

Zu den Dimensionselementen gehören `Sunday` – `Saturday`, die den Wochentag des Treffers darstellen. Die Reihenfolge der Dimensionselemente berücksichtigt standardmäßig den ersten Wochentag in [Kalender anpassen](/help/admin/tools/manage-rs/edit-settings/general/custom-calendar.md).
