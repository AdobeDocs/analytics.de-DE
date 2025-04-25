---
title: Klassifizierungssatz-Manager
description: Verwalten Sie Klassifizierungssätze in Adobe Analytics.
exl-id: b1a6721b-8e5d-4ee6-af6b-cda31c9f8b00
feature: Classifications
source-git-commit: a2a5e29eee46840d894ebf8d6184f8d6af9eee29
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 7%

---

# Klassifizierungssatz-Manager

Mit dem Classification Set Manager können Sie Klassifizierungssätze erstellen, bearbeiten oder löschen.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]**

Klassifizierungssätze bestehen aus **Abonnements** (Kombinationen aus Report Suite und Dimension) und **Klassifizierungsnamen** (Dimensionen, die Klassifizierungsdaten enthalten). Abonnements werden unter [Einstellungen](settings.md) konfiguriert, während Klassifizierungsnamen unter [Schema](schema.md) konfiguriert werden.

## Filtern von Klassifizierungssätzen

Auf der linken Seite des Classification Set Manager finden Sie Filtereinstellungen, um den gewünschten Klassifizierungssatz zu finden. Durch Klicken auf das Filtersymbol wird die Sichtbarkeit der Filtereinstellungen ein-/ausgeblendet. Sie können Klassifizierungssätze nach **[!UICONTROL Tags]** oder **[!UICONTROL Report Suite)]**.

![Klassifizierungssatzfilter](../../assets/classification-set-filters.png)

Beachten Sie, dass jeweils 1.000 Klassifizierungssätze vorgeladen werden. Die in der linken Leiste angezeigten Filter spiegeln die Optionen für die Sätze wider, die vorgeladen werden.

## Classification Set Manager-Spalten

Die folgenden Spalten sind im Classification Set Manager verfügbar:

* **[!UICONTROL Klassifizierungssatz]**: Der Name des Klassifizierungssatzes. Wenn Sie auf den Namen eines Klassifizierungssatzes klicken [ dessen Einstellungen ](settings.md).
* **[!UICONTROL Abonnements]**: Die Anzahl der Abonnements, für die dieser Klassifizierungssatz gilt.
* **[!UICONTROL Klassifizierungen]**: Die Anzahl der Klassifizierungsdimensionen, die der Klassifizierungssatz enthält.
* **[!UICONTROL Automated]**: Bestimmt, ob der Klassifizierungssatz so konfiguriert ist, dass Daten automatisch aus einem Cloud-Speicherort importiert werden. Die Automatisierung kann im (Schema) des Klassifizierungssatzes [ werden](schema.md).
* **[!UICONTROL Zuletzt geändert]**: Datum und Uhrzeit der letzten Änderung des Klassifizierungssatzes.

## Erstellen oder Bearbeiten von Optionen

Die folgenden Schaltflächen sind im Classification Set Manager verfügbar:

* **[!UICONTROL Hinzufügen]**: [Erstellen](create.md) eines Klassifizierungssatzes.
* **[!UICONTROL Suche nach Titel]**: Suchen nach Klassifizierungssätzen nach Namen.
* **[!UICONTROL Mehr laden]**: Der Classification Set Manager zeigt zunächst bis zu 1000 Klassifizierungssätze an. Mit dieser Schaltfläche werden 1000 weitere Klassifizierungssätze geladen.
* **Spalten ein-/ausblenden**: Ein-/Ausschalten der Sichtbarkeit für eine beliebige Spalte außer [!UICONTROL Klassifizierungssatz].

Wählen Sie einen oder mehrere Klassifizierungssätze aus, indem Sie auf das Kontrollkästchen neben dem gewünschten Klassifizierungssatz klicken. Bei Auswahl eines Klassifizierungssatzes werden die folgenden Optionen angezeigt:

* **[!UICONTROL Tag]**: Fügen Sie ein oder mehrere Tags zu den ausgewählten Klassifizierungssätzen hinzu, um Klassifizierungssätze zu organisieren oder zu gruppieren, damit sie später leichter zu finden sind.
* **[!UICONTROL Löschen]**: Löscht den Klassifizierungssatz. Klassifizierungsdimensionen, die auf diesem Klassifizierungssatz basieren, sind nicht mehr verfügbar. Geplante Projekte, die den gelöschten Klassifizierungssatz verwenden, verwenden weiterhin abhängige Dimensionen, bis das geplante Projekt erneut gespeichert wird.
* **[!UICONTROL Konsolidieren]**: Beginnen Sie eine neue [Konsolidierung](../consolidations/process.md).
* **[!UICONTROL Umbenennen]**: Umbenennen des ausgewählten Klassifizierungssatzes.
