---
title: Downloadlink
description: Der Name des Downloadlinks.
feature: Dimensions
exl-id: 078014a2-1f09-4177-9575-b44c5da25816
source-git-commit: 418e8d467ca29267314e14fba99783d0cb3d05a9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 28%

---

# Downloadlink

Die Dimension „Downloadlink[&#x200B; gibt &#x200B;](overview.md) Namen der auf Ihrer Site implementierten Downloadlinks an. Diese Dimension ist nützlich, wenn Sie mehr über das Verhalten von Besuchern bei Downloadlinks erfahren möchten, z. B. um:

* Welche Dateien werden am häufigsten von Ihrer Website heruntergeladen?
* Ob bestimmte Dateien während bestimmter Zeiträume häufiger heruntergeladen werden.
* Ob Besucher unterschiedliche Dateitypen herunterladen, wenn sie angeboten werden.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2` Abfragezeichenfolge &#x200B;](/help/implement/validate/query-parameters.md) Bildanforderungen in Abhängigkeit vom Wert in der `pe` Abfragezeichenfolge. Die `pe` Abfragezeichenfolge bestimmt, welche Link-Dimension den `pev2` erhält:

* **[Benutzerspezifischer Link](custom-link.md)**: `lnk_o`
* **Downloadlink** (diese Seite): `lnk_d`
* **[Exitlink](exit-link.md)**: `lnk_e`

Wenn `pev2` nicht angegeben ist, wird stattdessen die Link-URL (`pev1`) als Dimensionswert verwendet. Wenn ein Link-Name explizit angegeben wird, beträgt die maximale Länge 100 Byte. Die von der Link-URL abgeleiteten Werte unterliegen dieser Beschränkung nicht.

Um diese Dimension mit AppMeasurement zu füllen, senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md) Bildanforderung mit dem Argument vom Typ „Link“ von `"d"`. Setzen Sie das Argument für den Link-Namen auf den gewünschten Wert:

```js
s.tl(true,"d","Example download link");
```

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren. Wenn kein Link-Name angegeben wird, werden Dimensionselemente stattdessen als unformatierte URLs angezeigt. Diese rohen URLs sind in Berichten schwieriger zu interpretieren. Daher sollten Sie nach Möglichkeit einen beschreibenden Link-Namen angeben.
