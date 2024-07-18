---
title: Einstiegsdimensionen
description: Führt Einstiegsdimensionen und deren Verwendung auf.
keywords: Entrypage, Einstiegsbereich, Einstiegs-Server, Custom Insight zum Einstieg
feature: Dimensions
exl-id: 424e2a9a-05ac-4397-921b-c8d7567348ed
source-git-commit: 66be48d0f41061d259cc53fb835ebd155294a710
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 75%

---

# Einstiegsdimensionen

*Auf dieser Hilfeseite wird beschrieben, wie Einstiege als [Dimension](overview.md) funktionieren. Informationen dazu, wie Einstiege als Metrik funktionieren, finden Sie unter der Metrik [Einstiege](../metrics/entries.md).*

Einstiegsdimensionen sind [besuchsbasiert](../metrics/visits.md). Sie zeichnen das erste Dimensionselement auf und behalten es für die gesamte Dauer des Besuchs bei. Einstiegsdimensionen sind für alle Variablen verfügbar, bei denen die Pfadsetzung unter [Traffic-Variablen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen aktiviert ist.

>[!TIP]
>Wenn Sie Daten basierend auf dem ersten Treffer eines Besuchs anstelle des ersten bei einem Besuch angezeigten Werts sehen möchten, können Sie ein [Segment](/help/components/segmentation/seg-overview.md) verwenden. Verwenden Sie einen Trefferbehälter, bei dem [Treffertiefe](hit-depth.md) gleich 1 ist, und verwenden Sie dann dieses Segment mit der gewünschten Variablen.

## Füllen von Einstiegsdimensionen mit Daten

Ein gegebener Eintrag [dimension](overview.md) basiert auf der zugehörigen Traffic-Variablen. Wenn die Nicht-Einstiegsvariable über Daten verfügt, enthält die zugehörige Einstiegsdimension auch Daten. Für Einstiegsdimensionen sind keine Implementierungsänderungen erforderlich, wenn Ihre Traffic-Variablen Daten enthalten.

## Dimensionselemente

Da Einstiegsvariablen typischerweise auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basieren, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Die Werte in einer gegebenen Einstiegsdimension stimmen mit den Dimensionselementen in der zugehörigen Nicht-Einstiegsdimension überein. Beispielsweise ähneln die Dimensionselemente in der Dimension „Entrypage“ den Dimensionselementen in der Dimension „Seite“.

## Ursprüngliche Entrypage

Die Dimension „Ursprüngliche Entrypage“ unterscheidet sich von anderen Einstiegsdimensionen. Anstatt die Entrypage für einen bestimmten Besuch beizubehalten, wird die erste Entrypage für die gesamte Dauer des Cookies dieses Besuchers beibehalten. Wenn Sie z. B. bei Ihrem ersten Besuch der Website zu `https://example.com/page4` gehen und ein Jahr später zu `https://example.com/store`, wird `https://example.com/page4` als Dimensionselement für die Dimension „Ursprüngliche Entrypage“ angegeben.
