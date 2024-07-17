---
title: Activity Map-Seite
description: Der Seitenname, an dem auf einen Link geklickt wurde.
feature: Dimensions
role: User, Admin
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 6%

---

# Activity Map-Seite

Die Dimension &quot;Activity Map-Seite&quot;[](overview.md) zeigt die Seite an, auf der sich ein Besucher befand, als auf einen Link geklickt wurde. Sie können diese Dimension verwenden, um zu bestimmen, welche Seiten Links enthalten, auf die am häufigsten geklickt wird. Diese Dimension wird auch von der Activity Map-Überlagerung verwendet, um zu bestimmen, welche Links angezeigt werden sollen.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.page` ab. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfasst diese Kontextdatenvariable automatisch Daten, wenn auf Links geklickt wird.

Für einen Link, auf den geklickt wurde, erfasst diese Kontextdatenvariable den Wert in der Dimension [Seite](page.md) . Wenn die Dimension Seite keinen Wert enthält, wird stattdessen die Dimension [Seiten-URL](page-url.md) verwendet (ähnlich wie der Fallback, den die Dimension Seite verwendet). Activity Map-Daten werden normalerweise beim nächsten Treffer gesendet, nachdem auf einen Link geklickt wurde. Mit dieser Dimension können Sie den Seitenwert beim Klicken auf den Link anstelle des Seitenwerts beim Senden von Daten ermitteln.

## Dimensionselemente

Zu den Dimension-Elementen gehören alle Werte, die in der Dimension [Seite](page.md) gefunden werden.
