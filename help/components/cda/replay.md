---
title: Funktionsweise der Wiederholung
description: Verstehen Sie das Konzept der „Wiederholung“ in der geräteübergreifenden Analyse.
exl-id: 0b7252ff-3986-4fcf-810a-438d9a51e01f
source-git-commit: d4a70859027508cdd64affbb506fc64a3c4806cb
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 95%

---

# Funktionsweise der Wiederholung

Cross-Device Analytics führt in einer virtuellen Report Suite zwei Durchgänge an Daten durch:

* **Live-Stitching**: die geräteübergreifende Analyse versucht, jeden Treffer beim Eintreten zu zuzuordnen. Neue Geräte in der Report Suite, die sich noch nie angemeldet haben, werden in der Regel nicht auf dieser Ebene zugeordnet. Bereits erkannte Geräte werden sofort zugeordnet.
* **Wiederholung**: Ungefähr einmal pro Woche „wiederholt“ die geräteübergreifende Analyse die Daten anhand der gelernten eindeutigen Kennungen. In dieser Phase werden neue Geräte in der Report Suite zugeordnet.

## Beispieltabelle

Die folgenden Tabellen veranschaulichen, wie beide CDA-Methoden ([Feldbasiertes Stitching](field-based-stitching.md) und [Gerätediagramm](device-graph.md)) die Anzahl der eindeutigen Personen berechnen:

### Live-Stitching

Sobald ein Treffer erfasst wird, versucht die geräteübergreifende Analyse, ihn bekannten Geräten zuzuordnen. Betrachten wir das folgende Beispiel, in dem Bob zwei Geräte verwendet.

*Daten, wie sie am Tag der Erfassung erscheinen:*

| Zeitstempel | ECID | eVar1 oder CustomerID | Erläuterung des Treffers | Metrik „Personen“ (kumulativ) mit Gerätediagramm | Metrik „Personen“ (kumulativ) mit feldbasiertem Stitching |
| --- | --- | --- | --- | --- | --- |
| `1` | `246` | – | Bob auf seinem Desktop-Computer, nicht authentifiziert | `1` (246) | `1` (246) |
| `2` | `246` | `Bob` | Bob meldet sich auf seinem Desktop an. | `1` (246) | `2` (246 und Bob) |
| `3` | `3579` | – | Bob auf seinem Mobilgerät, nicht authentifiziert | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `4` | `3579` | `Bob` | Bob meldet sich auf einem Mobilgerät an | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `5` | `246` | – | Bob greift erneut auf Ihre Site auf dem Desktop zu, nicht authentifiziert | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `6` | `246` | `Bob` | Bob meldet sich erneut auf seinem Desktop an | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `7` | `3579` | – | Bob ruft Ihre Site erneut auf einem Mobilgerät auf | `2` (246 und 3579) | `3` (246, Bob und 3579) |
| `8` | `3579` | `Bob` | Bob meldet sich erneut auf einem Mobilgerät an | `2` (246 und 3579) | `3` (246, Bob und 3579) |

Sowohl nicht authentifizierte als auch authentifizierte Treffer auf neuen Geräten werden (vorübergehend) als separate Personen gezählt.

* **Wenn Sie das Gerätediagramm verwenden**, werden nicht authentifizierte Treffer auf erkannten Geräten live zugeordnet, sobald ein Cluster vom Gerätediagramm veröffentlicht wird. Die Veröffentlichung von Clustern dauert zwischen drei Stunden und zwei Wochen.

   Eine dritte kumulative Person wird ebenfalls hinzugefügt, wenn ein Cluster veröffentlicht wird. Diese dritte Person repräsentiert den Cluster selbst, zusätzlich zu den einzelnen Geräten. Diese dritte „Person“ bleibt bestehen, bis die Daten wiedergegeben werden.

   Die Zuordnung funktioniert geräteübergreifend erst nach der Veröffentlichung eines Clusters, und selbst dann wird erst ab diesem Zeitpunkt live zugeordnet. Im obigen Beispiel werden noch keine Treffer geräteübergreifend zugeordnet. Die geräteübergreifende Attribution bei vorhandenen Treffern funktioniert erst nach der Wiederholungszuordnung.
* **Wenn feldbasiertes Stitching verwendet wird**, werden nicht authentifizierte Treffer auf erkannten Geräten von diesem Punkt an live zugeordnet.

   Die Attribution funktioniert, sobald die identifizierende benutzerdefinierte Variable mit einem Gerät verknüpft ist. Im obigen Beispiel werden alle Treffer mit Ausnahme der Treffer 1 und 3 live zugeordnet (sie verwenden alle die Kennung `Bob`). Die Attribution funktioniert bei Treffern 1 und 3 nach der Wiederholungszuordnung.

>[!NOTE]
>
>Treffer mit Zeitstempel, die älter als 12 Stunden sind, werden im Live-Fluss nicht zugeordnet. Diese Treffer sind jedoch in der Wiederholungszuordnung enthalten, solange sie im Lookback-Fenster für die Wiederholung fallen.

### Wiederholungszuordnung

Die Wiederholung wird entweder täglich oder wöchentlich durchgeführt, je nachdem, wie Sie die Cross-Device-Analyse konfiguriert haben. Während der Wiederholung versucht die Cross-Device-Analyse, historische Daten in einem definierten Rückblickfenster neu darzustellen:

* Bei der täglichen Wiederholung entspricht das Rückblickfenster 1 Tag.
* Bei wöchentlicher Wiederholung wird ein Rückblickfenster von 7 Tagen verwendet.

Wenn ein Gerät Daten anfänglich sendet, ohne authentifiziert zu sein, und sich dann anmeldet, verknüpft die geräteübergreifende Analyse diese nicht authentifizierten Treffer mit der richtigen Person. Die folgende Tabelle stellt dieselben Daten wie oben dar, zeigt jedoch unterschiedliche Zahlen basierend auf der Wiederholung der Daten.

*Dieselben Daten nach der Wiederholung:*

| Zeitstempel | ECID | eVar1 oder CustomerID | Erläuterung des Treffers | Metrik „Personen“ (kumulativ) mit Gerätediagramm | Metrik „Personen“ (kumulativ) mit feldbasiertem Stitching |
| --- | --- | --- | --- | --- | --- |
| `1` | `246` | – | Bob auf seinem Desktop-Computer, nicht authentifiziert | `1` (Cluster1) | `1` (Bob) |
| `2` | `246` | `Bob` | Bob meldet sich auf seinem Desktop an. | `1` (Cluster1) | `1` (Bob) |
| `3` | `3579` | – | Bob auf seinem Mobilgerät, nicht authentifiziert | `1` (Cluster1) | `1` (Bob) |
| `4` | `3579` | `Bob` | Bob meldet sich auf einem Mobilgerät an | `1` (Cluster1) | `1` (Bob) |
| `5` | `246` | – | Bob greift erneut auf Ihre Site auf dem Desktop zu, nicht authentifiziert | `1` (Cluster1) | `1` (Bob) |
| `6` | `246` | `Bob` | Bob meldet sich erneut auf seinem Desktop an | `1` (Cluster1) | `1` (Bob) |
| `7` | `3579` | – | Bob ruft Ihre Site erneut auf einem Mobilgerät auf | `1` (Cluster1) | `1` (Bob) |
| `8` | `3579` | `Bob` | Bob meldet sich erneut auf einem Mobilgerät an | `1` (Cluster1) | `1` (Bob) |
