---
title: Verwalten von Konsolidierung von Klassifizierungssätzen
description: Erfahren Sie, wie Sie einen oder mehrere Klassifizierungssätze zu einem einzigen Klassifizierungssatz zusammenfassen.
exl-id: 0be97ca4-56c3-4642-9347-924812e88e8c
feature: Classifications
source-git-commit: 77599d015ba227be25b7ebff82ecd609fa45a756
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 3%

---

# Verwalten von Klassifizierungskonsolidierungen

Wenn Sie über mehrere Klassifizierungssätze verfügen, die ähnliche Klassifizierungsdaten enthalten, können Sie diese zu einem einzigen Klassifizierungssatz zusammenfassen. Wenn Sie zwei oder mehr Klassifizierungssätze zusammenfassen, generiert Adobe einen neuen Klassifizierungssatz, der alle Klassifizierungsdaten aus jedem einzelnen Klassifizierungssatz enthält. Konsolidierungen sind nützlich, wenn Sie Daten in viele Report Suites hochgeladen haben. Oder wenn Sie Dimensionen haben, die dieselben Klassifizierungsdaten enthalten, und sie zu einem einzigen Workflow zusammenführen möchten.

Sie müssen Produktadministratorzugriff für Adobe Analytics haben, um den Konsolidierungs-Manager für Klassifizierungssätze anzeigen zu können.



So verwalten Sie Klassifizierungskonsolidierungen:

1. Wählen Sie **[!UICONTROL Hauptbenutzeroberfläche]** Komponenten“ aus und klicken Sie auf **[!UICONTROL Klassifizierungssätze]**.
1. Wählen **[!UICONTROL unter]** die Registerkarte **[!UICONTROL Konsolidierungen]** aus.


## Classification Consolidations Manager

Der **[!UICONTROL Classification Sets - Konsolidierungs]**-Manager verfügt über die folgenden Elemente der Benutzeroberfläche:

![Klassifizierungssätze - Konsolidierungs-Manager](assets/classifications-sets-consolidations.png)



### Klassifizierungskonsolidierungsliste

Die ➊ zeigt Klassifizierungskonsolidierungen an, die erstellt und validiert wurden und möglicherweise konsolidiert werden. Die Liste umfasst die folgenden Spalten:

| Spalte | Beschreibung |
|---|---|
| **[!UICONTROL Konsolidierungsname]** | Der Name der Konsolidierung der Klassifizierungssätze. |
| **[!UICONTROL Aktueller Auftrag]** | Der mit der Konsolidierung der Klassifizierungssätze verknüpfte Vorgang. |
| **[!UICONTROL Status]** | Der Status der Konsolidierung der Klassifizierungssätze. Mögliche Werte sind: **[!UICONTROL Erstellt]**, **[!UICONTROL Abgebrochen]**, **[!UICONTROL Abbruch]**, **[!UICONTROL Validierung]**, **[!UICONTROL Validierung]**, **[!UICONTROL Validiert]**, **[!UICONTROL Vergleich]**, **[!UICONTROL Vergleich]**, **[!UICONTROL Konsolidierung]**, **[!UICONTROL Übergeben]**, **&#x200B;**, Konsolidierung fehlgeschlagen **[!UICONTROL ,Konsolidierung]**&#x200B;**[!UICONTROL ,]**&#x200B;**&#x200B;**, **[!UICONTROL Validierung]** **&#x200B;**&#x200B;**&#x200B;**, |
| **[!UICONTROL Erstellungszeit]** | Die Erstellungszeit der Konsolidierung der Klassifizierungssätze. |
| **[!UICONTROL Abschlusszeit]** | Die Abschlusszeit der Klassifizierungskonsolidierungen. |


Um die Größe einer Spalte in der Klassifizierungskonsolidierungsliste zu ändern, haben Sie folgende Möglichkeiten:

* Bewegen Sie den Mauszeiger über das Spaltentrennzeichen und ziehen Sie das Spaltentrennzeichen auf die gewünschte Spaltenbreite.
* Wählen Sie ![ChevronDown](/help/assets/icons/ChevronDown.svg) und wählen Sie **[!UICONTROL Spaltengröße ändern]**. Mit einer vertikalen Linie mit der Schaltfläche Größe ändern können Sie die Größe der Spalte in das gewünschte Format ändern.

So sortieren Sie eine Spalte in der Klassifizierungskonsolidierungsliste

* Wählen Sie ![ChevronDown](/help/assets/icons/ChevronDown.svg) und wählen Sie **[!UICONTROL Aufsteigend sortieren]** oder **[!UICONTROL Absteigend sortieren]**. Ein Pfeil (↑↓) gibt an, welche Spalte sortiert ist.

### Suchen und Schaltflächen

