---
description: Erfahren Sie, wie Sie Kapazitätsprobleme bei Spitzen während der Berichterstellung mit Reporting Activity Manager diagnostizieren und beheben können.
title: Reporting Activity Manager
feature: Admin Tools
mini-toc-levels: 3
exl-id: f638c6a9-1c2c-4936-a787-281269f95afc
source-git-commit: 815e50e30fa6a0bce1bf78f33843070f96f52de8
workflow-type: tm+mt
source-wordcount: '1935'
ht-degree: 11%

---

# Berichtsaktivität im Reporting Activity Manager anzeigen

Mit dem [!UICONTROL Reporting Activity Manager] können Administratoren während Spitzenzeiten der Berichterstellung schnell Probleme mit der Berichtskapazität diagnostizieren und beheben.

Weitere Informationen zum Reporting-Aktivitäts-Manager, einschließlich der wichtigsten Vorteile und Berechtigungsanforderungen, finden Sie unter [Übersicht über den Reporting-Aktivitäts-Manager](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md).

## Berichtsaktivität für alle Report Suites anzeigen {#view-all-report-suites}

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Berichterstellungsaktivitäts-Manager]**.

   Eine Liste Ihrer aktivierten Basis-Report Suites wird angezeigt.

   ![Berichtswarteschlange](assets/reporting-activity1.png)

1. (Optional) Sie können die Liste der Report Suites durchsuchen oder filtern:

   * Verwenden Sie das Suchfeld, um nach einer bestimmten Report Suite zu suchen. Geben Sie den Namen oder die ID der Report Suite ein und die Liste der Report Suites wird bei der Eingabe aktualisiert.

   * Wählen Sie das Symbol [!UICONTROL **Filter**] ![Filtersymbol](assets/filter-icon.png) aus, um die Liste der Filteroptionen zu erweitern. Sie können nach [!UICONTROL **Favoriten**] oder [!UICONTROL **Status**] filtern.

     Um eine Report Suite als Favoriten zu markieren, wählen Sie das Sternsymbol links neben dem Report Suite-Namen aus.

     <!-- (does this option still exist?) 1. (Optional) Select **[!UICONTROL Refresh]** at the top-right to refresh the data. -->

1. Zeigen Sie Nutzungsinformationen zu den einzelnen Report Suites an. Die in der Tabelle angezeigten Daten stellen die Berichtsaktivität für die Report Suite zum Zeitpunkt des letzten Ladevorgangs der Seite dar.

   Die folgenden Spalten sind verfügbar:

   | UI-Element | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Report Suite]** | Die zugrunde liegende Report Suite, deren Berichtsaktivität von Ihnen überwacht wird. |
   | **[!UICONTROL Virtual Report Suites]** | Zeigt alle Virtual Report Suites an, die in diese zugrunde liegende Report Suite einfließen. Virtual Report Suites ermöglichen eine höhere Komplexität von Berichtsanfragen aufgrund zusätzlich anwendbarer Filter- und Segmentierungsebenen. Alle Anforderungen, die von Virtual Report Suites stammen, werden in der zugrunde liegenden Report Suite kombiniert. |
   | **[!UICONTROL Kapazitätsauslastung]** | Der Prozentsatz der verwendeten Berichtskapazität der Report Suite in Echtzeit. <p>**Hinweis** Eine Nutzungskapazität von 100 % deutet nicht unbedingt darauf hin, dass Sie sofort mit dem Abbrechen von Berichtsanforderungen beginnen sollten. 100 % der Nutzkapazität können gesund sein, wenn die durchschnittliche Wartezeit vernünftig ist. Andererseits könnte die Nutzungskapazität von 100 % auf ein Problem hindeuten, wenn auch die Anzahl der Anforderungen in der Warteschlange wächst.</p> |
   | **[!UICONTROL In Warteschlange gestellte Anforderungen]** | Die Anzahl der zu verarbeitenden Anforderungen. <!-- ??? --> |
   | **[!UICONTROL Wartezeit in der Warteschlange]** | Die durchschnittliche Wartezeit, bevor die Verarbeitung von Anforderungen beginnt. <!-- ???? --> |
   | **[!UICONTROL Status]** | Folgende Status sind möglich: <ul><li>[!UICONTROL **Aktiv**] (blau): Berichte wurden in den letzten 2 Stunden für die Report Suite ausgeführt. Die in der Tabelle angezeigten Daten stellen die Berichtskapazität für die Report Suite zum Zeitpunkt des letzten Ladevorgangs der Seite dar.</li><li>[!UICONTROL **Inaktiv**] (grau): In den letzten 2 Stunden wurden keine Berichte für die Report Suite ausgeführt, sodass keine Daten für die Report Suite angezeigt werden.</li></ul> |

   {style="table-layout:auto"}

