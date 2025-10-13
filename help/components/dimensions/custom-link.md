---
title: Benutzerspezifischer Link
description: Der Name des benutzerspezifischen Links.
feature: Dimensions
exl-id: c153f710-f03f-4be6-8e18-5ebf2ed80f01
source-git-commit: a15d2b596c1e8b70e91efb49dd607fdbb0ceec3c
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 75%

---

# Benutzerspezifischer Link

Die Dimension „Benutzerspezifischer [&quot; &#x200B;](overview.md) die Namen der auf Ihrer Site implementierten benutzerspezifischen Links an. Diese Dimension ist nützlich, wenn Sie wissen möchten, auf welche Links Besucher am häufigsten klicken.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`pev2`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen für Treffer, die auch die Abfragezeichenfolge `pe` mit dem Wert `lnk_o` aufweisen. Wenn die `pe` Abfragezeichenfolge im Treffer einen anderen Wert hat, erfasst diese Dimension keine Daten. Die maximale Länge dieser Dimension beträgt 100 Byte.

Wenn Sie mit AppMeasurement Daten an diese Dimension senden möchten, senden Sie eine [`tl()`](/help/implement/vars/functions/tl-method.md)-Bildanforderung mit einem Link-Typ-Argument `"o"`. Geben Sie im Linkname-Argument den gewünschten Wert an.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, dass Sie Links basierend auf Ihren Berichtsanforderungen in aussagekräftige Kategorien gruppieren.
