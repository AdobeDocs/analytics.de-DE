---
title: Benutzerspezifischer Link
description: Der Name des benutzerspezifischen Links.
feature: Dimensions
exl-id: c153f710-f03f-4be6-8e18-5ebf2ed80f01
TQID: https://experienceleague.adobe.com/x4IAGJjozPnLsft1e9xs68L6TNDJbHW0H4Z23p9EDNg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 20%
---
# Benutzerspezifischer Link

Die Dimension „Benutzerspezifischer [&quot; &#x200B;](overview.md) die Namen der auf Ihrer Site implementierten benutzerspezifischen Links an. Benutzerdefinierte Links sind ein flexibler Tracking-Mechanismus für alle Interaktionen, bei denen es sich nicht um einen Dateidownload oder eine ausgehende Navigation handelt. Häufige Beispiele sind Klicks auf Schaltflächen, interne Navigation oder Formularinteraktionen. Diese Dimension ist nützlich, wenn Sie verstehen möchten, mit welchen dieser Interaktionen Besucherinnen und Besucher am meisten interagieren.

## Füllen dieser Dimension mit Daten

Diese Dimension wird durch [Linktracking-Aufrufe (`tl()`) &#x200B;](/help/implement/vars/functions/tl-method.md). Es gibt keine dedizierte Variable zum Festlegen. Senden Sie stattdessen eine `tl()` Bildanforderung mit dem Argument des Typs „Link“ von `"o"` und legen Sie das Argument des Typs „Link-Name“ auf den gewünschten Wert fest. Die `pe` Abfragezeichenfolge leitet den Link-Namen an die richtige Link-Dimension weiter (`lnk_o` für [benutzerspezifische Links](custom-link.md), `lnk_d` für [Downloadlinks](download-link.md) und `lnk_e` für [Exitlinks](exit-link.md)). Wenn kein Link-Name angegeben wird, wird stattdessen die Link-URL als Dimensionswert verwendet, und von der URL abgeleitete Werte unterliegen nicht der Byte-Beschränkung.

```js
s.tl(true,"o","Example custom link");
```

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`tl()`](/help/implement/vars/functions/tl-method.md) |
| **Feld Web SDK/XDM** | Keine |
| **Abfrageparameter** | [`pev2`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<linkName>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 100 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren. Wenn kein Link-Name angegeben wird, werden Dimensionselemente stattdessen als unformatierte URLs angezeigt. Diese rohen URLs sind in Berichten schwieriger zu interpretieren. Daher sollten Sie nach Möglichkeit einen beschreibenden Link-Namen angeben.
