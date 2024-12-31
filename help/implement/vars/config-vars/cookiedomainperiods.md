---
title: cookieDomainPeriods
description: (Veraltet) Hilft AppMeasurement bei der Bestimmung, wo Cookies gespeichert werden sollen, wenn die Domain auf oberster Ebene einer Website einen Punkt enthält.
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
>Diese Variable wird nicht mehr unterstützt. Wenn Sie eine der folgenden Anwendungen anwenden:
>
>* AppMeasurement v2.26.x oder höher
>* Adobe Analytics-Erweiterung v1.9.4 oder höher
>* Adobe Experience Cloud ID-Dienst
>
>Diese Variable tut nichts, da die entsprechende Bibliothek automatisch die Domain erkennt, in der Cookies gesetzt werden sollen.

Mithilfe der `cookieDomainPeriods`-Variable konnte AppMeasurement bestimmen, wo Analytics-Cookies gesetzt werden sollen, indem angegeben wurde, dass die Domain der obersten Ebene einen zusätzlichen Zeitraum enthält. Diese Variable ermöglichte AppMeasurement, den zusätzlichen Zeitraum in der Domain auf oberster Ebene zu berücksichtigen und Cookies am richtigen Ort zu setzen. Wenn die Domain auf oberster Ebene Ihrer Website keinen zusätzlichen Zeitraum enthält, ist diese Variable nicht erforderlich.

* Bei Domänen wie `example.co.uk` oder `www.example.co.jp` setzen Sie diese Variable auf `"3"`.
* Legen Sie für Domains wie `example.nsw.gov.au` diese Variable auf `"4"` fest.
* Lassen Sie bei Domains wie `example.com` oder `products.example.org` das Festlegen dieser Variablen aus oder legen Sie sie auf `"2"` fest.

>[!TIP]
>
>Berücksichtigen Sie für diese Variable keine Subdomains. Legen Sie beispielsweise nicht `cookieDomainPeriods` für die Beispiel-URL `store.toys.example.com` fest. AppMeasurement erkennt, dass Cookies auf `example.com` gespeichert werden, auch auf URLs mit vielen Subdomains.

Bei Implementierungen unter AppMeasurement v2.26.x oder höher wird das [`s_ac`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics)-Cookie verwendet, um automatisch die richtige Cookie-Domain zu ermitteln. Die -Bibliothek versucht zunächst, ein Cookie zu schreiben, das zwei Domain-Punkte enthält. Wenn das Setzen dieses Cookies fehlschlägt, wird es erneut versucht, einschließlich weiterer Domain-Punkte, bis es erfolgreich ist. Dieses Cookie wird nach dem Setzen sofort gelöscht.

## Punkte für Cookie-Domains, die die Web-SDK verwenden

Web SDK bestimmt automatisch die richtige Domain zum Setzen von Cookies.

## Cookie-Domain-Punkte unter Verwendung der Adobe Analytics-Erweiterung

**[!UICONTROL Domain-Punkte]** ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Domänenpunkte] angezeigt wird.

Legen Sie dieses Feld so fest, dass nur in Domains der obersten Ebene mit einem Punkt `3` wird. Andernfalls kann dieses Feld leer gelassen werden.

## Punkte bei Cookie-Domains beim AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `cookieDomainPeriods`-Variable ist eine Zeichenfolge, die normalerweise auf `"3"` festgelegt ist, nur in Domains der obersten Ebene, die einen Punkt enthalten. Der Standardwert ist `"2"`, was für die meisten Domains der obersten Ebene wie `.com` und `.org` gilt.

```js
// Manually set cookieDomainPeriods for domains with a period in the top-level domain, such as www.example.co.uk
s.cookieDomainPeriods = "3";
```
