---
description: Erfahren Sie, wie Sie mit dem Reporting Activity Manager Kapazitätsprobleme bei Spitzen während der Berichterstellung diagnostizieren und beheben können.
title: Reporting Activity Manager
feature: Admin Tools
mini-toc-levels: 3
exl-id: f638c6a9-1c2c-4936-a787-281269f95afc
source-git-commit: e09234ca27fbf923e026aa1f2ed0ebfed636bf7c
workflow-type: tm+mt
source-wordcount: '1989'
ht-degree: 100%

---

# Anzeigen der Berichtsaktivität im Reporting Activity Manager

Der [!UICONTROL Reporting Activity Manager] ermöglicht Admins das schnelle Diagnostizieren und Beheben von Problemen mit der Berichtskapazität während Spitzenzeiten des Reportings.

Weitere Informationen zum Reporting Activity Manager, einschließlich der wichtigsten Vorteile und Berechtigungsanforderungen, finden Sie unter [Überblick über den Reporting Activity Manager](/help/admin/tools/reporting-activity-manager/reporting-activity-overview.md).

## Anzeigen der Berichtsaktivität für alle Report Suites {#view-all-report-suites}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_tools_reportingactivitymanager_connections"
>title="Verbindungen"
>abstract="Diese Tabelle zeigt die Verbindungen, für die Sie zur Verwaltung der Reporting-Aktivität berechtigt sind. Informationen zu den einzelnen Verbindungen finden Sie in den jeweiligen Spalten der Tabelle."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="tools_reportingactivitymanager_connections"
>title="Verbindungen"
>abstract="Diese Tabelle zeigt die Verbindungen, für die Sie zur Verwaltung der Reporting-Aktivität berechtigt sind. Informationen zu den einzelnen Verbindungen finden Sie in den jeweiligen Spalten der Tabelle."

<!-- markdownlint-enable MD034 -->

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

   Es wird eine Liste Ihrer aktivierten, zugrunde liegenden Report Suites angezeigt.

   ![Berichtswarteschlange](assets/reporting-activity1.png)

1. (Optional) Sie können die Liste der Report Suites durchsuchen oder filtern:

   * Wenn Sie nach einer bestimmten Report Suite suchen möchten, verwenden Sie das Suchfeld. Beginnen Sie mit der Eingabe des Namens oder der ID der Report Suite. Die Liste der Report Suites wird während der Eingabe aktualisiert.

   * Wählen Sie das [!UICONTROL **Filter**]-Symbol ![Filtersymbol](assets/filter-icon.png) aus, um die Liste der Filteroptionen zu erweitern. Sie können nach [!UICONTROL **Favoriten**] oder [!UICONTROL **Status**] filtern.

     Um eine Report Suite als Favoriten zu markieren, wählen Sie das Sternsymbol links neben dem Namen der Report Suite aus.

     <!-- (does this option still exist?) 1. (Optional) Select **[!UICONTROL Refresh]** at the top-right to refresh the data. -->

1. Anzeigen von Nutzungsinformationen zu jeder Report Suite. Die in der Tabelle angezeigten Daten stellen die Berichtsaktivität für die Report Suite zum Zeitpunkt des letzten Seitenladevorgangs dar.

   Die folgenden Spalten sind verfügbar:

   | UI-Element | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Report Suite]** | Die zugrunde liegende Report Suite, deren Berichtsaktivität von Ihnen überwacht wird. |
   | **[!UICONTROL Virtual Report Suites]** | Zeigt alle Virtual Report Suites an, die in diese zugrunde liegende Report Suite einfließen. Virtual Report Suites ermöglichen eine höhere Komplexität von Berichtsanfragen aufgrund zusätzlich anwendbarer Filter- und Segmentierungsebenen. Alle Anfragen, die von Virtual Report Suites stammen, werden kombiniert und gelangen zur zugrunde liegenden Report Suite. |
   | **[!UICONTROL Kapazitätsauslastung]** | Der prozentuale Anteil, wie viel der Berichterstellungskapazität der Report Suite in Echtzeit verwendet wird. <p>**Hinweis** Bei einer Nutzungskapazität von 100 % sollten Sie nicht unbedingt sofort mit dem Abbrechen von Berichtsanfragen beginnen. Eine Nutzungskapazität von 100 % kann in Ordnung sein, wenn die durchschnittliche Wartezeit angemessen bleibt. Andererseits könnte eine Nutzungskapazität von 100 % ein Problem darstellen, wenn auch die Anzahl der Anfragen in der Warteschlange zunimmt.</p> |
   | **[!UICONTROL Anfragen in der Warteschlange]** | Die Anzahl der Anfragen, die auf die Verarbeitung warten. <!-- ??? --> |
   | **[!UICONTROL Wartezeit in der Warteschlange]** | Die durchschnittliche Wartezeit, bevor die Verarbeitung von Anfragen beginnt. <!-- ???? --> |
   | **[!UICONTROL Status]** | Die verschiedenen Status sind: <ul><li>[!UICONTROL **Aktiv**] (blau): In den letzten 2 Stunden wurden Berichte für die Report Suite ausgeführt. Die in der Tabelle angezeigten Daten stellen die Berichtskapazität für die Report Suite zum Zeitpunkt des letzten Seitenladevorgangs dar.</li><li>[!UICONTROL **Inaktiv**] (grau): In den letzten 2 Stunden wurden keine Berichte zur Report Suite ausgeführt, sodass keine Daten für die Report Suite angezeigt werden.</li></ul> |

   {style="table-layout:auto"}

