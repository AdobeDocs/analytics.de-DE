---
title: Tag
description: Der Tag, an dem die Metrik aufgetreten ist.
feature: Dimensions
exl-id: 2f93ae8b-422c-4e1e-81d3-43cc0aa442c4
TQID: https://experienceleague.adobe.com/q9gioxGcmj2xB-yamZUyM3jLLlTpT4NHq1CFCMqm-6I
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
source-wordcount: '149'
ht-degree: 59%
---
# Tag

Die „Tag[-Dimension](overview.md) zeigt den Tag an, an dem eine bestimmte Metrik aufgetreten ist. Das erste Dimensionselement ist der erste Tag im Datumsbereich und das letzte Dimensionselement der letzte Tag im Datumsbereich. Diese Dimension ist für Trend-Berichte von entscheidender Bedeutung, da sie es Ihnen ermöglicht, Metriken im Zeitverlauf anzuzeigen.

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

Die Dimensionelemente umfassen das Datum eines bestimmten Tages. Sie umfassen den Monat, den Tag und das Jahr als Teil des Dimensionselements.
