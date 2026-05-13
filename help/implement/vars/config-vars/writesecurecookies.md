---
title: writeSecureCookies
description: Ermöglicht AppMeasurement das Setzen von Cookies mit dem Secure-Attribut.
feature: Appmeasurement Implementation
exl-id: 0e03d621-5770-4c25-981d-e4af1431ec69
role: Admin, Developer
TQID: https://experienceleague.adobe.com/-tuPYoFSzQb6-auIIAuihn--8Hb6vTKjIhhFd1XfXRQ
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 278
ht-degree: 77%

---

# writeSecureCookies

Mit der Variablen `writeSecureCookies` kann AppMeasurement [sichere Cookies](https://en.wikipedia.org/wiki/Secure_cookie) für Analytics einrichten. Diese Einstellung gilt sowohl für Besucher-ID-Cookies, die von AppMeasurement gesetzt werden, als auch für Cookies, die Sie mit der `Util.CookieWrite()`-Methode festlegen. Sie erfordert AppMeasurement 2.18.0 oder höher.

`writeSecureCookies` gilt nur für Cookies, die von AppMeasurement-JavaScript (`s_fid`, `s_cc` und `s_sq`) gesetzt werden. Cookies, die von der `https`-Antwort (`s_vi` und `s_ecid`) gesetzt werden, können auf „sicher“ gesetzt werden, indem Sie sich an die Kundenunterstützung von Adobe wenden.

Weitere Informationen zu Analytics-Cookies finden Sie [hier](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=de).

>[!WARNING]
>
>Wenn Sie die Variable `writeSecureCookies` aktivieren, stellen Sie sicher, dass der gesamte Inhalt auf Ihrer Site sicher über HTTPS bereitgestellt wird. Die Datenerfassung funktioniert nicht ordnungsgemäß, wenn diese Variable aktiviert ist und Sie unsicheren Inhalt auf Ihrer Seite haben.

## Verwenden sicherer Cookies mit der Web-SDK

Wenn Ihre Site das HTTPS-Protokoll verwendet, wird das Attribut „Secure“ für alle Cookies festgelegt, die von Web SDK gesetzt werden.

## Schreiben sicherer Cookies mit der Adobe Analytics-Erweiterung

[!UICONTROL Sichere Cookies schreiben] ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Kontrollkästchen [!UICONTROL Sichere Cookies schreiben] angezeigt wird.

## s.writeSecureCookies in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die Variable `s.writeSecureCookies` ist ein boolescher Wert, der bestimmt, ob AppMeasurement beim Erstellen eines Cookies das Secure-Attribut einrichtet. Der Standardwert lautet `false`. Legen Sie diese Variable auf `true` fest, wenn der gesamte Inhalt auf Ihrer Site sicher ist und Cookies, die von AppMeasurement gesetzt werden, das Secure-Attribut aufweisen sollen.

```js
s.writeSecureCookies = true;
```
