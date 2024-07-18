---
title: Domain
description: Die Organisation oder der ISP, die bzw. den der Besucher für den Internetzugang verwendet.
feature: Dimensions
exl-id: 292dc256-e9e7-47be-8586-774f1c047011
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 52%

---

# Domain

Die Dimension &quot;Domäne&quot;[](overview.md) gibt die Zugriffspunkte an, die Besucher für den Internetzugang verwenden.

## Füllen dieser Dimension mit Daten

Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um die Zugriffspunkt-Domain zu bestimmen. Zur Bestimmung der Zugriffspunkt-Domain werden verschiedene Methoden verwendet, einschließlich Reverse DNS Lookup. Es ist keine Konfiguration erforderlich und es gibt keine Variable zum Ausfüllen.

* Bei AppMeasurement-Implementierungen funktioniert diese Dimension standardmäßig.
* Aktivieren Sie für Web SDK-Implementierungen die [!UICONTROL Netzwerksuche] bei der [ Konfiguration eines Datenspeichers](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Beispiele für Dimensionselemente sind `comcast.net`, `rr.com`, `sbcglobal.net` und `amazonaws.com`. Diese Domänen sind Zugriffspunkte und nicht notwendigerweise die Domäne, die einen ISP oder eine Organisation repräsentiert.

Dimensionswerte von `None` bedeuten, dass der Inhaber der IP-Adresse des Zugriffspunkts keine Domain angegeben hat.
