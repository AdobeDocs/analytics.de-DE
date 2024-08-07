---
title: Browser-Typ
description: Die Organisation, die den Browser erstellt hat.
feature: Dimensions
exl-id: 2a88ebc6-879e-4e5b-a8e5-40a32d54ac1b
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 67%

---

# Browser-Typ

Die Dimension &quot;Browsertyp&quot;[Dimension](overview.md) listet die Organisationen auf, die den vom Besucher verwendeten Browser erstellt haben. Diese Dimension ist nützlich, wenn Sie sehen möchten, welche übergeordneten Browser von Besuchern verwendet werden. Sie ist insofern nützlicher als die Dimension „Browser“, als sie verschiedene Versionen desselben Browsers nicht als separate Dimensionselemente auflistet.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Adobe arbeitet mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um Suchen zwischen Benutzeragent und Browser zu unterhalten.

* Bei AppMeasurement-Implementierungen funktioniert diese Dimension standardmäßig.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Gerätesuche] bei der [ Konfiguration eines Datastreams](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören die Organisationen, die Browser erstellen. Zu den gängigen Dimensionselementen gehören `"Google"` (die Ersteller von [!DNL Chrome]), `"Apple"` (die Ersteller von [!DNL Safari]), `"Microsoft"` (die Ersteller von [!DNL Edge]) und `"Mozilla"` (die Ersteller von [!DNL Firefox]).
