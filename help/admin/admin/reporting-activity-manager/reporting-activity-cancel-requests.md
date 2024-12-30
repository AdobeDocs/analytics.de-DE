---
description: Erfahren Sie, wie Sie Kapazitätsprobleme bei Spitzen während der Berichterstellung mit Reporting Activity Manager diagnostizieren und beheben können.
title: Abbrechen von Berichtsanfragen in Reporting Activity Manager
feature: Admin Tools
exl-id: 37a2fa8f-7804-4220-a508-ec66996b3801
role: Admin
source-git-commit: 815e50e30fa6a0bce1bf78f33843070f96f52de8
workflow-type: tm+mt
source-wordcount: '1438'
ht-degree: 13%

---

# Abbrechen von Berichtsanfragen in Reporting Activity Manager

Mit [!UICONTROL Reporting Activity Manager] können Administratoren Berichtsanfragen schnell diagnostizieren und abbrechen, um Probleme mit der Berichtskapazität während Spitzenzeiten beim Reporting zu beheben.

Beachten Sie beim Abbrechen von Berichtsanfragen Folgendes:

* Sie können bestimmte Anfragen abbrechen, alle Anfragen eines bestimmten Benutzers abbrechen oder alle Anfragen im Zusammenhang mit einem bestimmten Projekt abbrechen.

  Wenn Sie eine Anfrage abbrechen, wird die Aktion in den &quot;[&quot; ](/help/admin/admin/logs.md). Die Spalte [!UICONTROL **Ereignistyp**] wird als [!UICONTROL **Admin-Aktion**] angezeigt, und eine Beschreibung des Abbruchs ist in der Spalte [!UICONTROL **Ereignis**] verfügbar.

* Wenn Sie Anfragen abbrechen, können Sie auch nachfolgende Anfragen für einen bestimmten Zeitraum einschränken.

  Wenn Sie eine nachfolgende Anfrage einschränken, wird die Aktion in den &quot;[&quot; ](/help/admin/admin/logs.md). Die Spalte [!UICONTROL **Ereignistyp**] wird als [!UICONTROL **Admin-Aktion**] angezeigt, und eine Beschreibung der Einschränkung ist in der Spalte [!UICONTROL **Ereignis**] verfügbar.

* Sie können eine Anfrage nicht abbrechen, wenn die Spalte [!UICONTROL **Benutzer**] einer Anfrage als [!UICONTROL **Nicht erkannt**] angezeigt wird. In diesem Fall bedeutet dies, dass sich der Benutzer in einer Unternehmensanmeldung befindet, für die Sie keine Administratorrechte haben.

Weitere Informationen zu Reporting Activity Manager, einschließlich der wichtigsten Vorteile und Berechtigungsanforderungen, finden Sie unter [Reporting Activity Manager - Übersicht](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md).

## Abbrechen spezifischer Anfragen

Sie können einzelne Anfragen abbrechen, die eine große Menge an Berichtskapazität beanspruchen.

1. Navigieren Sie in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie die Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting Activity Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die [!UICONTROL **Anfragen**] aus und wählen Sie dann eine oder mehrere Anfragen aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anfragen abbrechen**] aus.

   Das [!UICONTROL **Abbrechen _x_ Berichtanfragen**] wird angezeigt.

1. Das Feld Abbruchsmeldung zeigt die Meldung an, die Benutzern angezeigt wird, wenn ihre Anfragen abgebrochen werden. Es wird eine Standardmeldung bereitgestellt. Sie können die Standardmeldung aktualisieren, um weitere Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anfragen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option [!UICONTROL **Nachfolgende Anfragen einschränken**]

      ![Nachfolgende Anfragen einschränken](assets/restrict-subsequent-requests.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzer und Projekt**] | Benutzende, die mit den ausgewählten Anfragen verknüpft sind, werden vorübergehend von der Ausführung von Berichtsanfragen für die ausgewählten Projekte ausgeschlossen. |
      | [!UICONTROL **Benutzende**] | Benutzende, die mit den ausgewählten Anträgen verknüpft sind, können vorübergehend keine weiteren Reporting-Anfragen stellen. |
      | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Anfragen verknüpft sind, werden vorübergehend von allen Reporting-Anfragen ausgeschlossen. |
      | [!UICONTROL **Beschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt werden sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!-- double-check this --><p>Sie können eine Einschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

      {style="table-layout:auto"}

1. Wählen [!UICONTROL **Mit Abbruch fortfahren**].

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die den Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis, wenn Benutzende auf einen abgebrochenen Bericht zugreifen](#experience-when-users-access-a-cancelled-report).

## Anfragen nach Benutzer abbrechen

Sie können alle Anfragen abbrechen, die mit einem oder mehreren Benutzern verknüpft sind.

1. Navigieren Sie in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie die Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting Activity Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die [!UICONTROL **Benutzer**] und dann einen oder mehrere Benutzer aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anfragen abbrechen**] aus.

   Das [!UICONTROL **Abbrechen _x_-Berichtsanfragen von x Benutzern**] wird angezeigt.

