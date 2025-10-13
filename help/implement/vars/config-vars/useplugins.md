---
title: usePlugins
description: Aktivieren oder deaktivieren Sie die doPlugins()-Funktion.
feature: Appmeasurement Implementation
exl-id: e8499acf-d8b9-490c-9f67-ad9a8f6ca7df
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 34%

---

# usePlugins

Wenn `usePlugins` aktiviert ist, wird die [`doPlugins()`](../functions/doplugins.md)-Funktion kurz vor der AppMeasurement-Kompilierung ausgeführt und ein Treffer an Adobe gesendet. Aktivieren Sie diese Variable, wenn Sie die `doPlugins()`-Funktion verwenden.

## Verwenden des `onBeforeEventSend` Callbacks mithilfe der Web-SDK

Web SDK verfügt zwar über keinen booleschen Wert, der die Ausführung zusätzlicher Logik handhabt, bevor Daten an Adobe gesendet werden, Sie können jedoch den `onBeforeEventSend`-Callback registrieren, um Daten zu ändern. Weitere Informationen [&#x200B; Sie in der &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=de#modifying-events-globally) zu Web SDK unter „Globales Ändern von Ereignissen“.

## Verwenden von Plug-ins mit der Adobe Analytics-Erweiterung

Adobe bietet eine Erweiterung mit der Bezeichnung „Common Analytics Plugins“, mit der Sie die meisten [Plug-ins“ &#x200B;](../plugins/impl-plugins.md) können. Installieren Sie die Erweiterung und rufen Sie das gewünschte Plug-in in einer Regel auf.

Wenn das gewünschte Plug-in nicht in der Adobe-Erweiterung enthalten ist, verwenden Sie den Editor für benutzerspezifischen Code entsprechend der AppMeasurement-Syntax.

## s.usePlugins in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.usePlugins`-Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `doPlugins()`-Funktion aufruft. Der Standardwert lautet `false`. Setzen Sie diese Variable auf `true`, wenn Sie die `doPlugins()`-Funktion in Ihrer Implementierung verwenden.

```js
s.usePlugins = true;
```
