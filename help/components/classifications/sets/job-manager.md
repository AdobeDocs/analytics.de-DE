---
title: Classification Jobs Manager
description: Erfahren Sie, wie Sie aktuelle und abgeschlossene Klassifizierungsaufträge anzeigen, die aus Klassifizierungssätzen generiert wurden.
exl-id: 0470e131-79c6-4906-85f0-530d360ac227
feature: Classifications
source-git-commit: 2ced7cd61c4119347be2ef0fba9b8d60ee6c4df2
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 2%

---

# Anzeigen von und Ausführen von Klassifizierungsaufträgen

Der Classification Jobs Manager zeigt aktuelle und abgeschlossene Klassifizierungsaufträge an, die für Klassifizierungssätze generiert werden. Sie können den Manager auch verwenden, um Klassifizierungsdaten oder Vorlagen für einen bestimmten Auftrag herunterzuladen.

So zeigen Sie Klassifizierungsaufträge an und führen Aktionen für sie durch:


1. Wählen Sie **[!UICONTROL Komponenten]** in der oberen Menüleiste von Adobe Analytics aus und wählen Sie dann **[!UICONTROL Klassifizierungssätze]**.
1. Wählen **[!UICONTROL unter]** die Registerkarte **[!UICONTROL Vorgänge]** aus.

## Classification Jobs Manager

Der **[!UICONTROL Klassifizierungssätze - Aufträge]** Manager verfügt über die folgenden Elemente der Benutzeroberfläche:

![Klassifizierungssätze - Job Manager](manage/assets/classifications-sets-jobs.png)



### Liste der Klassifizierungsaufträge

Die **[!UICONTROL Klassifizierungsaufträge]** Liste ➊ zeigt Klassifizierungsaufträge an. Die Liste umfasst die folgenden Spalten:

| Spalte | Beschreibung |
|---|---|
| **[!UICONTROL Vorgangs-ID]** | Die Kennung des Klassifizierungsauftrags. |
| **[!UICONTROL Klassifizierungssatz]** | Der Klassifizierungssatz, der mit dem Klassifizierungsvorgang verknüpft ist. |
| **[!UICONTROL size]** | Die Größe der Datei, die als Teil des Klassifizierungsauftrags exportiert oder importiert wurde. |
| **[!UICONTROL Status]** | Der Status des Klassifizierungsauftrags. Mögliche Werte sind: **[!UICONTROL Erstellt]**, **[!UICONTROL In Warteschlange]**, **[!UICONTROL Validiert]**, **[!UICONTROL Fehlgeschlagene Validierung]**, **[!UICONTROL Verarbeitung]**, **[!UICONTROL Verarbeitung]**, **[!UICONTROL Fehlgeschlagene Verarbeitung]** , **[!UICONTROL Abgeschlossen]** oder **[!UICONTROL Fortschritt]**. Bewegen Sie gegebenenfalls den Mauszeiger über den Warnhinweis ![Warnhinweis](/help/assets/icons/Alert.svg), um zusätzliche Informationen anzuzeigen. |
| **[!UICONTROL Dateiname]** | Gibt den Namen oder die Funktion an, die zum Importieren oder Exportieren der Datei als Teil des Klassifizierungsauftrags verwendet wird. Mögliche Werte sind: <ul><li>*kein Wert*</li><li>Der Name der Datei, die als Teil des Klassifizierungsauftrags verarbeitet wird.</li><li>**[!UICONTROL SAINT-Export]**: Der Vorgang ist ein Export aus der [Legacy-Klassifizierungsschnittstelle](/help/components/classifications/importer/c-working-with-saint.md).</li><li>**[!UICONTROL Export für _Klassifizierungssatz_ bei _Zeitstempel_]**: Der Auftrag ist ein Download aus der [schema](manage/schema.md#download)-Oberfläche.</li></ul> |
| **[!UICONTROL Vorgangstyp]** | Der Typ des Klassifizierungsauftrags. Mögliche Werte sind: **[!UICONTROL Import]** oder **[!UICONTROL Export]**. |
| **[!UICONTROL Quelle]** | Die Quelle des Klassifizierungsauftrags. Mögliche Werte sind: **[!UICONTROL Web-API]**, **[!UICONTROL Direct API Upload]**, **[!UICONTROL Adobe]**, **[!UICONTROL SAINT]** oder **[!UICONTROL Unknown]**. |
| **[!UICONTROL Geänderte Zeilen]** | Die Anzahl der geänderten Zeilen, die der Klassifizierungsauftrag geändert hat. |
| **[!UICONTROL Zeilen insgesamt]** | Die Anzahl der Zeilen insgesamt, die der Klassifizierungsvorgang verarbeitet hat. |
| **[!UICONTROL Abschlusszeit]** | Die Abschlusszeit des Klassifizierungsauftrags. |
| **[!UICONTROL Datei-Download]** | Verwenden Sie ![Herunterladen](/help/assets/icons/Download.svg), um die Datei (Vorlage oder Daten) herunterzuladen, die mit dem Klassifizierungsauftrag verknüpft sind. |

Um die Größe einer Spalte in der Liste der Klassifizierungsaufträge zu ändern, haben Sie folgende Möglichkeiten:

* Bewegen Sie den Mauszeiger über das Spaltentrennzeichen und ziehen Sie das Spaltentrennzeichen auf die gewünschte Spaltenbreite.
* Wählen Sie ![ChevronDown](/help/assets/icons/ChevronDown.svg) und wählen Sie **[!UICONTROL Spaltengröße ändern]**. Mit einer vertikalen Linie mit der Schaltfläche Größe ändern können Sie die Größe der Spalte in das gewünschte Format ändern.

So sortieren Sie eine Spalte in der Liste der Klassifizierungsaufträge

* Wählen Sie ![ChevronDown](/help/assets/icons/ChevronDown.svg) und wählen Sie **[!UICONTROL Aufsteigend sortieren]** oder **[!UICONTROL Absteigend sortieren]**. Ein Pfeil (↑↓) gibt an, welche Spalte sortiert ist.


### Suchen und Schaltflächen

In dem Bereich, der über der Liste der Klassifizierungsaufträge ➋, haben Sie folgende Möglichkeiten:

* Suchen ![Suchen](/help/assets/icons/Search.svg) nach Klassifizierungsaufträgen. Die Ergebnisse werden in der Liste der Klassifizierungsaufträge angezeigt. Wählen ![CrossSize200](/help/assets/icons/CrossSize200.svg) aus, um die Suche zu löschen.
* Entfernen Sie alle Filter, die auf die Liste der Klassifizierungsaufträge angewendet werden. Wählen Sie ![CrossSize100](/help/assets/icons/CrossSize100.svg) aus, um einen Filter zu entfernen.
* Wählen Sie ![MoreCircle](/help/assets/icons/MoreCircle.svg) aus, um weitere 1000 Klassifizierungsaufträge zu laden. Zunächst werden in der Liste der Klassifizierungssätze bis zu 1000 Klassifizierungsaufträge angezeigt.
* Definieren Sie die Spalten der Auftragsliste für Klassifizierungssätze. Wählen Sie ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) aus und wählen Sie im Dialogfeld **[!UICONTROL Tabelle anpassen]** die Spalten aus, die unter **[!UICONTROL Select columns to show]**. Wählen Sie **[!UICONTROL Anwenden]** aus, um die Spalteneinstellungen anzuwenden.



