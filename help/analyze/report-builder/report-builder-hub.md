---
title: Report Builder-Hub
description: Erfahren Sie mehr über den Report Builder Hub.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: e18381ea-b7d4-4d7a-9ded-23b2d06fa204
source-git-commit: ff1722416fe5062d16c12185d17271ebc2d6b624
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 22%

---

# Report Builder-Hub


Der Report Builder-Hub ist der rechte Bereich, der in Ihrer Excel-Arbeitsmappe angezeigt wird, wenn Sie ![AdobeLogoRedonWhite](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]** in der Excel-Multifunktionsleiste auswählen.

Verwenden Sie den Report Builder-Hub, um Datenblöcke zu erstellen, zu aktualisieren, zu löschen und zu verwalten.

Der Report Builder-Hub enthält die Schaltflächen ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]**, ![TableManage](/help/assets/icons/TableManage.svg) **[!UICONTROL Manage]** und ![Calendar](/help/assets/icons/Calendar.svg)**[!UICONTROL Schedule]**, das **[!UICONTROL Commands]**-Bedienfeld und das **[!UICONTROL Quick Edit]**-Bedienfeld.

![Report Builder Hub](assets/hub51.png){zoomable="yes"}


Auswählen

* ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]**, um [neue Datenblöcke zu erstellen](create-a-data-block.md).
* ![TableManage](/help/assets/icons/TableManage.svg) **[!UICONTROL Manage]** zum [Verwalten vorhandener Datenblöcke](manage-reportbuilder.md).
* ![Kalender](/help/assets/icons/Calendar.svg) **[!UICONTROL Zeitplan]** zum [Verwalten von Zeitplänen zum Senden Ihrer Arbeitsmappe per E-Mail](schedule-reportbuilder.md).

## Befehlsfenster

Verwenden Sie das Bedienfeld **[!UICONTROL Befehle]**, um auf Befehle zuzugreifen, die mit den ausgewählten Zellen oder einer vorherigen Aktion kompatibel sind.

| Befehle | Verfügbar wenn… | Zweck |
|------|------------------|--------|
| ![Bearbeiten](/help/assets/icons/Edit.svg) **[!UICONTROL Datenblock bearbeiten]** | Die ausgewählte Zelle bzw. der ausgewählte Zellenbereich ist nur Teil eines Datenblocks. | Dient zum Bearbeiten eines Datenblocks. |
| ![Aktualisieren](/help/assets/icons/Refresh.svg) **[!UICONTROL Datenblock aktualisieren]** | Die Auswahl enthält mindestens einen Datenblock. Der Befehl aktualisiert nur die Datenblöcke in der Auswahl. | Dient zum Aktualisieren eines oder mehrerer Datenblöcke. |
| ![DocumentRefresh](/help/assets/icons/DocumentRefresh.svg) **[!UICONTROL Alle Datenblöcke aktualisieren]** | Die Arbeitsmappe enthält einen oder mehrere Datenblöcke. | Dient zum Aktualisieren aller Datenblöcke in der Arbeitsmappe |
| ![Senden](/help/assets/icons/Send.svg) **[!UICONTROL Arbeitsmappe senden]** | Die Arbeitsmappe enthält einen oder mehrere Datenblöcke. | Dient zum [Senden der Arbeitsmappe als Datei per E-Mail](schedule-reportbuilder.md). |
| ![Kopieren](/help/assets/icons/Copy.svg) **[!UICONTROL Datenblock kopieren]** | Die ausgewählte Zelle oder der ausgewählte Zellbereich ist Teil eines oder mehrerer Datenblöcke. | Dient zum Kopieren eines Datenblocks. |
| ![Cut](/help/assets/icons/Cut.svg) **[!UICONTROL Datenblock ausschneiden]** | Die ausgewählte Zelle oder der ausgewählte Zellbereich ist Teil eines oder mehrerer Datenblöcke. | Verwenden Sie , um einen Datenblock auszuschneiden. |
| ![Löschen](/help/assets/icons/Delete.svg) **[!UICONTROL Datenblock löschen]** | Die ausgewählte Zelle bzw. der ausgewählte Zellenbereich ist nur Teil eines Datenblocks. | Zum Löschen eines Datenblocks verwenden |

## Bedienfeld „Schnellbearbeitung“

Wenn Sie einen oder mehrere Datenblöcke in einem Arbeitsblatt auswählen, zeigt Report Builder das Bedienfeld &quot;**[!UICONTROL &quot;]**. Sie können das Bedienfeld **[!UICONTROL Schnellbearbeitung]** verwenden, um Parameter in einem oder mehreren Datenblöcken gleichzeitig zu ändern.

