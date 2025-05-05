---
title: abort
description: Die Variable „abort“ ist ein boolescher Wert, der verhindert, dass ein Treffer an die Adobe-Datenerfassungs-Server gesendet wird.
feature: Variables
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
role: Admin, Developer
source-git-commit: 5ef8ba686a13f8b4ab592c0b48a9c074b0477fcf
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 39%

---

# abort

Die Variable `abort` ist ein boolescher Wert, der verhindern kann, dass der nächste Tracking-Aufruf an Adobe gesendet wird. Ähnliche Funktionen sind in der Web-SDK verfügbar, mit denen Sie `false` zurückgeben können, bevor ein XDM-Ereignis gesendet wird.

## Senden eines Ereignisses mit der Web SDK-Erweiterung abbrechen

Verwenden Sie das [!UICONTROL Ein-Ereignis vor dem Rückruf] Code-Editor und geben Sie `false` zurück.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter &lbrace;4 **[!UICONTROL Adobe Experience Platform Web SDK]** auf die Schaltfläche Konfigurieren.
1. Klicken [!UICONTROL &#x200B; unter „Datenerfassung] auf die Schaltfläche **[!UICONTROL Bearbeiten vor dem Rückruf-Code senden]**.
1. Fügen Sie im Code-Editor den folgenden Code unter einer beliebigen Bedingung ein, unter der Sie das Senden von Daten an Edge abbrechen möchten:

```js
return false;
```

## Manuelles Senden eines Ereignisses abbrechen, indem die Web-SDK implementiert wird

Verwenden Sie den `onBeforeEventSend` Callback und geben Sie `false` zurück. Weitere Informationen [ Sie in der ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=de#modifying-events-globally) zu Web SDK unter „Globales Ändern von Ereignissen“.

```js
alloy("configure"), {
    "onBeforeEventSend": function(content) {
        return false;
    }
}
```

## Verwenden der abort-Variablen in der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.abort in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.abort`-Variable ist ein boolescher Wert. Der Standardwert lautet `false`.

* Wenn auf `true` gesetzt, sendet der nächste Tracking-Aufruf ([`t()`](../functions/t-method.md) oder [`tl()`](../functions/tl-method.md)) keine Daten an Adobe.
* Wenn diese Variable auf `false` gesetzt oder nicht definiert ist, hat sie keine Auswirkung.

```js
s.abort = true;
```

>[!NOTE]
>
>Die `abort`-Variable wird nach jedem Tracking-Aufruf auf `false` zurückgesetzt. Wenn Sie nachfolgende Tracking-Aufrufe auf derselben Seite abbrechen möchten, setzen Sie `abort` erneut auf `true`.

Die `abort` kann in der [`doPlugins()`](../functions/doplugins.md) festgelegt werden. Dies ist die letzte Funktion, die ausgeführt wird, bevor eine Bildanforderung an den Adobe gesendet wird. Dieses Beispiel funktioniert ähnlich wie der `onBeforeEventSend` Callback unter Verwendung der Web-SDK.

```js
s.doPlugins = function(s) {
    s.campaign = s.Util.getQueryParam("cid");
    if ((!s.campaign) && (!s.events)) {
        s.abort = true;
    }
};
```

Damit können Sie die Logik zentralisieren, mit der Sie Aktivitäten ermitteln, die Sie nicht nachverfolgen möchten, z. B. einige benutzerspezifische Links oder externe Links in Display-Anzeigen.
