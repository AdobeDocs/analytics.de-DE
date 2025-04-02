---
description: Erfahren Sie, wie Sie mit dem Reporting Activity Manager Kapazitätsprobleme bei Spitzen während der Berichterstellung diagnostizieren und beheben können.
title: Abbrechen von Berichtsanfragen im Reporting Activity Manager
feature: Admin Tools
exl-id: 37a2fa8f-7804-4220-a508-ec66996b3801
role: Admin
source-git-commit: 815e50e30fa6a0bce1bf78f33843070f96f52de8
workflow-type: ht
source-wordcount: '1438'
ht-degree: 100%

---

# Abbrechen von Berichtsanfragen im Reporting Activity Manager

Der [!UICONTROL Reporting Activity Manager] ermöglicht Admins das schnelle Diagnostizieren und Abbrechen von Berichtsanfragen, um Probleme mit der Berichtskapazität während Spitzenzeiten des Reportings zu beheben.

Beachten Sie beim Abbrechen von Berichtsanfragen Folgendes:

* Sie können bestimmte Anfragen abbrechen, alle Anfragen einer bestimmten Person abbrechen oder alle Anfragen im Zusammenhang mit einem bestimmten Projekt abbrechen.

  Wenn Sie eine Anfrage abbrechen, wird die Aktion in den [Protokollen](/help/admin/admin/logs.md) dokumentiert. Die Spalte [!UICONTROL **Ereignistyp**] wird als [!UICONTROL **Admin-Aktion**] angezeigt, und eine Beschreibung des Abbruchs ist in der Spalte [!UICONTROL **Ereignis**] verfügbar.

* Wenn Sie Anfragen abbrechen, können Sie auch nachfolgende Anfragen für einen bestimmten Zeitraum einschränken.

  Wenn Sie eine nachfolgende Anfrage einschränken, wird diese Aktion in den [Protokollen](/help/admin/admin/logs.md) dokumentiert. Die Spalte [!UICONTROL **Ereignistyp**] wird als [!UICONTROL **Admin-Aktion**] angezeigt, und eine Beschreibung der Einschränkung ist in der Spalte [!UICONTROL **Ereignis**] verfügbar.

* Sie können eine Anfrage nicht abbrechen, wenn die Spalte [!UICONTROL **Benutzer**] einer Anfrage als [!UICONTROL **Nicht erkannt**] angezeigt wird. In diesem Fall bedeutet dies, dass sich die Person in einer Unternehmensanmeldung befindet, für die Sie keine Admin-Berechtigungen haben.

Weitere Informationen zum Reporting Activity Manager, einschließlich der wichtigsten Vorteile und Berechtigungsanforderungen, finden Sie unter [Überblick über den Reporting Activity Manager](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md).

## Abbrechen von bestimmten Anfragen

Sie können einzelne Anfragen abbrechen, die eine große Menge an Berichtskapazität beanspruchen.

1. Navigieren Sie dazu in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie die Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Anzeigen der Berichtsaktivität im Reporting Activity Manager](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die Registerkarte [!UICONTROL **Anfragen**] dann eine oder mehrere Anfragen aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anfragen abbrechen**].

   Das Dialogfeld [!UICONTROL **Berichtsanfragen abbrechen _x_**] wird angezeigt.

