---
title: trackExternalLinks
description: Aktivieren oder deaktivieren Sie das automatische Linktracking für Exitlinks.
feature: Variables
exl-id: a34d4ffa-ff82-460e-af7d-1a4be85fc631
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 60%

---

# trackExternalLinks

Adobe bietet die Möglichkeit, ausgehende Links zu verfolgen, ohne die [`tl()`](../functions/tl-method.md)-Methode für jeden Exitlink manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie das automatische Linktracking für Exitlinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle geklickten Link-URLs mit den Werten in [`linkInternalFilters`](linkinternalfilters.md) und [`linkExternalFilters`](linkexternalfilters.md). Bei Übereinstimmung wird automatisch ein Exitlinktracking-Aufruf ausgelöst.

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

## Ausgehende Links mit der Adobe Analytics-Erweiterung verfolgen

„Ausgehende Links verfolgen“ ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL Ausgehende Links verfolgen] angezeigt wird.

Aktivieren Sie das Kontrollkästchen, um das automatische Tracking von Exitlinks zu aktivieren.

## s.trackExternalLinks in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

`s.trackExternalLinks` ist ein boolescher Wert, der das automatische Tracking von Exitlinks aktiviert oder deaktiviert. Wenn Sie ausgehende Links nicht verfolgen oder die `tl()`-Methode zum Tracking von Exitlinks lieber manuell aufrufen möchten, setzen Sie diese Variable auf `false`.

```js
s.trackExternalLinks = true;
```