### Panel „Filter“

Wählen Sie ![Filter](/help/assets/icons/Filter.svg) aus, um die ➌ des Filterbedienfelds anzuzeigen, mit der Sie die Liste der Klassifizierungsaufträge filtern können. Sie können nach folgenden Kriterien filtern:

* **[!UICONTROL Klassifizierungssatz]**. Wählen Sie einen oder mehrere Klassifizierungssätze aus, um die Liste der Klassifizierungsaufträge zu filtern.
* **[!UICONTROL Abschlusszeit]**. Wählen Sie einen der möglichen Werte aus, um die Liste der Klassifizierungsaufträge nach Abschlusszeit zu filtern.
* **[!UICONTROL Status]**. Wählen Sie einen der möglichen Werte aus, um die Liste der Klassifizierungsaufträge nach Status zu filtern.
* **[!UICONTROL Vorgangstyp]**. Wählen Sie einen der möglichen Werte aus, um die Liste der Klassifizierungsaufträge nach Auftragstyp zu filtern.
* **[!UICONTROL Source]**. Wählen Sie einen der möglichen Werte aus, um die Liste der Klassifizierungsaufträge nach der Quelle zu filtern.


Wählen Sie ![Filter](/help/assets/icons/Filter.svg) **[!UICONTROL Filter ausblenden]** aus, um das Bedienfeld „Filter“ auszublenden.

Beachten Sie, dass die im Bedienfeld Filter angezeigten Filter die Optionen für die vorab geladenen Klassifizierungsaufträge widerspiegeln.


<!--

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Jobs]**

You cannot create jobs from this interface. Create jobs by uploading data to a classification set (either manually or through a configured external location), requesting a download file, or requesting a template file.

## Filter classification sets

The left side of the Classification set job manager provides filter settings to locate the desired job. Clicking the filter icon toggles the filter settings visibility. You can filter Classification sets by **[!UICONTROL Classification set]**, **[!UICONTROL Completion time]**, **[!UICONTROL Status]**, **[!UICONTROL Job Type]**, or **[!UICONTROL Source]**.

![Classification set job filters](../assets/classification-set-job-filters.png)

Additional filter options are available above the Classification set job manager columns:

* **[!UICONTROL Search by title]**: Search for jobs by filename.
* **[!UICONTROL Load more]**: The Classification set job manager initially displays up to 1000 jobs. If more jobs exist, click this button to load 1000 more jobs.
* **Show/Hide columns**: Toggle visibility for any column besides [!UICONTROL Filename] and [!UICONTROL Completion time].

## Classification set job manager columns

The following columns are available in the Classification set job manager:

* **[!UICONTROL Filename]**: The name of the upload or download file.
* **[!UICONTROL Classification set]**: The name of the Classification set that the file applies to. You can click the Classification set name to reach the Classification set's [Settings](manage/settings.md).
* **[!UICONTROL Size]**: The size of the file.
* **[!UICONTROL Status]**: The status of the job processing the file.
  * **[!UICONTROL Created]**: The job was submitted.
  * **[!UICONTROL Queued]**: The file is ready to be processed, and is waiting for a classification server to process the file.
  * **[!UICONTROL Validated]**: The file is valid and is waiting to be processed.
  * **[!UICONTROL Failed validation]**: The file is formatted incorrectly or otherwise invalid. The file does not go through processing.
  * **[!UICONTROL Processing]**: The file is actively being processed by Adobe.
  * **[!UICONTROL Failed processing]**: The file failed processing.
  * **[!UICONTROL Complete]**: Processing is complete. Classification data is visible in reporting.
  * **[!UICONTROL Failed]**: Generic failure not related to validation or processing.
* **[!UICONTROL Job type]**: The type of job.
* **[!UICONTROL Source]**: The job source.
* **[!UICONTROL File download]**: Only applies to download jobs, such as downloading classification data or downloading templates. When a download is ready, this column provides a download link.
* **[!UICONTROL Modified lines]**: The number of modified lines.
* **[!UICONTROL Completed lines]**: The number of completed lines.
* **[!UICONTROL Completion time]**: The date and time that the job completed (or failed).
-->