## Anzeigen der Berichtsaktivität für eine einzelne Report Suite

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Reporting Activity Manager**] aus.

1. Klicken Sie auf den verknüpften Titel einer Report Suite, für die Sie Details anzeigen möchten.

   Daten zur Berichtsaktivität werden für die von Ihnen ausgewählte Report Suite angezeigt.

   <!-- Need to update this screenshot: ![report suite](assets/indiv-report-ste.png) -->

1. (Optional) Beim ersten Laden einer Verbindung im Reporting für Activity Manager entsprechen die angezeigten Daten den aktuellen Nutzungsmetriken. Um aktualisierte Metriken nach dem ersten Laden anzuzeigen, wählen Sie die Schaltfläche [!UICONTROL **Aktualisieren**] aus, um die Seite manuell zu aktualisieren.

1. Verwenden Sie die verfügbaren Diagramme und Tabellen, um die Berichtsaktivität in der Report Suite nachzuvollziehen.

   * [Anzeigen von Diagrammen](#view-graphs)

   * [Anzeigen von Tabellen](#view-table)

### Anzeigen von Diagrammen

Die folgenden Diagramme helfen Ihnen, die Aktivitäten in der Report Suite besser nachzuvollziehen.

Wenn keine Diagramme sichtbar sind, wählen Sie die Schaltfläche [!UICONTROL **Diagramme anzeigen**] aus.

#### Diagramm „Nutzung“ {#utilization}

Das Diagramm „Nutzung“ zeigt die Berichtsnutzung für die ausgewählte Report Suite in den letzten zwei Stunden an.

Bewegen Sie den Mauszeiger über das Diagramm, um die Zeitpunkte anzuzeigen, an denen der Prozentsatz der Nutzungskapazität für diese Minute am höchsten war.

* **X-Achse**: Die Berichtsnutzungskapazität in den letzten zwei Stunden.
* **Y-Achse**: Der Prozentsatz der Berichtsnutzungskapazität in Minuten.

  ![Diagramm Nutzung](assets/utilization-graph.png)

#### Diagramm „Unterschiedliche Benutzende“

Das Diagramm „Unterschiedliche Benutzende“ zeigt die Berichtsaktivität für die ausgewählte Report Suite in den letzten zwei Stunden an.

Bewegen Sie den Mauszeiger über das Diagramm, um die Zeitpunkte anzuzeigen, an denen die maximale Anzahl von Benutzenden für diese Minute am höchsten war.

* **X-Achse**: Die Berichtsaktivität in den letzten zwei Stunden.
* **Y-Achse**: Die Anzahl der Benutzenden, die Berichtsanfragen gestellt haben, für jede Minute.

  ![Diagramm Anfragen](assets/distinct-users-graph.png)

#### Diagramm „Anfragen“

Das Diagramm „Anfragen“ zeigt die Anzahl der in den letzten zwei Stunden verarbeiteten und in die Warteschlange gestellten Anfragen für die ausgewählte Report Suite an.

Bewegen Sie den Mauszeiger über das Diagramm, um die Zeitpunkte anzuzeigen, an denen die maximale Anzahl von Anfragen für diese Minute am höchsten war.

* **X-Achse**: Die Anzahl der verarbeiteten und abgeschlossenen Anfragen in den letzten zwei Stunden.
* **Y-Achse**: Die Anzahl der verarbeiteten Anfragen (grün) und der in die Warteschlange gestellten Anfragen (violett) für jede Minute.

  ![Diagramm Unterschiedliche Benutzende](assets/requests-graph.png)

#### Diagramm „In Warteschlange“

Das Diagramm „In Warteschlange“ zeigt die durchschnittliche Warteschlangenwartezeit (in Sekunden) für Berichtsanfragen für die ausgewählte Report Suite in den letzten zwei Stunden an.

Bewegen Sie den Mauszeiger über das Diagramm, um die Zeitpunkte anzuzeigen, an denen die maximale durchschnittliche Wartezeit für diese Minute am höchsten war.

* **X-Achse**: Die durchschnittliche Warteschlangenwartezeit für Berichtsanfragen in den letzten zwei Stunden.
* **Y-Achse**: Die durchschnittliche Wartezeit (in Sekunden).

  ![Diagramm Unterschiedliche Benutzende](assets/queueing-graph.png)

### Anzeigen von Tabellen {#view-table}

Berücksichtigen Sie beim Anzeigen einer Tabelle Folgendes:

* Sie können Daten anzeigen, indem Sie oben in der Datentabelle eine der folgenden Registerkarten auswählen: [!UICONTROL **Anfrage**], [!UICONTROL **Benutzer**], [!UICONTROL **Projekt**] oder [!UICONTROL **Anwendung**].

* Sie können die Liste der Verbindungen durchsuchen oder filtern:

   * Wenn Sie nach einer bestimmten Verbindung suchen möchten, verwenden Sie das Suchfeld. Beginnen Sie mit der Eingabe des Namens oder der ID der Verbindung. Die Liste der Verbindungen wird während der Eingabe aktualisiert.

   * Wählen Sie das [!UICONTROL **Filter**]-Symbol ![Filtersymbol](assets/filter-icon.png) aus, um die Liste der Filteroptionen zu erweitern. Sie können nach [!UICONTROL **Status**], [!UICONTROL **Komplexität**], [!UICONTROL **Anwendung**], [!UICONTROL **Benutzer**] oder [!UICONTROL **Projekt**] filtern.

   * Sie können [!UICONTROL **Diagramme ausblenden**] auswählen, um nur die Tabelle anzuzeigen.

![Tabellenregisterkarten](assets/report-activity-tabs.png)

#### Anzeigen von Daten nach Anfrage

Wenn Sie die Registerkarte [!UICONTROL **Anfrage**] auswählen, sind in der Tabelle die folgenden Spalten verfügbar:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Anfrage-ID**] | Eine eindeutige ID, die zur Fehlerbehebung verwendet werden kann. Um die ID zu kopieren, wählen Sie die Anfrage und dann die Option [!UICONTROL **Anfrage-IDs kopieren**] aus. |
| [!UICONTROL **Ausführungszeit**] | Die Dauer der Anfrage. |
| [!UICONTROL **Startzeit**] | Der Zeitpunkt, zu dem die Verarbeitung der Anfrage begonnen hat (Administrator-Ortzeit). |
| [!UICONTROL **Wartezeit**] | Die Wartezeit für die Anfrage bis zu ihrer Verarbeitung. Dieser Wert liegt im Allgemeinen bei „0“, wenn genügend Kapazität vorhanden ist. |
| [!UICONTROL **Programm**] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Zielgruppen usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Warnhinweise</li><li>Links „Für alle freigeben“</li><li>Jede andere Anwendung, die die Analytics-Reporting-Engine abfragt</li></ul> |
| [!UICONTROL **Benutzer**] | Die Person, die die Anfrage initiiert hat. <p>**Hinweis:** Wenn der Wert dieser Spalte [!UICONTROL **Nicht erkannt**] lautet, bedeutet dies, dass sich die Benutzerin bzw. der Benutzer in einer Unternehmensanmeldung befindet, für die Sie keine Admin-Berechtigungen haben.</p> |
| [!UICONTROL **Projekt**] | Gespeicherte Workspace-Projektnamen, API-Berichts-IDs usw. (Metadaten können von Programm zu Programm variieren.) |
| [!UICONTROL **Status**] | Statusindikatoren: <ul><li>**Läuft**: Die Anfrage wird derzeit verarbeitet.</li><li>**Ausstehend**: Die Anfrage wartet auf die Verarbeitung.</li></ul> |
| [!UICONTROL **Komplexität**] | Nicht alle Anträge benötigen gleich viel Zeit zur Bearbeitung. Die Komplexität der Anfrage kann eine allgemeine Vorstellung davon vermitteln, wie viel Zeit für die Bearbeitung der Anfrage benötigt wird. <p>Mögliche Werte sind:</p> <ul><li>[!UICONTROL **Niedrig**]</li><li>[!UICONTROL **Mittel**]</li><li>[!UICONTROL **Hoch**]</li></ul>Dieser Wert wird durch die Werte in den folgenden Spalten beeinflusst:<ul><li>[!UICONTROL **Monatsgrenzen**]</li><li>[!UICONTROL **Spalten**]</li><li>[!UICONTROL **Segmente**]</li></ul> |
| [!UICONTROL **Monatsgrenzen**] | Die Anzahl der Monate, die in einer Anfrage eingeschlossen sind. Erweiterte Monatsgrenzen erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Spalten**] | Die Anzahl der Metriken und Aufschlüsselungen in der Anfrage. Mehr Spalten erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Segmente**] | Die Anzahl der auf die Anfrage angewendeten Segmente. Mehr Segmente erhöhen die Komplexität der Anfrage. |

