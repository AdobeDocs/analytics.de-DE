---
title: Produkt
description: Der Name des Produkts.
feature: Dimensions
exl-id: 2649c200-4b0a-49a9-8592-9b9af72b91cf
TQID: https://experienceleague.adobe.com/SMFFeSTkQyQoSWNFc8qHJRxYkJQmiJoKd0v4rS6xRKc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 58%
---
# Produkt

Die „Dimension [Produkt](overview.md) gibt den Namen des Produkts im Treffer an. Dies ist für Implementierungen nützlich, die die `products`-Variable verwenden und Metriken für die Produkte anzeigen möchten, wie am häufigsten verkaufte oder angezeigte Artikel. Diese Dimension kann absichtlich leer sein, wenn Sie keine Produkte auf Ihrer Site haben.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf den Produktnamen in der [`products`](/help/implement/vars/page-vars/products.md), der die Zeichenfolge zwischen dem ersten und zweiten Semikolon (`;`) ist.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`products`](/help/implement/vars/page-vars/products.md) |
| **Feld Web SDK/XDM** | [`productListItems[].name`](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/commerce-details) |
| **Abfrageparameter** | [`products`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<products>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 100 Byte |
| **Persistenz** | Treffer |

## Dimensionselemente

Da diese Variable auf einer benutzerdefinierten Zeichenfolge in Ihrer Implementierung basiert, bestimmt Ihr Unternehmen, welche Dimensionselemente verwendet werden. Adobe empfiehlt, eine konsistente Namenskonvention für Produkte einzuführen. [Klassifizierungen](../classifications/classifications-overview.md) sind verfügbar, wenn Sie Produkte anders gruppieren oder einen benutzerfreundlicheren Namen angeben möchten. Adobe empfiehlt die Verwendung der Dimensionen „Produkt“ und „Kategorie“.
