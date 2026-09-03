---
description: Der Name des angeklickten Links.
title: Activity Map-Link
uuid: 67864bf9-33cd-46fa-89a8-4d83d3b81152
feature: Dimensions
role: User, Admin
exl-id: 6aef3a0f-d0dd-4c84-ad44-07b286edbe18
TQID: https://experienceleague.adobe.com/A5HaPb0TghRKVykJ9V2UMJ0mlsYElLkCyBwxzTd6VII
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 8%

---

# Activity Map-Link

Die Dimension &quot;Activity Map-[&quot; ](overview.md) die beliebtesten Links an, auf die geklickt wurde. Mithilfe dieser Dimension können Sie vergleichen, welche Links auf Ihrer Site am häufigsten verwendet werden, unabhängig davon, wo auf die Links geklickt wurde.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der `c.a.activitymap.link` [Kontextdatenvariable](/help/implement/vars/page-vars/contextdata.md) ab. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfasst diese Kontextdatenvariable beim Klicken auf Links automatisch Daten.

Für einen bestimmten Link, auf den geklickt wurde, sucht Activity Map nach folgenden Elementen (in der richtigen Reihenfolge):

1. Die `s_objectID` Variable
1. Der innere Text des Links
1. Das `alt` für Bilder
1. Das `title` Attribut
1. Das `src` für Bilder
1. Das `action` für Formulare

Wenn das angeklickte Element keines der oben genannten Kriterien enthält, erfasst Activity Map keine Daten für diesen Klick.

## Dimensionselemente

Dimension-Elemente enthalten den Link-Text oder andere Link-Attribute, auf die Besucher klicken. Die Site-Struktur und Implementierung Ihres Unternehmens bestimmt die erfassten Werte.
