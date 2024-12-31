---
title: trackingServerSecure
description: Stellen Sie fest, an welcher Position auf HTTPS-Seiten Bildanforderungen gesendet werden.
feature: Variables
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 66%

---

# trackingServerSecure

Adobe erfasst Daten auf Ihrer Website, indem es eine vom Besucher generierte Bildanforderung empfängt. Die `trackingServerSecure`-Variable bestimmt die Position, an der eine Bildanforderung über HTTPS gesendet wird. Außerdem wird festgelegt, an welcher Stelle die Cookies von Besuchern gespeichert werden. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

>[!WARNING]
>
>Wenn Sie diesen Wert ändern, sucht AppMeasurement an einer anderen Stelle nach Cookies. Die Zahl der Unique Visitors kann bei der Berichterstellung vorübergehend zu Spitzenwerten führen, da Besucher-Cookies an der neuen Position gesetzt werden.

## Edge-Domain unter Verwendung der Web-SDK-Erweiterung

Die Web-SDK verwendet die [!UICONTROL Edge]Domain, um sowohl den Tracking-Server als auch den sicheren Tracking-Server zu verarbeiten. Sie können den gewünschten Wert für die [!UICONTROL Edge-Domain] beim Konfigurieren der Web-SDK-Erweiterung festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter {4 **[!UICONTROL Adobe Experience Platform Web SDK]** auf die Schaltfläche Konfigurieren].[!UICONTROL 
1. Legen Sie das gewünschte Textfeld **[!UICONTROL Edge Domain]** fest.

Weitere Informationen [ Sie in der Web](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=de)SDK-Dokumentation unter „Konfigurieren der Adobe Experience Platform WebSDKErweiterung“.

>[!TIP]
>
>Wenn Ihr Unternehmen von einer AppMeasurement- oder Analytics-Erweiterungsimplementierung zum Web SDK wechselt, kann dieses Feld denselben in `trackingServerSecure` (oder `trackingServer`) enthaltenen Wert verwenden.

## Edge-Domain - Manuelle Implementierung der Web-SDK

Konfigurieren Sie die SDK mithilfe von [`edgeDomain`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de). Das Feld ist eine Zeichenfolge, die die Domain bestimmt, an die Daten gesendet werden sollen.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## SSL-Tracking-Server mit der Adobe Analytics-Erweiterung

[!UICONTROL SSL-Tracking-Server] ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL SSL-Tracking-Server] angezeigt wird.

Wenn dieses Feld leer gelassen wird, wird standardmäßig der Wert in der [`trackingServer`](trackingserver.md)-Variablen verwendet.

## s.trackingServerSecure im AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.trackingServerSecure`-Variable ist eine Zeichenfolge, die die Stelle enthält, an die Bildanforderungen gesendet werden sollen. Es handelt sich dabei fast immer um eine Unterdomäne Ihrer Website. Moderne Datenschutzpraktiken in Browsern machen Cookies von Drittanbietern häufig unzuverlässig. Wenn diese Variable leer ist, wird der Wert in der `s.trackingServer`-Variablen verwendet.

Der Wert für diese Variable ist fast immer eine Erstanbieter-Domäne, z. B. `data.example.com`. Weitere Informationen zum Erstanbieter-Cookie-Prozess finden Sie unter [Erstanbieter-Cookies in der Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=de) im Core Services-Benutzerhandbuch.

Die Person, die die Erstanbieter-Cookie-Implementierung anfänglich konfiguriert, definiert auch die verwendete Domain und Unterdomäne. Beispiel:

```js
s.trackingServerSecure = "data.example.com";
```

CNAME-Einträge verweisen normalerweise auf eine Subdomain auf `data.adobedc.net`, `sc.adobedc.net` oder `2o7.net`.
