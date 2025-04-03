---
description: Analytics-Inventar verwenden
title: Analytics-Inventar
feature: Admin Tools
role: Admin
hide: true
hidefromtoc: true
exl-id: 9fc985c8-93d7-4838-9342-72a6268ef96f
source-git-commit: 1e52aecdbb26dce0875b2df685ed2fa860eaba85
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 25%

---

# Analytics-Inventar {#analytics-inventory}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory"
>title="Analytics-Inventar"
>abstract="Diese Seite bietet einen umfassenden Überblick über Ihre Adobe Analytics-Umgebung, einschließlich der Anzahl der Projekte und Komponenten, Report Suites, Benutzenden und mehr. Diese Informationen sind besonders nützlich, wenn Sie mit den Vorbereitungen für die Aktualisierung auf Customer Journey Analytics beginnen."

<!-- markdownlint-enable MD034 -->

Das Analytics-Inventar bietet einen umfassenden Überblick über Ihre Adobe Analytics-Umgebung, einschließlich der Anzahl der Projekte und Komponenten, Report Suites, Benutzer und mehr. Diese Informationen sind besonders nützlich, wenn Sie mit den Vorbereitungen für die Aktualisierung auf Customer Journey Analytics beginnen.

Ziel dieser Anwendung ist es, Ihnen bei der Beantwortung der folgenden Fragen zu helfen:

* Welche Assets (z. B. Report Suites, Segmente, Benutzer, Workspace-Projekte, Daten-Feeds usw.) müssen Sie für Ihr Unternehmen aktualisieren und welche Assets können Sie hinterlassen?

* Nachdem Sie ermittelt haben, welche Assets migriert werden müssen:

   * Sollten Sie vor diesem Upgrade eine Bereinigung der Assets durchführen?

   * Sollten Sie im Rahmen dieses Prozesses eine Asset-Konsolidierung durchführen?

   * Wie sollte die Upgrade-Sequenz für Ihre Assets lauten?

   * Für welche Gruppe von Report Suites ist ein Upgrade erforderlich? Letzte?

## Zugriffsberechtigungen

Das Analytics-Inventar steht Benutzenden mit Adobe Analytics-Produktadministratorrechten in [Adobe Admin Console zur ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/admin-roles-in-analytics).

## Zugriff auf Analytics-Inventar

1. Klicken Sie **** Menü **[!UICONTROL Admin]** auf Analytics-Inventar. Oder gehen Sie zu **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Analytics-Inventar]**.

![analytics-inventory-menu](assets/an-inventory-menu.png)

1. Der Hauptbildschirm zeigt eine umfassende Bestandsaufnahme Ihrer Adobe Analytics-Umgebung:

   ![Hauptinventarbildschirm](assets/an_inventory.png)

   Insbesondere wird dieser Bildschirm angezeigt

   * Die Gesamtzahl der Analysis Workspace- und Mobile-Scorecard-Projekte, die unter dieser Organisation für alle Benutzenden aktiv sind.
   * Die Gesamtzahl der Segmente und berechneten Metriken, die unter dieser Organisation für alle Benutzer aktiv sind.
   * Die Gesamtzahl der definierten zugrunde liegenden Report Suites (Virtual Report Suites sind nicht enthalten).
   * Wenn die Media Analytics-Funktion aktiv ist und falls ja, in welchem Modus.
   * Die Gesamtzahl der unter dieser Organisation definierten Benutzer.


## Komponenten {#components}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-components"
>title="Komponenten"
>abstract="In diesem Abschnitt wird die Anzahl der Projekte, Segmente und berechneten Metriken angezeigt, die in Ihrer Adobe Analytics-Umgebung vorhanden sind. Projekte und Komponenten können zu Customer Journey Analytics migriert werden."

<!-- markdownlint-enable MD034 -->

