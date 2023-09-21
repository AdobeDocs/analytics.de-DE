---
title: Zeit vor Ereignis
description: Die Zeit zwischen der Metrik und dem ersten Treffer des Besuchs.
feature: Dimensions
exl-id: 2586673f-d908-4b69-901a-5fafe635d0d5
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 84%

---

# Zeit vor Ereignis

Die &quot;Zeit vor Ereignis&quot; [Dimension](overview.md) gibt die Zeit an, die zwischen dem ersten Treffer des Besuchs und der gewünschten Metrik verstrichen ist. Diese Dimension ist nützlich, um die Zeitdauer zu bestimmen, die zum Erzielen eines Erfolgsereignisses (z. B. einer Formularübermittlung oder eines Kaufs) benötigt wird.

## Füllen dieser Dimension mit Daten

Obwohl diese Dimension technisch bei allen Implementierungen vorkonfiguriert ist, funktioniert sie am besten mit benutzerspezifischen und Kaufereignissen. Adobe empfiehlt die Implementierung benutzerspezifischer Ereignisse auf Ihrer Site. Wenn Sie benutzerspezifische Ereignisse implementieren, ist für diese Dimension keine zusätzliche Implementierung erforderlich.

## Dimensionselemente

Zu den Dimensionselementen zählen zeitbasierte Behälter von `"Less than 1 minute"` bis `"More than 15 hours"`. Wenn ein Besucher beispielsweise 23 Minuten von seinem ersten Treffer bis zu einem Kauf benötigte, würde er unter das Dimensionselement `"10 to 30 minutes"` fallen. Die Buckets können für diese Metrik nicht angepasst werden.
