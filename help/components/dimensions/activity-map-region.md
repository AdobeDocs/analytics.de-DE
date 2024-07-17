---
title: Activity Map-Region
description: Die Region auf Ihrer Site, auf die geklickt wurde.
feature: Dimensions
role: User, Admin
source-git-commit: 05010d58ba2a3376473097e9d4543ee4415e83e1
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 5%

---

# Activity Map-Region

Die Dimension &quot;Activity Map Region&quot;[](overview.md) zeigt die Regionen auf Ihrer Site an, auf die am häufigsten geklickt wurde. Diese Dimension ist nützlich, wenn Sie Klicks über übergeordnete Regionen Ihrer Site hinweg anstelle einzelner Links vergleichen möchten. Dies ist auch für Bereiche Ihrer Site hilfreich, die dynamischen Inhalt bereitstellen. Wenn Sie beispielsweise eine Titelseite mit sich drehenden News-Artikeln haben, wäre die Verwendung der Dimension [Activity Map-Link](activity-map-link.md) schwierig, da sich der Linktext ständig ändert. Da diese Links jedoch dieselbe Region verwenden, können Sie die Leistung dieses Bereichs analysieren, auch wenn sich einzelne Links täglich ändern können.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) `c.a.activitymap.region` ab. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfasst diese Kontextdatenvariable automatisch Daten, wenn auf Links geklickt wird.

Überprüfen Sie für einen angeklickten Link das übergeordnete DOM-Element auf Folgendes (in der Reihenfolge):

* Ein Wert im Attribut, der durch [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md) festgelegt wird - standardmäßig auf das Attribut `id` gesetzt
* Ein Wert im Attribut `aria-label` , wenn das Attribut `role="region"`
* Die semantischen Elemente `<header>`, `<main>`, `<footer>` oder `<nav>` (nur Web SDK)

Wenn das übergeordnete DOM-Element keines der oben genannten Kriterien erfüllt, wird die Suche rekursiv in der DOM-Hierarchie fortgesetzt. Wenn keine übereinstimmenden Elemente gefunden werden, wird der Wert `BODY` zurückgegeben.

## Dimensionselemente

Zu den Dimensionen gehören Regionen, die Sie auf Ihrer Site gekennzeichnet haben. Bestimmte Regionswerte hängen davon ab, welche Attribute verwendet werden und ob semantische HTML-Elemente vorhanden sind.
