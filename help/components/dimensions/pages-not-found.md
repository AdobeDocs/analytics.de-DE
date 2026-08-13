---
title: Seiten nicht gefunden (Dimensionen)
description: URLs, die einen Fehler auf Ihrer Site zurückgegeben haben.
feature: Dimensions
exl-id: 28c22565-7fcf-49f1-8876-0db88f12a182
TQID: https://experienceleague.adobe.com/0S2WzNRJrtOa9ZPTg5cmbwxMLJE5tI6Qa3GtZs6GqKc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 73%

---

# Seiten nicht gefunden

*Auf dieser Hilfeseite wird beschrieben, wie „Seiten nicht gefunden“ als [Dimension“ ](overview.md). Weitere Informationen [ Funktionsweise als Metrik finden Sie ](../metrics/pages-not-found.md) Metrikseite „Seiten nicht gefunden“*

Die Dimension „Seiten nicht gefunden“ gibt URLs an, die einen Fehler enthalten. Diese Dimension ist nützlich, wenn Sie die Anzahl der Fehler verringern möchten, die Besucherinnen und Besucher auf Ihrer Site erhalten.

* Sie können diese Dimension in einer [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) verwenden, um zu sehen, durch welche Seiten Besucher klicken, um den Fehler zu erreichen. Anschließend können Sie mit Entwicklungs-Teams in Ihrem Unternehmen zusammenarbeiten, um den Link auf jeder Seite zu reparieren.
* Sie können diese Dimension mit der Dimension [Referrer](referrer.md) verwenden, um zu sehen, wo Besucher über externe Links zu Ihrer Site gelangen. Sie können dann entweder Umleitungen zum gewünschten Ort implementieren oder mit dem Drittanbieter zusammenarbeiten, um den Link zu reparieren.

>[!NOTE]
>
>In Data Warehouse heißt diese Dimension &quot;[!UICONTROL Seitentyp-Fehler].

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus den [`pageType`- und `g`-Abfragezeichenfolgen](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. Wenn die Abfragezeichenfolge `pageType` gleich `errorPage` ist, wird die Abfragezeichenfolge `g` (Seiten-URL) aufgezeichnet. AppMeasurement erfasst diese Daten mit der [`pageType`](/help/implement/vars/page-vars/pagetype.md)-Variable. Wenn die Variable `pageType` nicht definiert oder auf einen anderen Wert als `errorPage` festgelegt ist, werden keine Daten für diese Dimension erfasst.

## Dimensionselemente

Zu den Dimensionselementen gehören die URLs der Seiten auf Ihrer Site, auf denen ein Fehler aufgetreten ist.
