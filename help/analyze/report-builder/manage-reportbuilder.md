---
title: Verwalten von Datenblöcken in Report Builder
description: Erfahren Sie, wie Sie Datenblöcke in Report Builder verwalten.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 63e169b3-7e13-405e-83a4-17f2a9917ed2
source-git-commit: c3fe537967473754a3b5fe88c7b383647b2c742e
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 20%

---

# Verwalten von Datenblöcken

Sie können alle Datenblöcke in einer Arbeitsmappe mit dem [!UICONTROL Datenblock-Manager“ anzeigen und ]. Der [!UICONTROL Datenblock-Manager] bietet Such-, Filter- und Sortierfunktionen, mit denen Sie bestimmte Datenblöcke finden können. Nach Auswahl eines oder mehrerer Datenblöcke können Sie diese bearbeiten, löschen oder aktualisieren.

## Datenblöcke anzeigen

Um eine Tabelle anzuzeigen, die alle Datenblöcke in einer Arbeitsmappe auflistet, wählen Sie ![TableManage](/help/assets/icons/TableManage.svg) **[!UICONTROL Manage]**.

![Die Option „Verwalten“, um eine Liste aller Datenblöcke anzuzeigen.](./assets/image53.png){zoomable="yes"}

Der **[!UICONTROL Datenblock-Manager]** zeigt eine Tabelle mit allen in einer Arbeitsmappe vorhandenen Datenblöcken an.

![Die Liste aller in einer Arbeitsmappe vorhandenen Datenblöcke.](./assets/image52.png){zoomable="yes"}

Sie können mit ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) auswählen, welche Spalten angezeigt werden sollen.

## Datenblöcke sortieren

Sie können die Datenblocktabelle nach einer angezeigten Spalte sortieren. Sie können Datenblöcke beispielsweise nach Report Suites, Segmenten, Datumsbereich und anderen Variablen sortieren.

Um die Datenblocktabelle zu sortieren, wählen Sie eine Spaltenüberschrift aus. Wählen Sie dieselbe Spaltenüberschrift aus, um die Sortierreihenfolge umzukehren.


## Datenblöcke suchen

Suchen Sie mithilfe ![ Felds ](/help/assets/icons/Search.svg)Suche **[!UICONTROL _Suche_]** nach beliebigen Elementen in der Datenblocktabelle. Sie können beispielsweise nach Metriken suchen, die in den Datenblöcken oder in der Report Suite enthalten sind. Sie können auch nach Datumsangaben suchen, die in den Spalten „Datumsbereich“, „Änderungsdatum“ oder „Datum des letzten Durchgang“ angezeigt werden.


## Datenblöcke bearbeiten

Sie können Report Suites und Datumsbereiche für Datenblöcke bearbeiten. Oder die auf Datenblöcke angewendeten Segmente.

Sie können beispielsweise ein vorhandenes Segment in einem oder mehreren Datenblöcken durch ein neues Segment ersetzen.

1. Wählen Sie die zu aktualisierenden Datenblöcke aus. Sie können das Kontrollkästchen auf der obersten Ebene aktivieren, um alle Datenblöcke auszuwählen. Sie können aber auch einzelne Datenblöcke auswählen.

   ![Das Stiftsymbol „Bearbeiten“](./assets/image56.png){zoomable="yes"}

1. Wählen Sie ![Bearbeiten](/help/assets/icons/Edit.svg) aus, um das Fenster **[!UICONTROL Schnellbearbeitung]** anzuzeigen.

   ![Das Fenster „Schnellbearbeitung“](./assets/image58.png){zoomable="yes"}

1. Wählen Sie einen Link aus, um Report Suites, Datumsbereiche oder Segmente zu aktualisieren. In **[!UICONTROL Schnellbearbeitung]** - **[!UICONTROL Segmente]** können Sie die Segmente für die ausgewählten Datenblöcke hinzufügen, entfernen oder aktualisieren.

   ![Das Feld Segment hinzufügen im Fenster „Schnellbearbeitung“](./assets/image59.png){zoomable="yes"}

## Datenblöcke aktualisieren

Wählen Sie ![Aktualisieren](/help/assets/icons/Refresh.svg), um die Datenblocktabelle zu aktualisieren.

Um zu überprüfen, ob ein Datenblock aktualisiert wurde, rufen Sie das Aktualisierungsstatus-Symbol auf:

- Ein erfolgreich aktualisierter Datenblock zeigt einen ![CheckmarkCircleGreen](/help/assets/icons/CheckmarkCircleGreen.svg) an.

- Bei einem Datenblock, der nicht aktualisiert werden konnte, wird ein ![AlertRed](/help/assets/icons/AlertRed.svg) angezeigt.


