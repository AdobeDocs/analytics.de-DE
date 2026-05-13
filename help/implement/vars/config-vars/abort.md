---
title: abort
description: Die Variable „abort“ ist ein boolescher Wert, der verhindert, dass ein Treffer an die Adobe-Datenerfassungs-Server gesendet wird.
feature: Appmeasurement Implementation
exl-id: e4e25a89-272b-4444-b52b-c7fe2478ff30
role: Admin, Developer
TQID: https://experienceleague.adobe.com/xVOUnGUxNcQqBGAoDxefFBT1Yg2mKzpXLPSVFqOcJSM
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 343
ht-degree: 39%

---

# abort

Die Variable `abort` ist ein boolescher Wert, der verhindern kann, dass der nächste Tracking-Aufruf an Adobe gesendet wird. Ähnliche Funktionen sind in der Web-SDK verfügbar, mit denen Sie `false` zurückgeben können, bevor ein XDM-Ereignis gesendet wird.

## Senden eines Ereignisses mit der Web SDK-Erweiterung abbrechen

Verwenden Sie das [!UICONTROL Ein-Ereignis vor dem Rückruf] Code-Editor und geben Sie `false` zurück.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter {4 **[!UICONTROL Adobe Experience Platform Web SDK]** auf die Schaltfläche Konfigurieren].[!UICONTROL 
1. Klicken [!UICONTROL  unter „Datenerfassung] auf die Schaltfläche **[!UICONTROL Bearbeiten vor dem Rückruf-Code senden]**.
1. Fügen Sie im Code-Editor den folgenden Code unter einer beliebigen Bedingung ein, unter der Sie das Senden von Daten an Edge abbrechen möchten:

```js
return false;
```

## Manuelles Senden eines Ereignisses abbrechen, indem die Web-SDK implementiert wird

Verwenden Sie den `onBeforeEventSend` Callback und geben Sie `false` zurück. Weitere Informationen [ Sie in der ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#modifying-events-globally) zu Web SDK unter „Globales Ändern von Ereignissen“.

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

Die `abort` kann in der [`doPlugins()`](../functions/doplugins.md) festgelegt werden, die als letzte Funktion ausgeführt wird, bevor eine Bildanforderung an Adobe gesendet wird. Dieses Beispiel funktioniert ähnlich wie der `onBeforeEventSend` Callback unter Verwendung der Web-SDK.

```js
s.doPlugins = function(s) {
    s.campaign = s.Util.getQueryParam("cid");
    if ((!s.campaign) && (!s.events)) {
        s.abort = true;
    }
};
```

Damit können Sie die Logik zentralisieren, mit der Sie Aktivitäten ermitteln, die Sie nicht nachverfolgen möchten, z. B. einige benutzerspezifische Links oder externe Links in Display-Anzeigen.
