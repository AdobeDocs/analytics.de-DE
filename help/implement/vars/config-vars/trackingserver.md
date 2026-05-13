---
title: trackingServer
description: Die Domain, die zum Senden von Daten über HTTP an Adobe verwendet wird.
feature: Appmeasurement Implementation
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
role: Admin, Developer
TQID: https://experienceleague.adobe.com/6H8uZ4J-mT8NcC4OiiTgtBnP8eAgaMMzxzUHkS-9kGs
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
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 19%

---

# trackingServer

>[!IMPORTANT]
>
>Diese Variable wird nicht mehr unterstützt. Mit der Prävalenz von HTTPS verwenden Sie stattdessen [`trackingServerSecure`](trackingserversecure.md).

Die Variable `trackingServer` bestimmt die Domain, die AppMeasurement verwendet, um Daten über HTTP an Adobe zu senden. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

Vor dem [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/de/docs/id-service/using/home) bestimmte diese Variable auch, wo Drittanbieter-Cookies gesetzt wurden. Adobe empfiehlt dringend, nach Möglichkeit den ID-Service in allen Implementierungen zu verwenden.

AppMeasurement verwendet `trackingServer` als Fallback, wenn [`trackingServerSecure`](trackingserversecure.md) nicht festgelegt ist. Viele ältere Implementierungen legen keine `trackingServerSecure` fest und verwenden `trackingServer` als Ausweichlösung für sichere Seiten. Da HTTPS weit verbreitet ist, empfiehlt Adobe, nach Möglichkeit `trackingServerSecure` zu verwenden.
