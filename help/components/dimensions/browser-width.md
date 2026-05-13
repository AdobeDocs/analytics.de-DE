---
title: Browser-Breite – zusammengefasst
description: Die Breite des Browser-Fensters in Pixel.
feature: Dimensions
exl-id: f0cb28b6-260b-4c3d-bbf8-17fae7ef22a0
TQID: https://experienceleague.adobe.com/f9AknIwL-9ZMJ8tnGMxpUNmlkQiFmbjI3gtlP3KZtSQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 274
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
