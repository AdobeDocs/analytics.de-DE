---
title: Seiten-URL
description: Die URL der Seite.
feature: Dimensions
exl-id: 7c0ec494-d79b-4b65-9161-bdc48485af84
TQID: https://experienceleague.adobe.com/Qek7BUR15HjFpK-XaYQ-J9fkJQiBfNi-ZoqXqaACP0A
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 52%
---
# Seiten-URL

Die Dimension „Seiten-URL[&#x200B; führt &#x200B;](overview.md) URLs auf Ihrer Site auf.

>[!IMPORTANT]
>
>Diese Dimension ist nur in Data Warehouse verfügbar. Wenn Sie eine URL-Dimension in anderen Analytics-Lösungen verwenden möchten, kopieren Sie den Wert bei jedem Treffer in eine [eVar](evar.md).

## Füllen dieser Dimension mit Daten

AppMeasurement erfasst die Seiten-URL automatisch bei jedem [Seitenaufruf (`t()`)](/help/implement/vars/functions/t-method.md). Sie können den erfassten Wert mithilfe der Variablen [`pageURL`](/help/implement/vars/page-vars/pageurl.md) überschreiben. Wenn eine URL länger als 255 Byte ist, wird der Überlauf im `-g` Abfragezeichenfolgenparameter gespeichert. Protokoll- und Abfragezeichenfolgen sind in der URL enthalten. [Linktracking-Aufrufe (`tl()`) entfernen &#x200B;](/help/implement/vars/functions/tl-method.md) immer diese Dimension, auch wenn der URL-Wert vorhanden ist.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`pageURL`](/help/implement/vars/page-vars/pageurl.md) |
| **Feld Web SDK/XDM** | [`web.webPageDetails.URL`](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/data-types/webpage-details) |
| **Abfrageparameter** | [`g`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<pageUrl>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 255 Byte (kein festes Limit bei Überlauf) |
| **Persistenz** | Treffer |

## Füllen einer eVar mit der URL

Adobe empfiehlt, eine eVar für die verkettete Zeichenfolge `window.location.hostname + window.location.pathname` festzulegen. Diese Zeichenfolge funktioniert in der Regel besser als `window.location.href`, da sie Protokoll-, Abfragezeichenfolgen und Verankerungs-Tags auslässt.

Wenn Sie möchten, dass die eVar genau der Dimension „Seiten-URL“ in Data Warehouse entspricht, können Sie [dynamische Variablen](/help/implement/vars/page-vars/dynamic-variables.md) verwenden und die eVar bei jedem Treffer auf `D=g` setzen.

## Dimensionselemente

Zu den Dimensionselementen gehören die URLs der Seiten auf Ihrer Site.
