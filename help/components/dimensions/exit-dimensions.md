---
title: Ausstiegsdimensionen
description: Führt Ausstiegsdimensionen und deren Verwendung auf.
keywords: Exitpage, Exitsite-Abschnitt, Exitserver, Custom Insight zum Exit
feature: Dimensions
exl-id: b2b1ee88-e5c3-44b5-8159-85ec53d20258
TQID: https://experienceleague.adobe.com/YRjvhW8OzBlip9ok0-1D4rYSljkccpIAlDkqCQv7nyo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 94%

---

# Ausstiegsdimensionen

*Auf dieser Hilfeseite wird beschrieben, wie Exits als [Dimension](overview.md) funktionieren. Informationen dazu, wie Ausstiege als Metrik funktionieren, finden Sie unter der Metrik [Ausstiege](../metrics/exits.md).*

Ausstiegsdimensionen zeichnen das letzte Dimensionselement auf und wenden es rückwirkend auf alle Treffer im Besuch an. Ausstiegsdimensionen sind für alle Variablen verfügbar, bei denen die Pfadsetzung unter [Traffic-Variablen](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen aktiviert ist.

## Füllen von Ausstiegsdimensionen mit Daten

Eine gegebene Ausstiegsdimension basiert auf der zugehörigen Traffic-Variablen. Wenn die Nicht-Ausstiegsvariable über Daten verfügt, enthält die zugehörige Ausstiegsdimension auch Daten. Für Ausstiegsdimensionen sind keine Implementierungsänderungen erforderlich, wenn Ihre Traffic-Variablen Daten enthalten.

## Dimensionselemente

Da Ausstiegsvariablen typischerweise auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basieren, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Die Werte in einer gegebenen Ausstiegsdimension stimmen mit den Dimensionsdimensionen in der zugehörigen Nicht-Ausstiegsdimension überein. Beispielsweise ähneln die Dimensionselemente in der Dimension „Exitpage“ den Dimensionselementen in der Dimension „Seite“.
