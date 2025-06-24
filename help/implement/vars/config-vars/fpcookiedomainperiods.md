---
title: fpcookieDomainPeriods
description: Hilft AppMeasurement zu verstehen, welche Domain Cookies speichern soll, wenn Ihre Domain einen Punkt im Suffix hat.
feature: Appmeasurement Implementation
exl-id: e994a188-1dab-4bf0-912b-cd2f6a1032e0
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 86%

---

# fpCookieDomainPeriods

Mithilfe der `fpCookieDomainPeriods`-Variablen kann AppMeasurement ermitteln, wo Analytics-Cookies gesetzt werden, indem darauf hingewiesen wird, dass das Domänensuffix einen zusätzlichen Punkt enthält. Diese Variable ermöglicht es AppMeasurement, den zusätzlichen Punkt im Domänensuffix zu berücksichtigen und Cookies an der richtigen Stelle zu setzen. Sie erbt den Wert von [`cookieDomainPeriods`](cookiedomainperiods.md), ist jedoch nach wie vor eine Best Practice, wenn Sie eine Erstanbieter-Cookie-Implementierung verwenden.

* Bei Domänen wie `example.com` oder `www.example.com` muss diese Variable nicht eingestellt werden. Bei Bedarf können Sie diese Variable auf `"2"` setzen.
* Bei Domänen wie `example.co.uk` oder `www.example.co.jp` setzen Sie diese Variable auf `"3"`.

>[!IMPORTANT]
>
>Berücksichtigen Sie für diese Variable keine Subdomains. Legen Sie beispielsweise nicht `fpCookieDomainPeriods` für die Beispiel-URL `store.toys.example.com` fest. AppMeasurement erkennt standardmäßig, dass Cookies auf `example.com` gespeichert werden sollen. Das gilt auch für URLs mit vielen Unterdomänen.

## Punkte für Erstanbieter-Domains, die die Web-SDK verwenden

Web SDK kann ohne diese Variable die richtige Cookie-Speicherdomäne ermitteln.

## Punkte für Erstanbieter-Domains, die die Adobe Analytics-Erweiterung verwenden

„Erstanbieter-Domain-Punkte“ ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Erstanbieter-Domänenpunkte] angezeigt wird.

Setzen Sie dieses Feld nur bei Domänen, die einen Punkt im Suffix enthalten, auf `3`. Andernfalls kann dieses Feld leer gelassen werden.

## s.fpCookieDomainPeriods in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Variable `fpCookieDomainPeriods` ist eine Zeichenfolge, die normalerweise auf `"3"` gesetzt wird, und zwar nur bei Domänen, die einen Punkt in ihrem Suffix enthalten. Der Standardwert ist `"2"`, der für die meisten Domänen geeignet ist.

```js
// Manually set fpCookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.fpCookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.fpCookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.fpCookieDomainPeriods = "3" : s.fpCookieDomainPeriods = "2";
```
