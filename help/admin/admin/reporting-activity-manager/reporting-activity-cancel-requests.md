---
description: Erfahren Sie, wie Sie Kapazitätsprobleme bei Spitzen während der Berichterstellung mit Reporting Activity Manager diagnostizieren und beheben können.
title: Abbrechen von Berichtsanforderungen im Reporting Activity Manager
feature: Admin Tools
exl-id: 37a2fa8f-7804-4220-a508-ec66996b3801
role: Admin
source-git-commit: 815e50e30fa6a0bce1bf78f33843070f96f52de8
workflow-type: tm+mt
source-wordcount: '1438'
ht-degree: 13%

---

# Abbrechen von Berichtsanforderungen im Reporting Activity Manager

Mit dem [!UICONTROL Reporting Activity Manager] können Administratoren Reporting-Anforderungen schnell diagnostizieren und abbrechen, um Probleme mit der Berichtskapazität während Spitzenzeiten der Berichterstellung zu beheben.

Beachten Sie beim Abbrechen von Berichtsanforderungen Folgendes:

* Sie können bestimmte Anforderungen abbrechen, alle Anforderungen eines bestimmten Benutzers abbrechen oder alle Anforderungen im Zusammenhang mit einem bestimmten Projekt abbrechen.

  Wenn Sie eine Anforderung abbrechen, wird die Aktion in den [Protokollen](/help/admin/admin/logs.md) aufgezeichnet. Die Spalte [!UICONTROL **Ereignistyp**] wird als [!UICONTROL **Admin-Aktion**] angezeigt, und eine Beschreibung der Absage ist in der Spalte [!UICONTROL **Ereignis**] verfügbar.

* Wenn Sie Anforderungen abbrechen, können Sie auch nachfolgende Anforderungen für einen bestimmten Zeitraum einschränken.

  Wenn Sie eine nachfolgende Anforderung einschränken, wird die Aktion in den [Protokollen](/help/admin/admin/logs.md) aufgezeichnet. Die Spalte [!UICONTROL **Ereignistyp**] wird als [!UICONTROL **Admin-Aktion**] und eine Beschreibung der Beschränkung ist in der Spalte [!UICONTROL **Ereignis**] verfügbar.

* Sie können eine Anforderung nicht abbrechen, wenn die Spalte [!UICONTROL **Benutzer**] einer Anforderung als [!UICONTROL **Nicht erkannt**] angezeigt wird. In diesem Fall bedeutet dies, dass sich der Benutzer in einem Anmeldeunternehmen befindet, für das Sie keine Administratorberechtigungen haben.

Weitere Informationen zum Reporting-Aktivitäts-Manager, einschließlich der wichtigsten Vorteile und Berechtigungsanforderungen, finden Sie unter [Übersicht über den Reporting-Aktivitäts-Manager](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md).

## Bestimmte Anforderungen abbrechen

Sie können einzelne Anforderungen abbrechen, die eine große Menge an Berichtskapazität beanspruchen.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Berichterstellungsaktivitäts-Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting-Aktivitäts-Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die Registerkarte [!UICONTROL **Anforderungen**] und dann eine oder mehrere Anforderungen aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anforderungen abbrechen**] aus.

   Das Dialogfeld [!UICONTROL **Abbrechen _x_ der Berichtsanforderungen**] wird angezeigt.

