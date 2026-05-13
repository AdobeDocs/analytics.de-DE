---
title: cookieDomainPeriods
description: (Veraltet) Hilft AppMeasurement bei der Bestimmung, wo Cookies gespeichert werden sollen, wenn die Domain auf oberster Ebene einer Website einen Punkt enthält.
feature: Appmeasurement Implementation
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
TQID: https://experienceleague.adobe.com/bsJTIAuqcWoXWWus0oPME9LEwEMaiCGjd1ChmCuSjKY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 394
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

Die Variable `cookieDomainPeriods` half AppMeasurement dabei, zu bestimmen, wo Analytics-Cookies gesetzt werden sollen, indem angegeben wurde, dass die Domain der obersten Ebene einen zusätzlichen Zeitraum enthält. Diese Variable ermöglichte es AppMeasurement, den zusätzlichen Zeitraum in der Domain auf oberster Ebene zu berücksichtigen und Cookies am richtigen Ort festzulegen. Wenn die Domain auf oberster Ebene Ihrer Website keinen zusätzlichen Zeitraum enthält, ist diese Variable nicht erforderlich.

* Bei Domänen wie `example.co.uk` oder `www.example.co.jp` setzen Sie diese Variable auf `"3"`.
* Legen Sie für Domains wie `example.nsw.gov.au` diese Variable auf `"4"` fest.
* Lassen Sie bei Domains wie `example.com` oder `products.example.org` das Festlegen dieser Variablen aus oder legen Sie sie auf `"2"` fest.

>[!TIP]
>
>Berücksichtigen Sie für diese Variable keine Subdomains. Legen Sie beispielsweise nicht `cookieDomainPeriods` für die Beispiel-URL `store.toys.example.com` fest. AppMeasurement erkennt, dass Cookies auf `example.com` gespeichert werden, auch auf URLs mit vielen Subdomains.

Bei Implementierungen unter AppMeasurement v2.26.x oder höher wird das [`s_ac`](https://experienceleague.adobe.com/de/docs/core-services/interface/data-collection/cookies/analytics)-Cookie verwendet, um automatisch die richtige Cookie-Domain zu ermitteln. Die -Bibliothek versucht zunächst, ein Cookie zu schreiben, das zwei Domain-Punkte enthält. Wenn das Setzen dieses Cookies fehlschlägt, wird es erneut versucht, einschließlich weiterer Domain-Punkte, bis es erfolgreich ist. Dieses Cookie wird nach dem Setzen sofort gelöscht.

## Punkte für Cookie-Domains, die die Web-SDK verwenden

Web SDK bestimmt automatisch die richtige Domain zum Setzen von Cookies.

## Cookie-Domain-Punkte unter Verwendung der Adobe Analytics-Erweiterung

**[!UICONTROL Domain-Punkte]** ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Domänenpunkte] angezeigt wird.

Legen Sie dieses Feld so fest, dass nur in Domains der obersten Ebene mit einem Punkt `3` wird. Andernfalls kann dieses Feld leer gelassen werden.

## Punkte bei Cookie-Domains in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `cookieDomainPeriods`-Variable ist eine Zeichenfolge, die normalerweise auf `"3"` festgelegt ist, nur in Domains der obersten Ebene, die einen Punkt enthalten. Der Standardwert ist `"2"`, was für die meisten Domains der obersten Ebene wie `.com` und `.org` gilt.

```js
// Manually set cookieDomainPeriods for domains with a period in the top-level domain, such as www.example.co.uk
s.cookieDomainPeriods = "3";
```
