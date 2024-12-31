---
title: Städte
description: Die Stadt, aus der der Treffer stammt.
feature: Dimensions
exl-id: c04525bb-50d6-4d28-b5dc-335d089e184b
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 73%

---

# Städte

Die Dimension &quot;[&quot; ](overview.md) die Stadt an, aus der der Treffer stammt. Diese Dimension ist nützlich, um die beliebtesten Städte zu ermitteln, aus denen die Besucher beim Besuch Ihrer Website stammen. Sie könnten diese Daten nutzen, um sich auf lokale Werbung in diesen Städten zu konzentrieren, wie etwa Werbetafeln oder Werbe-Spots.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf interne Suchregeln von Adobe. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um Suchen zwischen IP-Adresse und Stadt zu verwalten.

* Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Geo-Suche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören Städter auf der ganzen Welt. Zu den Beispielwerten gehören `"New York (New York, United States)"`, `"Bangalore (Karnataka, India)"` oder `"London (London, United Kingdom)"`.

Einige Dimensionselemente können `"AOL"`, einen DFÜ-Dienstleister umfassen. Abonnenten dieses Dienstes wird ein Zugangspunkt zugewiesen, der auf dem Land basiert, in dem ihre Kontonummer eingerichtet ist. AOL-Benutzer verwenden die IP-Adresse dieses Zugriffspunkts. Da diese Dimension auf der IP-Adresse basiert, wird die Geolokalisierung des Zugangspunktes anstelle des tatsächlichen Standortes des Besuchers verwendet.

## Unterschiede zwischen gemeldetem und tatsächlichem Standort

Da diese Dimension auf der IP-Adresse basiert, kann in einigen Szenarien ein Unterschied zwischen dem gemeldeten und dem tatsächlichen Standort anzeigt werden:

* **IP-Adressen, die Unternehmensproxys darstellen**: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Standort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Die mobile IP-Zielerfassung funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Einige Fluggesellschaften befördern den IP-Verkehr über zentrale oder regionale Anlaufstellen.
* **Satelliten-ISP-Benutzer**: Es ist schwierig, den spezifischen Standort dieser Benutzer zu identifizieren, da sie in der Regel vom Uplink-Standort zu stammen scheinen.
* **Militärische und staatliche IPs**: Die Mitarbeiter sind weltweit unterwegs und der Zugriff erfolgt eher über ihren Heimatstandort als von der Basis oder der Behörde aus, in der sie gegenwärtig beschäftigt sind.
* **Proxys, die IP-Adressen aus Datenschutzgründen verdecken**: Services wie das Private Relay von Apple verbergen die wahre IP-Adresse, indem sie zufällig Daten über einen Vermittler oder Proxy senden. Dieser Proxy ersetzt dann eine andere IP-Adresse, bevor er an Adobe weitergeleitet wird.
