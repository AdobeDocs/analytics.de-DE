---
title: Konsolidierungs-Manager für Klassifizierungssatz
description: Konsolidieren Sie einen oder mehrere Klassifizierungssätze zu einem einzigen Klassifizierungssatz.
exl-id: 0be97ca4-56c3-4642-9347-924812e88e8c
feature: Classifications
source-git-commit: 5c2643a143e5c8e17fcf11cfa2da81183bc5c39a
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 6%

---

# Manager für Klassifizierungssatz-Konsolidierungen

Wenn Sie über mehrere Klassifizierungssätze verfügen, die ähnliche Daten enthalten, können Sie diese zu einem einzigen Klassifizierungssatz zusammenfassen. Wenn Sie zwei oder mehr Klassifizierungssätze zusammenfassen, generiert Adobe einen neuen Klassifizierungssatz, der alle Klassifizierungsdaten aus jedem einzelnen Klassifizierungssatz enthält. Konsolidierungen sind nützlich, wenn Sie Daten in viele Report Suites oder Dimensionen hochgeladen haben, die dieselben Klassifizierungsdaten enthalten, und sie zu einem einzigen Workflow zusammenführen möchten. Sie müssen Produktadministratorzugriff für Adobe Analytics haben, um den Konsolidierungs-Manager für Klassifizierungssätze anzeigen zu können.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Konsolidierungen]**

Sobald eine Konsolidierung ausgeführt wird, werden die ursprünglichen Klassifizierungssätze entfernt, wobei der konsolidierte Klassifizierungssatz an ihre Stelle tritt. Klicken Sie auf **[!UICONTROL Hinzufügen]**, um [Konsolidierung erstellen](process.md).

## Filtern von Klassifizierungssätzen

Auf der linken Seite des Konsolidierungs-Managers für Klassifizierungssätze finden Sie Filtereinstellungen, um die gewünschte Konsolidierung zu finden. Durch Klicken auf das Filtersymbol wird die Sichtbarkeit der Filtereinstellungen ein-/ausgeblendet. Sie können Konsolidierung nach **[!UICONTROL Status]**, **[!UICONTROL Abschlusszeit]** oder **[!UICONTROL Erstellungszeit]** filtern.

![Konsolidierungsfilter für Klassifizierungssätze](../../assets/classification-set-consolidation-filters.png)

Zusätzliche Filteroptionen sind über den Spalten des Konsolidierungs-Managers für Klassifizierungssätze verfügbar:

* **[!UICONTROL Suche nach Titel]**: Suchen nach Konsolidierungen anhand des Namens.
* **Spalten ein-/ausblenden**: Ein-/Ausschalten der Sichtbarkeit für eine beliebige Spalte außer [!UICONTROL Name].

## Konsolidierungs-Manager für Klassifizierungssatz

Die folgenden Spalten sind im Konsolidierungs-Manager für Klassifizierungssätze verfügbar:

* **[!UICONTROL Name]**: Der Name der Konsolidierung.
* **[!UICONTROL Aktueller Auftrag]**: Der aktuelle Auftrag. <!-- todo: better description -->
* **[!UICONTROL Status]**: Der Status der Konsolidierung. <!-- todo: get list of possible statuses -->
* **[!UICONTROL Erstellungsdatum]**: Datum und Uhrzeit der Erstellung der Konsolidierung.
* **[!UICONTROL Abschlussdatum]**: Datum und Uhrzeit des Abschlusses (oder Fehlschlagens) der Konsolidierung.
