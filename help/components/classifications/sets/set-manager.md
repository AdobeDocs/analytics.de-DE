---
title: Verwalten von Klassifizierungssätzen
description: Verwalten Sie Klassifizierungssätze in Adobe Analytics.
exl-id: b1a6721b-8e5d-4ee6-af6b-cda31c9f8b00
feature: Classifications
source-git-commit: cfa8335008548254786e46dfe634229edad5bd54
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
| **[!UICONTROL Klassifizierungssatz]** | Der Name des Klassifizierungssatzes. Wählen Sie den Namen aus[&#x200B; um den Klassifizierungssatz zu &#x200B;](create.md#edit-a-classification-set). |
| **[!UICONTROL Abonnements]** | Die Anzahl der Abonnements, für die der Klassifizierungssatz gilt. |
| **[!UICONTROL Klassifizierungen]** | Die Anzahl der Klassifizierungsdimensionen, die der Klassifizierungssatz enthält. |
| **[!UICONTROL Automated]** | Ist der Klassifizierungssatz so konfiguriert, dass Daten automatisch aus einem Cloud-Speicherort importiert werden oder nicht? Diese Automatisierung kann als Teil des Schemas [Klassifizierungssätze“ konfiguriert &#x200B;](manage/schema.md). |
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
| ![Umbenennen](/help/assets/icons/Rename.svg) | **[!UICONTROL Umbenennen]** | Benennen Sie einen Klassifizierungssatz um.<br/>Geben Sie im Dialogfeld **[!UICONTROL Umbenennen: _Klassifizierungssatz_]**&#x200B;einen neuen Namen ein und wählen Sie **[!UICONTROL Umbenennen]**. |
| ![Merge](/help/assets/icons/Merge.svg) | **[!UICONTROL Konsolidieren]** | [Konsolidieren Sie Klassifizierungssätze](/help/components/classifications/sets/consolidations/manage.md). |
| ![Löschen](/help/assets/icons/Delete.svg) | **[!UICONTROL Löschen]** | Löschen eines Klassifizierungssatzes.<br/>Der **[!UICONTROL Löschen _Klassifizierungssatz_?]** Dialogfeld wird angezeigt. Das Löschen eines Klassifizierungssatzes kann nicht rückgängig gemacht werden. Alle geplanten Projekte oder Konsolidierungen, die diesen Klassifizierungssatz verwenden, verwenden weiterhin die Definition dieses Klassifizierungssatzes, bis Sie die geplanten Projekte erneut speichern oder die geplanten Konsolidierungen erneut überprüfen. Wählen Sie **[!UICONTROL Löschen]** aus, um den Klassifizierungssatz zu löschen. |
| ![Beschriftung](/help/assets/icons/Label.svg) | **[!UICONTROL Tag]** | Kennzeichnen Sie den Klassifizierungssatz.<br/>Wählen Sie im Dialogfeld **[!UICONTROL Tag: _Klassifizierungssatz_]**&#x200B;ein oder mehrere Tags aus dem Dropdown-Menü&#x200B;**[!UICONTROL Tags]**&#x200B;aus, um Tags hinzuzufügen. Oder geben Sie ein oder mehrere neue Tags ein. Verwenden Sie ![CrossSize100](/help/assets/icons/CrossSize100.svg), um ein Tag zu entfernen. <br/>Wählen Sie **[!UICONTROL Speichern]**, um die Tags zu speichern. |


### Panel „Filter“

Wählen Sie ![Filter](/help/assets/icons/Filter.svg) aus, um die ➍ des Filterbedienfelds anzuzeigen, mit der Sie die Klassifizierungssatzliste filtern können. Sie können nach folgenden Kriterien filtern:

* **[!UICONTROL Tags]**: Wählen Sie ein oder mehrere Tags aus, um die Liste der Klassifizierungssätze nach Tags zu filtern.
* **[!UICONTROL Report Suite]**. Wählen Sie eine oder mehrere Report Suites aus, um die Liste der Klassifizierungssätze nach Report Suites zu filtern.

Wählen Sie ![Filter](/help/assets/icons/Filter.svg) **[!UICONTROL Filter ausblenden]** aus, um das Bedienfeld „Filter“ auszublenden.

Beachten Sie, dass die im Bedienfeld Filter angezeigten Filter die Optionen für die vorab geladenen Klassifizierungssätze widerspiegeln.
