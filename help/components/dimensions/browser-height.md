---
title: Browser-Höhe – zusammengefasst
description: Die Höhe des Browser-Fensters in Pixel.
feature: Dimensions
exl-id: bdfd2ef5-c200-4d6e-b478-3917fca66227
TQID: https://experienceleague.adobe.com/-MSFtBJDaiG0yYL6ZdpzbPY80uFJbdxB0gyBtKAkFzY
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 273
ht-degree: 87%

---

# Browser-Höhe

„Browser height - bucketed[ (Dimension](overview.md) zeigt die Höhe des Browser-Fensters an, klassifiziert in vordefinierte Gruppen. Diese Dimension ist nützlich, wenn Sie verstehen möchten, wo sich die Kante auf Ihrer Site für Besucher befindet. Wenn Sie wissen, wo die Kante ist, können Sie Inhalte für die Anzeige optimieren.

Diese Dimension unterscheidet sich von der Bildschirmhöhe. Die Browser-Höhe ist die Anzahl der Pixel im sichtbaren Browser-Bereich, während die Bildschirmhöhe die Höhe des gesamten Monitors in Pixel darstellt. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```javascript
console.log(`Browser height: ${window.innerHeight} pixels\nScreen height: ${screen.height} pixels`);
```

Die Browser-Höhe ist immer kleiner oder gleich der Bildschirmhöhe, da die Browser-Höhe keine Browser-Navigation oder -Ränder enthält.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`bh` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `window.innerHeight` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `bh` beim ersten Treffer jedes Besuchs einbeziehen.

Adobe behält die Browser-Höhe für einen Besuch bei. Wenn die Browser-Höhe während des Besuchs angepasst wird, wird die Anpassung nicht aufgezeichnet.

## Dimensionselemente

Dimension-Elemente enthalten alle erfassten Browser-Höhen, die in vordefinierte Gruppen klassifiziert sind. Wenn die Browser-Höhe eines Treffers beispielsweise `720` beträgt, wird sie im Dimensionselement `700 to 799` gruppiert.