## Berichtsaktivität für eine einzelne Report Suite anzeigen

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Reporting Activity Manager**] aus.

1. Wählen Sie den verknüpften Titel der Report Suite aus, für die Sie Details anzeigen möchten.

   Berichtsaktivitätsdaten werden für die von Ihnen ausgewählte Report Suite angezeigt.

   <!-- Need to update this screenshot: ![report suite](assets/indiv-report-ste.png) -->

1. (Optional) Wenn eine Verbindung zum ersten Mal im Reporting Activity Manager geladen wird, stellen die angezeigten Daten die aktuellen Nutzungsmetriken dar. Um nach dem ersten Laden aktualisierte Metriken anzuzeigen, wählen Sie die Schaltfläche [!UICONTROL **Aktualisieren**] aus, um die Seite manuell zu aktualisieren.

1. Verwenden Sie die verfügbaren Diagramme und Tabellen, um die Berichtsaktivität in der Report Suite zu verstehen.

   * [Diagramme anzeigen](#view-graphs)

   * [Tabelle anzeigen](#view-table)

### Diagramme anzeigen

Die folgenden Diagramme helfen Ihnen dabei, die Aktivitäten in der Report Suite besser zu verstehen.

Wenn keine Diagramme sichtbar sind, wählen Sie die Schaltfläche [!UICONTROL **Diagramme anzeigen**] aus.

#### Auslastungsdiagramm {#utilization}

Das Nutzungsdiagramm zeigt die Nutzung der Berichte für die ausgewählte Report Suite in den letzten 2 Stunden.

Bewegen Sie den Mauszeiger über das Diagramm, um Zeitpunkte anzuzeigen, an denen der Prozentsatz der Nutzungskapazität für diese Minute am höchsten war.

* **X-Achse**: Die Berichtsnutzungskapazität über die letzten 2 Stunden.
* **Y-Achse**: Der Prozentsatz der Berichtsnutzungskapazität nach Minuten.

  ![Nutzungsdiagramm](assets/utilization-graph.png)

#### Diagramm &quot;Unique Users&quot;

Das Diagramm Unique Users zeigt die Berichtsaktivität für die ausgewählte Report Suite in den letzten 2 Stunden an.

Bewegen Sie den Mauszeiger über das Diagramm, um die Zeitpunkte anzuzeigen, an denen die maximale Anzahl von Benutzern für diese Minute lag.

* **X-Achse**: Die Berichtsaktivität über den letzten 2-Stunden-Zeitraum.
* **Y-Achse**: Die Anzahl der Benutzer, die Berichterstellungsanforderungen gestellt haben, nach Minuten.

  ![Diagramm &quot;Unique Users&quot;](assets/distinct-users-graph.png)

#### Anforderungsdiagramm

Das Anforderungsdiagramm zeigt die Anzahl der verarbeiteten und in die Warteschlange gestellten Anforderungen für die ausgewählte Report Suite in den letzten 2 Stunden an.

Bewegen Sie den Mauszeiger über das Diagramm, um die Zeitpunkte anzuzeigen, an denen die maximale Anzahl von Anforderungen für diese Minute am höchsten war.

* **X-Achse**: Die Anzahl der verarbeiteten und abgeschlossenen Anforderungen im letzten 2-Stunden-Zeitraum.
* **Y-Achse**: Die Anzahl der verarbeiteten Anforderungen (grün) und Anforderungen in der Warteschlange (violett) nach Minuten.

  ![Diagramm &quot;Unique Users&quot;](assets/requests-graph.png)

#### Einreihungsdiagramm

Das Queuing-Diagramm zeigt die durchschnittliche Wartezeit (in Sekunden) für die Berichterstellungsanfragen für die ausgewählte Report Suite in den letzten 2 Stunden an.

Bewegen Sie den Mauszeiger über das Diagramm, um Zeitpunkte anzuzeigen, an denen die maximale durchschnittliche Wartezeit für diese Minute am höchsten war.

* **X-Achse**: Die durchschnittliche Wartezeit der Warteschlange für Berichterstellungsanfragen über den letzten 2-Stunden-Zeitraum.
* **Y-Achse**: Die durchschnittliche Wartezeit in Sekunden.

  ![Diagramm &quot;Unique Users&quot;](assets/queueing-graph.png)

### Tabelle anzeigen {#view-table}

Beachten Sie beim Anzeigen der Tabelle Folgendes:

* Sie können festlegen, dass Daten angezeigt werden, indem Sie auf eine der folgenden Registerkarten oben in der Datentabelle klicken: [!UICONTROL **Anfrage**], [!UICONTROL **Benutzer**], [!UICONTROL **Projekt**] oder [!UICONTROL **Anwendung**].

* Sie können die Liste der Verbindungen durchsuchen oder filtern:

   * Verwenden Sie das Suchfeld, um nach einer bestimmten Verbindung zu suchen. Beginnen Sie mit der Eingabe des Verbindungsnamens oder der ID und die Liste der Verbindungen wird bei der Eingabe aktualisiert.

   * Wählen Sie das Symbol [!UICONTROL **Filter**] ![Filtersymbol](assets/filter-icon.png) aus, um die Liste der Filteroptionen zu erweitern. Sie können nach [!UICONTROL **Status**], [!UICONTROL **Komplexität**], [!UICONTROL **Anwendung**], [!UICONTROL **Benutzer**] oder [!UICONTROL **Projekt**] filtern.

   * Sie können [!UICONTROL **Diagramme ausblenden**] auswählen, um nur die Tabelle anzuzeigen.

![Tabellenregisterkarten](assets/report-activity-tabs.png)

#### Daten nach Anforderung anzeigen

Wenn Sie die Registerkarte [!UICONTROL **Anforderung**] auswählen, sind die folgenden Spalten in der Tabelle verfügbar:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Anforderungs-ID**] | Eine eindeutige ID, die zur Fehlerbehebung verwendet werden kann. Um die ID zu kopieren, wählen Sie die Anforderung und dann die Option [!UICONTROL **Anforderungs-IDs kopieren**] aus. |
| [!UICONTROL **Zeitablauf**] | Dauer der Ausführung der Anfrage. |
| [!UICONTROL **Startzeit**] | Der Zeitpunkt, zu dem die Anfrage verarbeitet wurde (basierend auf der Ortszeit des Administrators). |
| [!UICONTROL **Wartezeit**] | Wie lange die Anfrage vor der Verarbeitung gewartet hat. Dieser Wert liegt im Allgemeinen bei &quot;0&quot;, wenn ausreichend Kapazität vorhanden ist. |
| [!UICONTROL **Programm**] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Warnhinweise</li><li>Für alle Links freigeben</li><li>Jede andere Anwendung, die die Analytics-Reporting-Engine abfragt</li></ul> |
| [!UICONTROL **Benutzer**] | Der Benutzer, der die Anfrage initiiert hat. <p>**Hinweis:** Wenn der Wert dieser Spalte [!UICONTROL **Unerkannt**] ist, bedeutet dies, dass sich der Benutzer in einem Anmeldeunternehmen befindet, für das Sie keine Administratorberechtigungen haben.</p> |
| [!UICONTROL **Projekt**] | Gespeicherte Workspace-Projektnamen, API-Berichts-IDs usw. (Metadaten können von Programm zu Programm variieren.) |
| [!UICONTROL **Status**] | Statusindikatoren: <ul><li>**Läuft**: Die Anfrage wird derzeit verarbeitet.</li><li>**Ausstehend**: Die Anfrage wartet auf die Verarbeitung.</li></ul> |
| [!UICONTROL **Komplexität**] | Nicht alle Anforderungen benötigen dieselbe Verarbeitungszeit. Die Anforderungskomplexität kann dabei helfen, eine allgemeine Vorstellung davon zu erhalten, wie viel Zeit für die Verarbeitung der Anfrage erforderlich ist. <p>Mögliche Werte:</p> <ul><li>[!UICONTROL **Niedrig**]</li><li>[!UICONTROL **Medium**]</li><li>[!UICONTROL **Hoch**]</li></ul>Dieser Wert wird durch die Werte in den folgenden Spalten beeinflusst:<ul><li>[!UICONTROL **Monatsgrenzen**]</li><li>[!UICONTROL **Spalten**]</li><li>[!UICONTROL **Segmente**]</li></ul> |
| [!UICONTROL **Monatsgrenzen**] | Die Anzahl der Monate, die in einer Anfrage enthalten sind. Mehr Monatsgrenzen erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Spalten**] | Die Anzahl der Metriken und Aufschlüsselungen in der Anforderung. Mehr Spalten erhöhen die Komplexität der Anforderung. |
| [!UICONTROL **Segmente**] | Die Anzahl der Segmente, die auf die Anforderung angewendet werden. Weitere Segmente erhöhen die Komplexität der Anforderung. |

