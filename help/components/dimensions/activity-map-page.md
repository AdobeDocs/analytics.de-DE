---
title: Activity Map-Seite
description: Der Seitenname, wenn auf einen Link geklickt wurde.
feature: Dimensions
role: User, Admin
exl-id: 8dc5d5a1-ee44-4c98-80fa-13dd1cf4edf2
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 6%

---

# Activity Map-Seite

Die Dimension &quot;Activity Map[&#x200B; zeigt &#x200B;](overview.md) Seite an, auf der sich ein Besucher befand, als auf einen Link geklickt wurde. Mithilfe dieser Dimension können Sie bestimmen, welche Seiten Links enthalten, auf die am häufigsten geklickt wird. Diese Dimension wird auch von der Activity Map-Überlagerung verwendet, um zu bestimmen, welche Links angezeigt werden sollen.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [&#x200B; &#x200B;](/help/implement/vars/page-vars/contextdata.md)Kontextdatenvariable`c.a.activitymap.page` ab. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfasst diese Kontextdatenvariable beim Klicken auf Links automatisch Daten.

Für einen bestimmten Link, auf den geklickt wurde, erfasst diese Kontextdatenvariable den Wert in der Dimension [Seite](page.md). Wenn die Seitendimension keinen Wert enthält, wird stattdessen die Dimension [Seiten-URL](page-url.md) verwendet (ähnlich wie beim Fallback, den die Seitendimension verwendet). Activity Map-Daten werden normalerweise beim nächsten Treffer gesendet, nachdem auf einen Link geklickt wurde. Mit dieser Dimension können Sie den Seitenwert bestimmen, wenn auf den Link geklickt wurde, und nicht den Seitenwert, wenn Daten gesendet wurden.

## Dimensionselemente

Dimension-Elemente enthalten alle Werte, die in der Dimension [Seite](page.md) enthalten sind.
