---
title: Browser-Breite – zusammengefasst
description: Die Breite des Browser-Fensters in Pixel.
feature: Dimensions
exl-id: f0cb28b6-260b-4c3d-bbf8-17fae7ef22a0
TQID: https://experienceleague.adobe.com/f9AknIwL-9ZMJ8tnGMxpUNmlkQiFmbjI3gtlP3KZtSQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 45%
---
# Browser-Breite

Die Dimension „Browser width - bucketed[ zeigt ](overview.md) Breite des Browser-Fensters an, klassifiziert in vordefinierte Gruppen. Diese Dimension ist nützlich, wenn Sie wissen möchten, wie breit Besuchern Ihr Inhalt angezeigt wird. Wenn Sie die Breite verstehen, in der Ihre Inhalte normalerweise angezeigt werden, können Sie diese Inhalte optimieren.

Diese Dimension unterscheidet sich von der Bildschirmbreite. Die Browser-Breite ist die Anzahl der Pixel im sichtbaren Browser-Bereich, während die Bildschirmbreite die Breite des gesamten Monitors in Pixel darstellt. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```javascript
console.log(`Browser width: ${window.innerWidth} pixels\nScreen width: ${screen.width} pixels`);
```

Die Browser-Breite ist immer kleiner als oder gleich der Bildschirmbreite, da die Browser-Breite keine Bildlaufleisten oder Ränder enthält.

>[!NOTE]
>
>Data Warehouse bietet außerdem die Dimension &quot;[!UICONTROL Browser width - granular], die die genaue Pixelbreite angibt, anstatt Werte in vordefinierten Buckets zu gruppieren.

## Füllen dieser Dimension mit Daten

Die Browser-Breite wird automatisch Client-seitig aus der `window.innerWidth`-Eigenschaft des Browsers erfasst. Dies funktioniert standardmäßig in jeder AppMeasurement- oder Web SDK (Tags)-Implementierung - es gibt keine Variable zum Festlegen. Wenn Sie Daten außerhalb von AppMeasurement oder der Web-SDK erfassen (z. B. über die API), senden Sie den Wert beim ersten Treffer jedes Besuchs. Wenn die Browser-Breite während des Besuchs angepasst wird, wird die Anpassung nicht aufgezeichnet.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (automatisch erfasst) |
| **Feld Web SDK/XDM** | Keine (automatisch erfasst) |
| **Abfrageparameter** | [`bw`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<browserWidth>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Wertebereich** | 0-65 535 |
| **Persistenz** | Besuch |

## Dimensionselemente

Dimension-Elemente enthalten alle erfassten Browser-Breiten, die in vordefinierte Gruppen klassifiziert sind. Wenn die Browser-Breite eines Treffers beispielsweise `1280` beträgt, wird sie im Dimensionselement `1200 to 1299` gruppiert.
