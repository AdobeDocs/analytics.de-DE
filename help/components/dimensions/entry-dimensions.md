---
title: Einstiegsdimensionen
description: Führt Einstiegsdimensionen und deren Verwendung auf.
keywords: Entrypage, Einstiegsbereich, Einstiegs-Server, Custom Insight zum Einstieg
feature: Dimensions
exl-id: 424e2a9a-05ac-4397-921b-c8d7567348ed
TQID: https://experienceleague.adobe.com/6a6Xy8SEqjcnuB1Acbwkesw6OA7Nggld5ppWtjYaj5k
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 292
ht-degree: 75%

---

# Einstiegsdimensionen

*Auf dieser Hilfeseite wird beschrieben, wie Einträge als [Dimension](overview.md) funktionieren. Informationen dazu, wie Einstiege als Metrik funktionieren, finden Sie unter der Metrik [Einstiege](../metrics/entries.md).*

Einstiegsdimensionen sind [besuchsbasiert](../metrics/visits.md). Sie zeichnen das erste Dimensionselement auf und behalten es für die gesamte Dauer des Besuchs bei. Einstiegsdimensionen sind für alle Variablen verfügbar, bei denen die Pfadsetzung unter [Traffic-Variablen](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen aktiviert ist.

>[!TIP]
>Wenn Sie Daten basierend auf dem ersten Treffer eines Besuchs anstelle des ersten bei einem Besuch angezeigten Werts anzeigen möchten, können Sie ein [Segment](/help/components/segmentation/seg-overview.md) verwenden. Verwenden Sie einen Treffer-Container[ bei dem „Treffertiefe](hit-depth.md) gleich 1 ist, und verwenden Sie dann dieses Segment mit der gewünschten Variablen.

## Füllen von Einstiegsdimensionen mit Daten

Ein bestimmter Eintrag [Dimension](overview.md) basiert auf seiner zugehörigen Traffic-Variablen. Wenn die Nicht-Einstiegsvariable über Daten verfügt, enthält die zugehörige Einstiegsdimension auch Daten. Für Einstiegsdimensionen sind keine Implementierungsänderungen erforderlich, wenn Ihre Traffic-Variablen Daten enthalten.

## Dimensionselemente

Da Einstiegsvariablen typischerweise auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basieren, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Die Werte in einer gegebenen Einstiegsdimension stimmen mit den Dimensionselementen in der zugehörigen Nicht-Einstiegsdimension überein. Beispielsweise ähneln die Dimensionselemente in der Dimension „Entrypage“ den Dimensionselementen in der Dimension „Seite“.

## Ursprüngliche Entrypage

Die Dimension „Ursprüngliche Entrypage“ unterscheidet sich von anderen Einstiegsdimensionen. Anstatt die Entrypage für einen bestimmten Besuch beizubehalten, wird die erste Entrypage für die gesamte Dauer des Cookies dieses Besuchers beibehalten. Wenn Sie z. B. bei Ihrem ersten Besuch der Website zu `https://example.com/page4` gehen und ein Jahr später zu `https://example.com/store`, wird `https://example.com/page4` als Dimensionselement für die Dimension „Ursprüngliche Entrypage“ angegeben.
