---
title: trackExternalLinks
description: Aktivieren oder deaktivieren Sie das automatische Linktracking für Exitlinks.
feature: Appmeasurement Implementation
exl-id: a34d4ffa-ff82-460e-af7d-1a4be85fc631
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/sFN18vtu4C0voXXXDo3LT-4uY4yyz8-ygwnZxIuABXM'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 340
ht-degree: 59%

---

# trackExternalLinks

Adobe bietet die Möglichkeit, ausgehende Links zu verfolgen, ohne die [`tl()`](../functions/tl-method.md)-Methode für jeden Exitlink manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie das automatische Linktracking für Exitlinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle geklickten Link-URLs mit den Werten in [`linkInternalFilters`](linkinternalfilters.md) und [`linkExternalFilters`](linkexternalfilters.md). Bei Übereinstimmung wird automatisch ein Exitlinktracking-Aufruf ausgelöst.

## Aktivieren oder Deaktivieren der Klick-Erfassung mithilfe der Web SDK-Erweiterung

Verwenden Sie das [!UICONTROL Aktivieren der Klick-Datenerfassung] beim Konfigurieren der Web-SDK. Dieses Kontrollkästchen verarbeitet sowohl Exit- als auch Download-Links.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter &lbrace;4 **[!UICONTROL Adobe Experience Platform Web SDK]** auf die Schaltfläche Konfigurieren.
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