{style="table-layout:auto"}

#### Anzeigen von Daten nach Benutzenden

Wenn Sie die Registerkarte [!UICONTROL **Benutzer**] auswählen, sind die folgenden Spalten in der Tabelle verfügbar:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Benutzende**] | Die Person, die die Anfrage initiiert hat. Wenn der Wert dieser Spalte [!UICONTROL **Nicht erkannt**] lautet, bedeutet dies, dass sich die Benutzerin bzw. der Benutzer in einer Unternehmensanmeldung befindet, für die Sie keine Admin-Berechtigungen haben. |
| [!UICONTROL **Anzahl der Anfragen**] | Die Anzahl der benutzerseitig initiierten Anfragen. |
| [!UICONTROL **Anzahl der Projekte**] | Die Anzahl der mit einer Person verknüpften Projekte. <!-- ??? --> |
| [!UICONTROL **Programm**] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Zielgruppen usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Warnhinweise</li><li>Links „Für alle freigeben“</li><li>Jede andere Anwendung, die die Analytics-Reporting-Engine abfragt</li></ul> |
| [!UICONTROL **Durchschnittliche Komplexität**] | Die durchschnittliche Komplexität der benutzerseitig initiierten Anfragen. <p>Nicht alle Anträge benötigen gleich viel Zeit zur Bearbeitung. Die Komplexität der Anfrage kann eine allgemeine Vorstellung davon vermitteln, wie viel Zeit für die Bearbeitung der Anfrage benötigt wird.</p><p>Der Wert in dieser Spalte basiert auf einem Score, der durch die Werte in den folgenden Spalten bestimmt wird:</p><ul><li>[!UICONTROL **Durchschnittliche Monatsgrenzen**]</li><li>[!UICONTROL **Durchschnittliche Spalten**]</li><li>[!UICONTROL **Durchschnittliche Segmente**]</li></ul> |
| [!UICONTROL **Durchschnittliche Monatsgrenzen**] | Die durchschnittliche Anzahl der in den Anfragen eingeschlossenen Monate. Erweiterte Monatsgrenzen erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Spalten**] | Die durchschnittliche Anzahl der Metriken und Aufschlüsselungen in den eingeschlossenen Anfragen. Mehr Spalten erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Segmente**] | Die durchschnittliche Anzahl der auf die eingeschlossenen Anfragen angewendeten Segmente. Mehr Segmente erhöhen die Komplexität der Anfrage. |

