---
title: trackingServer
description: Die Domain, die zum Senden von Daten über HTTP an Adobe verwendet wird.
feature: Appmeasurement Implementation
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
role: Admin, Developer
source-git-commit: 35675c2e65456a175d1516dd421b80d2af809286
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 13%

---

# trackingServer

>[!IMPORTANT]
>
>Diese Variable wird nicht mehr unterstützt. Mit der Prävalenz von HTTPS verwenden Sie stattdessen [`trackingServerSecure`](trackingserversecure.md).

Die Variable `trackingServer` bestimmt die Domain, die AppMeasurement verwendet, um Daten über HTTP an Adobe zu senden. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

Vor dem [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/en/docs/id-service/using/home) bestimmte diese Variable auch, wo Drittanbieter-Cookies gesetzt wurden. Adobe empfiehlt dringend, nach Möglichkeit den ID-Service in allen Implementierungen zu verwenden.

AppMeasurement verwendet `trackingServer` als Fallback, wenn [`trackingServerSecure`](trackingserversecure.md) nicht festgelegt ist. Viele ältere Implementierungen legen keine `trackingServerSecure` fest und verwenden `trackingServer` als Ausweichlösung für sichere Seiten. Da HTTPS weit verbreitet ist, empfiehlt Adobe, nach Möglichkeit `trackingServerSecure` zu verwenden.
