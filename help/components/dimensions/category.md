---
title: Kategorie
description: Die Produktkategorie des Treffers.
feature: Dimensions
exl-id: 3517b417-1a44-4d3e-ac16-93fdc5f36404
TQID: 'https://experienceleague.adobe.com/3G1qDbtVnRj8At-FU1fNaI8KLboMQvo8NKktinrTbs8'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2: id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 93%

---

# Kategorie

Die „Dimension[ „Kategorie](overview.md) zeigt die Produktkategorie des Treffers an. Dies ist für Implementierungen nützlich, die die `products`-Variable verwenden und Metriken für die Produktkategorie anzeigen möchten, wie am häufigsten verkaufte oder angezeigte Artikel. Diese Dimension kann absichtlich leer sein, wenn Sie keine Produkte auf Ihrer Site haben.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf den ersten Teil der Zeichenfolge in der [`products`](/help/implement/vars/page-vars/products.md)-Variable. Diese Dimension wird mit allen Elementen vor dem ersten Semikolon (`;`) gefüllt.

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, einzelne Produkte in aussagekräftige Kategorien zu gruppieren und dabei sowohl die Dimensionen „Produkt“ als auch „Kategorie“ zu verwenden.

>[!TIP]
>
>In früheren Versionen von Adobe Analytics waren der Dimension „Kategorie“ aufgrund ihrer Verarbeitungsarchitektur einige Einschränkungen auferlegt. Diese Einschränkungen wurden inzwischen entfernt, sodass Sie alle Metriken und Aufschlüsselungen verwenden können.
