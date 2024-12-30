---
description: Verwalten von Analytics-Benutzern und deren Assets in der Adobe Admin Console.
title: Verwalten von Analytics-Benutzern und -Assets
feature: Admin Tools
exl-id: 849a8279-4850-4458-bdd2-85052a17ee21
role: Admin
source-git-commit: 869b44b826de5cb35d13000133092397cb16ccaa
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 3%

---

# Verwalten von Legacy-Benutzerkonten, Assets und Gültigkeitsdauern

Sie können Legacy-Benutzerkonten, ihren Migrationsstatus, die Ablaufdaten, die Übertragung von Assets an andere Benutzer und mehr unter Verwendung von **[!UICONTROL Admin] > [!UICONTROL Alle Administratoren] > [!UICONTROL Analytics-Benutzer und -]** verwalten.

Der Bildschirm Benutzer zeigt eine Liste der aktuellen Adobe Analytics-Benutzer mit den folgenden Spalten:

| Spalte | Beschreibung |
|---|---|
| [!UICONTROL Benutzer-ID] | Die Benutzer-ID, mit der sich der Benutzer bei Adobe Analytics anmeldet. |
| [!UICONTROL Name] | Der Name des Benutzers. |
| [!UICONTROL Migrationsstatus] | Der Migrationsstatus von einem alten Benutzerkonto zu einer Enterprise ID oder Adobe ID.  Der Status kann „Nicht initiiert“, „In Warteschlange“ oder „Migriert“ sein. |
| [!UICONTROL E-Mail] | Die E-Mail des Benutzers. |
| [!UICONTROL Legacy-Anmeldung] | Der Status der bisherigen Anmeldung, die aktiviert oder deaktiviert werden kann. |
| [!UICONTROL Erstellt am] | Zeitstempel, wann das Benutzerkonto in der Adobe Analytics erstellt wurde. |
| [!UICONTROL Letzter Analytics-Zugriff] | Zeitstempel des letzten Zugriffs des Benutzerkontos auf Adobe Analytics, |
| [!UICONTROL Ablauf] | Ablaufdatum für das Benutzerkonto oder Ohne, wenn das Benutzerkonto nicht abläuft. |

![Benutzer](assets/users.png)

- Um nach einem bestimmten Benutzer zu suchen, verwenden Sie das Feld ![Suche](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) *Suche nach Titel*.
- Um die Liste nach Migrationsstatus zu filtern, wählen Sie ![Chevron](https://spectrum.adobe.com/static/icons/ui_18/ChevronSize100.svg) **[!UICONTROL Migrationsstatus]** aus.
- Um die Liste nach dem alten Anmeldestatus zu filtern, wählen Sie ![Chevron](https://spectrum.adobe.com/static/icons/ui_18/ChevronSize100.svg) **[!UICONTROL Legacy login]**.
- Um die Anzeige der Spalten zu ändern, wählen Sie ![Spalteneinstellungen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ColumnSettings_18_N.svg) und die Spalten aus dem Popup aus.

Sie können verschiedene Aktionen anwenden, wenn Sie einen oder mehrere Benutzer aus der Liste auswählen:

| Aktion | Beschreibung |
|---|---|
| ![Migrieren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Briefcase_18_N.svg) **[!UICONTROL Migrieren]** | Sie können einen oder mehrere Benutzer zu Enterprise IDs oder Adobe IDs migrieren. |
| ![Kalender gesperrt](https://spectrum.adobe.com/static/icons/workflow_18/Smock_CalendarLocked_18_N.svg) **[!UICONTROL Ablaufdatum festlegen]** | Sie können ein Ablaufdatum für die Verwendung der Legacy-Adobe Analytics-Anmeldung für die ausgewählten Benutzer festlegen.  Wählen Sie das Datum aus, um ein Kalenderpopup zur Angabe des Datums zu verwenden. Wählen Sie **[!UICONTROL Fertig]** aus, um den Ablauf zu bestätigen. |
| ![Assets übertragen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Switch_18_N.svg) **[!UICONTROL Assets übertragen]** | Diese Aktion ist nur verfügbar, wenn ein Benutzer ausgewählt wird. Wenn der Benutzer über Assets verfügt, die übertragen werden können, können Sie die Kontoelemente (wie Lesezeichen, Dashboards usw.) auswählen. Wählen Sie **[!UICONTROL Übertragen]** aus, um die Übertragung abzuschließen.<br/>![Überträgt Assets](assets/transfer-assets.png) |
| ![Konten löschen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL Konten löschen]** | Ein Dialogfeld wird angezeigt, um das Löschen der ausgewählten Konten zu bestätigen. Klicken Sie **[!UICONTROL OK]**, um die Konten zu löschen. Wählen Sie **[!UICONTROL Abbrechen]** zum Abbrechen aus. |
| ![In CSV exportieren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_FileCSV_18_N.svg) **[!UICONTROL In CSV exportieren]** | Diese Aktion lädt sofort eine Datei herunter, die eine kommagetrennte Werteliste der ausgewählten Benutzer mit ihren Details (Name, Migrationsstatus, E-Mail usw.) enthält. |

