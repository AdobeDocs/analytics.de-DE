---
title: Kategorie
description: Die Produktkategorie des Treffers.
feature: Dimensions
exl-id: 3517b417-1a44-4d3e-ac16-93fdc5f36404
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '155'
ht-degree: 100%

---

# Kategorie

Die Dimension „Kategorie“ gibt die Produktkategorie des Treffers an. Dies ist für Implementierungen nützlich, die die `products`-Variable verwenden und Metriken für die Produktkategorie anzeigen möchten, wie am häufigsten verkaufte oder angezeigte Artikel. Diese Dimension kann absichtlich leer sein, wenn Sie keine Produkte auf Ihrer Site haben.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf den ersten Teil der Zeichenfolge in der [`products`](/help/implement/vars/page-vars/products.md)-Variable. Diese Dimension wird mit allen Elementen vor dem ersten Semikolon (`;`) gefüllt.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, einzelne Produkte in aussagekräftige Kategorien zu gruppieren und dabei sowohl die Dimensionen „Produkt“ als auch „Kategorie“ zu verwenden.

>[!TIP]
>
>In früheren Versionen von Adobe Analytics waren der Dimension „Kategorie“ aufgrund ihrer Verarbeitungsarchitektur einige Einschränkungen auferlegt. Diese Einschränkungen wurden inzwischen entfernt, sodass Sie alle Metriken und Aufschlüsselungen verwenden können.