1. Das Nachrichtenfeld „Abbruch“ zeigt die Meldung an, die Benutzenden angezeigt wird, wenn ihre Anfragen abgebrochen werden. Es wird eine Standardmeldung bereitgestellt. Sie können die Standardmeldung aktualisieren, um weitere Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anfragen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option [!UICONTROL **Nachfolgende Anfragen einschränken**].

      ![Nachfolgende Anfragen einschränken](assets/restrict-subsequent-requests.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzende und Projekte**] | Benutzende, die mit den ausgewählten Anfragen verknüpft sind, werden vorübergehend von der Ausführung von Berichtsanfragen für die ausgewählten Projekte ausgeschlossen. |
      | [!UICONTROL **Benutzende**] | Benutzende, die mit den ausgewählten Anträgen verknüpft sind, können vorübergehend keine weiteren Reporting-Anfragen stellen. |
      | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Anfragen verknüpft sind, werden vorübergehend von allen Reporting-Anfragen ausgeschlossen. |
      | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt werden sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!-- double-check this --><p>Nachdem eine Einschränkung festgelegt wurde, können Sie sie nicht sofort wieder entfernen.</p> |

      {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Mit Abbruch fortfahren**].

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die Benutzende darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie diese in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis, wenn Benutzende auf einen abgebrochenen Bericht zugreifen](#experience-when-users-access-a-cancelled-report).

## Abbrechen von Anfragen nach Benutzerin bzw. Benutzer einschränken

Sie können alle Anfragen abbrechen, die mit einer Benutzerin bzw. einem Benutzer oder mehreren Benutzenden verknüpft sind.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie die Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Anzeigen der Berichtsaktivität im Reporting Activity Manager](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die Registerkarte [!UICONTROL **Benutzende**] und dann eine oder mehrere Personen aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anfragen abbrechen**].

   Das Dialogfeld [!UICONTROL **Berichtsanfragen abbrechen _x_**] wird angezeigt.

1. Das Nachrichtenfeld „Abbruch“ zeigt die Meldung an, die Benutzenden angezeigt wird, wenn ihre Anfragen abgebrochen werden. Es wird eine Standardmeldung bereitgestellt. Sie können die Standardmeldung aktualisieren, um weitere Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anfragen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option [!UICONTROL **Nachfolgende Anfragen einschränken**].

      ![Nachfolgende Anfragen nach Benutzenden einschränken](assets/restrict-subsequent-requests-user.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzende und Projekte**] | Ausgewählte Benutzende können vorübergehend keine Berichtsanfragen für die verknüpften Projekte stellen. |
      | [!UICONTROL **Benutzende**] | Ausgewählte Benutzende können vorübergehend keine Berichtsanfragen stellen. |
      | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Benutzenden verbunden sind, werden von allen Berichtsanfragen ausgeschlossen, die von anderen Benutzenden gestellt werden. |
      | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt werden sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Nachdem eine Einschränkung festgelegt wurde, können Sie sie nicht sofort wieder entfernen.</p> |

      {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Mit Abbruch fortfahren**].

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die Benutzende darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie diese in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis, wenn Benutzende auf einen abgebrochenen Bericht zugreifen](#experience-when-users-access-a-cancelled-report).

## Abbrechen von Anfragen nach Projekt

Sie können alle Anfragen abbrechen, die mit einem oder mehreren Projekten verknüpft sind.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie die Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Anzeigen der Berichtsaktivität im Reporting Activity Manager](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die Registerkarte [!UICONTROL **Projekte**] und dann ein oder mehrere Projekte aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anfragen abbrechen**].

   Das Dialogfeld [!UICONTROL **Berichtsanfragen von x Projekten abbrechen _x_**] wird angezeigt.