1. Das Feld Abbruchsmeldung zeigt die Meldung an, die Benutzern angezeigt wird, wenn ihre Anfragen abgebrochen werden. Es wird eine Standardmeldung bereitgestellt. Sie können die Standardmeldung aktualisieren, um weitere Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anfragen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option [!UICONTROL **Nachfolgende Anfragen einschränken**].

      ![Nachfolgende Anfragen nach Benutzer einschränken](assets/restrict-subsequent-requests-user.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzer und Projekt**] | Ausgewählte Benutzende können vorübergehend keine Berichtsanfragen für die verknüpften Projekte stellen. |
      | [!UICONTROL **Benutzende**] | Ausgewählte Benutzende können vorübergehend keine Berichtsanfragen stellen. |
      | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Benutzenden verbunden sind, werden von allen Berichtsanfragen ausgeschlossen, die von anderen Benutzenden gestellt werden. |
      | [!UICONTROL **Beschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt werden sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Sie können eine Einschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

      {style="table-layout:auto"}

1. Wählen [!UICONTROL **Mit Abbruch fortfahren**].

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die den Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis, wenn Benutzende auf einen abgebrochenen Bericht zugreifen](#experience-when-users-access-a-cancelled-report).

## Anfragen nach Projekt abbrechen

Sie können alle Anfragen abbrechen, die mit einem oder mehreren Projekten verknüpft sind.

1. Navigieren Sie in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Report Suite aus, in der Sie die Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting Activity Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die [!UICONTROL **Projekte**] und wählen Sie dann ein oder mehrere Projekte aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anfragen abbrechen**] aus.

   Das [!UICONTROL **Abbrechen _x_-Berichtsanfragen von x Projekten**] wird angezeigt.