{style="table-layout:auto"}

#### Anzeigen von Daten nach Projekt

Wenn Sie die Registerkarte [!UICONTROL **Projekt**] auswählen, sind die folgenden Spalten in der Tabelle verfügbar:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Projekt**] | Das Projekt, in dem die Anfragen initiiert wurden. |
| [!UICONTROL **Anzahl der Anfragen**] | Die Anzahl der mit dem Projekt verknüpften Anfragen. |
| [!UICONTROL **Anzahl der Benutzenden**] | Die Anzahl der mit dem Projekt verknüpften Benutzenden. <!-- ??? --> |
| [!UICONTROL **Programm**] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Zielgruppen usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Warnhinweise</li><li>Links „Für alle freigeben“</li><li>Jede andere Anwendung, die die Analytics-Reporting-Engine abfragt</li></ul> |
| [!UICONTROL **Durchschnittliche Komplexität**] | Die durchschnittliche Komplexität der im Projekt eingeschlossenen Anfragen. <p>Nicht alle Anträge benötigen gleich viel Zeit zur Bearbeitung. Die Komplexität der Anfrage kann eine allgemeine Vorstellung davon vermitteln, wie viel Zeit für die Bearbeitung der Anfrage benötigt wird.</p><p>Der Wert in dieser Spalte basiert auf einem Score, der durch die Werte in den folgenden Spalten bestimmt wird:</p><ul><li>[!UICONTROL **Durchschnittliche Monatsgrenzen**]</li><li>[!UICONTROL **Durchschnittliche Spalten**]</li><li>[!UICONTROL **Durchschnittliche Segmente**]</li></ul> |
| [!UICONTROL **Durchschnittliche Monatsgrenzen**] | Die durchschnittliche Anzahl der in den Anfragen eingeschlossenen Monate. Erweiterte Monatsgrenzen erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Spalten**] | Die durchschnittliche Anzahl der Metriken und Aufschlüsselungen in den eingeschlossenen Anfragen. Mehr Spalten erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Segmente**] | Die durchschnittliche Anzahl der auf die eingeschlossenen Anfragen angewendeten Segmente. Mehr Segmente erhöhen die Komplexität der Anfrage. |

