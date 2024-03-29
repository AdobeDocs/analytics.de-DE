---
title: tl
description: Senden Sie einen Linktracking-Aufruf an Adobe.
feature: Variables
exl-id: 470662b2-ce07-4432-b2d5-a670fbb77771
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 76%

---

# tl

Die `tl()`-Methode ist eine wichtige Kernkomponente von Adobe Analytics. Sie nimmt alle auf der Seite definierten Analytics-Variablen, kompiliert sie in eine Bildanforderung und sendet diese Daten an die Adobe-Datenerfassungs-Server. Sie funktioniert ähnlich wie die [`t()`](t-method.md)-Methode, allerdings inkrementiert diese Methode keine Seitenansichten. Sie ist nützlich, um Links und andere Elemente zu verfolgen, die nicht als vollständige Seitenladung betrachtet werden.

Wenn [`trackDownloadLinks`](../config-vars/trackdownloadlinks.md) oder [`trackExternalLinks`](../config-vars/trackexternallinks.md) aktiviert ist, ruft AppMeasurement automatisch die `tl()`-Methode auf, um Download- und Exitlinktracking-Daten zu senden. Wenn Ihr Unternehmen mehr Kontrolle über die zu verfolgenden Links und deren Verhalten haben möchte, können Sie die `tl()`-Methode manuell aufrufen. Benutzerspezifische Links können nur manuell verfolgt werden.

## Linktracking mit dem Web SDK

Das Web SDK unterscheidet nicht zwischen Seitenansichtsaufrufen und Linktracking-Aufrufen. Beide verwenden die Variable `sendEvent` Befehl.

Wenn Sie ein XDM-Objekt verwenden und möchten, dass Adobe Analytics ein bestimmtes Ereignis als Linktracking-Aufruf zählt, stellen Sie sicher, dass Ihre XDM-Daten Folgendes enthalten:

* Linkname: zugeordnet zu `xdm.web.webInteraction.name`.
* Link-URL: zugeordnet `xdm.web.webInteraction.URL`.
* Link-Typ: zugeordnet zu `xdm.web.webInteraction.type`. Gültige Werte sind `other` (benutzerspezifische Links), `download` (Downloadlinks) und `exit` (Exitlinks).

```js
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webInteraction": {
        "name": "My Custom Link",
        "URL": "https://example.com",
        "type": "other"
      }
    }
  }
});
```

Wenn Sie ein Datenobjekt verwenden und möchten, dass Adobe Analytics ein bestimmtes Ereignis als Linktracking-Aufruf zählt, stellen Sie sicher, dass Ihr Datenobjekt Folgendes enthält:

* Linkname: zugeordnet zu `data.__adobe.analytics.linkName`.
* Link-URL: zugeordnet `data.__adobe.analytics.linkURL`.
* Link-Typ: zugeordnet zu `data.__adobe.analytics.linkType`. Gültige Werte sind `o` (benutzerspezifische Links), `d` (Downloadlinks) und `e` (Exitlinks).

```js
alloy("sendEvent", {
  "data": {
    "__adobe": {
      "analytics": {
        "linkName": "My custom link",
        "linkURL": "https://example.com",
        "linkType": "o"
      }
    }
  }
});
```

## Linktracking mit der Adobe Analytics-Erweiterung

Die Adobe Analytics-Erweiterung verfügt über einen speziellen Speicherort, um einen Linktracking-Aufruf festzulegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
1. under [!UICONTROL Aktionen], klicken Sie auf die gewünschte Aktion oder klicken Sie auf die **&#39;+&#39;** -Symbol, um eine Aktion hinzuzufügen.
1. Legen Sie die [!UICONTROL Erweiterung] Dropdown-Liste zu **[!UICONTROL Adobe Analytics]** und die [!UICONTROL Aktionstyp] nach **[!UICONTROL Beacon senden]**.
1. Klicken Sie auf die Optionsschaltfläche `s.tl()`.

Sie können keine optionalen Argumente in der Analytics-Erweiterung festlegen.

## s.tl()-Methode in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.tl()`-Methode auf, wenn Sie einen Tracking-Aufruf an Adobe senden möchten.

```js
s.tl([Link object],[Link type],[Link name],[Override variable]);
```

### Link-Objekt (erforderlich)

Das Link-Objekt-Argument bestimmt, ob der Browser bis zu 500 ms wartet, bevor er von der Seite weg navigiert. Wenn eine Bildanforderung früher als 500 ms gesendet wird, navigiert die Seite sofort zum geklickten Link.

>[!NOTE]
>
>AppMeasurement aktiviert automatisch die [`useBeacon`](../config-vars/usebeacon.md)-Variable für Exitlinks, sodass dieses Argument in modernen Browsern nicht mehr benötigt wird. Dieses Argument wurde in früheren Versionen von AppMeasurement häufiger verwendet.

