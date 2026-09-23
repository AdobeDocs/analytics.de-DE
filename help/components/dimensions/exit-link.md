---
title: Exitlink
description: Der Name des Exitlinks.
feature: Dimensions
exl-id: 090d5fee-4b35-4be7-866c-5ef1d1c4c0a6
TQID: https://experienceleague.adobe.com/lGKBkR5e2arJxGmfIE4qN84oGtYJ2zkfn6luqxEUJ-w
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
source-wordcount: '251'
ht-degree: 22%
---
# Exitlink

Die Dimension „Exitlink[ zeigt ](overview.md) Namen der auf Ihrer Site implementierten Exitlinks an. Exitlinks verfolgen ausgehende Klicks, die Besucher von der aktuellen Domain wegführen. Diese Dimension ist nützlich, wenn Sie verstehen möchten, welche ausgehenden Links am häufigsten angeklickt werden.

## Füllen dieser Dimension mit Daten

Diese Dimension wird durch [Linktracking-Aufrufe (`tl()`) ](/help/implement/vars/functions/tl-method.md). Es gibt keine dedizierte Variable zum Festlegen. Senden Sie stattdessen eine `tl()` Bildanforderung mit dem Argument des Typs „Link“ von `"e"` und legen Sie das Argument des Typs „Link-Name“ auf den gewünschten Wert fest. Die `pe` Abfragezeichenfolge leitet den Link-Namen an die richtige Link-Dimension weiter (`lnk_o` für [benutzerspezifische Links](custom-link.md), `lnk_d` für [Downloadlinks](download-link.md) und `lnk_e` für [Exitlinks](exit-link.md)). Wenn kein Link-Name angegeben wird, wird stattdessen die Link-URL als Dimensionswert verwendet, und von der URL abgeleitete Werte unterliegen nicht der Byte-Beschränkung.

```js
s.tl(true,"e","Example exit link");
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
