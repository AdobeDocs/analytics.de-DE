---
title: cookieDomainPeriods
description: (Veraltet) Helfen Sie AppMeasurement, zu bestimmen, wo Cookies gespeichert werden, wenn die Domäne auf oberster Ebene einer Website einen Punkt enthält.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
source-git-commit: 1cdcc748e50c7eeffa98897006154aa0953ce7e3
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 18%

---

# cookieDomainPeriods

>[!IMPORTANT]
>Diese Variable wird nicht mehr unterstützt. Wenn Sie einen der folgenden Schritte verwenden:
>
>* AppMeasurement v2.26.x oder höher
>* Adobe Analytics-Erweiterung v1.9.4 oder höher
>* Adobe Experience Cloud ID-Dienst
>
>Diese Variable hat keine Auswirkung, da die entsprechende Bibliothek automatisch die Domäne erkennt, in der Cookies gesetzt werden sollen.

Die Variable `cookieDomainPeriods` half AppMeasurement bei der Bestimmung, wo Analytics-Cookies gesetzt werden sollten, indem sie angibt, dass die Domäne der obersten Ebene einen zusätzlichen Punkt enthielt. Diese Variable ermöglichte es AppMeasurement, den zusätzlichen Punkt in der Domäne auf oberster Ebene aufzunehmen und Cookies an der richtigen Stelle zu setzen. Wenn die Domäne der obersten Ebene Ihrer Website keinen zusätzlichen Punkt enthält, ist diese Variable nicht erforderlich.

* Bei Domänen wie `example.co.uk` oder `www.example.co.jp` setzen Sie diese Variable auf `"3"`.
* Legen Sie für Domänen wie `example.nsw.gov.au` diese Variable auf `"4"` fest.
* Bei Domänen wie `example.com` oder `products.example.org` dürfen Sie diese Variable nicht festlegen oder auf `"2"` setzen.

>[!TIP]
>
>Berücksichtigen Sie für diese Variable keine Subdomains. Legen Sie beispielsweise nicht `cookieDomainPeriods` für die Beispiel-URL `store.toys.example.com` fest. AppMeasurement erkennt, dass Cookies auf `example.com` gespeichert werden, selbst auf URLs mit vielen Subdomänen.

Bei Implementierungen auf AppMeasurement v2.26.x oder höher wird das Cookie [`s_ac`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) verwendet, um automatisch die richtige Cookie-Domäne zu ermitteln. Die Bibliothek versucht zunächst, ein Cookie mit zwei Domänenpunkten zu schreiben. Wenn das Setzen dieses Cookies fehlschlägt, wird ein weiterer Versuch unternommen, einschließlich weiterer Domänenpunkte, bis sie erfolgreich sind. Dieses Cookie wird sofort gelöscht, sobald es gesetzt wurde.

## Cookie-Domänenpunkte mit dem Web SDK

Das Web SDK bestimmt automatisch die richtige Domäne, in der Cookies gesetzt werden.

## Cookie-Domänenpunkte mit der Adobe Analytics-Erweiterung

**[!UICONTROL Domänenpunkte]** ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Domänenpunkte] angezeigt wird.

Setzen Sie dieses Feld nur auf Top-Level-Domänen, die einen Punkt enthalten, auf &quot;`3`&quot;. Andernfalls kann dieses Feld leer gelassen werden.

## Cookie-Domänenpunkte in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Variable &quot;`cookieDomainPeriods`&quot; ist eine Zeichenfolge, die normalerweise auf &quot;`"3"`&quot; gesetzt wird, und zwar nur bei Domänen auf oberster Ebene, die einen Punkt enthalten. Der Standardwert ist `"2"`, der für die meisten Top-Level-Domänen wie `.com` und `.org` geeignet ist.

```js
// Manually set cookieDomainPeriods for domains with a period in the top-level domain, such as www.example.co.uk
s.cookieDomainPeriods = "3";
```
