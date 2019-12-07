---
keywords: Analysis Workspace
title: Analysis Workspace – Übersicht
topic: Reports and analytics
uuid: 4df6be48-2c88-4b9d-9536-ed64ffbb6ee4
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Analysis Workspace – Übersicht

Im Analysis Workspace entfallen alle normalen Einschränkungen eines einzelnen Analytics-Berichts. Sie erhalten eine stabile und flexible Arbeitsfläche, in der Sie benutzerdefinierte Analyseprojekte erstellen können. Ziehen Sie per Drag-and-Drop eine beliebige Anzahl von Datentabellen, Visualisierungen und Komponenten (Dimensionen, Metriken, Segmente und Zeitgranularitäten) in ein Projekt. Erstellen Sie im Handumdrehen Aufschlüsselungen und Segmente, Kohorten für die Analyse sowie Warnhinweise und vergleichen Sie Segmente miteinander, führen Sie Fluss- sowie Fallout-Analysen durch und kuratieren und planen Sie Berichte für die Freigabe für andere in Ihrem Unternehmen.

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Workspace]**

## Überblickvideo {#section_B99BF8A326D94ECB91BD69C9888AD10C}

>[!VIDEO](https://www.youtube.com/watch?v=IHOy-QsvVcA)

Eine vollständige YouTube-Playlist ist [hier](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) verfügbar.

>[!NOTE]
>
>[Neuerungen in Analysis Workspace](/help/analyze/analysis-workspace/new-features-in-analysis-workspace.md) enthält aktuelle Informationen zu Funktionen.

## Vollständige Kontrolle über Projektelemente und Komponenten {#section_B7E3EDA3EDEE407D833F4FDB69646EEC}

Der Analysis Workspace ermöglicht Unabhängigkeit und Flexibilität:

* Drag-and-Drop von Komponenten (Dimensionen, Metriken, Segmente und Zeitgranularitäten)
* Drag-and-Drop von mehreren Visualisierungen in das Projekt
* Visualisierungen lassen sich in einem Projekt jederzeit verschieben, in der Größe verändern und stapeln

![](assets/fa_project_new.png)

Weitere Informationen finden Sie unter [Erstellen eines Projekts in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md).

## Mehrere Visualisierungen in einem Projekt {#section_B7670740C2D44130B21DAF0873280DA5}

Erstellen Sie per Drag-and-Drop beliebig viele Visualisierungen in einem Projekt.

![](assets/visualizations-multiple.png)

Erstellen Sie ein Projekt, das den Prozentsatz der Veränderung zeigt, mit mehreren Visualisierungen, die den Zellen in einer Freiform-Datentabelle entsprechen.

![](assets/visualizations-multiple02.png)

Weitere Informationen finden Sie unter [Erstellen eines Projekts in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md).

## Intra-Linking zu Bereichen und Visualisierungen {#section_253EA04E067F4A29A8B54CE2B7631086}

Mithilfe der [Rich-Text-Bearbeitungsfunktionen](/help/analyze/analysis-workspace/visualizations/text.md) von Analysis Workspace können Sie innerhalb eines Projekts von einem Textfeld aus Verknüpfungen zu bestimmten Bereichen und Visualisierungen anlegen, beispielsweise um das Inhaltsverzeichnis eines Projekts zu erstellen. Sie können diese Verknüpfungen dann wie eine Projektverknüpfung freigeben, um eine Person an eine bestimmte Visualisierung oder einen Bereich innerhalb eines Projekts weiterzuleiten. Die neuen Rechtsklickoptionen „Bereichslink abrufen“ und „Visualisierungslink abrufen“ wurden hinzugefügt. So fügen Sie Intra-Linking zu Ihrem Projekt hinzu:

1. Ziehen Sie eine Textvisualisierung in ein Projekt, z. B. neben eine Visualisierung oder Tabelle, für die Kontext erforderlich ist.
1. Füllen Sie das Textfeld z. B. mit einem Inhaltsverzeichnis und markieren Sie dann ein Element, das Sie mit einem Bereich oder einer Visualisierung verknüpfen möchten, z. B. Erfolgsmetriken.

   ![](assets/intra-linking1.png)

1. Scrollen Sie zu diesem Bereich bzw. zu dieser Visualisierung und klicken Sie mit der rechten Maustaste auf den Header des Bereichs.
1. Scrollen Sie nach unten und wählen Sie **[!UICONTROL Bereichslink abrufen]** oder **[!UICONTROL Visualisierungslink abrufen]** aus:

   ![](assets/intra-linking2.png)

1. Kopieren Sie diesen Link und fügen Sie ihn zum Erfolgsmetrik-Hyperlink in der Textvisualisierung hinzu. Klicken Sie auf das Häkchen, um den Text zu speichern.

Wenn Bereiche oder Visualisierungen innerhalb Ihres Projekts ausgeblendet sind, können Sie diese durch Klicken auf einen Link einblenden, um sie für Benutzer sichtbar zu machen.

> [!NOTE] Sie können diese Funktion auch über die Rechtsklickoption **[!UICONTROL Beschreibung bearbeiten]** verwenden.

## Verknüpfung zu anderen Projekten {#section_AE886C367C3E4F189B65B1BD9BCDBD8C}

Sie können Benutzer mit anderen u. U. für sie interessanten Projekten verknüpfen, indem Sie **[!UICONTROL Freigabe]** &gt; **[!UICONTROL Projektverknüpfung abrufen]** aufrufen und diesen Link z. B. in Projektbeschreibungen einbetten.

## Dynamische Visualisierung ausgewählter Zellen {#section_182CEC285E4547EBA4608D5F70C9D5D7}

Wenn Sie einzelne Zellen auswählen, wird die Visualisierung dynamisch geändert. [Synchronisieren und sperren](/help/analyze/analysis-workspace/analysis-workspace-features.md#section_9D66A001586F49CEB0C565581E44957C) Sie eine Visualisierung an ausgewählten Zellen.

![](assets/visualize-selected-cells.png)

## Ausgewählte Elemente oder Positionen sperren {#section_9D66A001586F49CEB0C565581E44957C}

Durch das Sperren von Visualisierungen können Sie steuern, welche Freiform-Datentabellenquellen den Visualisierungen entsprechen.

![](assets/manage-data-source.png)

[Data Sources verwalten](/help/analyze/analysis-workspace/visualizations/t-sync-visualization.md).

## Trend-Visualisierungen aus ausgewählten Zellen {#section_34930C967C104C2B9092BA8DCF2BF81A}

Erstellen Sie eine Visualisierung aus ausgewählten Zellen. (Rechtsklick &gt; **[!UICONTROL Trendauswahl]**.)

![](assets/trend-selection.png)

Trendauswahlen werden jetzt mit der Tabelle darunter **verknüpft**. Wenn Sie daher in der Tabelle eine andere Zeile auswählen, bezieht sich das Trend-Diagramm auf diese Zeile.

![](assets/trend-selection2.png)

## Aufschlüsselungen von Dimensionen und Dimensionselementen {#section_1380C1F9E51E4BFB8C5D35E7A53BC70D}

Als Händler erhalten Sie tiefere Einblicke in Ihre Kampagnen, als Sie je hatten, und verstehen so, wie Sie Ihre Kunden binden können. Sie können Ihre Daten für Ihre spezifischen Anforderungen unbegrenzt aufschlüsseln. Erstellen Sie Abfragen mithilfe relevanter Metriken, Dimensionen, Segmente, Zeitachsen und anderer Aufschlüsselungswerte für die Analyse.

![Schritt Ergebnis](assets/fa_data_table_actions.png)

[Schlüsseln Sie Dimensionen auf](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md).

## Segmente aus Tabellenauswahlen {#section_73BC3688089B426D969B3D5B606DA970}

Wählen Sie Zellen in der Freiformtabelle aus und erstellen Sie aus der Auswahl ein Segment.

Vergleichen Sie mehrere Segmente und erstellen Sie direkt Segmente, die Sie anwenden. Sie können mehrere Segmente anwenden, um den Fokus auf bestimmte Kunden zu legen, die aufgrund von Verhalten und Interaktion ausgewählt werden, und diese dann vergleichen und gegenüberstellen.

![](assets/segment_inline.png)

Ziehen Sie ein Segment auf der Projektebene auf den Freiformbereich, damit das Segment auf das gesamte Projekt angewendet wird.

![](assets/segment-panel.png)

Siehe [Segmente](/help/analyze/analysis-workspace/components/t-freeform-project-segment.md).

## Projekt- und Komponenten-Tagging {#section_F54D688132A541F2982326D5E022B90D}

In Analysis Workspace können Sie Tags auf Projekte und Komponenten anwenden:

* Anwenden oder Erstellen von Tags auf Projektebene im Informationsbereich (![](assets/information_icon.png)

* Rechtsklick auf Komponenten zum Taggen (oder Erstellen von Tags) im Komponentenbereich
* Suchen von Tags durch Eingabe von „#“ im Suchfeld

## Komponentenaktionen {#section_CBF4D0A5F63E4B0883077B8D852B800B}

Aktionen auf Komponentenebene führen Sie über das Menü „Aktionen“ durch, das sich oben in der linken Leiste von „Komponenten“ befindet. Wählen Sie eine Komponente aus und klicken Sie auf **[!UICONTROL Aktionen]**, um die Aktionen anzuzeigen.

| Komponentenaktion | Beschreibung |
|--- |--- |
| Tag | Organisieren oder verwalten Sie Komponenten, indem Sie Tags darauf anwenden. Dies wird dann bei der jeweiligen Komponentenverwaltung angezeigt, beispielsweise „Analysen“ &gt; „Komponenten“ &gt; „Segmente“ oder „Analysen“ &gt; „Komponenten“ &gt; „Projekte“. |
| Favorit | Fügen Sie die Komponente Ihrer Favoritenliste hinzu. Dies wird dann bei der jeweiligen Komponentenverwaltung angezeigt, beispielsweise „Analysen“ &gt; „Komponenten“ &gt; „Segmente“ oder „Analysen“ &gt; „Komponenten“ &gt; „Projekte“. |
| Genehmigen | Genehmigen Sie die Komponente, um sie zu autorisieren. Dies wird dann bei der jeweiligen Komponentenverwaltung angezeigt, beispielsweise „Analysen“ &gt; „Komponenten“ &gt; „Segmente“ oder „Analysen“ &gt; „Komponenten“ &gt; „Projekte“. |
| Freigabe | Gilt nur für Segmente. |
| Löschen | Gilt nur für Segmente. |

Weitere Informationen zu diesem Thema finden Sie unter [Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md).

## Beschreibung weiterer Funktionen {#section_5F06AE43C0194CFDBCA7EE0EA3C30B05}

**Was Sie ziehen und stapeln können**

Komponenten

* Dimensionen
* Segmente
* Metriken
* Datumsbereiche
* Zeitgranularitäten (Stunde, Tag, Woche usw.).

**Mehrere Freiformtabellen und mehrere Visualisierungen**

Es gibt keine technische Einschränkung für die Anzahl der Freiformtabellen und Visualisierungen, die Sie zum Bereich hinzufügen können. Sie können auch eine neue Visualisierung (oder einen Export in eine CSV-Datei) der einzelnen Freiformtabellen oder ausgewählten Zeilen einer Tabelle ausführen.

**Anordnen, Sortieren und Kopieren von Spalten**

* Sortieren der vordefinierten Datumsbereiche (ohne benutzerdefinierte Datumsbereiche)
* STRG (oder Command) + Klick + Ziehen einer Spalte kopiert die Spalte. Wenn Sie die Kopie ziehen, wird sie an der neuen Position in die Tabelle eingefügt.

Für weitere Informationen siehe [Tastaturbefehle in Analysis Workspace](/help/analyze/analysis-workspace/build-workspace-project/fa-shortcut-keys.md).

**Auswahlen und Aktionen**

Sie können Zeilen und Spalten ähnlich wie in Excel auswählen. Anschließend können Sie auf diesen Auswahlen Aktionen ausführen. Beispiel:

* Erstellen Sie Visualisierungen aus Auswahlen
* Kopieren Sie diese in die Zwischenablage (STRG + C oder Command + C)
* Schlüsseln Sie mehrere ausgewählte Zeilen auf. Wählen Sie die Zeilen aus und ziehen Sie dann eine Dimension auf die Auswahl. Oder klicken Sie mit der rechten Maustaste auf die Auswahl und verwenden Sie das Aufschlüsselungsmenü.

**Automatisches Speichern und nicht gespeicherte Änderungen**

Wenn Sie versuchen, den Browser zu schließen (oder die Zurück-Schaltfläche zu verwenden) und das Projekt noch nicht gespeichert wurde, werden Sie aufgefordert, Ihre Änderungen zu speichern. Wenn Ihr System abstürzt, erhalten Sie beim nächsten Laden des Projekts einen Warnhinweis, um den vorherigen Projektzustand wiederherzustellen.

Bereits bestehende (nicht neue) Projekte werden nur automatisch gespeichert, wenn der Browser abstürzt oder Sie aus einem anderen Grund keine Möglichkeit hatten, sie zu speichern.

**Alle Besuche**

Ein spezifisches Standardsegment von Analysis Workspace. *`All Visits`* zeigt die Summen für die Komponenten, die Sie zur Tabelle hinzufügen, an.

**Berechnete Metriken**

Verwenden Sie Berechnungen so, wie Sie Standardmetriken verwenden.

Siehe [Berechnete Metriken](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/).
