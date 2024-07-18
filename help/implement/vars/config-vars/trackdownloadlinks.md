---
title: trackDownloadLinks
description: Aktivieren oder deaktivieren Sie das automatische Linktracking für Downloadlinks.
feature: Variables
exl-id: d92f722b-d605-40ad-bb55-ec71219a47e3
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 59%

---

# trackDownLoadLinks

Adobe bietet die Möglichkeit, Downloadlinks zu verfolgen, ohne die [`tl()`](../functions/tl-method.md)-Methode für jeden Downloadlink manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie das automatische Linktracking für Downloadlinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle geklickten Link-URLs mit den Werten in [`linkDownloadFileTypes`](linkdownloadfiletypes.md). Bei Übereinstimmung wird automatisch ein Download-Linktracking-Aufruf ausgelöst.

## Aktivieren oder Deaktivieren der Klickkollektion mithilfe der Web SDK-Erweiterung

Verwenden Sie das Kontrollkästchen [!UICONTROL Klick-Datenerfassung aktivieren] bei der Konfiguration des Web SDK. Dieses Kontrollkästchen verarbeitet sowohl Exitlinks als auch Downloadlinks.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter [!UICONTROL Adobe Experience Platform Web SDK] auf die Schaltfläche **[!UICONTROL Konfigurieren]** .
1. Klicken Sie unter [!UICONTROL Datenerfassung] auf das Kontrollkästchen **[!UICONTROL Klick-Datenerfassung aktivieren]** .

## Aktivieren oder Deaktivieren der Klickkollektion durch manuelles Implementieren des Web SDK

Konfigurieren Sie das SDK mit &quot;[`clickCollectionEnabled`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html#clickCollectionEnabled)&quot;. Das Feld ist ein boolescher Wert, der bestimmt, ob mit Link-Klicks verknüpfte Daten automatisch erfasst werden. Der Standardwert lautet `true`. Setzen Sie diesen Wert auf `false` , wenn Sie das automatische Linktracking deaktivieren möchten. Diese Einstellung verarbeitet das automatische Linktracking für Download- und Exitlinks.

```json
alloy("configure", {
  "clickCollectionEnabled": true
});
```

## Tracking von Downloadlinks mit der Adobe Analytics-Erweiterung

„Downloadlinks verfolgen“ ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL Downloadlinks verfolgen] angezeigt wird.

Aktivieren Sie das Kontrollkästchen, um das automatische Tracking von Downloadlinks zu aktivieren.

## s.trackDownloadLinks in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

`s.trackDownloadLinks` ist ein boolescher Wert, der das automatische Tracking von Downloadlinks aktiviert oder deaktiviert. Wenn Sie Downloadlinks nicht verfolgen oder die `tl()`-Methode zum Tracking von Downloads lieber manuell aufrufen möchten, setzen Sie diese Variable auf `false`.

```js
s.trackDownloadLinks = true;
```
