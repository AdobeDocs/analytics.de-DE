---
title: t
description: Senden Sie einen Seitenansichts-Tracking-Aufruf an Adobe.
feature: Appmeasurement Implementation
exl-id: c4f5b9e2-57a3-4d89-8378-39b7a4737afc
role: Admin, Developer
TQID: https://experienceleague.adobe.com/xDA52lSi35dDd4zgvT3gt1Ufgbc-LTvLL84UEN2dQp8
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 469
ht-degree: 55%

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

## Senden eines Ereignisses mit der Web SDK-Erweiterung

Verwenden Sie eine Aktion, um das Senden von XDM-Ereignisdaten an Adobe zu konfigurieren. Der Datenstrom empfängt diese Daten, wendet alle konfigurierten Zuordnungen an und leitet diese Daten an Adobe Analytics weiter, wenn es sich um einen hinzugefügten Service zu diesem Datenstrom handelt.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
1. Klicken [!UICONTROL &#x200B; unter &#x200B;]Aktionen“ auf die gewünschte Aktion oder klicken Sie auf das Symbol **&#39;+&#39;**, um eine Aktion hinzuzufügen.
1. Legen Sie die [!UICONTROL Erweiterung] Dropdown-Liste auf **[!UICONTROL Adobe Experience Platform Web SDK]** und den [!UICONTROL Aktionstyp] auf **[!UICONTROL Ereignis senden]** fest.

## Manuelles Senden des Ereignisses mit Implementierung der Web-SDK

Verwenden Sie den Befehl `sendEvent` , um Daten an Adobe zu senden. Der Datenstrom empfängt diese Daten, wendet alle konfigurierten Zuordnungen an und leitet diese Daten an Adobe Analytics weiter, wenn es sich um einen hinzugefügten Service zu diesem Datenstrom handelt.

```js
alloy("sendEvent", {
  "xdm": {}
});
```

Weitere Informationen finden Sie unter [`sendEvent`](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/sendevent/overview) in der Web SDK-Dokumentation .

## Seitenansichts-Tracking-Aufruf mit der Adobe Analytics-Erweiterung

Die Adobe Analytics-Erweiterung in der Adobe Experience Platform-Datenerfassung verfügt über einen speziellen Ort, um einen Seitenansichts-Tracking-Aufruf festzulegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
1. Klicken [!UICONTROL &#x200B; unter &#x200B;]Aktionen“ auf die gewünschte Aktion oder klicken Sie auf das Symbol **&#39;+&#39;**, um eine Aktion hinzuzufügen.
1. Legen Sie [!UICONTROL &#x200B; Dropdown]Liste „Erweiterung“ auf **[!UICONTROL Adobe Analytics]** und den [!UICONTROL Aktionstyp] auf **[!UICONTROL Beacon senden]** fest.
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
