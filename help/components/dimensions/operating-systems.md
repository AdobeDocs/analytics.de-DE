---
title: Betriebssystem
description: Das Betriebssystem des Besuchers.
feature: Dimensions
exl-id: e3911ae0-d242-4da2-a4bc-b2f4877f9dd2
source-git-commit: 9c3e65392d6e5929ce1ecefbc460c1fd5576aed8
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 42%

---

# Betriebssystem

Die Dimension &quot;Betriebssystem&quot;[](overview.md) zeigt das Betriebssystem und die Version an, die der Besucher verwendet hat. Wenn Sie in Ihrer Web-Eigenschaft Funktionen haben, die betriebssystemspezifisch sind, hilft Ihnen diese Dimension zu verstehen, welche Betriebssysteme am häufigsten verwendet werden.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Adobe arbeitet mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um die Suche zwischen Benutzeragent und Betriebssystem zu unterstützen.

* Bei AppMeasurement-Implementierungen funktioniert diese Dimension standardmäßig.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Gerätesuche] bei der [ Konfiguration eines Datastreams](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören die Betriebssysteme, die Besucher verwenden. Beispiele sind `"Windows 10"`, `"OS X 10.15.7"` und `"Android 9"`.

## Tracking genauer Betriebssystemversionen

Wenn sich die Branche zu Client-Hinweisen bewegt, sind einige Betriebssystemversionen möglicherweise verwirrt. Beispielsweise können &quot;Windows 10&quot;und &quot;Windows 11&quot;unter &quot;Windows 10&quot;gruppiert werden, wenn Sie keine Client-Hinweise mit hoher Entropie erfassen. Weitere Informationen finden Sie unter [Client-Hinweise](/help/technotes/client-hints.md) im Technotes-Handbuch.
