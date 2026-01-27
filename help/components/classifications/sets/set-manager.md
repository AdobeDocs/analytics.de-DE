---
title: Verwalten von Klassifizierungssätzen
description: Verwalten Sie Klassifizierungssätze in Adobe Analytics.
exl-id: b1a6721b-8e5d-4ee6-af6b-cda31c9f8b00
feature: Classifications
source-git-commit: d5e1432569516d13d2de30a2cb30cebb067ab783
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 5%

---

# Verwalten von Klassifizierungssätzen

Sie können Klassifizierungssätze in der Verwaltungsoberfläche für Klassifizierungssätze erstellen, umbenennen, bearbeiten, konsolidieren, löschen und taggen. Sie können auch nach bestimmten Klassifizierungssätzen filtern und diese suchen.

So verwalten Sie Klassifizierungssätze:

1. Wählen Sie **[!UICONTROL Komponenten]** in der oberen Menüleiste von Adobe Analytics aus und wählen Sie dann **[!UICONTROL Klassifizierungssätze]**.
1. Wählen **[!UICONTROL unter]** die Registerkarte **[!UICONTROL Klassifizierungssätze]** aus.

## Classification Sets Manager

Der **[!UICONTROL Classification Sets]**-Manager verfügt über die folgenden Elemente der Benutzeroberfläche:

![Classification Sets Manager](assets/classification-sets-manage.png)


### Liste der Klassifizierungssätze

Die **[!UICONTROL Klassifizierungssätze]** Liste ➊ zeigt alle Klassifizierungssätze an. Die Liste umfasst die folgenden Spalten:

| Spalte | Beschreibung |
|---|---|
| **[!UICONTROL Klassifizierungssatz]** | Der Name des Klassifizierungssatzes. Wählen Sie den Namen aus[ um den Klassifizierungssatz zu ](create.md#edit-a-classification-set). |
| **[!UICONTROL Abonnements]** | Die Anzahl der Abonnements, für die der Klassifizierungssatz gilt. |
| **[!UICONTROL Klassifizierungen]** | Die Anzahl der Klassifizierungsdimensionen, die der Klassifizierungssatz enthält. |
| **[!UICONTROL Automated]** | Ist der Klassifizierungssatz so konfiguriert, dass Daten automatisch aus einem Cloud-Speicherort importiert werden oder nicht? Diese Automatisierung kann als Teil des Schemas [Klassifizierungssätze“ konfiguriert ](manage/schema.md). |
| **[!UICONTROL Zuletzt geändert]** | Der Zeitstempel der letzten Änderung des Klassifizierungssatzes. |

So ändern Sie die Größe einer Spalte in der Liste der Klassifizierungssätze:

* Bewegen Sie den Mauszeiger über das Spaltentrennzeichen und ziehen Sie das Spaltentrennzeichen auf die gewünschte Spaltenbreite.
* Wählen Sie ![ChevronDown](/help/assets/icons/ChevronDown.svg) und wählen Sie **[!UICONTROL Spaltengröße ändern]**. Mit einer vertikalen Linie mit der Schaltfläche Größe ändern können Sie die Größe der Spalte in das gewünschte Format ändern.

So sortieren Sie eine Spalte in der Liste der Klassifizierungssätze

* Wählen Sie ![ChevronDown](/help/assets/icons/ChevronDown.svg) und wählen Sie **[!UICONTROL Aufsteigend sortieren]** oder **[!UICONTROL Absteigend sortieren]**. Ein Pfeil (↑↓) gibt an, welche Spalte sortiert ist.

### Suchen und Schaltflächen

Im Bereich ➋ oben in der Liste der Klassifizierungssätze haben Sie folgende Möglichkeiten:

* Suchen ![Suchen](/help/assets/icons/Search.svg) nach Klassifizierungssätzen. Die Ergebnisse werden in der Liste der Klassifizierungssätze angezeigt. Wählen ![CrossSize200](/help/assets/icons/CrossSize200.svg) aus, um die Suche zu löschen.
* Entfernen Sie alle Filter, die auf die Liste der Klassifizierungssätze angewendet werden. Wählen Sie ![CrossSize100](/help/assets/icons/CrossSize100.svg) aus, um einen Filter zu entfernen.
* Wählen Sie ![MoreCircle](/help/assets/icons/MoreCircle.svg) aus, um weitere 1000 Klassifizierungssätze zu laden. Zunächst werden in der Liste der Klassifizierungssätze bis zu 1000 Klassifizierungssätze angezeigt.
* Wählen Sie ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL New]** aus, [einen neuen Klassifizierungssatz zu erstellen](create.md#create-a-classification-set).
* Definieren Sie die Spalten der Klassifizierungssatzliste. Wählen Sie ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) aus und wählen Sie im Dialogfeld **[!UICONTROL Tabelle anpassen]** die Spalten aus, die unter **[!UICONTROL Select columns to show]**. Wählen Sie **[!UICONTROL Anwenden]** aus, um die Spalteneinstellungen anzuwenden.


### Aktionsleiste

Wenn Sie einen oder mehrere Klassifizierungssätze in der Klassifizierungssatz-Liste auswählen, wird eine blaue Aktionsleiste ➌. Die folgenden Aktionen sind in der Aktionsleiste verfügbar:

| Symbol | Aktion | Beschreibung |
|---|---|---|
| ![Bearbeiten](/help/assets/icons/Edit.svg) | **[!UICONTROL Bearbeiten]** | [Bearbeiten Sie den Klassifizierungssatz](create.md#edit-a-classification-set) im Classification Set Builder. |
| ![Umbenennen](/help/assets/icons/Rename.svg) | **[!UICONTROL Umbenennen]** | Benennen Sie einen Klassifizierungssatz um.<br/>Geben Sie im Dialogfeld **[!UICONTROL Umbenennen: _Klassifizierungssatz_]**einen neuen Namen ein und wählen Sie **[!UICONTROL Umbenennen]**. |
| ![Merge](/help/assets/icons/Merge.svg) | **[!UICONTROL Konsolidieren]** | [Konsolidieren Sie Klassifizierungssätze](/help/components/classifications/sets/consolidations/manage.md). |
| ![Löschen](/help/assets/icons/Delete.svg) | **[!UICONTROL Löschen]** | Löschen eines Klassifizierungssatzes.<br/>Der **[!UICONTROL Löschen _Klassifizierungssatz_?]** Dialogfeld wird angezeigt. Das Löschen eines Klassifizierungssatzes kann nicht rückgängig gemacht werden. Alle geplanten Projekte oder Konsolidierungen, die diesen Klassifizierungssatz verwenden, verwenden weiterhin die Definition dieses Klassifizierungssatzes, bis Sie die geplanten Projekte erneut speichern oder die geplanten Konsolidierungen erneut überprüfen. Wählen Sie **[!UICONTROL Löschen]** aus, um den Klassifizierungssatz zu löschen. |
| ![Beschriftung](/help/assets/icons/Label.svg) | **[!UICONTROL Tag]** | Kennzeichnen Sie den Klassifizierungssatz.<br/>Wählen Sie im Dialogfeld **[!UICONTROL Tag: _Klassifizierungssatz_]**ein oder mehrere Tags aus dem Dropdown-Menü&#x200B;**[!UICONTROL Tags]**aus, um Tags hinzuzufügen. Oder geben Sie ein oder mehrere neue Tags ein. Verwenden Sie ![CrossSize100](/help/assets/icons/CrossSize100.svg), um ein Tag zu entfernen. <br/>Wählen Sie **[!UICONTROL Speichern]**, um die Tags zu speichern. |


### Panel „Filter“

Wählen Sie ![Filter](/help/assets/icons/Filter.svg) aus, um die ➍ des Filterbedienfelds anzuzeigen, mit der Sie die Klassifizierungssatzliste filtern können. Sie können nach folgenden Kriterien filtern:

* **[!UICONTROL Tags]**: Wählen Sie ein oder mehrere Tags aus, um die Liste der Klassifizierungssätze nach Tags zu filtern.
* **[!UICONTROL Report Suite]**. Wählen Sie eine oder mehrere Report Suites aus, um die Liste der Klassifizierungssätze nach Report Suites zu filtern.

Wählen Sie ![Filter](/help/assets/icons/Filter.svg) **[!UICONTROL Filter ausblenden]** aus, um das Bedienfeld „Filter“ auszublenden.

Beachten Sie, dass die im Bedienfeld Filter angezeigten Filter die Optionen für die vorab geladenen Klassifizierungssätze widerspiegeln.


<!-- old content

The Classification set manager allows you to create, edit, or delete classification sets.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]**

Classification sets consist of **Subscriptions** (report suite and dimension combinations) and **Classification names** (dimensions containing classification data). Subscriptions are configured under [Settings](settings.md), while classification names are configured under [Schema](schema.md).

## Filter classification sets

The left side of the Classification set manager provides filter settings to locate the desired classification set. Clicking the filter icon toggles the filter settings visibility. You can filter classification sets by **[!UICONTROL Tags]** or **[!UICONTROL Report suite]**.

![Classification set filters](../../assets/classification-set-filters.png)

Note that 1,000 classification sets are preloaded at a time. The filters shown in the left rail reflect the options for the sets that are preloaded.

## Classification set manager columns

The following columns are available in the Classification set manager:

* **[!UICONTROL Classification set]**: The classification set name. Clicking a classification set name edits its [settings](settings.md).
* **[!UICONTROL Subscriptions]**: The number of subscriptions that this classification set applies to.
* **[!UICONTROL Classifications]**: The number of classification dimensions that the classification set contains.
* **[!UICONTROL Automated]**: Determines if the classification set is configured to automatically import data from a cloud location. Automation can be configured in the classification set's [schema](schema.md).
* **[!UICONTROL Last Modified]**: The date and time that the classification set was last modified.

## Create or edit options

The following buttons are available in the Classification set manager:

* **[!UICONTROL Add]**: [Create](create.md) a classification set.
* **[!UICONTROL Search by title]**: Search for classification sets by name.
* **[!UICONTROL Load more]**: The Classification set manager initially displays up to 1000 classification sets. This button loads 1000 more classification sets.
* **Show/Hide columns**: Toggle visibility for any column besides [!UICONTROL Classification set].

Select one or more classification sets by clicking the checkbox next to the desired classification set. Selecting a classification set reveals the following options:

* **[!UICONTROL Tag]**: Add one or more tags to the selected classification sets, which allows you to organize or group classification sets to make them easier to locate in the future.
* **[!UICONTROL Delete]**: Deletes the classification set. Classification dimensions based on this classification set are no longer available. Scheduled projects using the deleted classification set continue using dependent dimensions until you resave the scheduled project.
* **[!UICONTROL Consolidate]**: Start a new [consolidation](../consolidations/process.md).
* **[!UICONTROL Rename]**: Rename the selected classification set.

-->