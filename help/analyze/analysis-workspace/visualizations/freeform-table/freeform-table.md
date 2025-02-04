---
title: Freiformtabelle
description: Freiformtabellen sind die Grundlage für die Analyse von Daten in Workspace
feature: Freeform Tables
role: User, Admin
exl-id: 7a0432f9-2cab-47be-bbd6-ede96cb840a3
source-git-commit: bb3e8b030af78f0d7758b4cff41d66f20695e11e
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 25%

---

# Freiformtabelle {#freeform-table-overview}


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_button"
>title="Freiformtabelle"
>abstract="Erstellen Sie eine leere Visualisierung einer Freiformtabelle, die Sie mithilfe von Dimensionen, Segmenten, Metriken und Datumsbereichen gestalten können. Sie können die Freiformtabelle als Grundlage für andere Visualisierungen verwenden."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_In diesem Artikel wird die Freiformtabellen-Visualisierung in {_}![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_Siehe [Freiformtabelle](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/freeform-table/freeform-table) für die_![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**-Version dieses Artikels._

>[!ENDSHADEBOX]


In Analysis Workspace bildet ![ Visualisierung ](/help/assets/icons/Table.svg)Freiformtabelle **[!UICONTROL die]** für die interaktive Datenanalyse. Sie können eine Kombination von [Komponenten](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) per Drag und Drop in die Zeilen und Spalten ziehen, um eine benutzerdefinierte Tabelle für Ihre Analyse zu erstellen. Da jede Komponente abgelegt wird, wird die Tabelle sofort aktualisiert, damit Sie schnell analysieren und tiefer graben können.

![Freiformtabelle mit Komponenten in Zeilen und Spalten, einschließlich Besuchen und Online-Bestellungen für mehrere Web-Seiten.](assets/opening-section.png)

So erstellen und konfigurieren Sie eine [!UICONTROL Freiformtabelle]:

* Fügen Sie eine Visualisierung ![Tabelle](/help/assets/icons/Table.svg) **[!UICONTROL Freiformtabelle)]**. Siehe [Hinzufügen einer Visualisierung zu einem Bedienfeld](../freeform-analysis-visualizations.md#add-visualizations-to-a-panel).

## Automatisierte Tabellen

Am schnellsten können Sie eine Tabelle erstellen, indem Sie Komponenten direkt in ein leeres Projekt, ein leeres Bedienfeld oder eine Freiformtabelle ablegen. Eine Freiformtabelle wird in einem empfohlenen Format erstellt. [Tutorial ansehen](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/auto-build-freeform-tables-in-analysis-workspace).

![Ein neues Bedienfeld, in dem die Komponente „Besuche“ im Arbeitsbereich abgelegt wird.](assets/automated-table.png)

## Freiformtabellen-Builder

Wenn Sie Ihrer Tabelle lieber zuerst mehrere Komponenten hinzufügen und dann die Daten rendern möchten, können Sie **[!UICONTROL Tabellengenerator aktivieren]** auswählen. Wenn der Builder aktiviert ist, können Sie Dimensionen, Aufschlüsselungen, Metriken und Filter per Drag-and-Drop verschieben, um Tabellen zu erstellen, die komplexere Fragen beantworten. Datenaktualisierungen nach Auswahl von **[!UICONTROL Erstellen]**.

![Ein Freiformtabellen-Builder mit ](assets/table-builder.png)

## Interaktionen

Es gibt verschiedene Arten, mit Freiformtabellen zu interagieren und sie anzupassen:

### Filtern und Sortieren

* Sie können [ Daten ](filter-and-sort.md) einer Tabelle filtern und sortieren.

### Zeilen

* Mit [GraphBarVerticalAdd](../freeform-analysis-visualizations.md#visualize) ![ können Sie schnell aus einer oder mehreren Zeilen eine neue Visualisierung ](/help/assets/icons/GraphBarVerticalAdd.svg).
* Sie können mehr Zeilen in einen einzigen Bildschirm einpassen, indem Sie die [Anzeigedichte](/help/analyze/analysis-workspace/build-workspace-project/view-density.md) des Projekts anpassen.
* Jede Dimensionsreihe kann bis zu 400 Zeilen anzeigen, bevor die Paginierung erfolgt. Wählen Sie die Zahl neben **[!UICONTROL Zeilen]** in der ersten Spaltenüberschrift aus, um weitere Zeilen auf einer Seite anzuzeigen. Navigieren Sie mit „ChevronRight![ in ](/help/assets/icons/ChevronRight.svg) ersten Spaltenüberschrift zu einer anderen Seite.
* Sie können Zeilen nach zusätzlichen Komponenten aufschlüsseln. Um mehrere Zeilen gleichzeitig aufzuschlüsseln, wählen Sie mehrere Zeilen aus und ziehen Sie dann die nächste Komponente auf die ausgewählten Zeilen. Weitere Informationen zu [Aufschlüsselungen](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md).
* Zeilen können [gefiltert](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md) werden, um einen reduzierte Anzahl von Elementen anzuzeigen. Weitere Einstellungen finden Sie unter [Zeileneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md).

### Spalten

* Komponenten können innerhalb von Spalten gestapelt werden, um gefilterte Metriken, tabellenübergreifende Analysen und mehr zu erstellen.
* Die Ansicht jeder Spalte kann unter den [Spalteneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md) angepasst werden.
* Mehrere Aktionen sind über das [Kontextmenü](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu) verfügbar. Das Menü bietet verschiedene Aktionen, je nachdem, ob Sie die Tabellenkopfzeile, Zeilen oder Spalten auswählen.


## Einstellungen

Wählen Sie ![Einstellung](/help/assets/icons/Setting.svg) aus, um **[!UICONTROL Tabelleneinstellungen]** anzuzeigen. Die folgenden spezifischen [ (Einstellungen](../freeform-analysis-visualizations.md#settings) sind verfügbar:

### Datenquelle

| Option | Beschreibung |
|---|---|
| **[!UICONTROL Verknüpfte]**. | Listet alle verknüpften Visualisierungen auf. |
| **[!UICONTROL Datenquelle anzeigen]** | Wenn diese Option deaktiviert ist, wird die Freiformtabelle, die als Datenquelle für die Visualisierung fungiert, in Workspace ausgeblendet. |

### Einstellungen

| Option | Beschreibung |
|---|---|
| **[!UICONTROL Die Datumsangaben in den einzelnen Spalten so ausrichten, dass sie alle in derselben Zeile beginnen]** | So ordnen Sie Datumsangaben in jeder Spalte so an, dass sie alle in derselben Zeile beginnen. |


## Kontextmenü

Die folgenden [Kontextmenü](../freeform-analysis-visualizations.md#context-menu)-Optionen sind in der Kopfzeile der Visualisierung verfügbar:

| Option | Beschreibung |
| --- | --- |
| **[!UICONTROL Kopierte Visualisierung einfügen]**n | Fügen Sie eine kopierte Visualisierung an einer anderen Stelle innerhalb des Projekts oder in ein ganz anderes Projekt ein. |
| **[!UICONTROL Daten in die Zwischenablage kopieren]** | Kopieren Sie Daten aus der Visualisierung in die Zwischenablage. |
| **[!UICONTROL Auswahl in Zwischenablage kopieren]** | Kopieren Sie die Auswahl aus der Visualisierung in die Zwischenablage. |
| **[!UICONTROL Objekte als CSV herunterladen (*Dimensionsname*)]** | Laden Sie sofort die Dimensionselemente (bis zu maximal 50.000) der Visualisierung auf Ihr lokales Gerät herunter. Maximal 50.000 Dimensionselemente für die ausgewählte Dimension. |
| **[!UICONTROL Visualisierung kopieren]** | Kopieren Sie die Visualisierung, sodass Sie die Visualisierung an einer anderen Stelle innerhalb des Projekts oder in ein ganz anderes Projekt einfügen können. |
| **[!UICONTROL Daten-CSV herunterladen]** | Laden Sie die angezeigten Daten der Visualisierung sofort auf Ihr lokales Gerät herunter. |
| **[!UICONTROL Visualisierung duplizieren]** | Erstellen Sie ein exaktes Duplikat der Visualisierung. |
| **[!UICONTROL Beschreibung bearbeiten]** | Hinzufügen (oder Bearbeiten) einer Textbeschreibung für die Visualisierung. Siehe [Text](../text.md). |
| **[!UICONTROL Visualisierungs-Link abrufen]** | Kopieren Sie einen Link und teilen Sie ihn direkt in der Visualisierung. Das Dialogfeld Link freigeben zeigt den Link an. Wählen Sie Kopieren aus, um den Link in die Zwischenablage zu kopieren. |
| **[!UICONTROL Neu starten]** | Löschen Sie die Konfiguration für die aktuelle Visualisierung, damit Sie sie von Grund auf neu konfigurieren können. |



## Videos

>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Übersicht zum Freiformtabellen-Builder](https://video.tv.adobe.com/v/31318?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Freiformtabellenfilter](https://video.tv.adobe.com/v/23232?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Freiformtabellen-Summen](https://video.tv.adobe.com/v/29273?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


>[!MORELIKETHIS]
>
>[Hinzufügen einer Visualisierung zu einem Bedienfeld](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[Visualisierungseinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[Kontextmenü der Visualisierung](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>



