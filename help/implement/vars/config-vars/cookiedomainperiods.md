---
title: cookieDomainPeriods
description: (Veraltet) Helfen Sie AppMeasurement, zu bestimmen, wo Cookies gespeichert werden, wenn die Domäne auf oberster Ebene einer Website einen Punkt enthält.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
source-git-commit: 75ae77c1da1b578639609888e794e13d965ef669
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 19%

---


# cookieDomainPeriods

>[!IMPORTANT]
>Diese Variable wird nicht mehr unterstützt. Wenn Sie AppMeasurement v2.26.x oder höher oder die Adobe Analytics-Erweiterung v1.9.4 oder höher verwenden, erkennt die Bibliothek automatisch die Domäne, in der Cookies gesetzt werden sollen.

Die `cookieDomainPeriods` hat AppMeasurement dabei geholfen zu bestimmen, wo Analytics-Cookies gesetzt werden sollten, indem angegeben wurde, dass die Domäne auf oberster Ebene einen zusätzlichen Punkt enthielt. Diese Variable ermöglichte es AppMeasurement, den zusätzlichen Punkt in der Domäne auf oberster Ebene aufzunehmen und Cookies an der richtigen Stelle zu setzen. Wenn die Domäne der obersten Ebene Ihrer Website keinen zusätzlichen Punkt enthält, ist diese Variable nicht erforderlich.

* Bei Domänen wie `example.co.uk` oder `www.example.co.jp` setzen Sie diese Variable auf `"3"`.
* Für Domänen wie `example.nsw.gov.au`setzen Sie diese Variable auf `"4"`.
* Für Domänen wie `example.com` oder `products.example.org`, lassen Sie die Einstellung dieser Variablen weg oder legen Sie sie auf `"2"`.

>[!TIP]
>
>Berücksichtigen Sie für diese Variable keine Subdomains. Legen Sie beispielsweise nicht `cookieDomainPeriods` für die Beispiel-URL `store.toys.example.com` fest. AppMeasurement erkennt, dass Cookies in gespeichert werden. `example.com`, auch bei URLs mit vielen Subdomänen.

Bei Implementierungen auf AppMeasurement v2.26.x oder höher muss die Variable [`s_ac`](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) -Cookie wird verwendet, um automatisch die richtige Cookie-Domäne zu ermitteln. Die Bibliothek versucht zunächst, ein Cookie mit zwei Domänenpunkten zu schreiben. Wenn das Setzen dieses Cookies fehlschlägt, wird ein weiterer Versuch unternommen, einschließlich weiterer Domänenpunkte, bis sie erfolgreich sind. Dieses Cookie wird sofort gelöscht, sobald es gesetzt wurde.

## Cookie-Domänenpunkte mit dem Web SDK

Das Web SDK bestimmt automatisch die richtige Domäne, in der Cookies gesetzt werden.

## Cookie-Domänenpunkte mit der Adobe Analytics-Erweiterung

**[!UICONTROL Domänenpunkte]** ist ein Feld unter dem [!UICONTROL Cookies] Akkordeon beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Domänenpunkte] angezeigt wird.

Setzen Sie dieses Feld auf `3` nur auf Domänen auf oberster Ebene, die einen Punkt enthalten. Andernfalls kann dieses Feld leer gelassen werden.

## Cookie-Domänenpunkte in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `cookieDomainPeriods` ist eine Zeichenfolge, die normalerweise auf `"3"`, nur auf Domänen auf oberster Ebene, die einen Punkt enthalten. Der Standardwert lautet `"2"`, die die meisten Top-Level-Domänen wie `.com` und `.org`.

```js
// Manually set cookieDomainPeriods for domains with a period in the top-level domain, such as www.example.co.uk
s.cookieDomainPeriods = "3";
```
