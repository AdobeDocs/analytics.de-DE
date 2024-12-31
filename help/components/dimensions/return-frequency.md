---
title: Rückkehrhäufigkeit
description: Die zusammengefasste Zeitspanne zwischen dem aktuellen Besuch und dem vorherigen Besuch.
feature: Dimensions
exl-id: 8ec31e17-a57d-416f-b471-c2c37a98d134
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 93%

---

# Rückkehrhäufigkeit

Die Dimension [Häufigkeit der Rückkehr](overview.md) gibt die Zeitspanne an, die zwischen Besuchen von wiederkehrenden Besuchern vergeht. Wenn ein Besucher zu Ihrer Site zurückkehrt, prüft Adobe, wie lange der vorherige Besuch zurückliegt, und erfasst den Treffer im entsprechenden Dimensionselement. Diese Dimension ist nützlich, um die Attraktivität und Relevanz Ihrer Website für Besucher im Zeitverlauf einzuschätzen. Sie kann auch dazu beitragen, die Auswirkungen der Inhalte und Werbeaktionen Ihrer Website auf Ihre Besucher zu ermitteln.

>[!TIP]
>
>Diese Dimension umfasst keine erstmaligen Besucher.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

Die Daten für diese Dimension werden beim ersten Treffer des Besuchs festgelegt und bleiben für die gesamte Dauer des Besuchs erhalten. Der Wert kann sich während des Besuchs nicht ändern.

## Dimensionselemente

Zu den Dimensionselementen gehören zeitbasierte Behälter, abhängig von der seit ihrem letzten Besuch verstrichenen Zeit.

* Weniger als ein Tag
* 1 bis 3 Tage
* 3 bis 7 Tage
* 7 bis 14 Tage
* 14 Tage bis 1 Monat
* Länger als 1 Monat

## Die Dimensionselemente werden unter den Behältern außerhalb des Datumsbereichs des Projekts angezeigt.

Wenn Sie den Datumsbereich eines Projekts festlegen, können Sie üblicherweise Dimensionselemente sehen, die sich auf Besuche außerhalb des Datumsbereichs beziehen. Beispiel: Ein Besucher besucht Ihre Site im Juli und zweimal an einem Tag im September. Die Dimension „Rückkehrhäufigkeit“ für den Monat September würde einen Besuch unter „Länger als 1 Monat“ und einen Besuch unter „Weniger als 1 Tag“ ausweisen.