* `this`: Warten Sie bis zu 500 ms, damit AppMeasurement Zeit zum Senden einer Bildanforderung hat. Standardwert.
* `true`: Nicht warten.

```JavaScript
// Include a 500ms delay with an exit link
s.tl(this,"e","Example exit link");

// Do not include a 500ms delay with an exit link
s.tl(true,"e","Example exit link");
```

### Link-Typ (erforderlich)

Das Link-Typ-Argument ist eine aus einem einzigen Buchstaben bestehende Zeichenfolge, die den Typ des Linktracking-Aufrufs bestimmt. Es gibt drei gültige Werte.

* `o`: Der Link ist ein [benutzerspezifischer Link](/help/components/dimensions/custom-link.md).
* `d`: Der Link ist ein [Downloadlink](/help/components/dimensions/download-link.md).
* `e`: Der Link ist ein [Exitlink](/help/components/dimensions/exit-link.md).

```js
// Send a custom link
s.tl(true,"o","Example custom link");

// Send a download link
s.tl(true,"d","Example download link");

// Send an exit link
s.tl(true,"e","Example exit link");
```

### Link-Name (empfohlen)

Das Link-Name-Argument ist eine Zeichenfolge, die das Linktracking-Dimensionselement bestimmt. Bei Verwendung der Dimensionen [Benutzerspezifischer Link](/help/components/dimensions/custom-link.md), [Downloadlink](/help/components/dimensions/download-link.md) oder [Exitlink](/help/components/dimensions/exit-link.md) beim Reporting enthält diese Zeichenfolge das Dimensionselement. Wird dieses Argument nicht festgelegt, dann wird die Variable [linkURL](../config-vars/linkurl.md) verwendet.

```js
// When using the Download link dimension, this method call increases the occurrences metric for "Sea turtle PDF report" by 1.
s.tl(true,"d","Sea turtle PDF report");
```

### Variablenüberschreibungen (optional)

Ermöglicht die Änderung von Variablenwerten für einen einzelnen Aufruf. Weitere Informationen finden Sie unter [Variablenüberschreibungen](../../js/overrides.md).

```js
var y = new Object();
y.eVar1 = "Override value";
y.linkTrackVars = "eVar1";
s.tl(true,"o","Example custom link",y);
```

## Beispiele und Anwendungsfälle

Senden Sie einen einfachen Linktracking-Aufruf direkt innerhalb eines HTML-Links:

```HTML
<a href="example.html" onClick="s.tl(true,'o','Example link');">Click here</a>
```

Verwenden Sie JavaScript, um einen einfachen Linktracking-Aufruf mithilfe von Methodenargumenten durchzuführen:

```JavaScript
s.tl(true,"o","Example link");
```

### Linktracking-Aufrufe innerhalb einer benutzerdefinierten Funktion

Sie können den Linktracking-Code in einer eigenständige JavaScript-Funktion zusammenfassen, die auf der Seite oder in einer verknüpften JavaScript-Datei definiert ist. Aufrufe können dann in der onClick-Funktion jedes Links erfolgen. Legen Sie Folgendes in einer JavaScript-Datei fest:

```JavaScript
function trackClickInteraction(name){
  s.linkTrackVars = "eVar1,eVar2";
  s.eVar1 = name;
  s.eVar2 = s.pageName;
  s.tl(true,"o",name);
}
```

Sie können die Funktion dann immer dann aufrufen, wenn Sie einen bestimmten Link verfolgen möchten:

```HTML
<!-- Use wherever you want to track links -->
<a href="example.html" onClick="trackClickInteraction('Example link');">Click here</a>
```

### Vermeiden des Trackings doppelter Links

Wenn `trackDownloadLinks` oder `trackExternalLinks` aktiviert ist, führt AppMeasurement automatisch einen Linktracking-Aufruf durch, wenn die richtigen Filter übereinstimmen. Wenn Sie `s.tl()` auch manuell für diese Link-Klicks aufrufen, können Sie doppelte Daten an Adobe senden. Doppelte Daten überhöhen die Berichtsnummern auf und machen sie weniger genau.

Beispielsweise sendet die folgende Funktion zwei Linktracking-Aufrufe für denselben Link-Klick (manuelle und automatische Downloadlinks):

```JavaScript
function trackDownload(obj) {
  s.tl(obj,"d","Example PDF download");
}
```

Mithilfe der folgenden geänderten Funktion können Sie doppelte Linktracking-Aufrufe vermeiden. Sie prüft zunächst, ob ein Link-Objekt existiert, und sendet nur dann einen manuellen Linktracking-Aufruf, wenn das Link-Objekt eine leere Zeichenfolge ist.

```JavaScript
function linkCode(obj) {
  var lt = obj.href != null ? s.lt(obj.href) : "";
  if (lt=="") {
    s.tl(obj,"d","Example PDF download");
  }
}
```