{style="table-layout:auto"}

#### Daten nach Benutzer anzeigen

Wenn Sie die Registerkarte [!UICONTROL **Benutzer**] auswählen, sind die folgenden Spalten in der Tabelle verfügbar:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Benutzer**] | Der Benutzer, der die Anfrage initiiert hat. Wenn der Wert dieser Spalte [!UICONTROL **Nicht erkannt**] ist, bedeutet dies, dass sich der Benutzer in einem Anmeldeunternehmen befindet, für das Sie keine Administratorberechtigungen haben. |
| [!UICONTROL **Anzahl der Anforderungen**] | Die Anzahl der vom Benutzer initiierten Anfragen. |
| [!UICONTROL **Anzahl der Projekte**] | Die Anzahl der mit dem Benutzer verknüpften Projekte. <!-- ??? --> |
| [!UICONTROL **Programm**] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Warnhinweise</li><li>Für alle Links freigeben</li><li>Jede andere Anwendung, die die Analytics-Reporting-Engine abfragt</li></ul> |
| [!UICONTROL **Durchschnittliche Komplexität**] | Die durchschnittliche Komplexität von Anforderungen, die vom Benutzer initiiert wurden. <p>Nicht alle Anforderungen benötigen dieselbe Verarbeitungszeit. Die Anforderungskomplexität kann dabei helfen, eine allgemeine Vorstellung davon zu erhalten, wie viel Zeit für die Verarbeitung der Anfrage erforderlich ist.</p><p>Der Wert in dieser Spalte basiert auf einem Wert, der durch die Werte in den folgenden Spalten bestimmt wird:</p><ul><li>[!UICONTROL **Durchschnittliche Monatsgrenzen**]</li><li>[!UICONTROL **Durchschnittliche Spalten**]</li><li>[!UICONTROL **Durchschnittliche Segmente**]</li></ul> |
| [!UICONTROL **Durchschnittliche Monatsgrenzen**] | Die durchschnittliche Anzahl der Monate, die in den Anforderungen enthalten sind. Mehr Monatsgrenzen erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Spalten**] | Die durchschnittliche Anzahl von Metriken und Aufschlüsselungen in den enthaltenen Anforderungen. Mehr Spalten erhöhen die Komplexität der Anforderung. |
| [!UICONTROL **Durchschnittliche Segmente**] | Die durchschnittliche Anzahl von Segmenten, die auf die enthaltenen Anforderungen angewendet werden. Weitere Segmente erhöhen die Komplexität der Anforderung. |

