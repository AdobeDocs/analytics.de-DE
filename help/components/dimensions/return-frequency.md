---
title: Rückkehrhäufigkeit
description: Die zusammengefasste Zeitspanne zwischen dem aktuellen Besuch und dem vorherigen Besuch.
feature: Dimensions
exl-id: 8ec31e17-a57d-416f-b471-c2c37a98d134
TQID: https://experienceleague.adobe.com/k0H7kOCgrBRY3cZckPXaJ9UgLBPTYWHxKT8gzeMQjcI
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
source-wordcount: '282'
ht-degree: 76%
---
# Rückkehrhäufigkeit

Die Dimension [Häufigkeit der Rückkehr](overview.md) gibt die Zeitspanne an, die zwischen Besuchen von wiederkehrenden Besuchern vergeht. Wenn eine Besucherin bzw. ein Besucher zu Ihrer Site zurückkehrt, prüft Adobe, wie lange der vorherige Besuch zurückliegt, und ordnet den Treffer dem entsprechenden Dimensionswert zu. Diese Dimension ist nützlich, um die Attraktivität und Relevanz Ihrer Website für Besucher im Zeitverlauf einzuschätzen. Sie kann auch dazu beitragen, die Auswirkungen der Inhalte und Werbeaktionen Ihrer Website auf Ihre Besucher zu ermitteln.

>[!TIP]
>
>Diese Dimension umfasst keine erstmaligen Besucher.

## Füllen dieser Dimension mit Daten

Adobe berechnet diese Dimension Server-seitig, indem der aktuelle Besuch mit dem vorherigen Besuch des Besuchers verglichen wird. Es gibt keine Variable zum Festlegen. Dies ist bei allen Implementierungen vorkonfiguriert.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (berechnet von Adobe) |
| **Feld Web SDK/XDM** | Keine (berechnet von Adobe) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | Besuch |

## Dimensionselemente

Zu den Dimensionswerten gehören zeitbasierte Buckets, abhängig von der seit ihrem letzten Besuch verstrichenen Zeit.

* Weniger als ein Tag
* 1 bis 3 Tage
* 3 bis 7 Tage
* 7 bis 14 Tage
* 14 Tage bis 1 Monat
* Länger als 1 Monat

## Dimensionswerte werden in Buckets außerhalb des Datumsbereichs des Projekts angezeigt.

Wenn Sie den Datumsbereich eines Projekts festlegen, können Sie üblicherweise Dimensionselemente sehen, die sich auf Besuche außerhalb des Datumsbereichs beziehen. Eine Besucherin bzw. ein Besucher kommt beispielsweise im Juli auf Ihre Site und kehrt im September zweimal am selben Tag zurück. Die Dimension „Rückkehrhäufigkeit“ für den Monat September würde einen Besuch unter „Länger als 1 Monat“ und einen Besuch unter „Weniger als 1 Tag“ anzeigen.
