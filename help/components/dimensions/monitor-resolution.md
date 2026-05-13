---
title: Bildschirmauflösung
description: Die Auflösung des Bildschirms des Besuchers in Pixeln.
feature: Dimensions
exl-id: 6bae65eb-4546-4d07-877d-6e257fbe6cfa
TQID: https://experienceleague.adobe.com/d3AuMT0seRbZpuKVGPeWo98Bkhc8tcJIP6gt4y-rq38
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 82%

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

Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `s` bei allen Bildanforderungen einbeziehen. Wenn die `s` Abfragezeichenfolge fehlt oder eine Datenerfassungsbibliothek anderweitig keine Bildschirmauflösung erfassen kann, werden diese Daten unter [!UICONTROL `Not Specified`] aufgeführt.

## Dimensionselemente

Die Dimensionselemente umfassen alle erfassten Monitorauflösungen. Zu den Beispielwerten gehören `1920 x 1080`, `1366 x 768` und `1280 x 720`.
