---
title: Benutzerspezifischer Link
description: Der Name des benutzerspezifischen Links.
feature: Dimensions
exl-id: c153f710-f03f-4be6-8e18-5ebf2ed80f01
TQID: https://experienceleague.adobe.com/x4IAGJjozPnLsft1e9xs68L6TNDJbHW0H4Z23p9EDNg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 9b4525e014170b72688044a6ead344b1bde8c39b
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 21%

---

# Benutzerspezifischer Link

Die Dimension „Benutzerspezifischer [&quot; ](overview.md) die Namen der auf Ihrer Site implementierten benutzerspezifischen Links an. Benutzerdefinierte Links sind ein flexibler Tracking-Mechanismus für alle Interaktionen, bei denen es sich nicht um einen Dateidownload oder eine ausgehende Navigation handelt. Häufige Beispiele sind Klicks auf Schaltflächen, interne Navigation oder Formularinteraktionen. Diese Dimension ist nützlich, wenn Sie verstehen möchten, mit welchen dieser Interaktionen Besucherinnen und Besucher am meisten interagieren.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2` Abfragezeichenfolge ](/help/implement/validate/query-parameters.md) Bildanforderungen in Abhängigkeit vom Wert in der `pe` Abfragezeichenfolge. Die `pe` Abfragezeichenfolge bestimmt, welche Link-Dimension den `pev2` erhält:

* **Benutzerspezifischer Link** (diese Seite): `lnk_o`
* **[Downloadlink](download-link.md)**: `lnk_d`
* **[Exitlink](exit-link.md)**: `lnk_e`

Wenn `pev2` nicht angegeben ist, wird stattdessen die Link-URL (`pev1`) als Dimensionswert verwendet. Wenn ein Link-Name explizit angegeben wird, beträgt die maximale Länge 100 Byte. Die von der Link-URL abgeleiteten Werte unterliegen dieser Beschränkung nicht.

Um diese Dimension mit AppMeasurement zu füllen, senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md) Bildanforderung mit dem Argument vom Typ „Link“ von `"o"`. Setzen Sie das Argument für den Link-Namen auf den gewünschten Wert:

```js
s.tl(true,"o","Example custom link");
```

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren. Wenn kein Link-Name angegeben wird, werden Dimensionselemente stattdessen als unformatierte URLs angezeigt. Diese rohen URLs sind in Berichten schwieriger zu interpretieren. Daher sollten Sie nach Möglichkeit einen beschreibenden Link-Namen angeben.
