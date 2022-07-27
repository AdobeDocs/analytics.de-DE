---
title: rfl
description: Entfernen Sie einen bestimmten Wert aus einer durch Zeichen getrennten Zeichenfolge.
feature: Variables
exl-id: d66b757e-b39f-4b6e-9999-6fbde87505af
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe-Plug-in: rfl („Remove From List“ (Aus Liste entfernen))

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `rfl`-Plug-in können Sie Werte aus getrennten Zeichenfolgen wie [`events`](../page-vars/events/events-overview.md), [`products`](../page-vars/products.md), [`list`](../page-vars/list.md) und anderen „sicher“ entfernen. Dieses Plug-in ist nützlich, wenn Sie bestimmte Werte aus einer mit Trennzeichen versehenen Zeichenfolge entfernen möchten, ohne sich Gedanken über Trennzeichen machen zu müssen. Mehrere andere Plug-ins sind auf diesen Code angewiesen, um korrekt zu funktionieren. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht gleichzeitig eine bestimmte Funktion für mehrere Analytics-Variablen ausführen müssen oder wenn Sie keine abhängigen Plug-ins verwenden.

Das Plug-in verwendet folgende Logik:

* Wenn der zu entfernende Wert existiert, behält das Plug-in alles in der Variablen, außer dem zu entfernenden Wert.
* Wenn der zu entfernende Wert nicht existiert, behält das Plug-in die ursprüngliche Zeichenfolge unverändert bei.

<!--## Install the plug-in using the Web SDK or the Adobe Analytics extension

Adobe offers an extension that allows you to use most commonly-used plug-ins.

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/data-collection) using your AdobeID credentials.
1. Click the desired tag property.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. If you haven't already, create a rule labeled "Initialize Plug-ins" with the following configuration:
    * Condition: None
    * Event: Core – Library Loaded (Page Top)
1. Add an action to the above rule with the following configuration:
    * Extension: Common Analytics Plugins
    * Action Type: Initialize RFP (Remove From List)
1. Save and publish the changes to the rule.-->

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: rfl (removeFromList) v2.1  */
function rfl(lv,vr,d1,d2,df){var b=lv,f=vr,e=d1,h=d2,g=df;if("-v"===b)return{plugin:"rfl",version:"2.1"};a:{if("undefined"!==typeof window.s_c_il){var c=0;for(var a;c<window.s_c_il.length;c++)if(a=window.s_c_il[c],a._c&&"s_c"===a._c){c=a;break a}}c=void 0}"undefined"!==typeof c&&(c.contextData.rfl="2.1");if(!b||!f)return"";c=[];a="";e=e||",";h=h||e;g=g||!1;b=b.split(e);e=b.length;for(var d=0;d<e;d++)-1<b[d].indexOf(":")&&(a=b[d].split(":"),a[1]=a[0]+":"+a[1],b[d]=a[0]),-1<b[d].indexOf("=")&&(a=b[d].split("="),a[1]=a[0]+"="+a[1],b[d]=a[0]),b[d]!==f&&a?c.push(a[1]):b[d]!==f?c.push(b[d]):b[d]===f&&g&&(a?c.push(a[1]):c.push(b[d]),g=!1),a="";return c.join(h)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `rfl`-Funktion verwendet die folgenden Argumente:

* **`lv`** (erforderlich, Zeichenfolge): Eine Variable (oder Zeichenfolge), die eine Liste mit getrennten Werten enthält.
* **`vr`** (erforderlich, Zeichenfolge): Der Wert, der aus dem `lv`-Argument entfernt werden soll. Adobe empfiehlt, während eines einzelnen `rfl`-Aufrufs nicht mehrere Werte zu entfernen.
* **`d1`** (optional, Zeichenfolge): Das Trennzeichen, das vom `lv`-Argument verwendet wird. Der Standardwert ist ein Komma (`,`).
* **`d2`** (optional, Zeichenfolge): Das Trennzeichen, das die Rückgabezeichenfolge verwenden soll. Die Standardeinstellung ist derselbe Wert wie das `d1`-Argument.
* **`df`** (optional, boolesch): Wenn auf `true` gesetzt, werden anstelle aller Instanzen nur doppelte Instanzen des `vr`-Arguments vom `lv`-Argument entfernt. Die Standardeinstellung ist `false`, wenn nicht festgelegt.

Der Aufruf dieser Methode gibt eine geänderte Zeichenfolge zurück, die das `lv`-Argument enthält, jedoch keine Instanzen (oder doppelten Instanzen) des im `vr`-Argument angegebenen Werts.

## Beispielaufrufe

### Beispiel 1

Wenn ...

```js
s.events = "event22,event24,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"event24");
```

... lautet der Endwert von s.events:

```js
s.events = "event22,event25";
```

### Beispiel 2

Wenn ...

```js
s.events = "event22,event24,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"event26");
```

... lautet der Endwert von s.events:

```js
s.events = "event22,event24,event25";
```

In diesem Beispiel hat der rfl-Aufruf keine Änderungen an s.events vorgenommen, da s.events „event26“ nicht enthielt.

### Beispiel 3

Wenn ...

```js
s.events = "event22,event24,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events);
```

... lautet der Endwert von s.events:

```js
s.events = "";
```

Wenn entweder das `lv`-Argument oder das `vr`-Argument leer ist (bei einem `rfl` Aufruf), dann liefert das Plug-in nichts zurück.

### Beispiel 4

Wenn ...

```js
s.prop4 = "hello|people|today";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.eVar5 = rfl(s.prop4,"people","|");
```

 ... lautet der Endwert von s.prop4 weiterhin ...

```js
s.prop4 = "hello|people|today";
```

... aber der Endwert von s.eVar5 lautet:

```js
s.eVar5 = "hello|today";
```

Beachten Sie, dass das Plug-in nur einen Wert zurückgibt; es setzt die durch das `lv`-Argument übergebene Variable nicht wirklich zurück.

### Beispiel 5

Wenn ...

```js
s.prop4 = "hello|people|today";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.prop4 = rfl(s.prop4,"people");
```

 ... lautet der Endwert von s.prop4 weiterhin ...

```js
s.prop4 = "hello|people|today";
```

Setzen Sie immer dann, wenn der `lv`-Argumentwert ein anderes Trennzeichen als den Standardwert (z. B. ein Komma) enthält, das `d1`-Argument.

### Beispiel 6

Wenn ...

```js
s.events = "event22,event23,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"EVenT23");
```

... lautet der Endwert von s.events:

```js
s.events = "event22,event23,event25";
```

Obwohl dieses Beispiel nicht praktikabel ist, zeigt es die Notwendigkeit, die Groß- und Kleinschreibung zu berücksichtigen.

### Beispiel 7

Wenn ...

```js
s.events = "event22,event23:12345,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"event23");
```

... lautet der Endwert von s.events:

```js
s.events = "event22,event25";
```

### Beispiel 8

Wenn ...

```js
s.events = "event22,event23:12345,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"event23:12345");
```

... lautet der Endwert von s.events:

```js
s.events = "event22,event23:12345,event25";
```

Wenn Sie ein Ereignis entfernen müssen, das eine Serialisierung und/oder numerische oder Währungs-Syntax verwendet, sollten Sie im `rfl`-Aufruf nur das Ereignis selbst angeben (d. h. ohne die nummerischen oder Währungswerte bzw. Serialisierung).

### Beispiel 9

Wenn ...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"event23");
```

... lautet der Endwert von s.events:

```js
s.events = "event22,event24,event25");
```

### Beispiel 10

Wenn ...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"event23", "", "",true);
```