In dieser ersten Version können Sie zusammenfassende Inventarnummern für Workspace-Projekte, -Segmente und berechnete Metriken anzeigen. In nachfolgenden Versionen können Sie diese Komponenten analysieren.

## Datenkonfiguration und -erfassung {#data-config}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-data-config"
>title="Datenkonfiguration und -erfassung"
>abstract="In diesem Abschnitt wird die Anzahl der Report Suites in Ihrer Adobe Analytics-Umgebung sowie Ihr Zugriff auf Streaming-Medien angezeigt. "

<!-- markdownlint-enable MD034 -->

### Report Suites

Die Ansicht Report Suites zeigt alle Report Suites an, die in einer Organisation definiert sind. Damit können Sie die folgenden Fragen beantworten:

* Welche Report Suites haben in den letzten 90 Tagen den meisten Treffer erhalten?
* Welche Report Suites haben in den letzten 90 Tagen keinen Treffer erhalten?
* Für welche Report Suites ist die größte Anzahl von Dimensionen definiert?
* Für welche Report Suites ist die größte Anzahl von Metriken definiert?

Die Antworten auf diese Fragen geben Ihnen eine gute Vorstellung davon, welche Report Suites die besten Kandidaten für die Migration sind.

1. Um Report Suites zu analysieren, navigieren Sie zu **[!UICONTROL Datenkonfiguration und -erfassung]** > **[!UICONTROL Report Suites]** und klicken Sie auf **[!UICONTROL Analysieren]**.

   ![Liste der Report Suites](assets/an_inv_rs.png)

   | Element | Beschreibung |
   | --- | --- |
   | Name | Der Name der Report Suite |
   | ID | Die Report Suite-ID (RSID). Gibt eine eindeutige ID an, die nur alphanumerische Zeichen enthalten darf. Diese ID kann nach dem Erstellen nicht mehr geändert werden. Adobe legt das erforderliche ID-Präfix fest, das ebenfalls nicht geändert werden kann. |
   | Vorkommnisse (letzte 90 Tage) | Wie viele Treffer hat diese Report Suite in den letzten 90 Tagen erhalten? |
   | Metriken | Wie viele Metriken sind in dieser Report Suite definiert? |
   | Dimensionen | Wie viele Dimensionen sind in dieser Report Suite definiert? |
   | Analytics for Target (A4T) aktiviert | Ist diese Report Suite für „Analytics [ Target“ ](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t)? |
   | Marketing-Kanäle aktiviert | Ist diese Report Suite für „Marketing[Kanäle“ ](https://experienceleague.adobe.com/en/docs/analytics/components/marketing-channels/c-getting-started-mchannel)? |
   | Source Connector aktiviert | [In Entwicklung] Ist diese Report Suite für den [Adobe Analytics Source-Connector für Report Suite-Daten ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/analytics) Adobe Experience Platform aktiviert? Anders ausgedrückt: Kann diese Report Suite mithilfe des Analytics Source Connectors nach Customer Journey Analytics migriert werden? |
   | Kalendertyp | Weitere Informationen finden Sie unter [Benutzerdefinierte Kalender](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/custom-calendar#) |

1. Beachten Sie Folgendes…

### In CSV exportieren

1. Um die Liste der Report Suites in eine CSV-Datei zu exportieren, klicken Sie auf **[!UICONTROL In CSV exportieren]**.

1. Die CSV-Datei wird im Ordner „Downloads“ angezeigt.

1. Öffnen und speichern Sie sie mit einer Tabellenkalkulationsanwendung auf Ihrem Gerät.


## Benutzerverwaltung {#user-management}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-user-management"
>title="Benutzerverwaltung"
>abstract="In diesem Abschnitt wird die Anzahl der Benutzenden in Ihrer Adobe Analytics-Umgebung angezeigt."

<!-- markdownlint-enable MD034 -->

Die Benutzerverwaltung wird in einer späteren Version des Analytics-Inventars verfügbar sein.