Im Bereich ➋ oben in der Liste der Klassifizierungskonsolidierungen haben Sie folgende Möglichkeiten:

* Suchen ![Suchen](/help/assets/icons/Search.svg) nach Klassifizierungskonsolidierungen. Die Ergebnisse werden in der Liste der Klassifizierungskonsolidierungen angezeigt. Wählen ![CrossSize200](/help/assets/icons/CrossSize200.svg) aus, um die Suche zu löschen.
* Entfernen Sie alle Filter, die auf die Konsolidierungsliste für Klassifizierungssätze angewendet werden. Wählen Sie ![CrossSize100](/help/assets/icons/CrossSize100.svg) aus, um einen Filter zu entfernen.
* Erstellen Sie eine Konsolidierung neuer Klassifizierungssätze. Wählen Sie ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL New]** aus, um das Dialogfeld für die Konsolidierung von Klassifizierungssätzen zu öffnen und eine neue Konsolidierung von Klassifizierungssätzen zu definieren.
* Definieren Sie die Spalten der Liste Klassifizierungskonsolidierungen . Wählen Sie ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) aus und wählen Sie im Dialogfeld **[!UICONTROL Tabelle anpassen]** die Spalten aus, die unter **[!UICONTROL Select columns to show]**. Wählen Sie **[!UICONTROL Anwenden]** aus, um die Spalteneinstellungen anzuwenden.


### Aktionsleiste

Wenn Sie einen oder mehrere Klassifizierungssätze in der Klassifizierungssatz-Liste auswählen, wird eine blaue Aktionsleiste ➌. Die folgenden Aktionen sind in der Aktionsleiste verfügbar:

| Symbol | Aktion | Beschreibung |
|---|---|---|
| ![Bearbeiten](/help/assets/icons/Edit.svg) | **[!UICONTROL Bearbeiten]** | [Bearbeiten Sie die Konsolidierung der Klassifizierungssätze](process.md#edit-a-consolidation) |
| ![ViewDetail](/help/assets/icons/ViewDetail.svg) | **[!UICONTROL Ansicht]** | Details zur Konsolidierung des Klassifizierungssatzes anzeigen. Je nach Status können Sie [&#x200B; Konsolidierung &#x200B;](process.md#approve) oder [abbrechen](process.md#cancel). |


### Panel „Filter“

Wählen Sie ![Filter](/help/assets/icons/Filter.svg) aus, um die ➍ des Filterbedienfelds anzuzeigen, mit der Sie die Liste der Klassifizierungskonsolidierungen filtern können. Sie können nach folgenden Kriterien filtern:

* **[!UICONTROL Status]**. Wählen Sie einen der möglichen Werte aus, um die Liste der Klassifizierungskonsolidierungen nach Status zu filtern. |
* **[!UICONTROL Abschlusszeit]**. Wählen Sie einen der möglichen Werte aus, um die Liste der Klassifizierungskonsolidierungen nach Fertigstellungszeit zu filtern.
* **[!UICONTROL Erstellungszeit]**. Wählen Sie einen der möglichen Werte aus, um die Liste der Klassifizierungskonsolidierungen nach Fertigstellungszeit zu filtern.


Wählen Sie ![Filter](/help/assets/icons/Filter.svg) **[!UICONTROL Filter ausblenden]** aus, um das Bedienfeld „Filter“ auszublenden.

Beachten Sie, dass die im Bedienfeld Filter angezeigten Filter die Optionen für die vorab geladenen Klassifizierungskonsolidierungen widerspiegeln.


<!--

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Consolidations]**

Once a consolidation is run, the original classification sets are removed, with the consolidated classification set taking their place. Click **[!UICONTROL Add]** to [Create a consolidation](process.md).

## Filter classification sets

The left side of the Classification set consolidation manager provides filter settings to locate the desired consolidation. Clicking the filter icon toggles the filter settings visibility. You can filter consolidations by **[!UICONTROL Status]**, **[!UICONTROL Completion time]**, or **[!UICONTROL Creation time]**.

![Classification set consolidation filters](../../assets/classification-set-consolidation-filters.png)

Additional filter options are available above the Classification set consolidation manager columns:

* **[!UICONTROL Search by title]**: Search for consolidations by name.
* **Show/Hide columns**: Toggle visibility for any column besides [!UICONTROL Name].

## Classification set consolidation manager columns

The following columns are available in the Classification set consolidation manager:

* **[!UICONTROL Name]**: The name of the consolidation.
* **[!UICONTROL Current job]**: The current job. 
* **[!UICONTROL Status]**: The status of the consolidation. 
* **[!UICONTROL Creation date]**: The date and time that the consolidation was created.
* **[!UICONTROL Completion date]**: The date and time that the consolidation completed (or failed).

-->
