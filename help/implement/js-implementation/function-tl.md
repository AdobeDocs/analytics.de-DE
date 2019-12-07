---
description: Dateidownloads und Exitlinks können automatisch anhand von Parametern verfolgt werden, die in der AppMeasurement für JavaScript-Datei festgelegt sind.
keywords: Analytics Implementation
subtopic: Link tracking
title: Die s.tl()-Funktion – Linktracking
topic: Developer and implementation
uuid: f28f071a-8820-4f74-89cd-fd2333a21f22
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Die s.tl()-Funktion – Linktracking

Wenn Ihr Unternehmen mehr Kontrolle über die zu verfolgenden Links und deren Verhalten hat, wird ein manuelles Linktracking empfohlen. Verwenden Sie die Funktion „s.tl()“, um Bildanforderungen zum Linktracking mit dem exakten Inhalt manuell zu senden. Wenn nur grundlegendes Linktracking erforderlich ist, lesen Sie `s.trackDownloadLinks` und `s.trackExternalLinks` unter [Konfigurationsvariablen](c-variables/configuration-variables.md). Benutzerspezifische Links können nicht automatisch verfolgt werden.

> [!NOTE] Linktracking-Code ist häufig sehr spezifisch für Ihre Site und Ihre Berichterstattungsanforderungen. Adobe empfiehlt, dass Sie über Erfahrungen bei der vorherigen Implementierung verfügen oder einen Implementierungsberater haben, um zu verstehen, wie Sie diese Funktion je nach Ihren geschäftlichen Anforderungen verwenden.

## Syntax und Beispiele

Grundlegende Syntax:

`s.tl(`**`this`**`,`**`linkType`**`,`**`linkName`**`,`**`variableOverrides`**`,`**`doneAction`**`);`

Grundlegende Beispiele:

```HTML
<!-- Basic HTML link example-->
<a href="example.html" onClick="s.tl(this,'o','Example link');">Click here</a>
```

```JavaScript
// Basic JavaScript link example
s.tl(this,'o','Example Link');
```

### this/true (erforderlich)

Das erste Argument bestimmt, ob der Browser bis zu 500 ms wartet, bevor er von der Seite weg navigiert. Wenn eine Bildanforderung früher als 500 ms gesendet wird, navigiert die Seite sofort zum angeklickten Link.

* `this`: Warten Sie bis zu 500 ms, damit AppMeasurement Zeit zum Senden einer Bildanforderung hat. Standardwert.
* `true`: Nicht warten. Wenn der Link von der Seite weg navigiert, wird möglicherweise keine Bildanforderung gesendet.

Die Verzögerung ist nur erforderlich, wenn ein Link die Seite verlässt.

```JavaScript
// Include 500ms delay
s.tl(this,'o','Example link');

// Do not include 500ms delay
s.tl(true,'o','Example link');
```

### linkType (erforderlich)

Das zweite Argument hat drei gültige Werte, abhängig von der Art des Links, den Sie erfassen möchten. Es bestimmt, welche Dimension in Adobe Analytics die Bildanforderung füllt.

* `d`: Dateiladungen
* `e`: Exitlinks
* `o`: Benutzerspezifische Links

```JavaScript
// Populates the File Downloads dimension
s.tl(this,'d','Example link');

// Populates the Exit Links dimension
s.tl(this,'e','Example link');

// Populates the Custom Links dimension
s.tl(this,'o','Example link');
```

### linkName (erforderlich)

Dieses Argument kann ein beliebiger benutzerdefinierter Wert von bis zu 100 Byte sein. Es bestimmt den Dimensionswert in der Berichterstellung.

```JavaScript
// Populates the Custom Link dimension with "Referral click to example.com"
s.tl(this,'o','Referral click to example.com');

// Populates the Download link dimension with "Last quarter performance PDF"
s.tl(this,'d','Last quarter performance PDF');
```

### variableOverrides (optional)

Ermöglicht die Änderung von Variablenwerten für einen einzelnen Aufruf. Wenn Sie das doneAction-Argument verwenden und keine Variablenüberschreibungen haben, verwenden Sie `null`.

### doneAction (optional)

Gibt eine Navigationsaktion an, die nach Abschluss des Nachverfolgungslink-Aufrufs ausgeführt wird. Erfordert die Verwendung von `s.useForcedLinkTracking` und `s.forcedLinkTrackingTimeout`. Die Variable doneAction kann die Zeichenfolge `navigate` sein, wodurch die Methode den `document.location` auf das „href“-Attribut von `linkObject` festlegt. Die Variable doneAction kann auch eine Funktion sein, die eine erweiterte Anpassung ermöglicht.

Wenn Sie für doneAction in einem `onClick``false`-Ankerereignis einen Wert angeben, müssen Sie nach dem `s.tl`-Aufruf „“ zurückgeben, um die standardmäßige Browsernavigation zu verhindern.
Um das Standardverhalten zu imitieren und der vom href-Attribut angegebenen URL zu folgen, müssen Sie als doneAction eine `navigate`-Zeichenfolge angeben. Optional können Sie zur Verarbeitung des Navigationsereignisses auch eine eigene Funktion angeben, die Sie dann als doneAction übergeben.

```JavaScript
s.tl(this,'e','Example link',null,'navigate');return false;
```

## JavaScript-Funktionen beim Linktracking

Sie können den Linktracking-Code in einer eigenständige JavaScript-Funktion zusammenfassen, die auf der Seite oder in einer verknüpften JavaScript-Datei definiert ist. Aufrufe können dann in der onClick-Funktion jedes Links erfolgen.

```JavaScript
// Set in AppMeasurement file or page code
function trackClickInteraction(name){
    s.linkTrackVars='eVar16,eVar17';
    s.eVar16 = name;
    s.eVar17 = s.pageName;
    s.tl(true,'o',name);
}
```

```HTML
<!-- Use wherever you want to track links -->
<a href="example.html" onClick="trackClickInteraction('Example link');">Click here</a>
```

## Vermeiden von doppelten Linkzählungen {#section_9C3F73DE758F4727943439DED110543C}

Es ist möglich, dass Links doppelt gezählt werden, wenn der Link normalerweise durch automatisches Herunterladen von Dateien oder Verlassen des Linktracking erfasst wird. Wenn Sie beispielsweise PDF-Downloads automatisch nachverfolgen, führt ein `s.tl`-Auruf zu einer doppelten Download-Anzahl:

```JavaScript
function trackDownload(obj) {}
    s.tl(obj,'d','PDF Document');
}
```

Um sicherzustellen, dass der Link nicht doppelt gezählt wird, verwenden Sie die folgende geänderte JavaScript-Funktion:

```JavaScript
function linkCode(obj) {
    var lt = obj.href != null ? s.lt(obj.href) : "";
    if (lt=="") {
        s.tl(obj,'d','PDF Document');
    }
}
```
