---
title: Zeit vor Ereignis
description: Die Zeit zwischen der Metrik und dem ersten Treffer des Besuchs.
feature: Dimensions
exl-id: 2586673f-d908-4b69-901a-5fafe635d0d5
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '157'
ht-degree: 100%

---

# Zeit vor Ereignis

Die Dimension „Zeit vor Ereignis“ zeigt den Zeitraum an, der zwischen dem ersten Treffer des Besuchs und der gewünschten Metrik verstrichen ist. Diese Dimension ist nützlich, um die Zeitdauer zu bestimmen, die zum Erzielen eines Erfolgsereignisses (z. B. einer Formularübermittlung oder eines Kaufs) benötigt wird.

## Füllen dieser Dimension mit Daten

Obwohl diese Dimension technisch bei allen Implementierungen vorkonfiguriert ist, funktioniert sie am besten mit benutzerspezifischen und Kaufereignissen. Adobe empfiehlt die Implementierung benutzerspezifischer Ereignisse auf Ihrer Site. Wenn Sie benutzerspezifische Ereignisse implementieren, ist für diese Dimension keine zusätzliche Implementierung erforderlich.

## Dimensionselemente

Zu den Dimensionselementen zählen zeitbasierte Behälter von `"Less than 1 minute"` bis `"More than 15 hours"`. Wenn ein Besucher beispielsweise 23 Minuten von seinem ersten Treffer bis zu einem Kauf benötigte, würde er unter das Dimensionselement `"10 to 30 minutes"` fallen. Die Buckets können für diese Metrik nicht angepasst werden.
