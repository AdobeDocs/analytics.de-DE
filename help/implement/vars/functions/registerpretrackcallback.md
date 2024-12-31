---
title: registerPreTrackCallback
description: Erstellen Sie Callback-Funktionen, bevor Sie einen Treffer an Adobe senden.
feature: Variables
exl-id: 11c960d7-ded4-441a-822f-463d3a137d2d
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 55%

---

# registerPreTrackCallback

Mit der `registerPreTrackCallback`-Variablen kann Ihr Unternehmen eine JavaScript-Funktion verbinden, nachdem eine Bildanforderungs-URL kompiliert wurde, aber bevor sie gesendet wird. Mit dieser Variablen können Sie von AppMeasurement erfasste Daten an eine Partner- oder interne Infrastruktur senden.

>[!WARNING]
>
>Führen Sie keine Tracking-Aufrufe wie [`t()`](t-method.md) oder [`tl()`](tl-method.md) innerhalb der `registerPreTrackCallback`-Variablen durch. Das Festlegen von Tracking-Aufrufen in dieser Variablen verursacht eine unendliche Schleife von Bildanforderungen!

Jedes Mal, wenn Sie die `registerPreTrackCallback`-Variable aufrufen, binden Sie diese Funktion jedes Mal ein, um sie bei jeder Kompilierung der URL einer Bildanforderung auszuführen. Vermeiden Sie es, dieselbe Funktion mehrmals mit demselben Seitenladevorgang zu registrieren.

>[!NOTE]
>
>Der Zeitpunkt und die Reihenfolge der Funktionen, die zwischen `registerPreTrackCallback` und `registerPostTrackCallback` ausgelöst werden, sind nicht gewährleistet. Vermeiden Sie Abhängigkeiten zwischen diesen beiden Funktionen.

## Rückruf vorab mit der Web SDK-Erweiterung verfolgen

Web SDK kann keine Funktion einbinden, nachdem Daten kompiliert wurden, aber bevor sie an Adobe gesendet werden. Sie können jedoch `onBeforeEventSend` verwenden, um eine Funktion zu registrieren, die unmittelbar vor dem Senden von Daten ausgeführt wird.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei ](https://experience.adobe.com/data-collection) Datenerfassungs-Benutzeroberfläche von Adobe Experience Platform an.[
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter {4 **[!UICONTROL Adobe Experience Platform Web SDK]** auf die Schaltfläche Konfigurieren].[!UICONTROL 
1. Klicken [!UICONTROL  unter „Datenerfassung] auf die Schaltfläche **[!UICONTROL Bearbeiten vor dem Rückruf-Code senden]**.
1. Platzieren Sie den gewünschten Code im Editor.

## Vorab-Tracking des Callbacks bei manueller Implementierung der Web-SDK

Web SDK kann keine Funktion einbinden, nachdem Daten kompiliert wurden, aber bevor sie an Adobe gesendet werden. Sie können jedoch `onBeforeEventSend` verwenden, um eine Funktion zu registrieren, die kurz vor dem Senden von Daten ausgeführt wird, ähnlich wie `doPlugins`. Weitere Informationen [ Sie in der ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) zu Web SDK unter „Globales Ändern von Ereignissen“.

```js
// Set the trackingCode XDM field to "New value"
alloy("configure", {
  "onBeforeEventSend": function(content) {
    content.xdm.marketing.trackingCode = "New value";
  }
})
```

## Rückruf vorab mit der Adobe Analytics-Erweiterung verfolgen

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.registerPreTrackCallback in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Funktion `s.registerPreTrackCallback` akzeptiert als einziges Argument eine Funktion. Die verschachtelte Funktion wird direkt vor dem Senden einer Bildanforderung ausgeführt.

```js
s.registerPreTrackCallback(function(){/* Desired code */});
```

Wenn Sie die Bildanforderungs-URL im Code verwenden möchten, verweisen Sie auf das `requestUrl`-Zeichenfolgenargument in der verschachtelten Funktion. Sie können die `requestUrl`-Variable für Ihre gewünschte Verwendung parsen. Die Anpassung dieser Variable hat keine Auswirkungen auf die Datenerfassung.

```js
s.registerPreTrackCallback(function(requestUrl){
  console.log(requestUrl); // Outputs the full image request URL
});
```

Sie können zusätzliche Argumente in die Funktion `s.registerPreTrackCallback` einfügen, die in der verschachtelten Funktion verwendet werden kann:

```js
s.registerPreTrackCallback(function(requestUrl,a,b,c) {
    console.log(requestUrl); // Full image request URL
    console.log(a); // param1
    console.log(b); // param2
    console.log(c); // param3
}, "param1", "param2", "param3");
```

>[!NOTE]
>
>Das Festlegen von Seitenvariablen oder das Ändern der `requestUrl`-Zeichenfolge in dieser Funktion hat **keine** Auswirkungen auf die Bildanforderung, die kurz nach diesem Funktionsaufruf gesendet wird. Verwenden Sie stattdessen die Variable [`doPlugins()`](doplugins.md).
