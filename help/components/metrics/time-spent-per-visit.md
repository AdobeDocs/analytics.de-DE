---
title: Besuchszeit pro Besuch (Metriken)
description: Die Zeit, die pro Besuch für das Dimensionselement verbracht wurde.
feature: Metrics
exl-id: 0f951196-66a2-4733-bb62-4555a9331efb
TQID: https://experienceleague.adobe.com/X1RtHTTmu0VIblFC3jANE7d6bIbtm4W5OvqFZDp8bLE
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 263
ht-degree: 88%

---

# Zeit pro Besuch (Sekunden)

*Auf dieser Hilfeseite wird beschrieben, wie „Zeit pro Besuch“ als Metrik funktioniert. Weitere Informationen finden Sie unter der Dimension [Zeit pro Besuch](../dimensions/time-spent-per-visit.md).*

Die [Metrik „Aufgewendete Zeit pro Besuch (Sekunden)“ &#x200B;](overview.md) die durchschnittliche Zeit an, die Besucherinnen und Besucher während jedes Besuchs mit einem bestimmten Dimensionselement interagieren.

Diese Metrik ist aufgrund ihrer unterschiedlichen Verarbeitungsarchitektur nicht in Data Warehouse verfügbar.

## Berechnung dieser Metrik

Diese Metrik verwendet die Formel [`[Total seconds spent]`](total-seconds-spent.md) `divided by (`[`[Visits]`](visits.md) `minus` [`[Bounces]`](bounces.md)`)`.

## Vergleich mit der durchschnittlichen Besuchszeit pro Site

Diese Metrik und die [Durchschnittliche Besuchszeit pro Site](average-time-on-site.md) sind ähnlich, weisen jedoch einige wesentliche Unterschiede auf. Beide Metriken verwenden „Gesamtbesuchszeit in Sekunden“ als Zähler. „Durchschnittliche Besuchszeit pro Site“ verwendet jedoch die Sequenzen, die ein Dimensionselement enthalten, als Nenner. „Zeit pro Besuch“ verwendet die Anzahl der Besuche als Nenner.

Aus diesem Grund geben diese Metriken ähnliche Ergebnisse auf Besuchsebene zurück, unterscheiden sich aber auf einer Trefferebene.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die Zeit pro Besuch der gesamten Dimension und der Zähler ist die Zeit pro Besuch des Dimensionselements. Wenn die Zeit pro Besuch der gesamten Dimension kürzer ist als die Zeit pro Besuch eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für die Zeit pro Besuch angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](time-spent.md).
