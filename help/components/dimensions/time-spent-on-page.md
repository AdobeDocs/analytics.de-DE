---
title: Besuchszeit pro Seite
description: Die Zeit, die ein Besucher auf der Seite verbracht hat.
feature: Dimensions
exl-id: 55af7286-7c37-48d2-925e-8b7ecb390e7f
TQID: https://experienceleague.adobe.com/2WS7gBdkpaYUvVqgoR5QTrPes2T2GJT5AEFyj9POcHA
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 85%

---

# Besuchszeit pro Seite

Die Dimension „Auf Seite verbrachte Zeit[&#x200B; erfasst &#x200B;](overview.md) Zeit, die eine Besucherin oder ein Besucher auf der Seite verbracht hat. Zur Berechnung werden die folgenden Schritte verwendet:

1. Sehen Sie sich für einen bestimmten Treffer den Zeitstempel an.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des nächsten Treffers im Besuch. Sowohl Seitenansichts- als auch Linktracking-Treffer werden gezählt.
3. Die Zeit, die zwischen diesen beiden Treffern verstrichen ist, zählt zur Besuchszeit.

Diese Dimension ist nützlich, wenn Sie verstehen möchten, wie lange Besucher mit einer bestimmten Metrik auf Ihrer Site interagieren.

>[!TIP]
>
>Die Besuchszeit wird beim letzten Treffer des Besuchs nicht gemessen, da keine nachfolgende Bildanforderung zur Messung der verstrichenen Zeit vorliegt. Dieses Konzept gilt auch für Besuche, die aus einem einzelnen Treffer (einem Absprung) bestehen.

Diese Dimension basiert auf Treffern, d. h. der Wert ist bei jedem Treffer unterschiedlich. Vergleichen Sie diese Dimension mit der [Zeit pro Besuch](time-spent-per-visit.md), die einer besuchsbasierten Dimension entspricht. Eine höhere Besuchszeit bedeutet, dass ein Besucher länger auf einer Seite bleibt (Treffer).

![Besuchszeit pro Seite](../metrics/assets/time-spent2.png)

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Für die Besuchszeit pro Seite gibt es mehrere Dimensionen:

* **Besuchszeit pro Seite – zusammengefasst**: Die Zeitdauer wird zusammengefasst. Dimensionselemente reichen von `"Less than 15 seconds"` bis `"More than 30 minutes"`. Die Zeit zwischen Treffern dauert in der Regel nicht länger als 30 Minuten. Bei der Verwendung von Treffern oder Datenquellen mit Zeitstempel können die Zeiten zwischen Treffern jedoch länger als 30 Minuten sein.
* **Besuchszeit pro Seite – präzise**: Jede Anzahl von Sekunden ist ein eindeutiges Dimensionselement.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](../metrics/time-spent.md).
