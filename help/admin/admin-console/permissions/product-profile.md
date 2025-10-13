---
title: Produktprofile für Adobe Analytics
description: Erfahren Sie, wie Produktprofile als Berechtigungsvorgaben verwendet werden können, die Produktadministratoren Benutzern in einer Organisation zuweisen können.
exl-id: 834e4cf1-20b0-4c9d-939a-19e00494c8dd
feature: Admin Tools
role: Admin
source-git-commit: 8f1a17d2b07d5b37ef6d3d3f426234b29be61319
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 65%

---

# Produktprofile für Adobe Analytics

Produktprofile sind Berechtigungsvorgaben, die Produktadministratoren Benutzern in einer Organisation zuweisen können. Wenn Sie ein Produktprofil erstellen und diesem Produktprofil einen Experience Cloud-Benutzer zuweisen, übernehmen diese die im Produktprofil enthaltenen Berechtigungselemente.

Allgemeine Informationen zu Produktprofilen, einschließlich der Erstellung von Produktprofilen und der Zuweisung von Benutzenden, finden Sie [Verwalten von Produktprofilen für &#x200B;](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html) im Enterprise-Benutzerhandbuch.

## Produktprofiladministratoren

Produktprofiladministratoren sind eine optionale Gruppe, die Benutzer zu diesem Produktprofil hinzufügen oder entfernen kann. Beachten Sie, dass ein Produktprofiladministrator nicht mit einem Produktadministrator identisch ist:

* Produktprofil-Administrierende haben keinen vollständigen Zugriff auf Adobe Analytics. Der uneingeschränkte Zugriff auf Adobe Analytics ist Produktadministratoren vorbehalten.
* Produktprofil-Administrierende können Berechtigungselemente in ihrem Produktprofil nicht anpassen.
* Produktprofiladministratoren können Benutzergruppen Produktprofile zuweisen oder entziehen.
* Produktprofiladministratoren eignen sich ideal für Teamleiter oder Manager, die für ihr Team den Zugriff auf Adobe Analytics gewähren und verwalten müssen. Für Einzelpersonen ist es nicht erforderlich, dass Systemadministratoren oder Produktadministratoren sich die Mühe geben, Zugriff auf Adobe Analytics zu gewähren.

Informationen zur Ernennung von Produktprofil-Administrierenden finden Sie im Abschnitt „Verwalten von Produktprofil-Administrierenden“ im Artikel [Verwalten von Produktprofilen für Enterprise-Benutzende](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html) im Enterprise-Benutzerhandbuch.

## Adobe Analytics-Berechtigungselemente

Für den Zugriff auf Adobe Analytics sind mindestens folgende Berechtigungen in einem Produktprofil erforderlich:

* Das Produktprofil muss Zugriff auf mindestens eine Report Suite haben
* Das Produktprofil muss zum Berechtigungselement für Analytics-Tools **Workspace Project Access&rbrace;**.

### Report Suites

Ermöglicht Zugriff auf Report Suites, die zu Ihrer Organisation in Analytics gehören. Ein Benutzer muss zu mindestens einer Report Suite gehören, um Zugriff auf Adobe Analytics erhalten zu können.

### Metriken

Ermöglicht Zugriff auf Metriken in Ihrer Report Suite. Metriken werden als ihre jeweilige Komponente in Analysis Workspace aufgeführt.

Benutzerdefinierte Metriken werden als „Benutzerspezifisches Ereignis 1-1000“ bezeichnet, um sie unabhängig von Report Suites zu halten. Wenn „Benutzerspezifisches Ereignis 1“ ein aktiviertes Berechtigungselement ist, hat dieser Benutzer Zugriff auf „event1“ in allen Report Suites des Produktprofils.

### Dimensionen

Gewährt Zugriff auf Dimensionen in Ihrer Report Suite. Dimensionen werden in Analysis Workspace als ihre jeweilige Komponente aufgelistet.

Benutzerdefinierte Variablen, wie z. B. eVars, werden als „Benutzerspezifische Konversion 1-250“ bezeichnet, um sie unabhängig von Report Suites zu halten. Wenn „Benutzerspezifische Konversion 1“ ein aktiviertes Berechtigungselement ist, hat dieser Benutzer Zugriff auf „eVar1“ in allen Report Suites des Produktprofils.

### Report Suite-Tools

Die Berechtigungselemente der Report Suite-Tools gewähren Zugriff auf Funktionen, die spezifisch für die Report Suites sind, auf die der Benutzer Zugriff hat. Eine vollständige Liste der Berechtigungselemente und Beschreibungen finden Sie unter [Report Suite-Tools](report-suite-tools.md).

### Analytics-Werkzeuge

Die Berechtigungselemente der Analytics-Tools gewähren Zugriff auf Funktionen, die unabhängig von den Report Suite-Einstellungen sind. Eine vollständige Liste der Berechtigungselemente und Beschreibungen finden Sie bei den [Produktprofilberechtigungen für Analytics-Werkzeuge](analytics-tools.md).

## Produktprofilentwickler

Entwickler sind mit Benutzenden vergleichbar, allerdings können sie die Experience Cloud-API in Adobe Developer verwenden. Weitere Informationen finden Sie im Enterprise-Benutzerhandbuch unter [Verwalten von Entwicklern und Entwicklerinnen](https://helpx.adobe.com/de/enterprise/using/manage-developers.html). Wenn einem Benutzer Entwicklerzugriff für ein beliebiges Profil gewährt wird, kann er auf die Dev-Konsole (console.adobe.io) zugreifen und Adobe Analytics-Integrationen bearbeiten. Die für den Benutzer autorisierten Aufrufe und Antworten der Analytics-API hängen von den Nettoberechtigungen aller Profile ab, auf die der Entwicklerzugriff besteht.

Beispielsweise kann ein Entwickler mit Profilberechtigungen, die alle Metriken, alle Dimensionen und eine Report Suite enthalten, API-Aufrufe durchführen, die für jede Komponente innerhalb dieser Report Suite relevant sind. Wenn das Berechtigungselement zur Anomalieerkennung hinzugefügt wird, können API-Antworten Anomaliedaten enthalten. Als Faustregel gilt: Wenn ein Profil Zugriff auf ein Szenario in der Adobe Analytics-Benutzeroberfläche gewährt, ermöglicht der Entwicklerzugriff auf ein ähnlich definiertes Profil entsprechende API-Aufrufe und -Antworten.
