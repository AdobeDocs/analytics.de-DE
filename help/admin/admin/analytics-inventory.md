---
description: Analytics-Inventar verwenden
title: Analytics-Inventar
feature: Admin Tools
role: Admin
exl-id: 9fc985c8-93d7-4838-9342-72a6268ef96f
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 20%

---

# Analytics-Inventar {#analytics-inventory}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory"
>title="Analytics-Inventar"
>abstract="Diese Seite bietet einen umfassenden Überblick über Ihre Adobe Analytics-Umgebung, einschließlich der Anzahl der Projekte und Komponenten, Report Suites, Benutzenden und mehr. Diese Informationen sind besonders nützlich, wenn Sie mit den Vorbereitungen für die Aktualisierung auf Customer Journey Analytics beginnen."

<!-- markdownlint-enable MD034 -->

Das Analytics-Inventar bietet einen umfassenden Überblick über Ihre Adobe Analytics-Umgebung, einschließlich der Anzahl der Projekte und Komponenten, Report Suites, Benutzer und mehr. Diese Informationen sind besonders nützlich, wenn Sie mit den Vorbereitungen für die Aktualisierung auf Customer Journey Analytics beginnen.

Das Ziel des Analytics-Inventars besteht darin, Ihnen bei der Beantwortung der folgenden Fragen zu helfen:

* Welche Assets (z. B. Report Suites, Segmente, Benutzer, Workspace-Projekte usw.) müssen für Ihr Unternehmen migriert werden und welche Assets können Sie hinterlassen?

* Nachdem Sie ermittelt haben, welche Assets migriert werden müssen:

   * Sollten Sie vor diesem Upgrade eine Bereinigung der Assets durchführen?

   * Sollten Sie im Rahmen dieses Prozesses eine Asset-Konsolidierung durchführen?

   * Wie sollte die Upgrade-Sequenz für Ihre Assets lauten?

   * Welche Report Suites sollten zuerst oder zuletzt aktualisiert werden?

## Berechtigungen