## Datenblöcke löschen

Löschen eines oder mehrerer Datenblöcke:

1. Einen oder mehrere Datenblöcke auswählen.
1. Wählen Sie ![Löschen](/help/assets/icons/Delete.svg) aus.
1. Wählen Sie **[!UICONTROL Dialogfeld]** Datenblock löschen **** oder **[!UICONTROL Abbrechen]**, um den Löschvorgang abzubrechen.

## Datenblöcke gruppieren

Sie können Datenblöcke mithilfe des Dropdown-Menüs **[!UICONTROL Gruppieren nach]** gruppieren oder einen Spaltentitel auswählen.

Um Datenblöcke nach Spalten zu sortieren, wählen Sie den Spaltentitel aus. Um Datenblöcke nach Gruppen zu gruppieren, wählen Sie einen Gruppennamen aus dem Dropdown-Menü **[!UICONTROL Gruppieren nach]** aus. Der folgende Screenshot zeigt beispielsweise Datenblöcke, die nach Report Suite gruppiert sind.

Sie können Gruppierung verwenden, um schnell Datenblöcke auszuwählen, für die Sie ein gemeinsames Element ändern möchten, z. B. ein Segment.

![Datenblock-Manager mit der Liste „Gruppieren nach Blatt“.](./assets/group-data-blocks.png){zoomable="yes"}



<!--

# Manage Data Blocks in Report Builder

You can view and manage all data blocks in a workbook using the Data Block Manager. The Data Block Manager provides search, filter, and sort capabilities that allow you to quickly locate specific data blocks. After selecting one or more data blocks, you can edit, delete, or refresh the selected data blocks.

![The Data block manager screen.](./assets/image52.png)

## View Data Blocks

Click **Manage** to view a list of all data blocks in a workbook.

![The Manage option to view a list of all data blocks.](./assets/image53.png)

The Data Block Manager lists all data blocks present in a workbook. 

## Sort the Data Blocks list

You can sort the data block list by a displayed column. For example, you can sort the data block list by report suites, segments, date range, and other variables.

To sort the data block list, click a column heading.

![Sorting the data blocks.](./assets/image54.png)

## Search the Data Block list

Use the Search field to locate anything in the data block table. For example, you could search for metrics contained in the data blocks or report suite. You can also search for dates appearing in the date range, date modified, or last run date columns.

![Using the Search field to locate anything in the data block table.](./assets/image55.png)

## Edit Data Blocks

You can edit the report suite, date range, or the segments applied to one or more data blocks.

For example, you can replace an existing segment with a new segment in one or more data blocks.

1. Select the data blocks that you want to update. You can select the top-level check box to select all data blocks or you can select individual data blocks.

   ![The pencil edit icon](./assets/image56.png)

1. Click the edit icon to display the Quick edit window.

   ![The Quick edit window](./assets/image58.png)

1. Select a segment link to update report suites, date ranges, or segments.

   ![The Add Segment field in the Quick edit window](./assets/image59.png)

## Refresh Data Blocks

Click the refresh icon to refresh the data blocks in the list.

<img src="./assets/refresh-icon.png" width="15%" alt="Refresh icon"/>

To verify if a data block is refreshed, view the refresh status icon. 

A successfully refreshed data block displays a checkmark in a green circle: <img src="./assets/refresh-success.png" width="5%" alt="Green circle with check mark icon"/>. 

A data block that has failed to refresh displays a warning icon: <img src="./assets/refresh-failure.png" width="5%" alt="Red triangle with exclamation mark icon"/>.This makes it easy to identify if any data blocks have errors.


![Data block manager showing refresh status for each data block listed.](./assets/image512.png)

## Delete a Data Block

1. Select a data block in the Data Block manager. 
1. Click the trash can icon to delete the selected data block.

## Group Data Blocks

You can group data blocks using the **Group by** drop-down menu or you can click a column title. To sort data blocks by column, click the column title. To group data blocks by groups, select a group name from the **Group by** drop-down menu. For example, the screenshot below shows data blocks grouped by Sheet. It shows data blocks grouped by Sheet1 and Sheet2.  This is useful, for example, in the segment-replacing use case. If you have multiple segments applied to each data block, it is helpful to create a group containing all the data blocks that you want to replace. Then you can easily select and edit them all at once.

![Data block manager showing the Group by Sheet list.](./assets/group-data-blocks.png)

## Modify the Data Block Manager view

You can modify which columns are visible in the Data Block Manager window.


Click the column list <img src="./assets/image515.png" width="3%" alt="Column list icon"/> icon to select which columns are listed in the Data Block Manager. Select a column name to display the column. Deselect the column name to remove the column from view.

![Data block manager showing the column list](./assets/image516.png)

-->