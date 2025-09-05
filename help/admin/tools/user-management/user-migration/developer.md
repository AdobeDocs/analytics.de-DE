---
description: Listet die von der Benutzermigration betroffenen APIs auf
title: Von der Benutzermigration betroffene APIs
feature: Admin Tools
exl-id: 82d0a1cd-1e25-4157-9bb9-bba1049fdc48
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 95%

---

# Von der Benutzermigration betroffene APIs{#apis-affected-by-the-migration}

Adobe migriert alle Analytics-Anmeldeunternehmen weg von [!DNL my.omniture.com] und hin zur Authentifizierung über Adobe Experience Cloud. Sobald ein Unternehmen mit dieser Migration beginnt, wird die programmgemäße Benutzererstellung und -verwaltung durch die Analytics-spezifischen Berechtigungen und `GetLoginKey`-Methoden, die mit den Versionen 1.3 und 1.4 der Analytics Admin-API verfügbar sind, nicht mehr unterstützt. Solche Aktionen sind nun in Experience Cloud über [!DNL adobe.io] möglich.

## Betroffene API-Methoden {#methods}

Die folgenden API-Methoden in den Versionen v1.3 und v1.4 der Admin-API werden nach Beginn der Benutzermigration nicht mehr unterstützt:

* Company.GetLoginKey
* Permissions.AddLogin
* Permissions.Authenticate
* Permissions.DeleteGroup
* Permissions.DeleteLogin
* Permissions.GetGroup
* Permissions.GetGroups
* Permissions.GetLogin
* Permissions.GetLogins
* Permissions.GetReportSuiteGroups
* Permissions.RemoveLoginSegment
* Permissions.SaveGroup
* Permissions.SaveLogin
* Permissions.GetLoginSegment

## Maßnahmen, die Sie ergreifen können {#actions}

Sollte Ihr Unternehmen diese Methoden derzeit verwenden, erhalten Sie nach dem 31. März 2018 eine Migrationsbenachrichtigung. Die Benachrichtigung erfolgt mindestens 30 Tage vor Beginn der Migration Ihres Unternehmens auf die Experience Cloud-Authentifizierung. Ab diesem Zeitpunkt werden diese Methoden nicht mehr unterstützt.

Wenn Ihr Unternehmen keine dieser Methoden verwendet, ist keine weitere Aktion erforderlich, außer sicherzustellen, dass Sie diese Methoden nicht verwenden.

Weitere Informationen:

* [Allgemeines User Management – Start](https://helpx.adobe.com/de/enterprise/help/users.html)
* [User Managements-API-Forum](https://community.adobe.com/t5/enterprise-teams/bd-p/enterprise-and-teams)
* [Migration von Analytics User Access and Management zu Experience Cloud](/help/admin/tools/user-management/user-migration/c-migration-tool.md)
