---
title: Bildschirmauflösung
description: Die Auflösung des Bildschirms des Besuchers in Pixeln.
feature: Dimensions
exl-id: 6bae65eb-4546-4d07-877d-6e257fbe6cfa
TQID: https://experienceleague.adobe.com/d3AuMT0seRbZpuKVGPeWo98Bkhc8tcJIP6gt4y-rq38
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
source-wordcount: '289'
ht-degree: 51%
---
# Bildschirmauflösung

Die „Bildschirmauflösung“ [Dimension](overview.md) zeigt die Höhe und Breite des aktiven Displays in Pixel an. Diese Dimension ist nützlich, wenn Sie wissen möchten, wo sich die Kante auf Ihrer Site für Besucher befindet oder wie breit Besucher ihr Browser-Fenster gestalten können. Wenn Sie wissen, wo die Kante ist, können Sie Inhalte für die Anzeige optimieren.

Diese Dimension unterscheidet sich von Browser [Höhe](browser-height.md) und [Breite](browser-width.md). Die Browserhöhe/-breite ist die Anzahl der Pixel im sichtbaren Browser-Bereich, während die Bildschirmauflösung die Anzahl der Pixel des gesamten Monitors ist. Wenn Sie den Unterschied zwischen diesen beiden Variablen auf Ihrem Computer sehen möchten, öffnen Sie die Browser-Konsole (F12 bei den meisten Browsern) und kopieren Sie den folgenden Code in die Konsole:

```js
"Monitor resolution: " + screen.width + "x" + screen.height + "; Browser resolution: " + window.innerWidth + "x" + window.innerHeight;
```

Browserdimensionen sind immer kleiner als die Bildschirmauflösung, da Browser-Dimensionen keine Browsernavigation oder Rahmen enthalten.

## Füllen dieser Dimension mit Daten

Die Bildschirmauflösung wird automatisch Client-seitig aus den `screen.width`- und `screen.height` des Browsers erfasst. Dies funktioniert standardmäßig in jeder AppMeasurement- oder Web SDK (Tags)-Implementierung - es gibt keine Variable zum Festlegen. Wenn Sie Daten außerhalb von AppMeasurement oder der Web-SDK erfassen (z. B. über die API), senden Sie den Wert in Bildanfragen. Wenn sie fehlt oder eine Datenerfassungsbibliothek anderweitig keine Bildschirmauflösung erfassen kann, werden diese Daten unter [!UICONTROL `Not Specified`] aufgeführt.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (automatisch erfasst) |
| **Feld Web SDK/XDM** | Keine (automatisch erfasst) |
| **Abfrageparameter** | [`s`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<resolution>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 20 Byte |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Die Dimensionselemente umfassen alle erfassten Bildschirmauflösungen. Zu den Beispielwerten gehören `1920 x 1080`, `1366 x 768` und `1280 x 720`.
