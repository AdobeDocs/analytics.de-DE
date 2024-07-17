---
title: t
description: Senden Sie einen Seitenansichts-Tracking-Aufruf an Adobe.
feature: Variables
exl-id: c4f5b9e2-57a3-4d89-8378-39b7a4737afc
role: Admin, Developer
source-git-commit: e47bee837faf9b8cf080d878da860795ced014d5
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 56%

---

# t() 

Die `t()`-Methode ist eine wichtige Kernkomponente von Adobe Analytics. Sie nimmt alle auf der Seite definierten Analytics-Variablen, kompiliert sie in eine Bildanforderung und sendet diese Daten an die Adobe-Datenerfassungs-Server.

Betrachten Sie beispielsweise den folgenden JavaScript-Code:

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Define config variables and page variables
s.trackingServerSecure = "data.example.com";
s.eVar1 = "Example dimension item";

// Compile the variables on the page into an image request to Adobe
s.t();
```

Beim Ausführen der `t()`-Methode werden alle definierten Analytics-Variablen verwendet und eine URL auf der Grundlage dieser Variablen formuliert. Einige Analytics-Variablen bestimmen die URL des Bildes, während andere Variablen die Parameterwerte der Abfragezeichenfolge bestimmen.

```text
https://data.example.com/b/ss/examplersid/1/?v1=Example%20dimension%20item
```

Adobe empfängt die Bildanforderung und analysiert dann die Parameter für Anforderungsheader, URL und Abfragezeichenfolge. Datenerfassungs-Server geben dann ein transparentes 1x1-Pixel-Bild zurück, das unsichtbar auf Ihrer Website angezeigt wird.

## Ereignis mit der Web SDK-Erweiterung senden

Verwenden Sie eine Aktion, um das Senden von XDM-Ereignisdaten an Adobe zu konfigurieren. Der Datastream empfängt diese Daten, wendet konfigurierte Zuordnungen an und leitet diese Daten an Adobe Analytics weiter, wenn es sich um einen hinzugefügten Dienst für diesen Datastream handelt.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
1. Klicken Sie unter [!UICONTROL Aktionen] auf die gewünschte Aktion oder klicken Sie auf das Symbol **&#39;+&#39;** , um eine Aktion hinzuzufügen.
1. Setzen Sie die Dropdownliste [!UICONTROL Erweiterung] auf **[!UICONTROL Adobe Experience Platform Web SDK]** und den Aktionstyp ] auf **[!UICONTROL Ereignis senden]**.[!UICONTROL 

## Ereignis manuell zur Implementierung des Web SDK senden

Verwenden Sie den Befehl `sendEvent` , um Daten an Adobe zu senden. Der Datastream empfängt diese Daten, wendet konfigurierte Zuordnungen an und leitet diese Daten an Adobe Analytics weiter, wenn es sich um einen hinzugefügten Dienst für diesen Datastream handelt.

```js
alloy("sendEvent", {
  "xdm": {}
});
```

Weitere Informationen finden Sie unter [Ereignisse verfolgen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=de) in der Web SDK-Dokumentation.

## Seitenansichts-Tracking-Aufruf mit der Adobe Analytics-Erweiterung

Die Adobe Analytics-Erweiterung in der Adobe Experience Platform-Datenerfassung verfügt über einen speziellen Speicherort, um einen Seitenansichts-Tracking-Aufruf festzulegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
1. Klicken Sie unter [!UICONTROL Aktionen] auf die gewünschte Aktion oder klicken Sie auf das Symbol **&#39;+&#39;** , um eine Aktion hinzuzufügen.
1. Setzen Sie die Dropdownliste [!UICONTROL Erweiterung] auf **[!UICONTROL Adobe Analytics]** und den Aktionstyp [!UICONTROL 5} auf **[!UICONTROL Beacon senden]**.]
1. Klicken Sie auf die Optionsschaltfläche `s.t()`.

## s.t()-Methode in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.t()`-Methode auf, wenn Sie einen Tracking-Aufruf an Adobe senden möchten.

```js
s.t();
```

Optional können Sie ein Objekt als Argument verwenden, um Variablenwerte zu überschreiben. Weitere Informationen finden Sie unter [Variablenüberschreibungen](../../js/overrides.md).

```js
var y = new Object();
y.eVar1 = "Override value";
s.t(y);
```

>[!NOTE]
>
>In früheren Versionen von AppMeasurement wurden mehrere Code-Zeilen verwendet, um diese Funktion aufzurufen. Der zusätzliche Code enthielt historisch gesehen Workarounds für verschiedene Browser. Die Standardisierung und Best Practices in modernen Browsern erfordern diesen Code-Block nicht mehr. Jetzt wird nur noch der `s.t()`-Methodenaufruf benötigt.
