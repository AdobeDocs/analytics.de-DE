---
title: Browser
description: Name und Version des verwendeten Browsers.
feature: Dimensions
exl-id: 2bdf2a5a-3482-43fa-b2e1-fbea892918fb
TQID: https://experienceleague.adobe.com/J6rDfVwmRZpRLrultdurQkRih2HcPygjcjwO0bkms5E
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
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
source-wordcount: 202
ht-degree: 59%

---

# Browser

&quot;[!UICONTROL Browser]&quot; [Dimension](overview.md) zeigt den Namen und die Version des Browsers an, der den Treffer sendet. Diese Dimension ist nützlich, wenn Sie die gängigsten Browser messen möchten, die Besucher verwenden. Beim Testen neuer Versionen Ihrer Site können Sie diese Tests mit den wichtigsten Browsern in dieser Dimension ausführen, um den Aufwand für die Qualitätssicherung zu optimieren.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Adobe arbeitet mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um Suchen zwischen Benutzeragenten und Browser zu verwalten.

* Bei AppMeasurement-Implementierungen ist diese Dimension vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Gerätesuche] beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören die verwendeten Browsernamen und -versionen. Verschiedene Versionen desselben Browsers sind separate Dimensionselemente.

Einige Dimensionselemente enthalten `"(unknown version)"` anstelle ihrer Versionsnummer. Dieses Dimensionselement verweist auf eine neuere Browser-Version, die Adobe noch nicht zu ihren Lookup-Tabellen hinzugefügt hat. Da Browser häufig aktualisiert werden, ist `"(unknown version)"` für einen bestimmten Browser üblich und vorübergehend. Adobe aktualisiert die Suchtabellen in der Regel während der monatlichen Wartungsversionen.