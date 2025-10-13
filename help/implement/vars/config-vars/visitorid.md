---
title: visitorID
description: Verwenden Sie eine benutzerdefinierte Besucher-ID.
feature: Appmeasurement Implementation
exl-id: cb336042-01a1-4a66-a947-a221a7919c1b
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 71%

---

# visitorID

Adobe verwendet verschiedene Methoden zur Identifizierung von Besuchern Ihrer Website. Die `visitorID`-Variable setzt alle anderen Methoden zur Besucheridentifizierung außer Kraft.

>[!IMPORTANT]
>
>Adobe empfiehlt, diese Variable nicht zu verwenden. Verwenden Sie stattdessen den [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de).

## Besucher-ID bei Verwendung der Adobe Analytics-Erweiterung

[!UICONTROL Besucher-ID] ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Besucher-ID] angezeigt wird.

Weisen Sie dieses Feld dem Datenelement zu, das Ihre benutzerdefinierte Besucher-ID enthält. Legen Sie für dieses Feld keinen statischen Wert fest.

## s.visitorID in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.visitorID`-Variable ist eine Zeichenfolge, die eine benutzerdefinierte eindeutige Kennung für den Besucher enthält. Gültige Werte sind alphanumerische Zeichen bis zu 100 Byte. Verwenden Sie in dieser Variablen keine Bindestriche, Leerzeichen, Unterstriche oder Symbole.

>[!WARNING]
>
>Wenn Sie die `visitorID`-Variable während eines Besuchs festlegen, führen die Daten zu zwei separaten Unique Visitors.

```js
s.visitorID = "abc123";
```

>[!CAUTION]
>
>Eine ungültige Implementierung von benutzerdefinierten Besucher-IDs kann zu fehlerhaften Daten und schlechter Berichtsleistung führen. Wenn diese Variable einen Standardwert enthält (z. B. `"0"` oder `"NULL"`), behandelt Adobe diese Treffer so, als wären sie derselbe Besucher. Diese Situation führt zu falschen Daten, da die Besucherzahlen niedrig sind und Segmente auf Besucherebene nicht wie erwartet funktionieren. Falsch implementierte benutzerdefinierte Besucher-IDs führen auch zu einer hohen Belastung der Verarbeitungs-Server, was die [Latenz](/help/technotes/latency.md) erhöht und die Berichtsleistung verringert.

## Besucher-ID bei Verwendung der Web-SDK

Mit Adobe Experience Platform Edge Network können Sie mehrere Kennungen mithilfe der XDM-Identitätszuordnung [Identity Map) &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/overview.html#using-identitymap). Jede Identität in einer Identitätszuordnung hat einen anderen Namespace. Sie können angeben, welcher Namespace für die Besucher-ID als Teil der [Datenstromkonfiguration“ verwendet werden &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#analytics). Wenn Sie nach der Konfiguration ein Ereignis senden, dessen Wert für diesen Namespace angegeben ist, wird es automatisch als Besucher-ID in Analytics verwendet.
