---
title: Wochentag/Wochenende
description: Bestimmt, ob der Treffer an einem Wochentag oder an einem Wochenende stattgefunden hat.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
TQID: https://experienceleague.adobe.com/9TJv-49ub1zHsgEGtBeoJVoHhsBktlOr7QhmgLdLRSo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
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
source-wordcount: '155'
ht-degree: 49%
---
# Wochentag/Wochenende

Die Dimension „Wochentag/Wochenende[&#x200B; gibt insight &#x200B;](overview.md), ob der Treffer an einem Wochentag (Montag bis Freitag) oder am Wochenende (Samstag bis Sonntag) stattgefunden hat. Die Uhrzeit des Treffers basierend auf der [Zeitzone der Report Suite](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md).

## Füllen dieser Dimension mit Daten

Diese Dimension wird aus dem Zeitstempel jedes Treffers abgeleitet. Es gibt keine Variable, die festgelegt werden kann. Seine einzige Abhängigkeit ist die Zeitzone der Report Suite, die den Wochentag für jeden Treffer bestimmt.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom Trefferzeitstempel) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom Trefferzeitstempel) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | Treffer |

## Dimensionselemente

Diese Dimension enthält immer genau zwei Dimensionselemente: `"Weekday"` und `"Weekend"`. Das Dimensionselement `"Weekday"` gilt für alle Treffer von Montag bis Freitag, während das Dimensionselement `"Weekend"` für alle Treffer am Samstag und Sonntag gilt.