1. Im Feld Abbruchsnachricht wird die Nachricht angezeigt, die Benutzern angezeigt wird, wenn ihre Anforderungen abgebrochen werden. Eine Standardnachricht wird bereitgestellt. Sie können die Standardnachricht aktualisieren, um zusätzliche Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anforderungen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option zum [!UICONTROL **Einschränken nachfolgender Anforderungen**]

      ![Einschränken nachfolgender Anforderungen](assets/restrict-subsequent-requests.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzer und Projekt**] | Benutzende, die mit den ausgewählten Anfragen verknüpft sind, werden vorübergehend von der Ausführung von Berichtsanfragen für die ausgewählten Projekte ausgeschlossen. |
      | [!UICONTROL **Benutzer**] | Benutzende, die mit den ausgewählten Anträgen verknüpft sind, können vorübergehend keine weiteren Reporting-Anfragen stellen. |
      | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Anfragen verknüpft sind, werden vorübergehend von allen Reporting-Anfragen ausgeschlossen. |
      | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt sein sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!-- double-check this --><p>Sie können eine Beschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

      {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Mit Abbruch fortfahren**] aus.

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis beim Zugriff auf einen abgebrochenen Bericht](#experience-when-users-access-a-cancelled-report).

## Abbrechen von Anforderungen durch den Benutzer

Sie können alle Anforderungen abbrechen, die mit einem oder mehreren Benutzern verknüpft sind.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Berichterstellungsaktivitäts-Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting-Aktivitäts-Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die Registerkarte [!UICONTROL **Benutzer**] und dann einen oder mehrere Benutzer aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anforderungen abbrechen**] aus.

   Das Dialogfeld [!UICONTROL **Abbrechen _x_ der Berichtsanforderungen von x Benutzern**] wird angezeigt.

1. Im Feld Abbruchsnachricht wird die Nachricht angezeigt, die Benutzern angezeigt wird, wenn ihre Anforderungen abgebrochen werden. Eine Standardnachricht wird bereitgestellt. Sie können die Standardnachricht aktualisieren, um zusätzliche Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anforderungen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option zum [!UICONTROL **Einschränken nachfolgender Anforderungen**].

      ![Einschränken nachfolgender Anforderungen durch Benutzer](assets/restrict-subsequent-requests-user.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzer und Projekt**] | Ausgewählte Benutzende können vorübergehend keine Berichtsanfragen für die verknüpften Projekte stellen. |
      | [!UICONTROL **Benutzer**] | Ausgewählte Benutzende können vorübergehend keine Berichtsanfragen stellen. |
      | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Benutzenden verbunden sind, werden von allen Berichtsanfragen ausgeschlossen, die von anderen Benutzenden gestellt werden. |
      | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt sein sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Sie können eine Beschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

      {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Mit Abbruch fortfahren**] aus.

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis beim Zugriff auf einen abgebrochenen Bericht](#experience-when-users-access-a-cancelled-report).

## Anforderungen nach Projekt abbrechen

Sie können alle Anforderungen abbrechen, die mit einem oder mehreren Projekten verknüpft sind.

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Berichterstellungsaktivitäts-Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting-Aktivitäts-Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die Registerkarte [!UICONTROL **Projekte**] und dann ein oder mehrere Projekte aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anforderungen abbrechen**] aus.

   Das Dialogfeld [!UICONTROL **Abbrechen _x_ für Berichtsanforderungen von x Projekten**] wird angezeigt.

