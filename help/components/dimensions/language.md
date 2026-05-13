---
title: Sprache
description: Die bevorzugte Spracheinstellung im Browser.
feature: Dimensions
exl-id: 590406a4-d336-42c7-8048-e7cd8e611d43
TQID: https://experienceleague.adobe.com/KC8nBiwUbQaE8Wi5OVKdjwP-sTijGYYMBK74M-TnOFs
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 91%

---

# Sprache

Die Dimension [Sprache](overview.md) zeigt die wichtigsten Sprachen an, in denen Besucherinnen und Besucher Inhalte lieber sehen. Diese Dimension ist nützlich, wenn Sie die am häufigsten bevorzugten Sprachen der Besucher verstehen möchten, um die Lokalisierungsbemühungen zu unterstützen.

>[!NOTE]
>
>Diese Dimension erfasst nicht die Sprache Ihrer Site. Wenn Sie die Sprache Ihrer Site in einer Dimension erfassen möchten, empfiehlt Adobe die Verwendung einer benutzerdefinierten Variable, z. B. einer [eVar](evar.md).

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `Accept-Language` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Die Dimensionselemente enthalten die Anzeigenamen der bevorzugten Sprachen der Besucher. Beispiele sind `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"` und `"Spanish (Spain)"`. Wenn eine Bildanforderung keine gültige Sprache in der HTTP-Kopfzeile enthält, lautet das Dimensionselement `"None"`.
