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

Die Dimension „Betriebssystem[ gibt ](overview.md) Betriebssystem und die Version an, die der Besucher verwendet hat. Wenn Sie in Ihrer Web-Eigenschaft Funktionen haben, die betriebssystemspezifisch sind, hilft Ihnen diese Dimension zu verstehen, welche Betriebssysteme am häufigsten verwendet werden.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Adobe arbeitet mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um die Suche zwischen dem Benutzeragenten und dem Betriebssystem aufrechtzuerhalten.

* Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Gerätesuche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören die Betriebssysteme, die Besucher verwenden. Beispiele sind `"Windows 10"`, `"OS X 10.15.7"` und `"Android 9"`.

## Verfolgen genauer Betriebssystemversionen

Wenn die Branche auf Client-Hinweise zusteuert, werden einige Betriebssystemversionen möglicherweise verschmolzen. Beispielsweise können „Windows 10“ und „Windows 11“ beide unter „Windows 10“ gruppiert werden, wenn Sie keine Client-Hinweise mit hoher Entropie erfassen. Weitere Informationen finden [ unter ](/help/technotes/client-hints.md) im Technote-Handbuch.
