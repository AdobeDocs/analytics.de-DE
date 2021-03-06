---
title: US-DMA
description: Das ausgewiesene Marktgebiet des Treffers.
feature: Dimensions
exl-id: 156d5755-2e93-4240-bde3-1d537422b7bf
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '267'
ht-degree: 100%

---

# US-DMA

Die Dimension „US-DMA“ gibt das ausgewiesene Marktgebiet (DMA) des Besuchers an. Sie basiert auf den von [Nielsen](https://www.nielsen.com/us/en/intl-campaigns/dma-maps/) erstellten Medienmärkten.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf interne Suchregeln von Adobe. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit Nielsen zusammen, um die Suche zwischen IP-Adresse und DMA zu unterstützen. Diese Dimension ist bei allen Implementierungen vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen gehören das DMA und der DMA-Code des Besuchers. Der dreistellige Code ist keine Postleitzahl, sondern der DMA-Code von Nielsen. Zu den Beispielwerten gehören `"Dallas-Ft. Worth (623)"`, `"New York (501)"` oder `"Los Angeles (803)"`. Das Dimensionselement `"No Metro (0)"` umfasst den gesamten internationalen Traffic außerhalb der Vereinigten Staaten.

## Unterschiede zwischen gemeldetem und tatsächlichem Standort

Da diese Dimension auf der IP-Adresse basiert, kann in einigen Szenarien ein Unterschied zwischen dem gemeldeten und dem tatsächlichen Standort anzeigt werden:

* **IP-Adressen, die Unternehmensproxys darstellen**: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Standort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Die mobile IP-Zielerfassung funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Eine Reihe von Netzbetreibern transportiert den IP-Traffic über zentralisierte oder regionale POPs (Points of Presence).
* **Satelliten-ISP-Benutzer**: Es ist schwierig, den spezifischen Standort dieser Benutzer zu identifizieren, da sie in der Regel vom Uplink-Standort zu stammen scheinen.
* **Militärische und staatliche IPs**: Die Mitarbeiter sind weltweit unterwegs und der Zugriff erfolgt eher über ihren Heimatstandort als von der Basis oder der Behörde aus, in der sie gegenwärtig beschäftigt sind.
