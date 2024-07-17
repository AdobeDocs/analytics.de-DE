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

Die Dimension &quot;Activity Map-Link&quot;[](overview.md) enthält die beliebtesten Links, auf die geklickt wurde. Sie können diese Dimension verwenden, um zu vergleichen, welche Links auf Ihrer Site am häufigsten verwendet werden, unabhängig davon, wo auf die Links geklickt wurde.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.link` ab. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfasst diese Kontextdatenvariable automatisch Daten, wenn auf Links geklickt wird.

Für einen Link, auf den geklickt wurde, sucht Activity Map in der angegebenen Reihenfolge nach Folgendem:

1. Die Variable `s_objectID`
1. Der innere Text des Links
1. Das Attribut `alt` für Bilder
1. Das Attribut `title`
1. Das Attribut `src` für Bilder
1. Das Attribut `action` für Formulare

Wenn das angeklickte Element keines der oben genannten Kriterien enthält, erfasst Activity Map keine Daten für diesen Klick.

## Dimensionselemente

Zu den Dimension-Elementen gehören der Linktext oder andere Link-Attribute, auf die Besucher klicken. Die Site-Struktur und Implementierung Ihres Unternehmens bestimmt die exakten erfassten Werte.
