---
title: Zeit pro Besuch
description: Die Zeit, die pro Besuch für das Dimensionselement verbracht wurde.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '259'
ht-degree: 100%

---


# Zeit pro Besuch (Sekunden)

*Auf dieser Hilfeseite wird beschrieben, wie „Zeit pro Besuch“ als Metrik funktioniert. Weitere Informationen finden Sie unter der Dimension [Zeit pro Besuch](../dimensions/time-spent-per-visit.md).*

Die Metrik „Zeit pro Besuch (Sekunden)“ gibt die durchschnittliche Zeit an, die Besucher während jedes Besuchs mit einem bestimmten Dimensionselement interagieren.

Diese Metrik ist aufgrund ihrer unterschiedlichen Verarbeitungsarchitektur nicht in Data Warehouse verfügbar.

## Berechnung dieser Metrik

Diese Metrik verwendet die Formel [`Total seconds spent`](total-seconds-spent.md) `divided by` ([`Visits`](visits.md) `minus` [`Bounces`](bounces.md)).

## Vergleich mit der durchschnittlichen Besuchszeit pro Site

Diese Metrik und die [Durchschnittliche Besuchszeit pro Site](average-time-on-site.md) sind ähnlich, weisen jedoch einige wesentliche Unterschiede auf. Beide Metriken verwenden „Gesamtbesuchszeit in Sekunden“ als Zähler. „Durchschnittliche Besuchszeit pro Site“ verwendet jedoch die Sequenzen, die ein Dimensionselement enthalten, als Nenner. „Zeit pro Besuch“ verwendet die Anzahl der Besuche als Nenner.

Aus diesem Grund geben diese Metriken ähnliche Ergebnisse auf Besuchsebene zurück, unterscheiden sich aber auf einer Trefferebene.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die Zeit pro Besuch der gesamten Dimension und der Zähler ist die Zeit pro Besuch des Dimensionselements. Wenn die Zeit pro Besuch der gesamten Dimension kürzer ist als die Zeit pro Besuch eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für die Zeit pro Besuch angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](time-spent.md).