1. Das Feld Abbruchsmeldung zeigt die Meldung an, die Benutzern angezeigt wird, wenn ihre Anfragen abgebrochen werden. Es wird eine Standardmeldung bereitgestellt. Sie können die Standardmeldung aktualisieren, um weitere Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anfragen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option [!UICONTROL **Nachfolgende Anfragen einschränken**].

      ![Nachfolgende Anfragen nach Projekt einschränken](assets/restrict-subsequent-requests-project.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzer und Projekt**] | Ausgewählte Projekte werden vorübergehend von allen Berichtsanfragen der verknüpften Benutzenden ausgeschlossen. |
      | [!UICONTROL **Benutzende**] | Benutzende, die mit den ausgewählten Projekten verknüpft sind, können vorübergehend keine weiteren Berichtsanfragen stellen. |
      | [!UICONTROL **Projekt**] | Ausgewählte Projekte werden vorübergehend von Berichtsanfragen anderer Benutzer ausgeschlossen. |
      | [!UICONTROL **Beschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt werden sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Sie können eine Einschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

      {style="table-layout:auto"}

1. Wählen [!UICONTROL **Mit Abbruch fortfahren**].

   In Analysis Workspace wird eine Benachrichtigung angezeigt, die den Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis, wenn Benutzende auf einen abgebrochenen Bericht zugreifen](#experience-when-users-access-a-cancelled-report).

## Anfragen nach Anwendung abbrechen

Sie können alle Anfragen abbrechen, die mit einer oder mehreren Anwendungen verbunden sind. Beim Abbrechen von mit einer Anwendung verknüpften Anfragen können Sie die mit dieser Anwendung verknüpften Anfragen für einen bestimmten Zeitraum weiter einschränken.

Die Anwendungen umfassen Folgendes:

* Analysis Workspace-Benutzeroberfläche
* Geplante Projekte im Workspace
* Report Builder
* Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.
* API-Aufrufe aus der API 1.4 oder 2.0
* Warnhinweise
* Für alle freigeben - Links
* Jede andere Anwendung, die die Analytics-Reporting-Engine abfragt

So brechen Sie Anfragen nach Anwendung ab:

1. Navigieren Sie in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

1. Wählen Sie die Verbindung aus, bei der Sie Berichtsanfragen abbrechen möchten. <!--double-check this step-->

   Weitere Informationen zu den auf dieser Seite verfügbaren Daten finden Sie unter [Berichtsaktivität im Reporting Activity Manager anzeigen](/help/admin/admin/reporting-activity-manager/reporting-activity.md).

1. Wählen Sie die [!UICONTROL **Anwendungen**] und wählen Sie dann eine oder mehrere Anwendungen aus.

   <!-- add screenshot -->

1. Wählen Sie [!UICONTROL **Anfragen abbrechen**] aus.

   Das [!UICONTROL **Abbrechen _x_-Berichtsanfragen von x Projekten**] wird angezeigt.

1. Das Feld Abbruchsmeldung zeigt die Meldung an, die Benutzern angezeigt wird, wenn ihre Anfragen abgebrochen werden. Es wird eine Standardmeldung bereitgestellt. Sie können die Standardmeldung aktualisieren, um weitere Details anzugeben.

1. (Optional) So beschränken Sie zukünftige Anfragen für einen bestimmten Zeitraum:

   1. Aktivieren Sie die Option [!UICONTROL **Nachfolgende Anfragen einschränken**]

      ![Nachfolgende Anfragen nach Anwendung einschränken](assets/restrict-subsequent-requests-application.png)

   1. Wählen Sie aus den folgenden Optionen:

      | Option | Funktion |
      |---------|----------|
      | [!UICONTROL **Benutzer und Projekt**] | Ausgewählte Programme werden vorübergehend von Berichtsanfragen der zugehörigen Benutzer und Projekte ausgeschlossen.<p>Dies ist die am wenigsten einschränkende Option.</p> |
      | [!UICONTROL **Benutzende**] | Benutzerinnen und Benutzer, die mit den ausgewählten Programmen verknüpft sind, dürfen keine Berichtsanfragen stellen. |
      | [!UICONTROL **Projekt**] | Projekte, die mit den ausgewählten Programmen verknüpft sind, sind von allen Berichtsanfragen eines Benutzers ausgeschlossen. |
      | [!UICONTROL **Beschränkt für**] | Wählen Sie aus, wie lange Anforderungen eingeschränkt werden sollen. Sie können zwischen 1 Minute (Standard), 5 Minuten, 10 Minuten, 15 Minuten oder 30 Minuten wählen. <!--double-check this--> <p>Sie können eine Einschränkung nicht frühzeitig entfernen, nachdem sie festgelegt wurde.</p> |

      {style="table-layout:auto"}

1. Wählen [!UICONTROL **Mit Abbruch fortfahren**].

   In der Anwendung (z. B. in Analysis Workspace) wird eine Benachrichtigung angezeigt, die den Benutzer darüber informiert, dass die Anfrage abgebrochen wurde. Weitere Informationen dazu, wie dies in Analysis Workspace angezeigt wird, finden Sie unter [Erlebnis, wenn Benutzende auf einen abgebrochenen Bericht zugreifen](#experience-when-users-access-a-cancelled-report).

## Erlebnis, wenn Benutzer auf einen abgebrochenen Bericht zugreifen

In Analysis Workspace sehen Benutzerinnen und Benutzer die folgenden Meldungen, wenn sie versuchen, auf einen Bericht oder eine Visualisierung zuzugreifen, der bzw. die von einem Abbruch betroffen ist:

### Nachricht zum Projekt

Wenn ein(e) Benutzende(r) versucht, auf ein Projekt zuzugreifen, das von einem Abbruch betroffen ist, wird eine Meldung angezeigt, die ihn/sie darüber informiert, dass der Bericht vorübergehend eingeschränkt ist:

![Nachricht zum Projektabbruch](assets/workspace-canceled-report.png)

### Nachricht zur Visualisierung

Wenn ein(e) Benutzende(r) versucht, auf eine Visualisierung zuzugreifen, die von einem Abbruch betroffen ist, wird eine Meldung angezeigt, die ihn/sie darüber informiert, dass die Datenverarbeitung für den Bericht vorübergehend eingeschränkt ist:

![Nachricht zum Abbruch der Visualisierung](assets/workspace-cancelled-visualization.png)
