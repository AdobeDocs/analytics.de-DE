---
title: Zeit vor Ereignis
description: Die Zeit zwischen der Metrik und dem ersten Treffer des Besuchs.
exl-id: 2586673f-d908-4b69-901a-5fafe635d0d5
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '149'
ht-degree: 100%

---

# Zeit vor Ereignis

Die Dimension „Zeit vor Ereignis“ zeigt den Zeitraum an, der zwischen dem ersten Treffer des Besuchs und der gewünschten Metrik verstrichen ist. Diese Dimension ist nützlich, um die Zeitdauer zu bestimmen, die zum Erzielen eines Erfolgsereignisses (z. B. einer Formularübermittlung oder eines Kaufs) benötigt wird.

## Füllen dieser Dimension mit Daten

Obwohl diese Dimension technisch bei allen Implementierungen vorkonfiguriert ist, funktioniert sie am besten mit benutzerspezifischen und Kaufereignissen. Adobe empfiehlt die Implementierung benutzerspezifischer Ereignisse auf Ihrer Site. Wenn Sie benutzerspezifische Ereignisse implementieren, ist für diese Dimension keine zusätzliche Implementierung erforderlich.

## Dimensionselemente

Zu den Dimensionselementen zählen zeitbasierte Behälter von `"Less than 1 minute"` bis `"More than 15 hours"`. Wenn ein Besucher beispielsweise 23 Minuten von seinem ersten Treffer bis zu einem Kauf benötigte, würde er unter das Dimensionselement `"10 to 30 minutes"` fallen.
