---
title: registerPostTrackCallback
description: Erstellen Sie Callback-Funktionen, nachdem Sie einen Treffer an Adobe gesendet haben.
feature: Appmeasurement Implementation
exl-id: b2124b89-2bab-4cca-878c-18d62377a8f3
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 73%

---

# registerPostTrackCallback

Die `registerPostTrackCallback`-Variable ermöglicht es Ihrer Organisation, eine JavaScript-Funktion unmittelbar nach der erfolgreichen Übermittlung eines Treffers an Adobe zu aktivieren. Wenn ein Tracking-Aufruf fehlschlägt, wird diese Funktion nicht ausgeführt. Mit dieser Variablen können Sie von AppMeasurement erfasste Daten an eine Partner- oder interne Infrastruktur senden oder Variablenwerte in Einzelseitenanwendungen bereinigen.

>[!WARNING]
>
>Führen Sie keine Tracking-Aufrufe wie [`t()`](t-method.md) oder [`tl()`](tl-method.md) innerhalb der `registerPostTrackCallback`-Variablen durch. Das Festlegen von Tracking-Aufrufen in dieser Variablen verursacht eine unendliche Schleife von Bildanforderungen!

Jedes Mal, wenn Sie die `registerPostTrackCallback`-Variable aufrufen, binden Sie diese Funktion so ein, dass sie unmittelbar nach dem erfolgreichen Senden einer Bildanforderung ausgeführt wird. Vermeiden Sie es, dieselbe Funktion mehrmals mit demselben Seitenladevorgang zu registrieren.

>[!NOTE]
>
>Der Zeitpunkt und die Reihenfolge der Funktionen, die zwischen [`registerPreTrackCallback`](registerpretrackcallback.md) und `registerPostTrackCallback` ausgelöst werden, sind nicht gewährleistet. Vermeiden Sie Abhängigkeiten zwischen diesen beiden Funktionen.

## Nachverfolgen von Callback mit der Web SDK-Erweiterung

Bald verfügbar!

## Nach dem Tracking erfolgt ein Callback, bei dem die Web-SDK manuell implementiert wird

Sie können ein JavaScript Promise verwenden, wenn Sie ein Ereignis senden, um eine Funktion zu registrieren, nachdem Daten erfolgreich an Adobe gesendet wurden.

```js
alloy("sendEvent",{
  "xdm": {}
}).then(function(result) {
  Console.Log("Data was successfully sent.");
});
```

Weitere Informationen [ Sie in der Dokumentation zu Web](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=de#handling-responses-from-events)SDK unter „Umgang mit Antworten von Ereignissen“.

## Registrieren von Callback nach Tracking mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.registerPostTrackCallback in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Funktion `s.registerPostTrackCallback` akzeptiert als einziges Argument eine Funktion. Die verschachtelte Funktion wird direkt nach dem erfolgreichen Senden einer Bildanforderung ausgeführt.

```js
s.registerPostTrackCallback(function(){/* Desired code */});
```

Wenn Sie die Bildanforderungs-URL im Code verwenden möchten, verweisen Sie auf das `requestUrl`-Zeichenfolgenargument in der verschachtelten Funktion. Sie können die `requestUrl`-Variable für Ihre gewünschte Verwendung parsen. Die Anpassung dieser Variable hat keine Auswirkungen auf die Datenerfassung.

```js
s.registerPostTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

Zusätzliche Argumente können in die `s.registerPostTrackCallback`-Funktion aufgenommen werden, die in der verschachtelten Funktion verwendet werden kann:

```js
s.registerPostTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

## Anwendungsfall

Die Registrierung der [`clearVars()`](clearvars.md)-Funktion im Callback nach Tracking kann für Einzelseitenanwendungen von Vorteil sein. Jedes Mal, wenn Sie einen Treffer erfolgreich an Adobe senden, wird die `clearVars()`-Funktion ausgeführt. Ihre Implementierung kann dann Variablen erneut definieren, ohne sich Gedanken über falsche vorhandene Werte machen zu müssen.

```js
s.registerPostTrackCallback(function(){s.clearVars();});
```