{style="table-layout:auto"}

#### Anzeigen von Daten nach Anwendung

Wenn Sie die Registerkarte [!UICONTROL **Anwendung**] auswählen, sind die folgenden Spalten in der Tabelle verfügbar:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Programm**] | Die Anwendung, in der die Anfragen initiiert wurden. |
| [!UICONTROL **Anzahl der Anfragen**] | Die Anzahl der mit der Anwendung verknüpften Anfragen. |
| [!UICONTROL **Anzahl der Benutzenden**] | Die Anzahl der mit der Anwendung verknüpften Benutzenden. <!--???--> |
| [!UICONTROL **Anzahl der Projekte**] | Die Anzahl der mit der Anwendung verknüpften Projekte. <!--???--> |
| [!UICONTROL **Durchschnittliche Komplexität**] | Die durchschnittliche Komplexität der mit der Anwendung verknüpften Anfragen. <p>Nicht alle Anträge benötigen gleich viel Zeit zur Bearbeitung. Die Komplexität der Anfrage kann eine allgemeine Vorstellung davon vermitteln, wie viel Zeit für die Bearbeitung der Anfrage benötigt wird.</p><p>Der Wert in dieser Spalte basiert auf einem Score, der durch die Werte in den folgenden Spalten bestimmt wird:</p>Der Wert in dieser Spalte basiert auf einem Score, der durch die Werte in den folgenden Spalten bestimmt wird:<ul><li>[!UICONTROL **Durchschnittliche Monatsgrenzen**]</li><li>[!UICONTROL **Durchschnittliche Spalten**]</li><li>[!UICONTROL **Durchschnittliche Segmente**]</li></ul> |
| [!UICONTROL **Durchschnittliche Monatsgrenzen**] | Die durchschnittliche Anzahl der in den Anfragen eingeschlossenen Monate. Erweiterte Monatsgrenzen erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Spalten**] | Die durchschnittliche Anzahl der Metriken und Aufschlüsselungen in den eingeschlossenen Anfragen. Mehr Spalten erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Segmente**] | Die durchschnittliche Anzahl der auf die eingeschlossenen Anfragen angewendeten Segmente. Mehr Segmente erhöhen die Komplexität der Anfrage. |

{style="table-layout:auto"}

<!--

## Frequently asked questions {#faq}

| Question | Answer |
| --- | --- |
|  |  |

{style="table-layout:auto"}

-->