1. Das Nachrichtenfeld „Abbruch“ zeigt die Meldung an, die Benutzenden angezeigt wird, wenn ihre Anfragen abgebrochen werden. Es wird eine Standardmeldung bereitgestellt. Sie können die Standardmeldung aktualisieren, um weitere Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anfragen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option [!UICONTROL **Nachfolgende Anfragen einschränken**].

      ![Nachfolgende Anfragen nach Projekt einschränken](assets/restrict-subsequent-requests-project.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzende und Projekt**] | Die ausgewählten Projekte werden vorübergehend von allen Berichtsanfragen der verknüpften Benutzenden ausgeschlossen. |
      | [!UICONTROL **Benutzende**] | Benutzende, die mit den ausgewählten Projekten verknüpft sind, können vorübergehend keine weiteren Berichtsanfragen stellen. |
      | [!UICONTROL **Projekt**] | Ausgewählte Projekte werden vorübergehend von jeder Berichtsanfrage durch beliebige Benutzende ausgeschlossen. |
      | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt werden sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Nachdem eine Einschränkung festgelegt wurde, können Sie sie nicht sofort wieder entfernen.</p> |

      {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Mit Abbruch fortfahren**].

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die Benutzende darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie diese in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis, wenn Benutzende auf einen abgebrochenen Bericht zugreifen](#experience-when-users-access-a-cancelled-report).

## Abbrechen von Anfragen nach Anwendung

Sie können alle Anfragen abbrechen, die mit einer oder mehrerer Anwendungen verknüpft sind. Wenn Sie Anfragen abbrechen, die mit einer Anwendung verknüpft sind, können Sie nachfolgende Anfragen, die mit dieser Anwendung verknüpft sind, für einen bestimmten Zeitraum weiter einschränken.

Zu den Anwendungen zählen Folgende:

* Analysis Workspace-Benutzeroberfläche
* Geplante Projekte im Workspace
* Report Builder
* Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.
* API-Aufrufe aus der API 1.4 oder 2.0
* Warnhinweise
* Links „Für alle freigeben“
* Jede andere Anwendung, die die Analytics-Reporting-Engine abfragt

So brechen Sie Anfragen nach Anwendung ab:

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Verbindung aus, in der Sie die Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Anzeigen der Berichtsaktivität im Reporting Activity Manager](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die Registerkarte [!UICONTROL **Anwendungen**] und dann ein oder mehrere Anwendungen aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anfragen abbrechen**].

   Das Dialogfeld [!UICONTROL **Berichtsanfragen von x Projekten abbrechen _x_**] wird angezeigt.

1. Das Nachrichtenfeld „Abbruch“ zeigt die Meldung an, die Benutzenden angezeigt wird, wenn ihre Anfragen abgebrochen werden. Es wird eine Standardmeldung bereitgestellt. Sie können die Standardmeldung aktualisieren, um weitere Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anfragen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option [!UICONTROL **Nachfolgende Anfragen einschränken**].

      ![Nachfolgende Anfragen nach Anwendung einschränken](assets/restrict-subsequent-requests-application.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzende und Projekt**] | Ausgewählte Anwendungen werden vorübergehend von allen Berichtsanfragen der verknüpften Benutzenden und Projekte ausgeschlossen.<p>Dies ist die am wenigsten einschränkende Option.</p> |
      | [!UICONTROL **Benutzende**] | Benutzende, die mit den ausgewählten Anwendungen verknüpft sind, können vorübergehend keine weiteren Berichtsanfragen stellen. |
      | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Anwendungen verbunden sind, werden von allen Berichtsanfragen ausgeschlossen, die von anderen Benutzenden gestellt werden. |
      | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt werden sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Nachdem eine Einschränkung festgelegt wurde, können Sie sie nicht sofort wieder entfernen.</p> |

      {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Mit Abbruch fortfahren**].

   In der Anwendung wird eine Benachrichtigung angezeigt (wie in Analysis Workspace), die Benutzende darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie diese in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis, wenn Benutzende auf einen abgebrochenen Bericht zugreifen](#experience-when-users-access-a-cancelled-report).

## Erlebnis, wenn Benutzende auf einen abgebrochenen Bericht zugreifen

In Analysis Workspace sehen Benutzerinnen und Benutzer die folgenden Meldungen, wenn sie versuchen, auf einen Bericht oder eine Visualisierung zuzugreifen, der bzw. die von einem Abbruch betroffen ist:

### Meldung zum Projekt

Wenn Benutzende versuchen, auf ein Projekt zuzugreifen, das von einem Abbruch betroffen ist, wird eine Meldung angezeigt, die sie darüber informiert, dass der Bericht vorübergehend eingeschränkt ist:

![Meldung zum Projektabbruch](assets/workspace-canceled-report.png)

### Meldung zur Visualisierung

Wenn Benutzende versuchen, auf eine Visualisierung zuzugreifen, die von einem Abbruch betroffen ist, wird eine Meldung angezeigt, die sie darüber informiert, dass die Datenverarbeitung für den Bericht vorübergehend eingeschränkt ist:

![Meldung zum Abbruch der Visualisierung](assets/workspace-cancelled-visualization.png)
