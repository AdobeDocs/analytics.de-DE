---
title: Ausstiegsdimensionen
description: Führt Ausstiegsdimensionen und deren Verwendung auf.
keywords: Exitpage, Exitsite-Abschnitt, Exitserver, Custom Insight zum Exit
feature: Dimensions
exl-id: b2b1ee88-e5c3-44b5-8159-85ec53d20258
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 94%

---

# Ausstiegsdimensionen

*Auf dieser Hilfeseite wird beschrieben, wie Exits als [Dimension](overview.md) funktionieren. Informationen dazu, wie Ausstiege als Metrik funktionieren, finden Sie unter der Metrik [Ausstiege](../metrics/exits.md).*

Ausstiegsdimensionen zeichnen das letzte Dimensionselement auf und wenden es rückwirkend auf alle Treffer im Besuch an. Ausstiegsdimensionen sind für alle Variablen verfügbar, bei denen die Pfadsetzung unter [Traffic-Variablen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen aktiviert ist.

## Füllen von Ausstiegsdimensionen mit Daten

Eine gegebene Ausstiegsdimension basiert auf der zugehörigen Traffic-Variablen. Wenn die Nicht-Ausstiegsvariable über Daten verfügt, enthält die zugehörige Ausstiegsdimension auch Daten. Für Ausstiegsdimensionen sind keine Implementierungsänderungen erforderlich, wenn Ihre Traffic-Variablen Daten enthalten.

## Dimensionselemente

Da Ausstiegsvariablen typischerweise auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basieren, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Die Werte in einer gegebenen Ausstiegsdimension stimmen mit den Dimensionsdimensionen in der zugehörigen Nicht-Ausstiegsdimension überein. Beispielsweise ähneln die Dimensionselemente in der Dimension „Exitpage“ den Dimensionselementen in der Dimension „Seite“.
