---
title: Benutzerspezifischer Link
description: Der Name des benutzerspezifischen Links.
feature: Dimensions
exl-id: c153f710-f03f-4be6-8e18-5ebf2ed80f01
source-git-commit: 5c1d50fa09b0fad228f24018de2b062d09b0fe5f
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 21%

---

# Benutzerspezifischer Link

Die Dimension „Benutzerspezifischer [&quot; &#x200B;](overview.md) die Namen der auf Ihrer Site implementierten benutzerspezifischen Links an. Benutzerdefinierte Links sind ein flexibler Tracking-Mechanismus für alle Interaktionen, bei denen es sich nicht um einen Dateidownload oder eine ausgehende Navigation handelt. Häufige Beispiele sind Klicks auf Schaltflächen, interne Navigation oder Formularinteraktionen. Diese Dimension ist nützlich, wenn Sie verstehen möchten, mit welchen dieser Interaktionen Besucherinnen und Besucher am meisten interagieren.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2` Abfragezeichenfolge &#x200B;](/help/implement/validate/query-parameters.md) Bildanforderungen in Abhängigkeit vom Wert in der `pe` Abfragezeichenfolge. Die `pe` Abfragezeichenfolge bestimmt, welche Link-Dimension den `pev2` erhält:

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