... lautet der Endwert von s.events:

```js
s.events = "event22,event23,event24,event25");
```

### Beispiel 11

Wenn ...

```js
s.events = "event22,event23,event23,event23,event24,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"event23", "", "|",true);
```

... lautet der Endwert von s.events:

```js
s.events = "event22|event23|event24|event25");
```

### Beispiel 12

Wenn ...

```js
s.events = "event22,event23,event24,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"event23,event24");
```

... lautet der Endwert von s.events:

```js
s.events = "event22,event23,event24,event25";
```

Das Festlegen mehrerer Werte im `vr`-Argument wird nicht unterstützt. Die `rfl`-Logik im obigen Beispiel würde zunächst die Werte im `lv`-Argument (d. h. s.events) aufspalten und dann versuchen, jeden abgegrenzten Wert mit dem vollständigen `vr`-Argumentwert (d. h. `"event23,event24"`) abzugleichen.

### Beispiel 13

Wenn ...

```js
s.events = "event22,event23,event24,event25";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.events = rfl(s.events,"event23");
s.events = rfl(s.events,"event24");
```

... lautet der Endwert von s.events:

```js
s.events = "event22,event25");
```

Jeder aus der Liste zu entfernende Wert sollte in seinem eigenen `rfl`-Aufruf enthalten sein.

### Beispiel 14

Wenn ...

```js
s.linkTrackVars = "events,eVar1,eVar2,eVar3";
```

 ... und der folgende Code ausgeführt wird ...

```js
s.linkTrackVars = rfl(s.linkTrackVars,"eVar2", ",", ",", false);
```

...lautet der Endwert von s.linkTrackVars:

```js
s.linkTrackVars = "events,eVar1,eVar3";
```

Die letzten drei Argumente (d. h. &quot;,&quot;,&quot;,&quot;,false) am Ende dieses `rfl`-Aufrufs sind nicht erforderlich, sind aber auch nicht hinderlich, da sie mit den Standardeinstellungen übereinstimmen.

### Beispiel 15

Wenn ...

```js
s.events = "event22,event23,event24";
```

 ... und der folgende Code ausgeführt wird ...

```js
rfl(s.events,"event23");
```

...lautet der Endwert von s.events weiterhin:

```js
s.events = "event22,event23,event24";
```

Beachten Sie auch hier, dass das Plug-in nur einen Wert zurückgibt; es setzt die durch das `lv`-Argument übergebene Variable nicht wirklich zurück.

## Versionsverlauf

### 2.1 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 2.01 (17. September 2019)

* Geringfügige Fehlerbehebung für den Standardwert des Trennzeichens.

### 2.0 (16. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe).
* Die Notwendigkeit für das `join`-Plug-in wurde entfernt.

### 1.0 (18. Juli 2016)

* Erste Version.
