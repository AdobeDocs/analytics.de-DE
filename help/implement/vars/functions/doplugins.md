---
title: doPlugins
description: Konfigurieren Sie die Logik, kurz bevor ein Treffer kompiliert und an Adobe gesendet wird.
feature: Appmeasurement Implementation
exl-id: c5113be3-04b3-4dd2-8481-ba13149750ca
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 63%

---

# doPlugins

Die `doPlugins`-Variable dient als „letzte Chance“, um Werte in Ihrer Implementierung festzulegen. Dies ist der ideale Ort, um Aufrufe an [Plug-in-Methoden](../plugins/impl-plugins.md) durchzuführen und beliebige Variablen festzulegen, bevor eine Bildanforderung gesendet wird. Falls [`usePlugins`](../config-vars/useplugins.md) aktiviert ist, wird dies automatisch ausgeführt, unmittelbar bevor eine Bildanforderung kompiliert und an Adobe gesendet wird, einschließlich:

* Alle Seitenansichtsaufrufe ([`t()`](t-method.md))
* Alle Linktracking-Aufrufe ([`tl()`](tl-method.md)), einschließlich automatischer Downloadlinks und Exitlinks

Verwenden Sie die `doPlugins`-Variable, um Plug-in-Code aufzurufen und endgültige Variablenwerte festzulegen, bevor eine Bildanforderung kompiliert und an Adobe gesendet wird.

## Verwenden des Rückruf-Codes „Ein Ereignis vor dem Senden“ mithilfe der Web SDK-Erweiterung

Anstelle von `doPlugins` verwendet die Web-SDK `onBeforeEventSend` mit ähnlichen Funktionen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter &lbrace;4 **[!UICONTROL Adobe Experience Platform Web SDK]** auf die Schaltfläche Konfigurieren[!UICONTROL .]
1. Klicken [!UICONTROL &#x200B; unter „Datenerfassung] auf die Schaltfläche **[!UICONTROL Bearbeiten vor dem Rückruf-Code senden]**.
1. Platzieren Sie den gewünschten Code im Editor.

## Verwenden `onBeforeEventSend` manuellen Implementieren der Web-SDK

Anstelle von `doPlugins` verwendet die Web-SDK `onBeforeEventSend` mit ähnlichen Funktionen. Weitere Informationen [&#x200B; Sie in der &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=de#modifying-events-globally) zu Web SDK unter „Globales Ändern von Ereignissen“.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Plug-ins, die die Adobe Analytics-Erweiterung verwenden

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
