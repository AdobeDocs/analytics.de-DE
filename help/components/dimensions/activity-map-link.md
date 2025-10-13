---
description: Der Name des angeklickten Links.
title: Activity Map-Link
uuid: 67864bf9-33cd-46fa-89a8-4d83d3b81152
feature: Dimensions
role: User, Admin
exl-id: 6aef3a0f-d0dd-4c84-ad44-07b286edbe18
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 8%

---

# Activity Map-Link

Die Dimension &quot;Activity Map-[&quot; &#x200B;](overview.md) die beliebtesten Links an, auf die geklickt wurde. Mithilfe dieser Dimension können Sie vergleichen, welche Links auf Ihrer Site am häufigsten verwendet werden, unabhängig davon, wo auf die Links geklickt wurde.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [&#x200B; &#x200B;](/help/implement/vars/page-vars/contextdata.md)Kontextdatenvariable`c.a.activitymap.link` ab. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfasst diese Kontextdatenvariable beim Klicken auf Links automatisch Daten.

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
