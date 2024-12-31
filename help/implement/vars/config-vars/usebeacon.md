---
title: useBeacon
description: Mit useBeacon können Sie AppMeasurement zur Verwendung der sendBeacon-API des Browsers zwingen.
feature: Variables
exl-id: a3c4174a-711d-4a35-9f36-9b1049c7db54
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 62%

---

# useBeacon

Die meisten modernen Browser enthalten die native Methode `navigator.sendBeacon()`. Sie sendet asynchron eine kleine Datenmenge über HTTP an einen Webserver. AppMeasurement kann die `navigator.sendBeacon()`-Methode verwenden, wenn die `useBeacon`-Variable aktiviert ist. Sie ist nützlich für Exitlinks und andere Situationen, in denen Sie Informationen vor dem Entladen der Seite senden möchten.

Wenn `useBeacon` aktiviert ist, verwendet der nächste an Adobe gesendete Treffer die `navigator.sendBeacon()`-Methode des Browsers anstelle einer standardmäßigen `GET`-Bildanforderung. Diese Variable gilt für [`s.t()`](../functions/t-method.md)- und [`s.tl()`](../functions/tl-method.md)-Bildanforderungen. Sie erfordert AppMeasurement 2.17.0 oder höher.

>[!TIP]
>
>AppMeasurement aktiviert automatisch `useBeacon` für Exitlink-Bildanforderungen.

Die `useBeacon`-Variable wird ignoriert, wenn der Besucher einen Browser verwendet, der `navigator.sendBeacon()` nicht unterstützt. Für die Verwendung dieser Variablen ist AppMeasurement 2.16.0 oder höher erforderlich.

## Verwenden der sendBeacon-API mit der Web SDK-Erweiterung

Das **[!UICONTROL Dokument wird entladen]** Kontrollkästchen innerhalb einer Aktionskonfiguration bestimmt, ob Daten, die an Adobe gesendet werden, die sendBeacon-API verwenden.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel.
1. Klicken [!UICONTROL  unter ]Aktionen“ auf die gewünschte Aktion oder klicken Sie auf das Symbol **&#39;+&#39;**, um eine neue Aktion hinzuzufügen.
1. Legen Sie die [!UICONTROL Erweiterung] Dropdown-Liste auf **[!UICONTROL Adobe Experience Platform SDK Web]** und den [!UICONTROL Aktionstyp] auf **[!UICONTROL Ereignis senden]**
1. Klicken Sie auf **[!UICONTROL rechten Seite auf das Kontrollkästchen]** Dokument wird entladen“.

Wenn dieses Kontrollkästchen aktiviert ist, werden Daten mithilfe der sendBeacon-API an Adobe gesendet. Es ist standardmäßig deaktiviert.

## Verwenden der sendBeacon-API für die manuelle Implementierung der Web-SDK

Setzen Sie `documentUnloading` beim Senden eines Ereignisses auf `true`. Wenn nicht festgelegt, ist der Standardwert `false`.

```json
alloy("sendEvent", {
  "documentUnloading": true,
  "xdm": {}
});
```

Weitere Informationen finden [ in der Web](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html#using-the-sendbeacon-api)SDK-Dokumentation unter „Verwenden der sendBeacon-API“.

## Verwenden von Beacon mithilfe der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.useBeacon im AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.useBeacon`-Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement die `navigator.sendBeacon()`-Methode des Browsers verwendet. Der Standardwert lautet `false`. Setzen Sie diese Variable vor dem Aufruf einer Tracking-Funktion auf `true`, wenn Sie die asynchrone Natur von `navigator.sendBeacon()` nutzen möchten.

```js
s.useBeacon = true;
```

>[!NOTE]
>
>Nach Ausführung eines Tracking-Aufrufs wird diese Variable auf `false` zurückgesetzt. Wenn Ihre Implementierung mehrere Bildanforderungen mit demselben Seitenladevorgang sendet (z. B. bei Single Page Applications), setzen Sie diese Variable vor jedem Tracking-Aufruf auf `true`.
