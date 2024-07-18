---
title: Betriebssystemtypen
description: Das Betriebssystem unabhängig von der Version.
feature: Dimensions
exl-id: 0afd5261-98e8-4247-865a-1b8844c53ff4
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 53%

---

# Betriebssystemtypen

Die Dimension &quot;Betriebssystemtypen&quot;[](overview.md) zeigt das übergeordnete Betriebssystem an, das der Besucher verwendet hat, unabhängig von bestimmten Versionen. Diese Dimension ist nützlich, um nicht nur zu verstehen, welches Betriebssystem und welche Version am häufigsten verwendet werden, sondern auch, welche typischen Besucher der Betriebssystemplattform verwenden.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Adobe arbeitet mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um die Suche zwischen Benutzeragent und Betriebssystemtyp zu unterstützen.

* Bei AppMeasurement-Implementierungen funktioniert diese Dimension standardmäßig.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Gerätesuche] bei der [ Konfiguration eines Datastreams](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Elementen der Dimension gehört der Typ des verwendeten Betriebssystems. Beispiele sind `"Microsoft Windows"`, `"Apple Macintosh"`, `"Google Android"` und `"Apple iOS"`.
