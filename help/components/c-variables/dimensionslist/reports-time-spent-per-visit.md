---
description: 'null'
solution: Analytics
title: Zeit pro Besuch
topic: Berichte
uuid: 76441e36-b7fe-4cf3-8d72-c51d558afa13
translation-type: tm+mt
source-git-commit: 77eac41cdcfe0ad71ffe81525f6de4dc6b2b48d4

---


# Zeit pro Besuch

Adobe Analytics bietet mehrere Möglichkeiten, die in Analytics-Berichten verbrachte Zeit zu bestimmen. In den meisten Fällen wird die Besuchszeit anhand der folgenden Schritte berechnet:

1. Betrachten Sie bei einem bestimmten Besuch den Zeitstempel des ersten Treffers.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des letzten Treffers des Besuchs.
3. Die Zeit, die zwischen diesen beiden Treffern vergangen ist, bestimmt die Zeit, die für diesen Besuch verbracht wurde.

Beachten Sie beim Anzeigen der Daten zur Besuchszeit von Dimensionen Folgendes:

* Sowohl Seitenansichten als auch die Linktracking-Treffertypen werden bei der Berechnung der Besuchszeitdaten berücksichtigt.
* Die Besuchszeit wird beim letzten Treffer des Besuchs nicht gemessen, da keine nachfolgende Bildanforderung zur Messung der verstrichenen Zeit vorliegt.
* Absprünge können die Besuchszeit nicht messen, da der Besuch aus einem einzelnen Treffer besteht.

Die Zeit pro Besuch misst die gesamte verstrichene Zeit eines Besuchs. Es gibt separate Dimensionen zwischen **granular** und **zusammengefasst**.

* **** Granular: Bei jedem Dimensionswert handelt es sich um eine andere Anzahl von Sekunden, aus denen ein Besuch besteht.
* **** Zusammengefasst: Jeder Dimensionswert ist ein vordefinierter Behälter:
   * Weniger als 1 Minute
   * 1-5 Minuten
   * 5-10 Minuten
   * 30-60 Minuten
   * 1-2 Stunden
   * 2-5 Stunden
   * 5-10 Stunden
   * 10-15 Stunden
   * Über 15 Stunden

> [!NOTE] [Besuche](../c-metrics/metrics-visit.md) enden in der Regel nach 12 Stunden Aktivität. Besuche können jedoch 12 Stunden überschreiten, wenn Treffer mit Zeitstempel oder Datenquellen verwendet werden.

Diese Dimension basiert auf Besuchen. Vergleichen Sie diese Dimension mit der auf der Seite[verbrachten ](reports-time-spent-on-page.md)Zeit (eine trefferbasierte Dimension).
