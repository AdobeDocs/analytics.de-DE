---
title: Activity Map-Seite
description: Der Seitenname, wenn auf einen Link geklickt wurde.
feature: Dimensions
role: User, Admin
exl-id: 8dc5d5a1-ee44-4c98-80fa-13dd1cf4edf2
TQID: https://experienceleague.adobe.com/WJ0uk-LqIABwehzzy79c2o1cd3EvI-AKUJ--vmLnKRE
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 6%

---

# Activity Map-Seite

Die Dimension &quot;Activity Map[ zeigt ](overview.md) Seite an, auf der sich ein Besucher befand, als auf einen Link geklickt wurde. Mithilfe dieser Dimension können Sie bestimmen, welche Seiten Links enthalten, auf die am häufigsten geklickt wird. Diese Dimension wird auch von der Activity Map-Überlagerung verwendet, um zu bestimmen, welche Links angezeigt werden sollen.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der `c.a.activitymap.page` [Kontextdatenvariable](/help/implement/vars/page-vars/contextdata.md) ab. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfasst diese Kontextdatenvariable beim Klicken auf Links automatisch Daten.

Für einen bestimmten Link, auf den geklickt wurde, erfasst diese Kontextdatenvariable den Wert in der Dimension [Seite](page.md). Wenn die Seitendimension keinen Wert enthält, wird stattdessen die Dimension [Seiten-URL](page-url.md) verwendet (ähnlich wie beim Fallback, den die Seitendimension verwendet). Activity Map-Daten werden normalerweise beim nächsten Treffer gesendet, nachdem auf einen Link geklickt wurde. Mit dieser Dimension können Sie den Seitenwert bestimmen, wenn auf den Link geklickt wurde, und nicht den Seitenwert, wenn Daten gesendet wurden.

## Dimensionselemente

Dimension-Elemente enthalten alle Werte, die in der Dimension [Seite](page.md) enthalten sind.