Die Änderungen, die Sie bei Verwendung der **[!UICONTROL Schnellbearbeitung]**-Abschnitte vornehmen, gelten für alle ausgewählten Datenblöcke.

### Report Suites

Datenblöcke rufen Daten aus einer ausgewählten Report Suite ab. Wenn mehrere Datenblöcke in einem Arbeitsblatt ausgewählt sind und sie keine Daten aus derselben Report Suite abrufen, wird der **Report Suites**-Link **[!UICONTROL _Mehrere_]** angezeigt.

Wenn Sie die Report Suite ändern, übernehmen alle Datenblöcke in der Auswahl die neue Report Suite. Komponenten im Datenblock werden basierend auf der ID mit der neuen Report Suite abgeglichen. Wenn eine Komponente nicht in einem Datenblock gefunden wird, wird die Komponente entfernt und durch **[!UICONTROL Ungültiger Wert]** ersetzt oder ![AlertRed](/help/assets/icons/AlertRed.svg) wird für die spezifische Komponente angezeigt.

Um die Report Suite zu ändern, wählen Sie eine neue Report Suite aus dem **[!UICONTROL Report Suite]** Dropdown-Menü aus.


### Datumsbereich

**Datumsbereich** zeigt den Datumsbereich für die ausgewählten Datenblöcke an. Wenn mehrere Datenblöcke mit mehreren Datumsbereichen ausgewählt sind, zeigt der Link **[!UICONTROL Datumsbereich]** &quot;**[!UICONTROL _&quot;_]**.

### Segmente

Der **Segmente**-Link zeigt eine zusammenfassende Liste der Segmente an, die von den ausgewählten Datenblöcken verwendet werden. Wenn mehrere Datenblöcke mit mehreren angewendeten Segmenten ausgewählt sind, wird der Link **Segmente** angezeigt **[!UICONTROL _Mehrere_]**.

>[!MORELIKETHIS]
>
>[Report Suite auswählen](select-report-suite.md)
>[Datumsbereich auswählen](select-date-range.md)
>[Arbeiten mit Filtern](work-with-segments.md)
>

<!--

Use the Report Builder hub to create, update, delete, and manage data blocks.

The Report Builder hub contains the Create, Manage, and Schedule buttons, the COMMANDS panel, and The QUICK EDIT panel.

<img src="./assets/hub51.png" alt="Report Builder Hub"/>


## Create, Manage, and Schedule buttons

Use the Create, Manage, and Schedule buttons to create new data blocks, manage existing data blocks, or schedule datablocks.

## COMMANDS panel

Use the COMMANDS panel to access commands that are compatible with the selected cells or a previous action.

### Commands

| Commands displayed      | Available when…   | Purpose          |
|------|------------------|--------|
| Edit data block | The selected cell or cells range is part of one data block only. | Used to edit a data block |
| Refresh data block | The selection contains at least one data block. The command refreshes only the data blocks in the selection. | Used to refresh one or more data blocks |
| Refresh all data blocks | The workbook contains one or more data blocks. | Used to refresh ALL data blocks in the workbook |
| Send workbook |   |  Send a workbook on a schedule. |
| Copy data block   | The selected cell or cell range is part of one or more data blocks. | Used to copy a data block   |
| Cut data block |   | Used to cut a data block |
| Delete data block | The selected cell or cells range is part of one data block only. | Used to delete a data block |

## QUICK EDIT panel

When you select one or more data blocks in a spreadsheet, Report Builder displays the QUICK EDIT panel. You can use the QUICK EDIT panel to change parameters in a single data block or to change parameters in multiple data blocks at the same time.

![The Quick Edit panel in Report Builder](./assets/hub2.png)

The changes made using the Quick Edit sections apply to all selected data blocks.

### Report suites

Data blocks pull data from a selected report suite. If multiple data blocks are selected in a worksheet and they don't pull data from the same report suite, the **Report Suites** link displays *Multiple*.

When you change the report suite, all data blocks in the selection adopt the new report suite. Components in the data block are matched to the new report suite based on ID, for example, matching ```evars```). If a component isn't found in a data block, a warning message is displayed and the component is removed from the data block.

To change the report suite, select a new report suite from the drop-down menu.

![The Report Builder Hub showing the report suite drop-down menu.](./assets/image16.png)

### Date range

**[!UICONTROL Date range]** shows the date range for the selected data blocks. If multiple data blocks are selected with multiple date ranges, the **[!UICONTROL Date range]** link displays *Multiple*. [Learn more](/help/analyze/report-builder/select-date-range.md)

### Segments

The **Segments** link displays a summary list of the segments used by the selected data blocks. If multiple data blocks are selected with multiple segments applied, the **Segments** link displays *Multiple*. [Learn more](/help/analyze/report-builder/work-with-segments.md)

-->