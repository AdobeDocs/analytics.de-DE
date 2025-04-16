---
title: Bildschirmauflösung
description: Die Auflösung des Bildschirms des Besuchers in Pixeln.
feature: Dimensions
exl-id: 6bae65eb-4546-4d07-877d-6e257fbe6cfa
source-git-commit: e3a1c1fde3809cb73b1bda091b8be43778515d1a
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 72%

---

# Bildschirmauflösung

Die „Bildschirmauflösung“ [Dimension](overview.md) zeigt die Höhe und Breite des aktiven Displays in Pixel an. Diese Dimension ist nützlich, wenn Sie wissen möchten, wo sich die Kante auf Ihrer Site für Besucher befindet oder wie breit Besucher ihr Browser-Fenster gestalten können. Wenn Sie wissen, wo die Kante ist, können Sie Inhalte für die Anzeige optimieren.

Diese Dimension unterscheidet sich von Browser [Höhe](browser-height.md) und [Breite](browser-width.md). Die Browserhöhe/-breite ist die Anzahl der Pixel im sichtbaren Browser-Bereich, während die Bildschirmauflösung die Anzahl der Pixel des gesamten Monitors ist. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "; Browser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

Browserdimensionen sind immer kleiner als die Bildschirmauflösung, da Browser-Dimensionen keine Browsernavigation oder Rahmen enthalten.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`s` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `screen.width` und `screen.height` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert.

Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den `s` Abfragezeichenfolgenparameter in Bildanforderungen einbeziehen. Wenn die `s` Abfragezeichenfolge fehlt oder eine Datenerfassungsbibliothek anderweitig keine Bildschirmauflösung erfassen kann, werden diese Daten unter [!UICONTROL `Not Specified`] aufgeführt.

## Dimensionselemente

Die Dimensionselemente umfassen alle erfassten Monitorauflösungen. Zu den Beispielwerten gehören `1920 x 1080`, `1366 x 768` und `1280 x 720`.
