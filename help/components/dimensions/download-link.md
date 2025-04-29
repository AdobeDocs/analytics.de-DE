---
title: Downloadlink
description: Der Name des Downloadlinks.
feature: Dimensions
exl-id: 078014a2-1f09-4177-9575-b44c5da25816
source-git-commit: a15d2b596c1e8b70e91efb49dd607fdbb0ceec3c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 74%

---

# Downloadlink

Die Dimension „Downloadlink[ gibt ](overview.md) Namen der auf Ihrer Site implementierten Downloadlinks an. Diese Dimension ist nützlich, wenn Sie mehr über das Verhalten von Besuchern bei Downloadlinks erfahren möchten, z. B. um:

* die Dateien zu bestimmen, die am häufigsten von Ihrer Site heruntergeladen werden.
* zu erkennen, ob bestimmte Dateien zu bestimmten Zeiten häufiger heruntergeladen werden.
* zu überprüfen, ob Besucher verschiedene Dateitypen herunterladen können, falls diese angeboten werden.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen für Treffer, die auch die Abfragezeichenfolge `pe` mit dem Wert `lnk_d` aufweisen. Wenn die `pe` Abfragezeichenfolge im Treffer einen anderen Wert hat, erfasst diese Dimension keine Daten. Die maximale Länge dieser Dimension beträgt 100 Byte.

Wenn Sie mit AppMeasurement Daten an diese Dimension senden möchten, senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md)-Bildanforderung mit einem Link-Typ-Argument `"d"`. Füllen Sie das Argument Link-Name mit dem gewünschten Wert:

```js
s.tl(true,"d","Example download link");
```

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren.
