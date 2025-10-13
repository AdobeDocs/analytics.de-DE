---
title: Activity Map-Region
description: Die Region auf Ihrer Site, auf die geklickt wurde.
feature: Dimensions
role: User, Admin
exl-id: e262e537-ce73-492a-8ab3-b88cd77cb8c5
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 5%

---

# Activity Map-Region

Die Dimension &quot;Activity Map[&#x200B; zeigt &#x200B;](overview.md) Regionen auf Ihrer Site an, auf die am häufigsten geklickt wurde. Diese Dimension ist nützlich, wenn Sie Klicks über übergreifende Bereiche Ihrer Site hinweg anstatt über einzelne Links vergleichen möchten. Dies ist auch für Bereiche Ihrer Site hilfreich, die dynamische Inhalte bereitstellen. Wenn Sie beispielsweise eine Startseite mit sich drehenden Nachrichtenartikeln haben, ist die Verwendung der Dimension [Activity Map Link](activity-map-link.md) schwierig, da sich der Link-Text ständig ändert. Da diese Links jedoch dieselbe Region verwenden, können Sie die Leistung dieses Bereichs analysieren, auch wenn sich einzelne Links täglich ändern können.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [&#x200B; &#x200B;](/help/implement/vars/page-vars/contextdata.md)Kontextdatenvariable`c.a.activitymap.region` ab. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfasst diese Kontextdatenvariable beim Klicken auf Links automatisch Daten.

Überprüfen Sie für einen bestimmten Link, auf den geklickt wurde, das übergeordnete DOM-Element auf Folgendes (in der richtigen Reihenfolge):

* Ein Wert im -Attribut, der durch [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md) festgelegt ist - standardmäßig auf das `id` -Attribut festgelegt
* Ein Wert im `aria-label` Attribut, wenn das Attribut `role="region"`
* Die semantischen Elemente `<header>`, `<main>`, `<footer>` oder `<nav>` (nur Web SDK)

Wenn das übergeordnete DOM-Element keines der oben genannten Kriterien erfüllt, wird die Suche rekursiv nach oben in der DOM-Hierarchie fortgesetzt. Wenn keine übereinstimmenden Elemente gefunden werden, wird der Wert `BODY` zurückgegeben.

## Dimensionselemente

Dimension-Elemente enthalten Regionen, die Sie auf Ihrer Site mit einer Beschriftung versehen haben. Bestimmte Regionswerte hängen davon ab, welche Attribute verwendet werden und ob semantische HTML-Elemente vorhanden sind.
