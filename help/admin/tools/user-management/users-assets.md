---
description: Verwalten von Analytics-Benutzern und deren Assets in der Adobe Admin Console.
title: Verwalten von Analytics-Benutzern und -Assets
feature: Admin Tools
exl-id: 849a8279-4850-4458-bdd2-85052a17ee21
role: Admin
TQID: 'https://experienceleague.adobe.com/d8CK9Vf-eaEU6P9386J1eO-JpD5u4l3VoqRcMwvXcW0'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
    internal-label: Dashboards
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
    internal-label: Admin Tools
subfeature_v2:
  - id: d124af73-4061-4b84-9063-ae2b60f2c1f3
    internal-label: User management
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 8badbfc74bdc95a8ab673d4f00fe13e0829e64bb
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 5%
---
# Verwalten von Legacy-Benutzerkonten, Assets und Gültigkeitsdauern

Sie können Legacy-Benutzerkonten, ihren Migrationsstatus, die Ablaufdaten, die Übertragung von Assets an andere Benutzer und mehr unter Verwendung von **[!UICONTROL Admin] > [!UICONTROL Alle Administratoren] > [!UICONTROL Analytics-Benutzer und -]** verwalten.

Der Bildschirm Benutzer zeigt eine Liste der aktuellen Adobe Analytics-Benutzer mit den folgenden Spalten:

| Spalte | Beschreibung |
|---|---|
| [!UICONTROL Benutzer-ID] | Die Benutzer-ID, mit der sich der Benutzer bei Adobe Analytics anmeldet. |
| [!UICONTROL Name] | Der Name des Benutzers. |
| [!UICONTROL Migrationsstatus] | Der Status der Migration von einem alten Benutzerkonto zu einem Enterprise ID oder Adobe ID.  Der Status kann „Nicht initiiert“, „In Warteschlange“ oder „Migriert“ sein. |
| [!UICONTROL E-Mail] | Die E-Mail des Benutzers. |
| [!UICONTROL Legacy-Anmeldung] | Der Status der bisherigen Anmeldung, die aktiviert oder deaktiviert werden kann. |
| [!UICONTROL Erstellt am] | Zeitstempel, wann das Benutzerkonto in der Adobe Analytics erstellt wurde. |
| [!UICONTROL Letzter Analytics-Zugriff] | Zeitstempel des letzten Zugriffs des Benutzerkontos auf Adobe Analytics, |
| [!UICONTROL Ablauf] | Ablaufdatum für das Benutzerkonto oder Ohne, wenn das Benutzerkonto nicht abläuft. |

![Benutzer](assets/users.png)

- Um nach einem bestimmten Benutzer zu suchen, verwenden Sie das Feld ![Suche](/help/assets/icons/Search.svg) *Suche nach Titel*.
- Um die Liste nach Migrationsstatus zu filtern, wählen Sie ![Chevron](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Migrationsstatus]** aus.
- Um die Liste nach dem alten Anmeldestatus zu filtern, wählen Sie ![Chevron](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Legacy login]**.
- Um die Anzeige der Spalten zu ändern, wählen Sie ![Spalteneinstellungen](/help/assets/icons/ColumnSetting.svg) und die Spalten aus dem Popup aus.

Sie können verschiedene Aktionen anwenden, wenn Sie einen oder mehrere Benutzer aus der Liste auswählen:

| Aktion | Beschreibung |
|---|---|
| ![Migrieren](/help/assets/icons/Briefcase.svg) **[!UICONTROL Migrieren]** | Sie können einen oder mehrere Benutzer zu Enterprise IDs oder Adobe IDs migrieren. |
| ![Kalender gesperrt](/help/assets/icons/CalendarLocked.svg) **[!UICONTROL Ablaufdatum festlegen]** | Sie können ein Ablaufdatum für die Verwendung der Legacy-Adobe Analytics-Anmeldung für die ausgewählten Benutzer festlegen.  Wählen Sie das Datum aus, um ein Kalenderpopup zur Angabe des Datums zu verwenden. Wählen Sie **[!UICONTROL Fertig]** aus, um den Ablauf zu bestätigen. |
| ![Assets übertragen](/help/assets/icons/Switch.svg) **[!UICONTROL Assets übertragen]** | Diese Aktion ist nur verfügbar, wenn ein Benutzer ausgewählt wird. Wenn der Benutzer über Assets verfügt, die übertragen werden können, können Sie die Kontoelemente (wie Lesezeichen, Dashboards usw.) auswählen. Wählen Sie **[!UICONTROL Übertragen]** aus, um die Übertragung abzuschließen.<br/>![Überträgt Assets](assets/transfer-assets.png) |
| ![Konten löschen](/help/assets/icons/Delete.svg) **[!UICONTROL Konten löschen]** | Ein Dialogfeld wird angezeigt, um das Löschen der ausgewählten Konten zu bestätigen. Klicken Sie **[!UICONTROL OK]**, um die Konten zu löschen. Wählen Sie zum Abbrechen **[!UICONTROL Abbrechen]** aus. |
| ![In CSV exportieren](/help/assets/icons/FileCSV.svg) **[!UICONTROL In CSV exportieren]** | Diese Aktion lädt sofort eine Datei herunter, die eine kommagetrennte Werteliste der ausgewählten Benutzer mit ihren Details (Name, Migrationsstatus, E-Mail usw.) enthält. |

