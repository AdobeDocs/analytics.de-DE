---
title: pageURL
description: Überschreiben Sie die automatisch erfasste Seiten-URL auf Ihrer Site.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# pageURL

AppMeasurement erfasst automatisch die Seiten-URL bei jedem Treffer. Wenn Sie die automatisch von AppMeasurement erfasste Seiten-URL außer Kraft setzen möchten, können Sie diese Variable verwenden. In den meisten Fällen müssen Sie diese Variable nicht festlegen.

> [!NOTE] Diese Variable ist keine verfügbare Dimension im Analysis Workspace. Sie ist nur in Data Warehouse und Data Feeds verfügbar. Wenn Sie die Seiten-URL als Dimension in Analysis Workspace verwenden möchten, sollten Sie die `pageURL` Variable bei jedem Treffer in eine eVar übergeben.

Manchmal sind URLs länger als 255 Byte. AppMeasurement verwendet den `g` Abfragezeichenfolgenparameter für die ersten 255 Byte der URL in Bildanforderungen. Wenn eine URL länger als 255 Byte ist, wird der Rest der URL im Abfragezeichenfolgen-Parameter gespeichert `-g` . Protokoll- und Abfragezeichenfolgen in der URL sind in dieser Variablen enthalten.

## Seiten-URL beim Starten der Adobe Experience Platform

Beim Start wird die Seiten-URL automatisch gefüllt. Sie können die Seiten-URL-Umgehung jedoch entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL Seiten-URL] .

Sie können die Seiten-URL auf einen beliebigen Zeichenfolgenwert einstellen.

## s.pageURL in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.pageURL` Variable ist eine Zeichenfolge, die die URL der Seite enthält. AppMeasurement erfasst diese Variable automatisch, Sie können jedoch ihren Wert bei Bedarf überschreiben.

```js
s.pageURL = "https://example.com";
```

Wenn Sie die Seiten-URL als Dimension in Berichten verwenden möchten, sollten Sie Folgendes in Ihrer Implementierung berücksichtigen:

```js
// Set eVar1 to page URL without protocol or query strings
s.eVar1 = window.location.hostname + window.location.pathname;
```
