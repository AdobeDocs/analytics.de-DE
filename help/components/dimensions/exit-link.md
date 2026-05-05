---
title: Exitlink
description: Der Name des Exitlinks.
feature: Dimensions
exl-id: 090d5fee-4b35-4be7-866c-5ef1d1c4c0a6
source-git-commit: 418e8d467ca29267314e14fba99783d0cb3d05a9
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 22%

---

# Exitlink

Die Dimension „Exitlink[&#x200B; zeigt &#x200B;](overview.md) Namen der auf Ihrer Site implementierten Exitlinks an. Exitlinks verfolgen ausgehende Klicks, die Besucher von der aktuellen Domain wegführen. Diese Dimension ist nützlich, wenn Sie verstehen möchten, welche ausgehenden Links am häufigsten angeklickt werden.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2` Abfragezeichenfolge &#x200B;](/help/implement/validate/query-parameters.md) Bildanforderungen in Abhängigkeit vom Wert in der `pe` Abfragezeichenfolge. Die `pe` Abfragezeichenfolge bestimmt, welche Link-Dimension den `pev2` erhält:

* **[Benutzerspezifischer Link](custom-link.md)**: `lnk_o`
* **[Downloadlink](download-link.md)**: `lnk_d`
* **Exitlink** (diese Seite): `lnk_e`

Wenn `pev2` nicht angegeben ist, wird stattdessen die Link-URL (`pev1`) als Dimensionswert verwendet. Wenn ein Link-Name explizit angegeben wird, beträgt die maximale Länge 100 Byte. Die von der Link-URL abgeleiteten Werte unterliegen dieser Beschränkung nicht.

Um diese Dimension mit AppMeasurement zu füllen, senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md) Bildanforderung mit dem Argument vom Typ „Link“ von `"e"`. Setzen Sie das Argument für den Link-Namen auf den gewünschten Wert:

```js
s.tl(true,"e","Example exit link");
```

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren. Wenn kein Link-Name angegeben wird, werden Dimensionselemente stattdessen als unformatierte URLs angezeigt. Diese rohen URLs sind in Berichten schwieriger zu interpretieren. Daher sollten Sie nach Möglichkeit einen beschreibenden Link-Namen angeben.
