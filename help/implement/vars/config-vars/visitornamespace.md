---
title: visitorNameSpace
description: (Eingestellt) Hilfe bei der Bestimmung der Drittanbieter-Cookie-Domain.
feature: Appmeasurement Implementation
exl-id: 4fea35c0-9998-4438-a2ca-af65a35a449e
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/RHVRufQsrgYigyj0n348-xAZqrDyvpiV83G7fhpo5Q0'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 89%

---

# visitorNamespace

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Verwenden Sie stattdessen [`trackingServer`](trackingserver.md).

In früheren Versionen von Adobe Analytics verwendete AppMeasurement die `visitorNameSpace`-Variable zur Bestimmung der Unterdomäne von `2o7.net`, in der Besuchercookies gespeichert werden. Durch die zunehmenden Datenschutzpraktiken in modernen Browsern werden die Cookies von Drittanbietern weniger zuverlässig. Mit der Einführung der Variablen `trackingServer` und [`trackingServerSecure`](trackingserversecure.md) wird `visitorNameSpace` nicht mehr benötigt.

>[!TIP]
>
>Adobe empfiehlt die Verwendung von Erstanbieter-Cookies auf Ihrer Website. Erstanbieter-Cookies verwenden diese Variable nicht.

## Besucher-Namespace unter Verwendung der Adobe Analytics-Erweiterung

[!UICONTROL Besucher-Namespace] ist ein Feld unter dem Akkordeon [!UICONTROL Cookies] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Cookies], wodurch das Feld [!UICONTROL Besucher-Namespace] angezeigt wird.

Adobe empfiehlt, dieses Feld nicht zu verwenden. Verwenden Sie stattdessen `trackingServer` und `trackingServerSecure`.

## s.visitorNamespace in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.visitorNamespace`-Variable ist eine Zeichenfolge, die einen eindeutigen Wert pro Organisation enthält. Alte AppMeasurement-Bibliotheken enthielten diesen eindeutigen Wert automatisch, wenn sie von früheren Versionen von Adobe Analytics heruntergeladen wurden. Aktuelle AppMeasurement-Bibliotheken verwenden diese Variable nur, wenn `trackingServer` und `trackingServerSecure` gesetzt sind.

Wenn Ihre Organisation diese Variable noch benötigt, wählen Sie einen Wert, der Ihre Organisation repräsentiert. Sie können diesen Wert in einem [Lösungsdesigndokument](../../prepare/solution-design.md) speichern.

```js
// If trackingServer is not set, cookies are stored under example.112.2o7.net
s.visitorNameSpace = "example";
```