1. Im Feld Abbruchsnachricht wird die Nachricht angezeigt, die Benutzern angezeigt wird, wenn ihre Anforderungen abgebrochen werden. Eine Standardnachricht wird bereitgestellt. Sie können die Standardnachricht aktualisieren, um zusätzliche Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anforderungen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option zum [!UICONTROL **Einschränken nachfolgender Anforderungen**].

      ![Einschränken nachfolgender Anforderungen nach Projekt](assets/restrict-subsequent-requests-project.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzer und Projekt**] | Ausgewählte Projekte werden vorübergehend von allen Berichtsanfragen der verknüpften Benutzenden ausgeschlossen. |
      | [!UICONTROL **Benutzer**] | Benutzende, die mit den ausgewählten Projekten verknüpft sind, können vorübergehend keine weiteren Berichtsanfragen stellen. |
      | [!UICONTROL **Projekt**] | Ausgewählte Projekte sind vorübergehend von jeglichen Berichtsanfragen eines Benutzers ausgeschlossen. |
      | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt sein sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Sie können eine Beschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

      {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Mit Abbruch fortfahren**] aus.

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis beim Zugriff auf einen abgebrochenen Bericht](#experience-when-users-access-a-cancelled-report).

## Anforderungen durch Anwendung abbrechen

Sie können alle Anforderungen abbrechen, die mit einer oder mehreren Anwendungen verknüpft sind. Beim Abbrechen von mit einer Anwendung verknüpften Anforderungen können Sie die mit dieser Anwendung verknüpften Anforderungen für einen bestimmten Zeitraum weiter einschränken.

Zu den Anwendungen gehören:

* Analysis Workspace-Benutzeroberfläche
* Geplante Projekte im Workspace
* Report Builder
* Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.
* API-Aufrufe aus der API 1.4 oder 2.0
* Warnhinweise
* Für alle Links freigeben
* Jede andere Anwendung, die die Analytics-Reporting-Engine abfragt

So brechen Sie Anfragen nach Anwendung ab:

1. Navigieren Sie in Adobe Analytics zu **[!UICONTROL Admin]** > **[!UICONTROL Berichterstellungsaktivitäts-Manager]**.

1. Wählen Sie die Verbindung aus, bei der Sie Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting-Aktivitäts-Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die Registerkarte [!UICONTROL **Anwendungen**] und dann eine oder mehrere Anwendungen aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anforderungen abbrechen**] aus.

   Das Dialogfeld [!UICONTROL **Abbrechen _x_ für Berichtsanforderungen von x Projekten**] wird angezeigt.

1. Im Feld Abbruchsnachricht wird die Nachricht angezeigt, die Benutzern angezeigt wird, wenn ihre Anforderungen abgebrochen werden. Eine Standardnachricht wird bereitgestellt. Sie können die Standardnachricht aktualisieren, um zusätzliche Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anforderungen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option zum [!UICONTROL **Einschränken nachfolgender Anforderungen**]

      ![Einschränken nachfolgender Anfragen nach Anwendung](assets/restrict-subsequent-requests-application.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzer und Projekt**] | Ausgewählte Anwendungen sind vorübergehend auf Berichterstellungsanforderungen der assoziierten Benutzer und Projekte beschränkt.<p>Dies ist die am wenigsten restriktive Option.</p> |
      | [!UICONTROL **Benutzer**] | Benutzer, die mit den ausgewählten Anwendungen verknüpft sind, können keine Berichterstellungsanfragen stellen. |
      | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Anwendungen verknüpft sind, sind auf alle Berichterstellungsanforderungen eines Benutzers beschränkt. |
      | [!UICONTROL **Eingeschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt sein sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Sie können eine Beschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

      {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Mit Abbruch fortfahren**] aus.

   In der Anwendung wird eine Benachrichtigung angezeigt (z. B. in Analysis Workspace), in der Benutzer darüber informiert werden, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis beim Zugriff auf einen abgebrochenen Bericht](#experience-when-users-access-a-cancelled-report).

## Erlebnis beim Zugriff auf einen abgebrochenen Bericht

In Analysis Workspace sehen Benutzer die folgenden Meldungen, wenn sie versuchen, auf einen Bericht oder eine Visualisierung zuzugreifen, der bzw. die von einem Abbruch betroffen ist:

### Nachricht im Projekt

Wenn Benutzer versuchen, auf ein Projekt zuzugreifen, das von einem Abbruch betroffen ist, wird ihnen eine Meldung angezeigt, dass der Bericht vorübergehend eingeschränkt ist:

![Nachricht über den Abbruch des Projekts](assets/workspace-canceled-report.png)

### Meldung bei der Visualisierung

Wenn Benutzer versuchen, auf eine Visualisierung zuzugreifen, die von einem Abbruch betroffen ist, wird ihnen eine Meldung angezeigt, dass die Datenverarbeitung für den Bericht vorübergehend eingeschränkt ist:

![Meldung über den Abbruch einer Visualisierung](assets/workspace-cancelled-visualization.png)
