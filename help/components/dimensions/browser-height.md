---
title: Browser-Höhe – zusammengefasst
description: Die Höhe des Browser-Fensters in Pixel.
feature: Dimensions
exl-id: bdfd2ef5-c200-4d6e-b478-3917fca66227
TQID: https://experienceleague.adobe.com/-MSFtBJDaiG0yYL6ZdpzbPY80uFJbdxB0gyBtKAkFzY
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
ht-degree: 40%
---
# Browser-Höhe

„Browser height - bucketed[ (Dimension](overview.md) zeigt die Höhe des Browser-Fensters an, klassifiziert in vordefinierte Gruppen. Diese Dimension ist nützlich, wenn Sie verstehen möchten, wo sich die Kante auf Ihrer Site für Besucher befindet. Wenn Sie wissen, wo die Kante ist, können Sie Inhalte für die Anzeige optimieren.

Diese Dimension unterscheidet sich von der Bildschirmhöhe. Die Browser-Höhe ist die Anzahl der Pixel im sichtbaren Browser-Bereich, während die Bildschirmhöhe die Höhe des gesamten Monitors in Pixel darstellt. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```javascript
console.log(`Browser height: ${window.innerHeight} pixels\nScreen height: ${screen.height} pixels`);
```

Die Browser-Höhe ist in der Regel kleiner oder gleich der Bildschirmhöhe, da die Browser-Höhe keine Browser-Navigation oder -Rahmen enthält.

>[!NOTE]
>
>Data Warehouse bietet außerdem die Dimension &quot;[!UICONTROL Browser height - granular]&quot;, die die genaue Pixelhöhe angibt, anstatt Werte in vordefinierten Buckets zu gruppieren.

## Füllen dieser Dimension mit Daten

Die Browser-Höhe wird automatisch Client-seitig aus der `window.innerHeight`-Eigenschaft des Browsers erfasst. Dies funktioniert standardmäßig in jeder AppMeasurement- oder Web SDK (Tags)-Implementierung - es gibt keine Variable zum Festlegen. Wenn Sie Daten außerhalb von AppMeasurement oder der Web-SDK erfassen (z. B. über die API), senden Sie den Wert beim ersten Treffer jedes Besuchs. Wenn die Browser-Höhe während des Besuchs angepasst wird, wird die Anpassung nicht aufgezeichnet.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (automatisch erfasst) |
| **Feld Web SDK/XDM** | Keine (automatisch erfasst) |
| **Abfrageparameter** | [`bh`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<browserHeight>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Wertebereich** | 0-65 535 |
| **Persistenz** | Besuch |

## Dimensionselemente

Dimension-Elemente enthalten alle erfassten Browser-Höhen, die in vordefinierte Gruppen klassifiziert sind. Wenn die Browser-Höhe eines Treffers beispielsweise `720` beträgt, wird sie im Dimensionselement `700 to 799` gruppiert.
