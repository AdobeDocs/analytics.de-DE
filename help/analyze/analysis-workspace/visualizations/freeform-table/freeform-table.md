---
title: Freiformtabelle
description: Freiformtabellen sind die Grundlage für die Analyse von Daten in Workspace
feature: Freeform Tables
role: User, Admin
exl-id: 7a0432f9-2cab-47be-bbd6-ede96cb840a3
source-git-commit: ef2b452a0dcb2659b49fc0507b096952a89ea2f4
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 65%

---

# Freiformtabelle

In Analysis Workspace bildet eine Freiformtabelle die Grundlage für die interaktive Analyse von Daten. Sie können eine Kombination von [Komponenten](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html?lang=de) per Drag und Drop in die Zeilen und Spalten ziehen, um eine benutzerdefinierte Tabelle für Ihre Analyse zu erstellen. Da jede Komponente abgelegt wird, wird die Tabelle sofort aktualisiert, sodass Sie sie schnell analysieren und vertiefen können.

## Erstellen einer einfachen Freiformtabelle

Sie beginnen mit einer leeren Freiformtabelle.

![Leere Freiformtabelle](assets/freeform-table-1.png)

Wenn Sie die Metrik **[!UICONTROL ** Besuche **]** auf der **[!UICONTROL ** Metrik hier ablegen (oder einer anderen Komponente)**]** ablegen, werden in der Freiformtabelle für den ausgewählten Kalenderzeitraum automatisch die Besuche pro Tag ausgefüllt.

![Freiformtabelle „Besuche](assets/freeform-table-2.png)

Wenn Sie dann die Dimension **[!UICONTROL ** Seite **]** ablegen, um die Dimensionsspalte **[!UICONTROL ** Tag **]** zu ersetzen, spiegelt die Freiformtabelle automatisch Besuche für jede Seite wider.

![Besuche nach Freiformtabelle der Seite](assets/freeform-table-3.png)

Sie können dann beispielsweise die Seite &quot;**[!UICONTROL **:5“ aufschlüsseln **]** indem Sie die Dimension **[!UICONTROL ** Marketing-Kanal **]** in der Zeile **[!UICONTROL ** Kategorie:5 **]** ablegen.

![Aufschlüsselung der Besuche nach Seiten-Freiformtabelle](assets/freeform-table-4.png)


## Automatisierte Tabellen

Wie oben gezeigt, besteht die schnellste Möglichkeit, eine Tabelle zu erstellen, darin, Komponenten direkt in ein leeres Projekt, ein leeres Bedienfeld oder eine Freiformtabelle abzulegen. Eine Freiformtabelle wird dann automatisch in einem empfohlenen Format erstellt. [Tutorial ansehen](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/auto-build-freeform-tables-in-analysis-workspace.html?lang=de).

![](assets/automated-table.png)

## Freiformtabellen-Builder

Wenn Sie Ihrer Tabelle lieber zuerst mehrere Komponenten hinzufügen und dann die Daten rendern möchten, können Sie Freiformtabellen-Builder aktivieren. Wenn der Builder aktiviert ist, können Sie für komplexe Fragen Tabellen mit vielen Dimensionen, Unterteilungen, Metriken und Segmenten per Drag-and-Drop erstellen. Daten werden nicht sofort aktualisiert. Sie werden erst aktualisiert, wenn Sie auf &quot;**[!UICONTROL &quot;]**.

![](assets/table-builder.png)

## Tabelleninteraktionen

Es gibt verschiedene Arten, mit Freiformtabellen zu interagieren und sie anzupassen:

* **Zeilen**
   * Sie können mehr Zeilen in einen einzigen Bildschirm einpassen, indem Sie die [Anzeigedichte](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html?lang=de) des Projekts anpassen.
   * Jede Dimensionsreihe kann bis zu 400 Zeilen anzeigen, bevor die Paginierung erfolgt. Klicken Sie auf die Zahl neben „Zeilen“, um weitere Zeilen auf einer Seite anzuzeigen. Mit dem Pfeil in der Kopfzeile navigieren Sie zu einer anderen Seite.
   * Zeilen können nach zusätzlichen Komponenten aufgeschlüsselt werden. Um mehrere Zeilen gleichzeitig zu aufzuschlüsseln, wählen Sie einfach mehrere Zeilen aus und ziehen dann die nächste Komponente auf die ausgewählten Zeilen. Weitere Informationen zu [Aufschlüsselungen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.html?lang=de).
   * Zeilen können [gefiltert](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.html?lang=de) werden, um einen reduzierte Anzahl von Elementen anzuzeigen. Weitere Einstellungen finden Sie unter [Zeileneinstellungen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.html?lang=de).

* **Spalten**
   * Komponenten können innerhalb von Spalten gestapelt werden, um segmentierte Metriken, tabellenübergreifende Analysen und mehr zu erstellen.
   * Die Ansicht jeder Spalte kann unter den [Spalteneinstellungen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html?lang=de) angepasst werden.
   * Über das [Kontextmenü](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/using-the-right-click-menu.html?lang=de) sind verschiedene Aktionen verfügbar. Das Menü enthält verschiedene Aktionen, je nachdem, ob Sie auf die Tabellenüberschrift, die Zeilen oder die Spalten klicken.

## Exportieren von Freiformtabellendaten

Erfahren Sie mehr über die [Exportoptionen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/download-send.html?lang=de) aller Daten für Analysis Workspace.

* Klicken Sie mit der rechten Maustaste und **[!UICONTROL Daten in Zwischenablage kopieren]** exportiert die angezeigten Tabellendaten. Wenn eine Tabellenauswahl vorgenommen wurde, lautet diese Option **[!UICONTROL Auswahl in Zwischenablage kopieren]**. Mit dem Hotkey **Strg + C** können auch ausgewählte Daten kopiert werden.
* Klicken Sie mit der rechten Maustaste und **[!UICONTROL Daten als CSV-Datei herunterladen]** lädt die angezeigten Tabellendaten als CSV-Datei herunter. Wenn eine Tabellenauswahl vorgenommen wurde, lautet diese Option **[!UICONTROL Auswahl als CSV-Datei herunterladen]**.
* Klicken Sie mit der rechten Maustaste **[!UICONTROL Projekt > Elemente als CSV herunterladen]** exportiert bis zu 50.000 Dimensionselemente für die ausgewählte Dimension.

Erfahren Sie mehr über die [Exportoptionen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/download-send.html?lang=de) aller Daten für Analysis Workspace.

![](assets/export-options.png)

## Videos

Freiformtabellen-Builder – Übersicht:

>[!VIDEO](https://video.tv.adobe.com/v/31318/?quality=12)

Freiformtabellen-Filter:

>[!VIDEO](https://video.tv.adobe.com/v/23232/?quality=12)

Gesamtwerte der Freiformtabelle:

>[!VIDEO](https://video.tv.adobe.com/v/29273/?quality=12)
