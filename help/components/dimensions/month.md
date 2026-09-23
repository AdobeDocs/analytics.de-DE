---
title: Monat
description: Der Monat, in dem die Metrik aufgetreten ist.
feature: Dimensions
exl-id: 77f7aa91-ea2e-482f-9a29-35912efb967a
TQID: https://experienceleague.adobe.com/wLCMW-pAsREGJV84IBPuae75Rwz6dWhL8TyxedyeH-U
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
source-wordcount: '138'
ht-degree: 56%
---
# Monat

Die Dimension „Monat[&#x200B; zeigt &#x200B;](overview.md) Monat an, in dem eine bestimmte Metrik aufgetreten ist. Das erste Dimensionselement ist der erste Monat im Datumsbereich und das letzte Dimensionselement der letzte Monat im Datumsbereich. Diese Dimension ist für Trend-Berichte von entscheidender Bedeutung, da sie es Ihnen ermöglicht, Metriken im Zeitverlauf anzuzeigen.

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

Die Dimensionselemente umfassen den Monat und das Jahr eines bestimmten Datums.
