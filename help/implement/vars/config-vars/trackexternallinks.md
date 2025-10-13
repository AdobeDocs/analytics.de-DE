---
title: trackExternalLinks
description: Aktivieren oder deaktivieren Sie das automatische Linktracking für Exitlinks.
feature: Appmeasurement Implementation
exl-id: a34d4ffa-ff82-460e-af7d-1a4be85fc631
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 60%

---

# trackExternalLinks

Adobe bietet die Möglichkeit, ausgehende Links zu verfolgen, ohne die [`tl()`](../functions/tl-method.md)-Methode für jeden Exitlink manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie das automatische Linktracking für Exitlinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle geklickten Link-URLs mit den Werten in [`linkInternalFilters`](linkinternalfilters.md) und [`linkExternalFilters`](linkexternalfilters.md). Bei Übereinstimmung wird automatisch ein Exitlinktracking-Aufruf ausgelöst.

## Aktivieren oder Deaktivieren der Klick-Erfassung mithilfe der Web SDK-Erweiterung

Verwenden Sie das [!UICONTROL Aktivieren der Klick-Datenerfassung] beim Konfigurieren der Web-SDK. Dieses Kontrollkästchen verarbeitet sowohl Exit- als auch Download-Links.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter &lbrace;4 **[!UICONTROL Adobe Experience Platform Web SDK]** auf die Schaltfläche Konfigurieren[!UICONTROL .]
1. Klicken [!UICONTROL &#x200B; unter &quot;]&quot; auf das Kontrollkästchen **[!UICONTROL Aktivieren]** Datenerfassung“.

## Aktivieren oder Deaktivieren der Klick-Sammlung Manuelles Implementieren der Web-SDK

Konfigurieren Sie die SDK mithilfe von [`clickCollectionEnabled`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de#clickCollectionEnabled). Bei dem Feld handelt es sich um einen booleschen Wert, der bestimmt, ob mit Link-Klicks verknüpfte Daten automatisch erfasst werden. Der Standardwert lautet `true`. Legen Sie diesen Wert auf `false` fest, wenn Sie die automatische Link-Überwachung deaktivieren möchten. Diese Einstellung behandelt die automatische Linkverfolgung für Download- und Exitlinks.

```json
alloy("configure", {
  "clickCollectionEnabled": true
});
```

## Nachverfolgen ausgehender Links mit der Adobe Analytics-Erweiterung

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
