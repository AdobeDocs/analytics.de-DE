---
title: Activity Map-Region
description: Die Region auf Ihrer Site, auf die geklickt wurde.
feature: Dimensions
role: User, Admin
exl-id: e262e537-ce73-492a-8ab3-b88cd77cb8c5
TQID: https://experienceleague.adobe.com/mmLp5-dgKGeovIOMPZxliyhfbpUSMLXca-3Qs6QA0SA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 249
ht-degree: 5%

---

# Activity Map-Region

Die Dimension &quot;Activity Map[ zeigt ](overview.md) Regionen auf Ihrer Site an, auf die am häufigsten geklickt wurde. Diese Dimension ist nützlich, wenn Sie Klicks über übergreifende Bereiche Ihrer Site hinweg anstatt über einzelne Links vergleichen möchten. Dies ist auch für Bereiche Ihrer Site hilfreich, die dynamische Inhalte bereitstellen. Wenn Sie beispielsweise eine Startseite mit sich drehenden Nachrichtenartikeln haben, ist die Verwendung der Dimension [Activity Map Link](activity-map-link.md) schwierig, da sich der Link-Text ständig ändert. Da diese Links jedoch dieselbe Region verwenden, können Sie die Leistung dieses Bereichs analysieren, auch wenn sich einzelne Links täglich ändern können.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der `c.a.activitymap.region` [Kontextdatenvariable](/help/implement/vars/page-vars/contextdata.md) ab. Wenn Ihre Implementierung [Activity Map](/help/analyze/activity-map/overview.md) verwendet, erfasst diese Kontextdatenvariable beim Klicken auf Links automatisch Daten.

Überprüfen Sie für einen bestimmten Link, auf den geklickt wurde, das übergeordnete DOM-Element auf Folgendes (in der richtigen Reihenfolge):

* Ein Wert im -Attribut, der durch [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md) festgelegt ist - standardmäßig auf das `id` -Attribut festgelegt
* Ein Wert im `aria-label` Attribut, wenn das Attribut `role="region"`
* Die semantischen Elemente `<header>`, `<main>`, `<footer>` oder `<nav>` (nur Web SDK)

Wenn das übergeordnete DOM-Element keines der oben genannten Kriterien erfüllt, wird die Suche rekursiv nach oben in der DOM-Hierarchie fortgesetzt. Wenn keine übereinstimmenden Elemente gefunden werden, wird der Wert `BODY` zurückgegeben.

## Dimensionselemente

Dimension-Elemente enthalten Regionen, die Sie auf Ihrer Site mit einer Beschriftung versehen haben. Bestimmte Regionswerte hängen davon ab, welche Attribute verwendet werden und ob semantische HTML-Elemente vorhanden sind.
