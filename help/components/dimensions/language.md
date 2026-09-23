---
title: Sprache
description: Die bevorzugte Spracheinstellung im Browser.
feature: Dimensions
exl-id: 590406a4-d336-42c7-8048-e7cd8e611d43
TQID: https://experienceleague.adobe.com/KC8nBiwUbQaE8Wi5OVKdjwP-sTijGYYMBK74M-TnOFs
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
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 65%
---
# Sprache

Die Dimension [Sprache](overview.md) zeigt die wichtigsten Sprachen an, in denen Besucherinnen und Besucher Inhalte lieber sehen. Diese Dimension ist nützlich, wenn Sie die am häufigsten bevorzugten Sprachen der Besucher verstehen möchten, um die Lokalisierungsbemühungen zu unterstützen.

>[!NOTE]
>
>Diese Dimension erfasst nicht die Sprache Ihrer Site. Wenn Sie die Sprache Ihrer Site in einer Dimension erfassen möchten, empfiehlt Adobe die Verwendung einer benutzerdefinierten Variable, z. B. einer [eVar](evar.md).

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `Accept-Language` in den Bildanforderungen. Dies funktioniert standardmäßig in jeder AppMeasurement- oder Web SDK (Tags)-Implementierung - es gibt keine Variable zum Festlegen.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (HTTP-Kopfzeile) |
| **Feld Web SDK/XDM** | Keine (HTTP-Kopfzeile) |
| **Abfrageparameter** | None (verwendet den `Accept-Language`-Header) |
| **XML-Tag** | [`<language>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Die Dimensionselemente enthalten die Anzeigenamen der bevorzugten Sprachen der Besucher. Beispiele sind `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"` und `"Spanish (Spain)"`. Wenn eine Bildanforderung keine gültige Sprache in der HTTP-Kopfzeile enthält, lautet das Dimensionselement `"None"`.
