---
title: Betriebssystem
description: Das Betriebssystem des Besuchers.
feature: Dimensions
exl-id: e3911ae0-d242-4da2-a4bc-b2f4877f9dd2
TQID: https://experienceleague.adobe.com/WM6GQ-AhLmtudRWXF6lOez6DaVxMBU3rSaEb2UdsXdc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 45%

---

# Betriebssystem

Die Dimension „Betriebssystem[&#x200B; gibt &#x200B;](overview.md) Betriebssystem und die Version an, die der Besucher verwendet hat. Wenn Sie in Ihrer Web-Eigenschaft Funktionen haben, die betriebssystemspezifisch sind, hilft Ihnen diese Dimension zu verstehen, welche Betriebssysteme am häufigsten verwendet werden.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Adobe arbeitet mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um die Suche zwischen Benutzeragenten und Betriebssystem zu verwalten.

* Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Gerätesuche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören die Betriebssysteme, die Besucher verwenden. Beispiele sind `"Windows 10"`, `"OS X 10.15.7"` und `"Android 9"`.

## Verfolgen genauer Betriebssystemversionen

Wenn die Branche auf Client-Hinweise zusteuert, werden einige Betriebssystemversionen möglicherweise verschmolzen. Beispielsweise können „Windows 10“ und „Windows 11“ beide unter „Windows 10“ gruppiert werden, wenn Sie keine Client-Hinweise mit hoher Entropie erfassen. Weitere Informationen finden [&#x200B; unter &#x200B;](/help/technotes/client-hints.md) im Technote-Handbuch.