{style="table-layout:auto"}

#### Daten nach Projekt anzeigen

Wenn Sie die Registerkarte [!UICONTROL **Projekt**] auswählen, sind die folgenden Spalten in der Tabelle verfügbar:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Projekt**] | Das Projekt, bei dem die Anfragen initiiert wurden. |
| [!UICONTROL **Anzahl der Anforderungen**] | Die Anzahl der mit dem Projekt verknüpften Anforderungen. |
| [!UICONTROL **Anzahl der Benutzer**] | Die Anzahl der mit dem Projekt verknüpften Benutzer. <!-- ??? --> |
| [!UICONTROL **Programm**] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Warnhinweise</li><li>Für alle Links freigeben</li><li>Jede andere Anwendung, die die Analytics-Reporting-Engine abfragt</li></ul> |
| [!UICONTROL **Durchschnittliche Komplexität**] | Die durchschnittliche Komplexität der Anforderungen, die im Projekt enthalten sind. <p>Nicht alle Anforderungen benötigen dieselbe Verarbeitungszeit. Die Anforderungskomplexität kann dabei helfen, eine allgemeine Vorstellung davon zu erhalten, wie viel Zeit für die Verarbeitung der Anfrage erforderlich ist.</p><p>Der Wert in dieser Spalte basiert auf einem Wert, der durch die Werte in den folgenden Spalten bestimmt wird:</p><ul><li>[!UICONTROL **Durchschnittliche Monatsgrenzen**]</li><li>[!UICONTROL **Durchschnittliche Spalten**]</li><li>[!UICONTROL **Durchschnittliche Segmente**]</li></ul> |
| [!UICONTROL **Durchschnittliche Monatsgrenzen**] | Die durchschnittliche Anzahl der Monate, die in den Anforderungen enthalten sind. Mehr Monatsgrenzen erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Spalten**] | Die durchschnittliche Anzahl von Metriken und Aufschlüsselungen in den enthaltenen Anforderungen. Mehr Spalten erhöhen die Komplexität der Anforderung. |
| [!UICONTROL **Durchschnittliche Segmente**] | Die durchschnittliche Anzahl von Segmenten, die auf die enthaltenen Anforderungen angewendet werden. Weitere Segmente erhöhen die Komplexität der Anforderung. |

