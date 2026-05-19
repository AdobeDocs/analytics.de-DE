---
title: account
description: (Eingestellt) Bestimmen Sie die Report Suite, an die Daten gesendet werden.
feature: Appmeasurement Implementation
exl-id: 075d20be-6109-4024-84c4-1d048678d2bd
role: Admin, Developer
TQID: https://experienceleague.adobe.com/TmNxbAFJXxEnMJZNNZKP1ldkmeYICEzKdNoptNChzko
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 38%

---

# account

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Verwenden Sie die [`s.sa()`](../functions/sa-method.md)-Funktion, wenn Sie bei Ihrer Implementierung die Ziel-Report Suite ändern müssen.

In früheren Versionen von Adobe Analytics hat die `account`-Variable die Report Suite ermittelt, an die Sie Daten senden möchten. Zum Senden von Daten an Adobe Analytics ist eine Report Suite-ID erforderlich.

* Wenn Sie Web SDK verwenden, befinden sich Report Suites in den Adobe Analytics-Diensteinstellungen innerhalb des Datenstroms, an den die Web SDK Daten sendet.
* Wenn Sie die Adobe Analytics-Erweiterung verwenden, befinden sich die Report Suites beim Konfigurieren [!UICONTROL &#x200B; Adobe Analytics]Erweiterung im Akkordeon Bibliotheksverwaltung .
* Wenn Sie die Funktion [`s_gi()`](../functions/s-gi.md) verwenden, um ein Analytics-Tracking-Objekt zu instanziieren, sind die Report Suite-ID(s) bereits als erforderliches Argument in der Funktion vorhanden.
