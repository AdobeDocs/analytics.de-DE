---
title: Freiformtabelle
description: Freiformtabellen sind die Grundlage für die Analyse von Daten in Workspace
feature: Freeform Tables
role: User, Admin
exl-id: 7a0432f9-2cab-47be-bbd6-ede96cb840a3
source-git-commit: bb3e8b030af78f0d7758b4cff41d66f20695e11e
workflow-type: ht
source-wordcount: '785'
ht-degree: 100%

---

# Freiformtabelle {#freeform-table-overview}


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_button"
>title="Freiformtabelle"
>abstract="Erstellen Sie eine leere Visualisierung einer Freiformtabelle, die Sie mithilfe von Dimensionen, Segmenten, Metriken und Datumsbereichen gestalten können. Sie können die Freiformtabelle als Grundlage für andere Visualisierungen verwenden."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_In diesem Artikel wird die Freiformtabellen-Visualisierung in_ ![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics** beschrieben._<br/>_Unter [Freiformtabelle](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/visualizations/freeform-table/freeform-table) finden Sie die Version dieses Artikels für_ ![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**._

>[!ENDSHADEBOX]


In Analysis Workspace bildet eine ![Table](/help/assets/icons/Table.svg) **[!UICONTROL Freiformtabellen]**-Visualisierung die Grundlage für die interaktive Analyse von Daten. Sie können eine Kombination von [Komponenten](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) per Drag-and-Drop in die Zeilen und Spalten ziehen, um eine benutzerdefinierte Tabelle für Ihre Analyse zu erstellen. Sobald eine Komponente abgelegt wird, wird die Tabelle aktualisiert, damit Sie schnell analysieren und weiter recherchieren können.

![Freiformtabelle mit Komponenten in Zeilen und Spalten, einschließlich Besuchen und Online-Bestellungen für mehrere Web-Seiten](assets/opening-section.png)

So erstellen und konfigurieren Sie eine [!UICONTROL Freiformtabelle]:

* Fügen Sie eine ![Table](/help/assets/icons/Table.svg) **[!UICONTROL Freiformtabellen]**-Visualisierung hinzu. Weitere Informationen finden Sie unter [Hinzufügen einer Visualisierung zu einem Panel](../freeform-analysis-visualizations.md#add-visualizations-to-a-panel)

## Automatisierte Tabellen

Am schnellsten können Sie eine Tabelle erstellen, indem Sie Komponenten direkt in ein leeres Projekt, ein leeres Bedienfeld oder eine Freiformtabelle ablegen. Eine Freiformtabelle wird in einem empfohlenen Format erstellt. [Tutorial ansehen](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/auto-build-freeform-tables-in-analysis-workspace).

![Ein neues Bedienfeld, in dem die Komponente „Besuche“ im Arbeitsbereich abgelegt wird](assets/automated-table.png)

## Freiformtabellen-Generator

Wenn Sie Ihrer Tabelle lieber zuerst mehrere Komponenten hinzufügen und erst dann die Daten rendern möchten, können Sie **[!UICONTROL Tabellengenerator aktivieren]** auswählen. Wenn der Generator aktiviert ist, können Sie für komplexere Fragen per Drag-and-Drop Tabellen mit Dimensionen, Unterteilungen, Metriken und Filtern erstellen. Die Daten werden nach Auswahl von **[!UICONTROL Erstellen]** aktualisiert.

![Ein Freiformtabellen-Generator mit ](assets/table-builder.png)

## Interaktionen

Es gibt verschiedene Arten, mit Freiformtabellen zu interagieren und sie anzupassen:

### Filtern und Sortieren

* Sie können die Daten in einer Tabelle [filtern und sortieren](filter-and-sort.md).

### Zeilen

* Mit ![GraphBarVerticalAdd](/help/assets/icons/GraphBarVerticalAdd.svg) können Sie aus einer oder mehreren Zeilen schnell [eine neue Visualisierung erstellen](../freeform-analysis-visualizations.md#visualize).
* Sie können mehr Zeilen in einen einzigen Bildschirm einpassen, indem Sie die [Anzeigedichte](/help/analyze/analysis-workspace/build-workspace-project/view-density.md) des Projekts anpassen.
* Jede Dimensionsreihe kann bis zu 400 Zeilen anzeigen, bevor die Paginierung erfolgt. Wählen Sie die Zahl neben **[!UICONTROL Zeilen]** in der ersten Spaltenüberschrift aus, um weitere Zeilen auf einer Seite anzuzeigen. Navigieren Sie mit ![ChevronRight](/help/assets/icons/ChevronRight.svg) in der ersten Spaltenüberschrift zu einer anderen Seite.
* Sie können Zeilen nach zusätzlichen Komponenten aufschlüsseln. Um mehrere Zeilen gleichzeitig aufzuschlüsseln, wählen Sie mehrere Zeilen aus und ziehen Sie dann die nächste Komponente auf die ausgewählten Zeilen. Weitere Informationen zu [Aufschlüsselungen](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md).
* Zeilen können [gefiltert](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md) werden, um einen reduzierte Anzahl von Elementen anzuzeigen. Weitere Einstellungen finden Sie unter [Zeileneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md).

### Spalten

* Komponenten können innerhalb von Spalten gestapelt werden, um gefilterte Metriken, tabellenübergreifende Analysen und mehr zu erstellen.
* Die Ansicht jeder Spalte kann unter den [Spalteneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md) angepasst werden.
* Über das [Kontextmenü](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu) sind verschiedene Aktionen verfügbar. Das Menü enthält verschiedene Aktionen, je nachdem, ob Sie die Tabellenüberschrift, die Zeilen oder die Spalten auswählen.


## Einstellungen

Wählen Sie ![Setting](/help/assets/icons/Setting.svg) aus, um die **[!UICONTROL Tabelleneinstellungen]** anzuzeigen. Die folgenden spezifischen [ Visualisierungseinstellungen](../freeform-analysis-visualizations.md#settings) sind verfügbar:

### Datenquelle

| Option | Beschreibung |
|---|---|
| **[!UICONTROL Verknüpfte Visualisierungen]**. | Listet alle verknüpften Visualisierungen auf. |
| **[!UICONTROL Datenquelle anzeigen]** | Wenn diese Option deaktiviert ist, wird die Freiformtabelle, die als Datenquelle für die Visualisierung fungiert, in Workspace ausgeblendet. |

### Einstellungen

| Option | Beschreibung |
|---|---|
| **[!UICONTROL Daten in allen Spalten so ausrichten, dass sie alle in derselben Zeile beginnen]** | Um die Daten in allen Spalten so auszurichten, dass sie alle in derselben Zeile beginnen, oder nicht. |


## Kontextmenü

Die folgenden [Kontextmenü](../freeform-analysis-visualizations.md#context-menu)-Optionen sind in der Kopfzeile der Visualisierung verfügbar:

| Option | Beschreibung |
| --- | --- |
| **[!UICONTROL Kopierte Visualisierung einfügen]**n | Fügen Sie eine kopierte Visualisierung an einer anderen Stelle innerhalb des Projekts oder in ein ganz anderes Projekt ein. |
| **[!UICONTROL Daten in Zwischenablage kopieren]** | Zum Kopieren der Daten aus der Visualisierung in die Zwischenablage. |
| **[!UICONTROL Auswahl in Zwischenablage kopieren]** | Zum Kopieren der Auswahl aus der Visualisierung in die Zwischenablage. |
| **[!UICONTROL Objekte als CSV herunterladen (*Dimensionsname*)]** | Zum sofortigen Herunterladen der Dimensionselemente (bis zu maximal 50.000) der Visualisierung auf Ihr lokales Gerät. Maximal 50.000 Dimensionselemente für die ausgewählte Dimension. |
| **[!UICONTROL Visualisierung kopieren]** | Zum Kopieren der Visualisierung, sodass Sie sie an einer anderen Stelle innerhalb des Projekts oder in ein ganz anderes Projekt einfügen können. |
| **[!UICONTROL Daten als CSV herunterladen]** | Lädt die angezeigten Daten der Visualisierung sofort auf Ihr lokales Gerät herunter. |
| **[!UICONTROL Visualisierung duplizieren]** | Erstellt ein exaktes Duplikat der Visualisierung. |
| **[!UICONTROL Beschreibung bearbeiten]** | Zum Hinzufügen (oder Bearbeiten) von Text zur Beschreibung der Visualisierung. Siehe [Text](../text.md). |
| **[!UICONTROL Visualisierungs-Link abrufen]** | Kopiert einen Link und gibt ihn direkt in der Visualisierung frei. Der Link wird im Dialogfeld „Link freigeben“ angezeigt. Wählen Sie „Kopieren“ aus, um den Link in die Zwischenablage zu kopieren. |
| **[!UICONTROL Neu starten]** | Löscht die Konfiguration für die aktuelle Visualisierung, damit Sie sie von Grund auf neu konfigurieren können. |



## Videos

>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Freiformtabellen-Builder – Übersicht](https://video.tv.adobe.com/v/33611?quality=12&learn=on&captions=ger){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Freiformtabellen-Filter](https://video.tv.adobe.com/v/327357?quality=12&learn=on&captions=ger){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Gesamtwerte der Freiformtabelle](https://video.tv.adobe.com/v/32921?quality=12&learn=on&captions=ger){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


>[!MORELIKETHIS]
>
>[Hinzufügen einer Visualisierung zu einem Bedienfeld](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[Visualisierungseinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[Kontextmenü der Visualisierung](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>



