---
title: doPlugins
description: Konfigurieren Sie die Logik, kurz bevor ein Treffer kompiliert und an Adobe gesendet wird.
feature: Variables
exl-id: c5113be3-04b3-4dd2-8481-ba13149750ca
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 63%

---

# doPlugins

Die `doPlugins`-Variable dient als „letzte Chance“, um Werte in Ihrer Implementierung festzulegen. Es ist der ideale Ort, um [Plug-in-Methoden](../plugins/impl-plugins.md) aufzurufen und alle gewünschten Variablen festzulegen, bevor eine Bildanforderung gesendet wird. Falls [`usePlugins`](../config-vars/useplugins.md) aktiviert ist, wird dies automatisch ausgeführt, unmittelbar bevor eine Bildanforderung kompiliert und an Adobe gesendet wird, einschließlich:

* Alle Seitenansichtsaufrufe ([`t()`](t-method.md))
* Alle Linktracking-Aufrufe ([`tl()`](tl-method.md)), einschließlich automatischer Downloadlinks und Exitlinks

Verwenden Sie die `doPlugins`-Variable, um Plug-in-Code aufzurufen und endgültige Variablenwerte festzulegen, bevor eine Bildanforderung kompiliert und an Adobe gesendet wird.

## Verwenden von On Before Event Send Callback-Code mit der Web SDK-Erweiterung

Anstelle von `doPlugins` verwendet das Web SDK `onBeforeEventSend` mit ähnlichen Funktionen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter [!UICONTROL Adobe Experience Platform Web SDK] auf die Schaltfläche **[!UICONTROL Konfigurieren]** .
1. Klicken Sie unter [!UICONTROL Datenerfassung] auf die Schaltfläche **[!UICONTROL Vor dem Senden des Rückruffods durch das Ereignis bearbeiten]** .
1. Platzieren Sie den gewünschten Code im Editor.

## Manuelles Implementieren des Web SDK mit `onBeforeEventSend`

Anstelle von `doPlugins` verwendet das Web SDK `onBeforeEventSend` mit ähnlichen Funktionen. Weitere Informationen finden Sie unter [Globales Ändern von Ereignissen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) in der Web SDK-Dokumentation.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Plug-ins mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.doPlugins in AppMeasurement und im benutzerdefinierten Code

Stellen Sie die `s.doPlugins`-Variable auf eine Funktion ein, die den gewünschten Code enthält. Die Funktion wird automatisch ausgeführt, wenn Sie einen Tracking-Aufruf ausführen.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!IMPORTANT]
>
>Setzen Sie eine Funktion in Ihrer Implementierung nur einmal auf die `doPlugins`-Variable. Wenn Sie die `doPlugins`-Variable mehrmals festlegen, wird nur der neueste Code verwendet.

## Beispiele

```js
// Set eVar1 to the web page's title
s.doPlugins = function() {
  s.eVar1 = window.document.title;
};

// Use the getPreviousValue plug-in (requires plug-in code outside the function)
s.doPlugins = function() {
  s.eVar1 = s.getPreviousValue(s.pageName,'gpv_pn');
}
```

>[!NOTE]
>
>Frühere Versionen von AppMeasurement hatten einen etwas anderen `doPlugins()`-Code. Adobe empfiehlt die Verwendung des oben genannten Formats als Best Practice.
