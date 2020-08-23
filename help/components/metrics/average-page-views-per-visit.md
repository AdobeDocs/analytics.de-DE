---
title: Durchschnittliche Seitenansichten pro Besuch
description: Die durchschnittliche Häufigkeit, mit der ein bestimmtes Dimensionselement während eines Besuchs angezeigt wurde.
translation-type: tm+mt
source-git-commit: 226bbce18750825d459056ac2a87549614eb3c2c
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 46%

---


# Durchschnittliche Seitenansichten pro Besuch

Die Dimension „Durchschnittliche Seitenansichten pro Besuch“ gibt an, wie viele Seitenansichten durchschnittlich in Ihrer gewünschten Dimension aufgetreten sind. Bei zeitbasierten Dimensionen können Sie sehen, wie sich die durchschnittliche Anzahl der Seitenansichten innerhalb eines Besuchs im Zeitverlauf entwickelt. Diese Metrik ist hilfreich, wenn Sie wissen möchten, wie oft Dimensionselemente bei einem Besuch angezeigt werden.

>[!TIP]
>
>Use this metric alongside another metric (such as [Visits](visits.md)) to obtain better insights. Wenn Sie diese Metrik selbst verwenden, erhalten Sie Dimensionselemente, die abweichende Ansichten pro Besuch enthalten. Dies ist in der Regel nicht wertvoll.

## Berechnung dieser Metrik

Diese Metrik wird mit der Formel [`Page views`](page-views.md)` divided by `[`Visits`](visits.md) berechnet.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die durchschnittliche Seitenanzahl der gesamten Dimension pro Besuch und der Zähler ist die durchschnittliche Ansicht des Dimensionselements pro Besuch. Wenn die durchschnittliche Ansicht der Seite pro Besuch der gesamten Dimension unter der durchschnittlichen Ansicht eines Dimensionselements pro Besuch liegt, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für durchschnittlichen Seitenansichten pro Besuch angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.