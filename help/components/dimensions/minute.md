---
title: Minute
description: Die Minute, in der die Metrik aufgetreten ist.
feature: Dimensions
exl-id: 63f13083-321f-4fd8-9352-e413e1ebf168
TQID: https://experienceleague.adobe.com/GRivRprXBteGxRZieSI3uyjHALDJ-0hHbZx3S9ldJW0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 76%

---

# Minute

Die Dimension „Minute[ zeigt die ](overview.md) an, in der eine bestimmte Metrik aufgetreten ist (abgerundet). Das erste Dimensionselement ist die erste Minute im Datumsbereich und das letzte Dimensionselement die letzte Minute im Datumsbereich. Diese Dimension ist für Trend-Berichte hilfreich, da sie es Ihnen ermöglicht, Metriken im Zeitverlauf anzuzeigen. Angesichts der Granularität dieser Dimension empfiehlt Adobe, den Datumsbereich des Berichte auf ein oder zwei Tage zu begrenzen.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Die Dimensionelemente enthalten eine bestimmte Minute innerhalb des Datumsbereichs eines Berichts und deren Datum. Sie sind als `HH:MM YYYY-MM-DD` formatiert. Dimension-Elemente, die mit `00:00` beginnen, entsprechen an diesem Tag Mitternacht, während Werte, die mit `23:59` beginnen, :59 23 Uhr für diesen Tag entsprechen.
