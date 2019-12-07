---
description: Gewähren Sie Benutzern Zugriff auf allgemeine Elemente (Rechnungsstellung, Protokolle usw.), Unternehmensverwaltung, Tools, Web-Services, Report Builder und die Data Connectors-Integration.
keywords: groups;permissions
subtopic: Users and groups
title: Anpassen von Berechtigungen für Analytics-Tools
topic: Admin tools
uuid: 8e86bc17-46d3-4c5e-ac25-9f3bfc29b8fa
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Anpassen von Berechtigungen für Analytics-Tools

>[!IMPORTANT]
>
>Die Verwaltung von Benutzern und Produkten wurde in die [Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html) verschoben. Sie werden von Adobe erfahren, wann Sie Benutzer migrieren müssen. Nachdem alle Benutzer migriert wurden, wird die Herausgabe neuer Hilfeinhalte für **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Benutzerverwaltung]** eingestellt.

Gewähren Sie Benutzern Zugriff auf allgemeine Elemente (Rechnungsstellung, Protokolle usw.), Unternehmensverwaltung, Tools, Web-Services, Report Builder und die Data Connectors-Integration.

**[!UICONTROL Benutzerverwaltung]** &gt; **[!UICONTROL Gruppen]** &gt; **[!UICONTROL Zugriff auf alle Berichte]** &gt; **[!UICONTROL Analytics-Tools]** &gt; **[!UICONTROL Anpassen]**

> [!NOTE] In der Herbstversion 2016 (20. Oktober) wurden neue Gruppenverwaltungsfunktionen eingeführt. Unter [Administrative Änderungen – Herbst 2016](/help/admin/user-management2/c-user-management/permissions-changes.md) finden Sie eine Zusammenfassung der Neuheiten.

## Berichtszugriff – Analytics-Tools

![](assets/report-access-analytics-tools.png)

Klicken Sie auf **[!UICONTROL Anpassen]**, um Elemente auszuwählen, auf die die Gruppe Zugriff erhalten soll.

## Feldbeschreibungen

Die Einstellungen auf dieser Seite beziehen sich auf die Report Suites, die auf der Seite „[!UICONTROL Benutzergruppe definieren]“ ausgewählt wurden.

