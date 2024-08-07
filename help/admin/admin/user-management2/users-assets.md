---
description: Verwalten Sie Analytics-Benutzer und deren Assets in der Adobe Admin Console.
title: Verwalten von Analytics-Benutzern und -Assets
feature: Admin Tools
exl-id: 849a8279-4850-4458-bdd2-85052a17ee21
role: Admin
source-git-commit: 869b44b826de5cb35d13000133092397cb16ccaa
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 3%

---

# Verwalten von alten Benutzerkonten, Assets und Ablaufdaten

Sie können ältere Benutzerkonten, ihren Migrationsstatus, die Ablaufdaten, die Übertragung von Assets an andere Benutzer und mehr mit **[!UICONTROL Admin] > [!UICONTROL Alle Admin] > [!UICONTROL Analytics-Benutzer und Admin]** verwalten.

Der Bildschirm &quot;Benutzer&quot;enthält eine Liste der aktuellen Adobe Analytics-Benutzer mit den folgenden Spalten:

| Spalte | Beschreibung |
|---|---|
| [!UICONTROL Benutzer-ID] | Die Benutzer-ID, mit der sich der Benutzer bei Adobe Analytics anmeldet. |
| [!UICONTROL Name] | Der Name des Benutzers. |
| [!UICONTROL Migrationsstatus] | Der Status der Migration von einem alten Benutzerkonto zu einer Enterprise ID oder Adobe ID.  Der Status kann nicht initiiert, in die Warteschlange gestellt oder migriert werden. |
| [!UICONTROL E-Mail] | Die E-Mail des Benutzers. |
| [!UICONTROL Veraltete Anmeldung] | Der Status der bisherigen Anmeldung, die aktiviert oder deaktiviert werden kann. |
| [!UICONTROL Erstellt am] | Zeitstempel der Erstellung des Benutzerkontos in der Adobe Analytics. |
| [!UICONTROL Letzter Analytics-Zugriff] | Zeitstempel des neuesten Zugriffs des Benutzerkontos auf Adobe Analytics, |
| [!UICONTROL Ablauf] | Ablaufdatum für das Benutzerkonto oder Keine , wenn das Benutzerkonto nicht abläuft. |

![Benutzer](assets/users.png)

- Um nach einem bestimmten Benutzer zu suchen, verwenden Sie das Feld ![Suche](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) *Suche nach Titel* .
- Um die Liste nach dem Migrationsstatus zu filtern, wählen Sie ![Chevron](https://spectrum.adobe.com/static/icons/ui_18/ChevronSize100.svg) **[!UICONTROL Migrationsstatus]** aus.
- Um die Liste nach dem alten Anmeldestatus zu filtern, wählen Sie ![Chevron](https://spectrum.adobe.com/static/icons/ui_18/ChevronSize100.svg) **[!UICONTROL Legacy login]** aus.
- Um die Anzeige der Spalten zu ändern, wählen Sie ![Spalteneinstellungen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ColumnSettings_18_N.svg) aus und wählen Sie die Spalten aus dem Popup aus.

Sie können verschiedene Aktionen anwenden, wenn Sie einen oder mehrere Benutzer aus der Liste auswählen:

| Aktion | Beschreibung |
|---|---|
| ![Migrieren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Briefcase_18_N.svg) **[!UICONTROL Migrieren]** | Sie können einen oder mehrere Benutzer zu Enterprise IDs oder Adobe IDs migrieren. |
| ![Kalender gesperrt](https://spectrum.adobe.com/static/icons/workflow_18/Smock_CalendarLocked_18_N.svg) **[!UICONTROL Gültigkeit festlegen]** | Sie können ein Ablaufdatum für die Verwendung der bisherigen Adobe Analytics-Anmeldedaten für die ausgewählten Benutzer festlegen.  Wählen Sie das Datum aus, an dem ein Kalender-Popup angezeigt werden soll, um das Datum anzugeben. Wählen Sie **[!UICONTROL Fertig]** aus, um den Ablauf zu bestätigen. |
| ![Transfer assets](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Switch_18_N.svg) **[!UICONTROL Transfer assets]** | Diese Aktion ist nur verfügbar, wenn ein Benutzer ausgewählt wird. Wenn der Benutzer über Assets verfügt, die übertragen werden können, können Sie die Kontoelemente auswählen (wie Lesezeichen, Dashboards usw.). Wählen Sie **[!UICONTROL Übertragen]** aus, um die Übertragung abzuschließen.<br/>![Überträgt Assets](assets/transfer-assets.png) |
| ![Konten löschen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL Konten löschen]** | Es wird ein Dialogfeld angezeigt, in dem der Löschvorgang der ausgewählten Konten bestätigt wird. Wählen Sie **[!UICONTROL OK]** aus, um die Konten zu löschen. Wählen Sie **[!UICONTROL Abbrechen]** aus, um abzubrechen. |
| ![Exportieren in CSV](https://spectrum.adobe.com/static/icons/workflow_18/Smock_FileCSV_18_N.svg) **[!UICONTROL Exportieren in CSV]** | Durch diese Aktion wird sofort eine Datei mit einer kommagetrennten Werteliste der ausgewählten Benutzer mit ihren Details (Name, Migrationsstatus, E-Mail usw.) heruntergeladen. |

