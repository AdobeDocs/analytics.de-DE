---
description: Listet die von der Benutzermigration betroffenen APIs auf
title: Von der Benutzermigration betroffene APIs
uuid: 9a5d43be-e146-476b-961e-49ea0a30b500
exl-id: 82d0a1cd-1e25-4157-9bb9-bba1049fdc48
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 88%

---

# Von der Benutzermigration betroffene APIs{#apis-affected-by-the-migration}

Adobe migriert alle Analytics-Anmeldeunternehmen weg von [!DNL my.omniture.com] und hin zur Authentifizierung über Adobe Experience Cloud. Sobald ein Unternehmen mit dieser Migration beginnt, wird die programmgemäße Benutzererstellung und -verwaltung durch die Analytics-spezifischen Berechtigungen und `GetLoginKey`-Methoden, die mit den Versionen 1.3 und 1.4 der Analytics Admin-API verfügbar sind, nicht mehr unterstützt. Solche Aktionen sind nun in Experience Cloud über [!DNL adobe.io] möglich.

## Betroffene API-Methoden {#section-d19051ac26cc49aeb124f767c4760254}

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

## Maßnahmen, die Sie ergreifen können {#section-8b0b89a862614f729ebdbe092ce99027}

Sollte Ihr Unternehmen diese Methoden derzeit verwenden, erhalten Sie nach dem 31. März 2018 eine Migrationsbenachrichtigung. Die Benachrichtigung erfolgt mindestens 30 Tage vor Beginn der Migration Ihres Unternehmens auf die Experience Cloud-Authentifizierung. Ab diesem Zeitpunkt werden diese Methoden nicht mehr unterstützt.

Wenn Ihr Unternehmen keine dieser Methoden verwendet, ist keine weitere Aktion erforderlich, außer sicherzustellen, dass Sie diese Methoden nicht verwenden.

Weitere Informationen:

* [Allgemeines User Management – Start](https://helpx.adobe.com/de/enterprise/help/users.html)
* [User Managements-APIs via adobe.io](https://www.adobe.io/apis/cloudplatform/usermanagement/docs/gettingstarted.html)
* [User Managements-API-Forum](https://forums.adobe.com/community/umapi/overview)
* [Migration des Analytics-Benutzerzugriffs und -managements zur Experience Cloud](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)
