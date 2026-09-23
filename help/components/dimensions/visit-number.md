---
title: Besuchsnummer
description: Der n-te Besuch des Besuchers.
feature: Dimensions
exl-id: daef34b3-c270-476d-a45c-a20be6138c6b
TQID: https://experienceleague.adobe.com/C6fccfJFGSA4iLuhp2X80aPym4ZcwbrLMaUS2LUfosg
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
source-wordcount: '201'
ht-degree: 77%
---
# Besuchsnummer

Die [Dimension](overview.md) „Besuchsnummer“ gibt an, in welchem Besuch sich die Besucherin oder der Besucher gerade befindet. Wenn ein neuer Besuch beginnt, wird das Element dieser Dimension um 1 erhöht. Diese Dimension ist hilfreich, wenn Sie verstehen möchten, wie stark Besucher interagieren, wenn sie auf Ihre Site zurückkehren. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch und kann nicht geändert werden. Sie gilt für die Lebensdauer des Besuchers, unabhängig vom Datumsbereich des Projekts.

## Füllen dieser Dimension mit Daten

Adobe berechnet diese Dimension Server-seitig aus dem Besuchsverlauf des Besuchers. Es gibt keine Variable zum Festlegen. Dies ist bei allen Implementierungen vorkonfiguriert.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (berechnet von Adobe) |
| **Feld Web SDK/XDM** | Keine (berechnet von Adobe) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | Besuch |

## Dimensionselemente

Zu den Dimensionselementen zählen die Zeichenfolge `"Visit number"`, gefolgt von der numerischen Darstellung des Besuchs, in dem sich der Besucher derzeit befindet. Wenn der Besucher beispielsweise noch nie zuvor Ihre Site besucht hat, gehört sein erster Besuch zum Dimensionselement `"Visit number 1"`. Wenn dies der 13. Besuch des Besuchers auf Ihrer Site ist, gehört er zum Dimensionselement `"Visit number 13"`.