Das Analytics-Inventar steht Benutzenden mit Adobe Analytics-Produktadministratorrechten in [Adobe Admin Console zur ](https://experienceleague.adobe.com/de/docs/analytics/admin/admin-console/admin-roles-in-analytics).

## Zugriff auf Analytics-Inventar

1. Klicken Sie **&#x200B;**&#x200B;Menü **[!UICONTROL Admin]** auf Analytics-Inventar. Oder gehen Sie zu **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Analytics-Inventar]**.

![analytics-inventory-menu](assets/an-inventory-menu.png)

1. Der Hauptbildschirm zeigt eine umfassende Bestandsaufnahme Ihrer Adobe Analytics-Umgebung:

   ![Hauptinventarbildschirm](assets/an_inventory.png)

   Insbesondere zeigt dieser Bildschirm Folgendes:

   * Die Gesamtzahl der Analysis Workspace- und Mobile-Scorecard-Projekte, die unter dieser Organisation und allen Benutzern aktiv sind.
   * Die Gesamtzahl der Segmente und berechneten Metriken, die unter dieser Organisation für alle Benutzer aktiv sind.
   * Die Gesamtzahl der definierten zugrunde liegenden Report Suites. Virtual Report Suites sind nicht enthalten.
   * Wenn die Media Analytics-Funktion aktiv ist und falls ja, in welchem Modus.
   * Die Gesamtzahl der in dieser Organisation definierten Benutzer.


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
>abstract="In diesem Abschnitt wird die Anzahl der Report Suites in Ihrer Adobe Analytics-Umgebung sowie Ihr Zugriff auf Streaming-Mediendienste angezeigt."

<!-- markdownlint-enable MD034 -->

### Report Suites

Die Ansicht Report Suites zeigt alle Report Suites an, die in einer Organisation definiert sind. Damit können Sie die folgenden Fragen beantworten:

* Welche Report Suites haben in den letzten 90 Tagen die meisten Treffer erhalten?
* Welche Report Suites haben in den letzten 90 Tagen keine Treffer erhalten?
* Für welche Report Suites ist die größte Anzahl von Dimensionen definiert?
* Für welche Report Suites ist die größte Anzahl von Metriken definiert?

Die Antworten auf diese Fragen geben Ihnen eine gute Vorstellung davon, welche Report Suites die besten Kandidaten für die Migration sind.

>[!NOTE]
>
>Diese Tabelle wird nur langsam und mit jeweils einem Zellenwert ausgefüllt.


1. Um Report Suites zu analysieren, navigieren Sie zu **[!UICONTROL Datenkonfiguration und -erfassung]** > **[!UICONTROL Report Suites]** und klicken Sie auf **[!UICONTROL Analysieren]**.

   ![Liste der Report Suites](assets/an_inv_rs.png)

   | Element | Beschreibung |
   | --- | --- |
   | Name | Der Name der Report Suite |
   | ID | Die Report Suite-ID (RSID). Gibt eine eindeutige ID an, die nur alphanumerische Zeichen enthalten darf. Diese ID kann nach dem Erstellen nicht mehr geändert werden. Adobe legt das erforderliche ID-Präfix fest, das ebenfalls nicht geändert werden kann. |
   | Vorkommnisse (letzte 90 Tage) | Die Metrik „Vorfälle“ zeigt die Anzahl der Treffer an, bei denen eine bestimmte Dimension festgelegt oder beibehalten wurde. Wie viele Treffer hat diese Report Suite in den letzten 90 Tagen erhalten? |
   | Metriken | Wie viele Metriken sind in dieser Report Suite definiert? |
   | Dimensionen | Wie viele Dimensionen sind in dieser Report Suite definiert? |
   | Analytics for Target (A4T) aktiviert | [Standardmäßig ausgeblendet] Ist diese Report Suite für &quot;[ for Target“ ](https://experienceleague.adobe.com/de/docs/target/using/integrate/a4t/a4t)? |
   | Marketing-Kanäle aktiviert | [Standardmäßig ausgeblendet] Ist diese Report Suite für (Marketing[Kanäle) ](https://experienceleague.adobe.com/de/docs/analytics/components/marketing-channels/c-getting-started-mchannel)? |
   | Quell-Connector aktiviert | Ist diese Report Suite für den [Adobe Analytics Source-Connector für Report Suite-Daten](https://experienceleague.adobe.com/de/docs/experience-platform/sources/connectors/adobe-applications/analytics) in Adobe Experience Platform aktiviert? Anders ausgedrückt: Kann diese Report Suite mithilfe des Analytics Source Connectors nach Customer Journey Analytics migriert werden? |
   | Kalendertyp | [Standardmäßig ausgeblendet] Weitere Informationen finden Sie unter [Benutzerdefinierte Kalender](https://experienceleague.adobe.com/de/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/custom-calendar#) |

#### Dimensionen analysieren

Dieser Bildschirm bietet eine detaillierte Ansicht aller für eine bestimmte Report Suite definierten Dimensionen. In dieser Ansicht können Sie die folgenden Fragen beantworten:

* Welche Dimensionen sind für diese Report Suite aktiviert?
* Was sind die zehn häufigsten Dimensionselemente der letzten 90 Tage für diese Dimension?

1. Klicken Sie auf **[!UICONTROL Seite Report Suite auf]** Link „Dimensionen“.

   | Element | Beschreibung |
   | --- | --- |
   | Name | Der Name der Dimension |
   | ID | Die Dimensions-ID. |
   | Typ | Der Typ der Dimension. Zu den möglichen Werten gehören Konversion, Traffic, Navigation, Traffic-Quellen, Kunden, Datum oder produktspezifische Adobe-Dimensionen wie AEM, Zielgruppe, Adobe Campaign, Mobile App usw. |
   | Beschreibung | Nicht alle Dimensionen haben Beschreibungen. |
   | Quell-Connector aktiviert | Ist diese Dimension für den [Adobe Analytics Source-Connector für Report Suite-Daten](https://experienceleague.adobe.com/de/docs/experience-platform/sources/connectors/adobe-applications/analytics) in Adobe Experience Platform aktiviert? Anders ausgedrückt: Kann diese Dimension mithilfe des Analytics Source Connectors zu Customer Journey Analytics migriert werden? |

1. Bestimmen Sie, welche Dimensionen für die Migration zu CJA sinnvoll sind.


#### Metriken analysieren

Dieser Bildschirm bietet eine detaillierte Ansicht aller Metriken, die für eine bestimmte Report Suite definiert sind. In dieser Ansicht können Sie die folgenden Fragen beantworten:

* Welche Metriken sind für diese Report Suite aktiviert?
* Was sind die Top-10-Metriken der letzten 90 Tage?

1. Klicken Sie auf **[!UICONTROL Seite Report Suite auf]** Link „Metriken“.


   | Element | Beschreibung |
   | --- | --- |
   | Name | Der Name der Metrik |
   | ID | Die Metrik-ID. |
   | Typ | Der Typ der Metrik. Zu den möglichen Werten gehören Konversion, Traffic, Navigation, Traffic-Quellen, Kunden, Datum oder produktspezifische Adobe-Dimensionen wie AEM, Zielgruppe, Adobe Campaign, Mobile App usw. |
   | Beschreibung | Nicht alle Dimensionen haben Beschreibungen. |
   | Quell-Connector aktiviert | Ist diese Metrik für den [Adobe Analytics Source Connector für Report Suite-Daten](https://experienceleague.adobe.com/de/docs/experience-platform/sources/connectors/adobe-applications/analytics) in Adobe Experience Platform aktiviert? Anders ausgedrückt: Kann diese Metrik mithilfe des Analytics Source Connectors nach Customer Journey Analytics migriert werden? |

1. Bestimmen Sie, welche Metriken für die Migration zu CJA sinnvoll sind.

### Exportieren in CSV

1. Um die Liste der Report Suites, Dimensionen oder Metriken in eine CSV-Datei zu exportieren, klicken Sie auf **[!UICONTROL In CSV exportieren]**.

1. Die CSV-Datei wird im Ordner „Downloads“ angezeigt.

1. Öffnen und speichern Sie sie mit einer Tabellenkalkulationsanwendung auf Ihrem Gerät.

>[!NOTE]
>
>Ausgefilterte Elemente und Spalten werden nicht in die CSV-Datei exportiert.


### Filtern, Suchen, Sortieren und Navigieren

* Sie können die Tabelle durchsuchen.
* Klicken Sie in der linken Leiste auf das Symbol Filtern , um nach „Typ“ zu filtern. Oder klicken Sie auf **[!UICONTROL Filter ausblenden]**.
* Sie können alle Spalten in aufsteigender/absteigender Reihenfolge sortieren (nur eine Spalte sortiert).
* Sie können auf Elemente im Breadcrumb klicken, um zu einem anderen Bildschirm zu navigieren.

## Benutzerverwaltung {#user-management}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="analytics-inventory-user-management"
>title="Benutzerverwaltung"
>abstract="In diesem Abschnitt wird die Anzahl der Benutzenden in Ihrer Adobe Analytics-Umgebung angezeigt."

<!-- markdownlint-enable MD034 -->

Die Benutzerverwaltung wird in einer späteren Version des Analytics-Inventars verfügbar sein.

## Migrieren von Komponenten

Mithilfe [Komponentenmigration](/help/admin/admin/component-migration/component-migration.md) können Adobe Analytics-Administratoren Analytics-Projekte und die zugehörigen Komponenten nach Customer Journey Analytics migrieren.

Der Migrationsvorgang umfasst:

* Neuerstellung von Adobe Analytics-Projekten in Customer Journey Analytics.

* Zuordnung von Dimensionen und Metriken aus Adobe Analytics-Report Suites zu Dimensionen und Metriken in Customer Journey Analytics-Datenansichten.