{style="table-layout:auto"}

#### Daten nach Anwendung anzeigen

Wenn Sie die Registerkarte [!UICONTROL **Anwendung**] auswählen, sind die folgenden Spalten in der Tabelle verfügbar:

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL **Programm**] | Die Anwendung, in der die Anfragen initiiert wurden. |
| [!UICONTROL **Anzahl der Anforderungen**] | Die Anzahl der mit der Anwendung verknüpften Anforderungen. |
| [!UICONTROL **Anzahl der Benutzer**] | Die Anzahl der mit der Anwendung verknüpften Benutzer. <!--???--> |
| [!UICONTROL **Anzahl der Projekte**] | Die Anzahl der mit der Anwendung verknüpften Projekte. <!--???--> |
| [!UICONTROL **Durchschnittliche Komplexität**] | Die durchschnittliche Komplexität der mit der Anwendung verknüpften Anforderungen. <p>Nicht alle Anforderungen benötigen dieselbe Verarbeitungszeit. Die Anforderungskomplexität kann dabei helfen, eine allgemeine Vorstellung davon zu erhalten, wie viel Zeit für die Verarbeitung der Anfrage erforderlich ist.</p><p>Der Wert in dieser Spalte basiert auf einem Wert, der durch die Werte in den folgenden Spalten bestimmt wird:</p>Der Wert in dieser Spalte basiert auf einem Wert, der durch die Werte in den folgenden Spalten bestimmt wird:<ul><li>[!UICONTROL **Durchschnittliche Monatsgrenzen**]</li><li>[!UICONTROL **Durchschnittliche Spalten**]</li><li>[!UICONTROL **Durchschnittliche Segmente**]</li></ul> |
| [!UICONTROL **Durchschnittliche Monatsgrenzen**] | Die durchschnittliche Anzahl der Monate, die in den Anforderungen enthalten sind. Mehr Monatsgrenzen erhöhen die Komplexität der Anfrage. |
| [!UICONTROL **Durchschnittliche Spalten**] | Die durchschnittliche Anzahl von Metriken und Aufschlüsselungen in den enthaltenen Anforderungen. Mehr Spalten erhöhen die Komplexität der Anforderung. |
| [!UICONTROL **Durchschnittliche Segmente**] | Die durchschnittliche Anzahl von Segmenten, die auf die enthaltenen Anforderungen angewendet werden. Weitere Segmente erhöhen die Komplexität der Anforderung. |

{style="table-layout:auto"}

<!--

## Frequently asked questions {#faq}

| Question | Answer |
| --- | --- |
|  |  |

{style="table-layout:auto"}

-->