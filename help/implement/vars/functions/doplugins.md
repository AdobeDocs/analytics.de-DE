---
title: doPlugins
description: Konfigurieren Sie die Logik, kurz bevor ein Treffer kompiliert und an Adobe gesendet wird.
exl-id: c5113be3-04b3-4dd2-8481-ba13149750ca
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 88%

---

# doPlugins

Die `doPlugins`-Variable dient als „letzte Chance“, um Werte in Ihrer Implementierung festzulegen. Falls [`usePlugins`](../config-vars/useplugins.md) aktiviert ist, wird dies automatisch ausgeführt, unmittelbar bevor eine Bildanforderung kompiliert und an Adobe gesendet wird, einschließlich:

* Alle Seitenansichtsaufrufe ([`t()`](t-method.md))
* Alle Linktracking-Aufrufe ([`tl()`](tl-method.md)), einschließlich automatischer Downloadlinks und Exitlinks

Verwenden Sie die `doPlugins`-Variable, um Plug-in-Code aufzurufen und endgültige Variablenwerte festzulegen, bevor eine Bildanforderung kompiliert und an Adobe gesendet wird.

## Plug-ins mit Tags in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein dediziertes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.doPlugins in AppMeasurement und im benutzerdefinierten Code in 

Stellen Sie die `s.doPlugins`-Variable auf eine Funktion ein, die den gewünschten Code enthält. Die Funktion wird automatisch ausgeführt, wenn Sie einen Tracking-Aufruf ausführen.

```js
s.doPlugins = function() {/* Desired code */};
```

>[!NOTE]
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