| Element | Beschreibung |
|--- |--- |
| **Allgemein** |  |
| [Code-Manager](/help/admin/admin/code-manager-admin.md) | Ermöglicht das Herunterladen von Datensammlungs-Code für Web- und mobile Plattformen. |
| Code-Manager – Web-Services | Ermöglicht es Nichtadministratoren, über Web-Services auf den Code-Manager zuzugreifen. |
| [Protokolle](/help/admin/admin/logs.md) | Ermöglicht Zugriff auf Protokolldateien, die anzeigen, wann sich Benutzer angemeldet haben, was genutzt und worauf zugegriffen wurde, sowie Report Suites und Admin-Änderungen. |
| Protokolle – Web-Services | Ermöglicht es Nichtadministratoren, über Web-Services auf Admin Tools-Protokolle zuzugreifen. |
| [Traffic-Management](/help/admin/c-traffic-management/traffic-management.md) | Auf der Seite „Traffic-Management“ können Sie Informationen zu erwarteten Änderungen des Trafficvolumens angeben. |
| Berechtigungsverwaltung | Ermöglicht Nichtadministratoren Zugriff auf Benutzerverwaltungsseiten in den Admin Tools. Diese Benutzer können die Einstellungen zwar lesen, aber nicht bearbeiten. |
| Berechtigungen (schreiben) – Web-Services | Erteilt Benutzern ohne Administratorrechte Lese- und Schreibberechtigungen für das Benutzermanagement der Web-Services.<br>Diese Einstellung bezieht sich insbesondere auf die angegebenen Berechtigungsaktionen in der Admin-API. |
| Berechtigungen (lesen) – Web-Services | Ermöglicht es Nichtadministratoren, Berechtigungseinstellungen in der Benutzerverwaltung über Web-Services einzusehen.<br>Diese Einstellung bezieht sich insbesondere auf die angegebenen Berechtigungsaktionen in der Admin-API. |
| **Unternehmensverwaltung** |  |
| [Sicherheit](/help/admin/company/security-manager.md) | Gewährt Zugriff auf die Sicherheits-Manager-Seite, über die der Zugriff auf Berichtsdaten gesteuert wird. Zu den Optionen gehören sichere Passwörter, Passwortablauf, IP-Anmeldebeschränkungen und E-Mail-Domänenbeschränkungen. |
| Support-Info | Gewährt Zugriff auf die Supportinformationen in den Unternehmenseinstellungen. |
| [Web-Services](/help/admin/company/web-services-admin.md) | Gewährt Zugriff auf die Web-Services-Seite in der Benutzeroberfläche der Admin Tools ([!UICONTROL Unternehmenseinstellungen] &gt; [!UICONTROL Web-Services]).<br>Mit der Web Services API erhalten Sie programmatischen Zugriff auf Adobe Analytics-Dienste, mit denen Sie verfügbare Funktionen über die Benutzeroberfläche duplizieren und erweitern können. |
| Single Sign-on (veraltet) | Gewährt Zugriff auf die Single Sign-on-Seite in den Admin Tools.<br>**Hinweis:** Single Sign-on wird in Adobe Experience Cloud mithilfe der [Kontoverknüpfung](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html) zwischen Experience Cloud und anderen Lösungen ermöglicht. |
| [Ausstehende Aktionen](/help/admin/company/pending-actions-admin.md) | Ermöglicht die Bearbeitung ausstehender Aktionen in den [!UICONTROL Unternehmenseinstellungen]. |
| [Co-Branding](/help/admin/company/co-branding-admin.md) | Ermöglicht das Co-Branding von Analytics. |
| [Voreinstellungen](/help/admin/admin/preferences-manager.md) | Ermöglicht Zugriff auf den [!UICONTROL Preference Manager]. |
| [Report Suites ausblenden](/help/admin/company/c-hide-report-suites.md) | Erteilt die Berechtigung zum Ausblenden von Report Suites in der Benutzeroberfläche von Adobe Analytics. |
| **Tools** | Mit diesen Einstellungen kann Zugriff auf Analytics-Tools (Oberflächen und Anwendungen) und erweiterte Funktionen wie Segmentierung und berechnete Metriken gewährt werden. |
| [Aktuelle Daten](https://marketing.adobe.com/resources/help/en_US/reference/data_latency.html) | Ermöglicht die Verwendung der Funktion „Aktuelle Daten“ für Berichte. |
| [Ad Hoc Analysis-Lizenzanwender](https://marketing.adobe.com/resources/help/en_US/dsc/) | Gewährt Zugriff auf [!UICONTROL Ad Hoc Analysis]. |
| Zugriff auf Web Services | Ermöglicht Nichtadministratoren Zugriff auf Web-Services. Erstellt Anmeldedaten für Web-Services. |
| [Report Builder](https://marketing.adobe.com/resources/help/en_US/arb/setup.html) | Ermöglicht Mitgliedern der Gruppe Zugriff auf [!UICONTROL Report Builder]-Lizenzen. |
| [Zugriff auf Analysis Workspace](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/) | Gewährt Benutzern Zugriff auf Analysis Workspace, die für [!DNL Adobe Analytics] empfohlene Berichtsschnittstelle. |
| [Reports &amp; Analytics](https://marketing.adobe.com/resources/help/en_US/sc/user/) | Gewährt Benutzern Zugriff auf Reports &amp; Analytics. |
| [Erstellung berechneter Metriken](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/) | Ermöglicht es Benutzern, berechnete Metriken zu erstellen. |
| [Erstellung von Segmenten](https://marketing.adobe.com/resources/help/en_US/analytics/segment/) | Ermöglicht es Benutzern, Segmente zu erstellen. |
| **Data Connectors** |  |
| Integrationen (erstellen, aktualisieren oder löschen) | Ermöglicht das Erstellen, Aktualisieren und Löschen von Data Connector-Integrationen. |
