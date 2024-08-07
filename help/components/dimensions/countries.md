---
title: Länder
description: Das Land, aus dem der Treffer stammt.
feature: Dimensions
exl-id: 47704b08-215d-4d2d-bcd4-1789e308c1c6
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 60%

---

# Länder

Die Dimension &quot;Länder&quot;[ ](overview.md) gibt das Land an, aus dem der Treffer stammt. Diese Dimension ist nützlich, um die beliebtesten Länder zu ermitteln, aus denen die Besucher beim Besuch Ihrer Website stammen. Sie können diese Daten verwenden, um sich auf Marketing-Maßnahmen in diesen Ländern zu konzentrieren oder sicherzustellen, dass Ihr Site-Erlebnis in Ländern mit unterschiedlichen Hauptsprachen optimal ist.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf interne Suchregeln von Adobe. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um die Suche zwischen IP-Adresse und Land zu unterstützen.

* Bei AppMeasurement-Implementierungen funktioniert diese Dimension standardmäßig.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Geo-Suche] beim [ Konfigurieren eines Datastreams](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören Länder auf der ganzen Welt. Zu den Beispielwerten gehören `"United States"`, `"United Kingdom"` oder `"India"`.

## Unterschiede zwischen gemeldetem und tatsächlichem Standort

Da diese Dimension auf der IP-Adresse basiert, kann in einigen Szenarien ein Unterschied zwischen dem gemeldeten und dem tatsächlichen Standort anzeigt werden:

* **IP-Adressen, die Unternehmensproxys darstellen**: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Standort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Die mobile IP-Zielerfassung funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Einige Netzbetreiber transportieren den IP-Traffic über zentralisierte oder regionale Standorte.
* **Satelliten-ISP-Benutzer**: Es ist schwierig, den spezifischen Standort dieser Benutzer zu identifizieren, da sie in der Regel vom Uplink-Standort zu stammen scheinen.
* **Militärische und staatliche IPs**: Die Mitarbeiter sind weltweit unterwegs und der Zugriff erfolgt eher über ihren Heimatstandort als von der Basis oder der Behörde aus, in der sie gegenwärtig beschäftigt sind.
* **Proxys, die aus Datenschutzgründen IP-Adressen verdecken**: Dienste wie der private Link von Apple verbergen die wahre IP-Adresse, indem sie Daten per Zufall über einen Vermittler oder Proxy senden. Dieser Proxy ersetzt dann eine andere IP-Adresse, bevor er an Adobe weitergeleitet wird.
