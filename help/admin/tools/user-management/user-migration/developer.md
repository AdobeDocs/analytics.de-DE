---
description: Listet die von der Benutzermigration betroffenen APIs auf
title: Von der Benutzermigration betroffene APIs
feature: Admin Tools
exl-id: 82d0a1cd-1e25-4157-9bb9-bba1049fdc48
role: Admin, Developer
TQID: https://experienceleague.adobe.com/vrfYIoa98hEoUVW17cwOLWTPk-3MIRS2wwLPB-ZB5DA
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9e2c89f4188c723b4623a6e7859b74ede15e155b
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 32%

---

# Von der Benutzermigration betroffene APIs{#apis-affected-by-the-migration}

Adobe migriert alle Analytics-Anmeldeunternehmen von der [!DNL my.omniture.com] auf die Authentifizierung über Adobe CX Enterprise. Sobald ein Unternehmen mit dieser Migration beginnt, wird die programmgemäße Benutzererstellung und -verwaltung durch die Analytics-spezifischen Berechtigungen und `GetLoginKey`-Methoden, die mit den Versionen 1.3 und 1.4 der Analytics Admin-API verfügbar sind, nicht mehr unterstützt. Solche Aktionen werden jetzt in CX Enterprise über `adobe.io` aktiviert.

## Betroffene API-Methoden {#methods}

Die folgenden API-Methoden in v1.3 und v1.4 der Admin-API werden nicht mehr unterstützt, sobald Sie mit der Benutzermigration beginnen:

* Company.GetLoginKey
* Permissions.AddLogin
* permissions.authenticate
* permissions.deleteGroup
* Permissions.DeleteLogin
* Permissions.GetGroup
* Permissions.GetGroups
* Permissions.GetLogin
* Permissions.GetLogins
* Permissions.GetReportSuiteGroups
* Permissions.RemoveLoginSegment
* Permissions.SaveGroup
* permissions.saveLogin
* Permissions.GetLoginSegment

## Maßnahmen, die Sie ergreifen können {#actions}

Wenn Ihr Unternehmen derzeit diese Methoden verwendet, suchen Sie ab dem 31. März 2018 nach einer Benachrichtigung vor der Migration. Die Benachrichtigung wird mindestens 30 Tage vor Beginn der Migration Ihres Unternehmens zur CX Enterprise-Authentifizierung gesendet. Zu diesem Zeitpunkt werden diese Methoden nicht mehr unterstützt.

Wenn Ihr Unternehmen keine dieser Methoden verwendet, sind keine anderen Maßnahmen erforderlich als sicherzustellen, dass Sie nicht mit der Verwendung dieser Methoden beginnen.

Für weitere Informationen:

* [Allgemeine Informationen zur Benutzerverwaltung](https://helpx.adobe.com/de/enterprise/help/users.html)
* [User Management-API-Forum](https://community.adobe.com/t5/enterprise-teams/bd-p/enterprise-and-teams)
* [Migration von Analytics User Access and Management zu CX Enterprise](/help/admin/tools/user-management/user-migration/c-migration-tool.md)
