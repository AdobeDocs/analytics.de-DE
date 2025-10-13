---
title: Browser-Breite – zusammengefasst
description: Die Breite des Browser-Fensters in Pixel.
feature: Dimensions
exl-id: f0cb28b6-260b-4c3d-bbf8-17fae7ef22a0
source-git-commit: 2601b0e5c3fa78237ce693801b8dd8c95b853b81
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 81%

---

# Browser-Breite

Die Dimension „Browser width - bucketed[&#x200B; zeigt &#x200B;](overview.md) Breite des Browser-Fensters an, klassifiziert in vordefinierte Gruppen. Diese Dimension ist nützlich, wenn Sie wissen möchten, wie breit Besuchern Ihr Inhalt angezeigt wird. Wenn Sie die Breite verstehen, in der Ihre Inhalte normalerweise angezeigt werden, können Sie diese Inhalte optimieren.

Diese Dimension unterscheidet sich von der Bildschirmbreite. Die Browser-Breite ist die Anzahl der Pixel im sichtbaren Browser-Bereich, während die Bildschirmbreite die Breite des gesamten Monitors in Pixel darstellt. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```javascript
console.log(`Browser width: ${window.innerWidth} pixels\nScreen width: ${screen.width} pixels`);
```

Die Browser-Breite ist immer kleiner als oder gleich der Bildschirmbreite, da die Browser-Breite keine Bildlaufleisten oder Ränder enthält.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`bw` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `window.innerWidth` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `bw` beim ersten Treffer jedes Besuchs einbeziehen.

Adobe behält die Browser-Breite für einen Besuch bei. Wenn die Browser-Breite während des Besuchs angepasst wird, wird die Anpassung nicht aufgezeichnet.

## Dimensionselemente

Dimension-Elemente enthalten alle erfassten Browser-Breiten, die in vordefinierte Gruppen klassifiziert sind. Wenn die Browser-Breite eines Treffers beispielsweise `1280` beträgt, wird sie im Dimensionselement `1200 to 1299` gruppiert.
