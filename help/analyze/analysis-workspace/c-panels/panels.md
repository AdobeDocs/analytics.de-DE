---
description: Ein Bedienfeld ist eine Sammlung von Tabellen und Visualisierungen
title: Übersicht über Bedienfelder
feature: Panels
role: User, Admin
exl-id: dd1a3c40-8b5b-47dd-86d9-da766575ee46
source-git-commit: 017559d2b909deb4bf87fb5fe41db8250f2ca2ac
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 68%

---

# Übersicht über Bedienfelder

Ein [!UICONTROL Bedienfeld] ist eine Sammlung von Tabellen und Visualisierungen. Sie können auf Bedienfelder über das Symbol oben links in Workspace oder über eine [leeres Bedienfeld](blank-panel.md). Panels sind hilfreich, wenn Sie Ihre Projekte nach Zeiträumen, Report Suites oder Analysen ordnen möchten. 

## Bedienfeldtypen

Die folgenden Bedienfeldtypen sind in Analysis Workspace verfügbar:

| Name des Bedienfelds | Beschreibung |
| --- | --- |
| [Leeres Bedienfeld](blank-panel.md) | Wählen Sie zum Beginnen Ihrer Analyse aus den verfügbaren Bedienfeldern und Visualisierungen. |
| [Bedienfeld „Quick Insights“](quickinsight.md) | Sie können rasch eine Freiformtabelle und eine entsprechende Visualisierung erstellen, um Einblicke schneller zu analysieren und bereitzustellen. |
| [Analytics for Target-Bedienfeld](a4t-panel.md) | Target-Aktivitäten und Erlebnisse in Analysis Workspace analysieren. |
| [Attributionsbedienfeld](attribution.md) | Vergleichen und visualisieren Sie im Handumdrehen eine beliebige Anzahl von Attributionsmodellen unter Verwendung verschiedener Dimensionen und Konversionskennzahlen. |
| [Freiform-Bedienfeld](freeform-panel.md) | Führen Sie unbegrenzte Vergleiche und Aufschlüsselungen durch und fügen Sie dann Visualisierungen hinzu, um eine ausführliche Story mit den Daten zu erzählen. |
| [Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“](average-minute-audience-panel.md) | Analysieren Sie die durchschnittliche Besucherzahl pro Minute im Laufe der Zeit, einschließlich Details zu Spitzenwerten und der Möglichkeit, diese aufzuschlüsseln und zu vergleichen. |
| [Bedienfeld „Gleichzeitige Medienbetrachter“](media-concurrent-viewers.md) | Analysieren Sie gleichzeitige Betrachter über einen längeren Zeitraum. Sie erhalten Details zum maximalen gleichzeitigen Zugriff und die Möglichkeit, aufzuschlüsseln und zu vergleichen. |
| [Bedienfeld „Mit Medienwiedergabe verbrachte Zeit“](media-playback-timespent/media-playback-time-spent.md) | Analysieren Sie gleichzeitige Betrachter über einen längeren Zeitraum. Sie erhalten Details zum maximalen gleichzeitigen Zugriff und die Möglichkeit, aufzuschlüsseln und zu vergleichen. |
| [Bedienfeld „Segmentvergleich“](c-segment-comparison/segment-comparison.md) | Vergleichen Sie schnell zwei Segmente über alle Datenpunkte hinweg, um automatisch relevante Unterschiede zu ermitteln. |

![](assets/panel-overview.png)

[!UICONTROL Quick Insights-], [!UICONTROL leere] und [!UICONTROL Freiform-]Bedienfelder eignen sich hervorragend als Ausgangspunkt für Ihre Analyse, während sich die Bedienfelder für [!UICONTROL Analytics for Target], [!UICONTROL Attribution IQ], [!UICONTROL gleichzeitige Medien-Viewer] und [!UICONTROL Segmentvergleich] mehr für erweiterte Analysen eignen. In Projekten steht eine `"+"`-Schaltfläche zur Verfügung, mit der Sie jederzeit leere Bedienfelder hinzufügen können.

Das standardmäßige Startbedienfeld ist das [!UICONTROL Freiform-]Bedienfeld. Sie können jedoch auch das [leere Bedienfeld](/help/analyze/analysis-workspace/c-panels/blank-panel.md) als Standard festlegen.

## Report Suite {#report-suite}

Tabellen und Visualisierungen innerhalb eines Bedienfelds leiten Daten von der [!UICONTROL Report Suite] ab, die oben rechts im Bedienfeld ausgewählt wurde. Von der Report Suite hängt auch ab, welche Komponenten in der linken Leiste verfügbar sind. In einem Projekt können Sie je nach Anwendungsfällen Ihrer Analyse eine oder [viele Report Suites](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html?lang=de) verwenden. Um eine einzelne Report Suite auf alle Bedienfelder in einem Projekt anzuwenden, **klicken Sie mit der rechten Maustaste auf die Bedienfeldkopfzeile > „Report Suite auf alle Bedienfelder anwenden“**.

Die Liste der Report Suites ist nach Relevanz sortiert, die Adobe danach definiert, wie kürzlich und häufig die Suite vom aktuellen Benutzer verwendet wurde und wie häufig die Suite innerhalb der Organisation eingesetzt wird.

![](assets/panel-report-suite.png)

## Kalender {#calendar}

Über den Panel-Kalender wird der Reporting-Bereich für Tabellen und Visualisierungen innerhalb eines Panels festgelegt.

>[!NOTE]
>Wenn in einer Tabelle, Visualisierung oder dem Ablegebereich eines Panels eine (violette) Datumsbereichskomponente verwendet wird, überschreibt sie den Panel-Kalender.

![](assets/panel-calendar.png)

Sie können unter den erweiterten Einstellungen Ihres Bedienfeldkalenders einen Datumsbereich auf Minutenebene anwenden. Wenn Sie Berichte zu einem Datumsbereich erstellen, der viele Tage umfasst, gilt als Startzeit der erste Tag und als Endzeit der letzte Tag in Ihrem Bereich.

## Ablegebereich {#dropzone}

Mit dem Ablegebereich eines Panels können Sie Segment- und Dropdown-Filter auf alle Tabellen und Visualisierungen innerhalb des Panels anwenden. Sie können einen oder mehrere Filter auf ein Bedienfeld anwenden. Der Titel über jedem Filter kann durch Klicken auf den Bearbeitungsstift geändert werden, oder Sie können mit der rechten Maustaste klicken, um ihn ganz zu entfernen.

### Segmentfilter

Ziehen Sie ein beliebiges Segment aus der linken Leiste in den Ablagebereich des Bedienfelds, um mit dem Filtern des Bedienfelds zu beginnen.

![Filter](/help/admin/admin/assets/filter.png)

### Ad-hoc-Segmentfilter

Komponenten, die keine Segmente sind, können auch direkt in die Dropzone gezogen werden, um Ad-hoc-Segmente zu erstellen. So sparen Sie Zeit und Mühe beim Aufrufen von Segment Builder. Auf diese Weise erstellte Segmente werden automatisch als Segmente auf Trefferebene definiert. Diese Definition kann geändert werden, indem Sie auf das Informationssymbol (i) neben dem Segment und dann auf das stiftförmige Bearbeitungssymbol klicken und sie in Segment Builder bearbeiten.

Ad-hoc-Segmente sind eine Art Schnellsegment und für das Projekt lokal verfügbar. Sie werden nicht in der linken Leiste angezeigt, es sei denn, Sie machen sie öffentlich.

Weitere Informationen finden Sie unter [Schnellsegmente](/help/analyze/analysis-workspace/components/segments/quick-segments.md).

### Statische Dropdown-Filter

Dropdown-Filter ermöglichen Ihnen die kontrollierte Interaktion mit den Daten. Sie können beispielsweise einen Dropdown-Filter für Gerätetypen hinzufügen, damit Sie das Bedienfeld nach Tablet, Mobiltelefon oder Desktop segmentieren können.

Dropdown-Filter können auch verwendet werden, um viele Projekte zu einem zusammenzufassen. Wenn Sie beispielsweise mehrere Versionen desselben Projekts mit unterschiedlichen Ländersegmenten verwenden, können Sie alle Versionen in einem Projekt zusammenfassen und einen Dropdown-Filter „Land“ hinzufügen.

![](assets/dropdown-filter-intro.png)

So erstellen Sie einen statischen Dropdown-Filter:

* Klicken Sie bei Dropdown-Filtern, die Dimensionselemente verwenden, in der linken Leiste auf das Pfeilsymbol neben der gewünschten Dimension. Diese Aktion legt alle verfügbaren Dimensionselemente offen. Mehrere Dimensionselemente aus dieser Liste auswählen mithilfe von `[Shift + Click]` oder `[Ctrl + Click]`und legen Sie sie dann in der Dropzone des Bedienfelds ab **während des Betriebs`[Shift]`**.
* Für Dropdown-Filter mit anderen Komponenten wie Metriken, Segmenten oder Datumsbereichen wählen Sie mehrere Komponenten mithilfe von `[Shift + Click]` oder `[Ctrl + Click]`. Auswahl in die Dropzone des Bedienfelds legen **während des Betriebs`[Shift]`**. Alle Komponententypen werden in diesem Kontext als Segmente behandelt.
* Ein einzelner Dropdown-Filter kann nur einen Komponententyp enthalten. Wenn Sie mehrere Komponententypen in Ihre Auswahl aufnehmen, wird pro Komponententyp ein separater Dropdown-Filter erstellt. Wenn Sie beispielsweise sowohl Metriken als auch Dimensionselemente in Ihre Auswahl aufnehmen, werden zwei separate Dropdown-Filter erstellt. Ein Dropdown-Filter enthält Dimensionselemente, der andere wiederum Metriken.

Wählen Sie eine der Optionen aus der Dropdownliste aus, um die Daten im Bedienfeld zu ändern. Sie können auch auf die Filterung von Bedienfelddaten verzichten, indem Sie **[!UICONTROL Kein Filter]**.

![](assets/create-dropdown.png)

Wenn Sie mit der rechten Maustaste auf einen Dropdown-Filter klicken, stehen folgende Optionen zur Verfügung:

* **[!UICONTROL Bezeichnung hinzufügen]**: Wenn Sie einem Projekt einen Dropdown-Filter hinzufügen, wird für eine Beschriftung automatisch der Komponentenname festgelegt. Wenn Sie den Titel löschen, können Sie ihn mit dieser Option erneut hinzufügen.
* **[!UICONTROL Titel löschen]**: Entfernen Sie den Text über einem Dropdown-Filter.
* **[!UICONTROL Dropdown-Filter löschen]**: Entfernt den Dropdown-Filter aus dem Bereich.

[Sehen Sie sich das Video an,](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-panels-to-organize-your-analysis-workspace-projects.html?lang=de) um mehr über das Hinzufügen von Dropdown-Filtern zu Ihrem Projekt zu erfahren.

<!--### Dynamic drop-down filters

Dynamic drop-down filters allow you to determine available values based on data within the panel's reporting range and values in other drop-down filters. For example, you can create two dynamic drop-downs using the [Countries](/help/components/dimensions/countries.md) dimension and [Cities](/help/components/dimensions/cities.md) dimension. When you select a country from the [!UICONTROL Countries] drop-down list, the [!UICONTROL Cities] drop-down list dynamically adjusts to only show cities within that country.

This same concept applies to all dimensions; only dimension items that appear within the panel's date range and selected filters are visible. Dimension items selected in static drop-down filters affect available values in dynamic drop-down filters. However, the inverse is not true; Dimension items selected in dynamic drop-down filters do not affect available values in static drop-down filters.

Manual selection of dimension items is available if you anticipate a certain dimension item to be collected in the future. You can also clear a dynamic drop-down filter so that it does not contain a value, allowing other dynamic drop-down filters to contain more values. Select **[!UICONTROL Clear All]** to clear the selection from all drop-down filters for that panel.

To create a dynamic drop-down filter:

* Drag and drop a single dimension into the panel dropzone **while holding `[Shift]`**.
* Dynamic drop-down filters are not available for metrics, segments, or date ranges.
* Right-click a drop-down filter and select **[!UICONTROL Delete filter]** to delete it.

Right-clicking a dynamic drop-down filter provides the same options as static drop-down filters.-->

## Rechtsklickmenü {#right-click}

Weitere Funktionen für ein Bedienfeld sind verfügbar, wenn Sie mit der rechten Maustaste auf die Bedienfeldkopfzeile klicken.

![Rechtsklickmenü](assets/right-click-menu.png)

Folgende Einstellungen sind verfügbar:

| Einstellung | Beschreibung |
| --- | --- |
| Kopiertes Bedienfeld/kopierte Visualisierung einfügen | Ermöglicht das Einfügen (&quot;Einfügen&quot;) eines kopierten Bedienfelds oder einer kopierten Visualisierung an einer anderen Stelle innerhalb des Projekts oder in ein anderes Projekt. |
| Bedienfeld kopieren | Ermöglicht Ihnen das Rechtsklicken und Kopieren eines Bedienfelds, sodass Sie es an einer anderen Stelle innerhalb des Projekts oder in ein anderes Projekt einfügen können. |
| Anwenden einer Report Suite auf alle Panels | Damit können Sie die Report Suite des aktiven Bedienfelds auf alle Bedienfelder im Projekt anwenden. |
| Bedienfeld duplizieren | Fertigt ein exaktes Duplikat des aktuellen Bedienfelds an, das Sie dann bearbeiten können. |
| Alle Bedienfelder reduzieren/erweitern | Reduziert und erweitert alle Projektbedienfelder. |
| Alle Visualisierungen im Bedienfeld reduzieren/erweitern | Reduziert bzw. erweitert alle Visualisierungen im aktuellen Bedienfeld. |
| Beschreibung bearbeiten | Hiermit können Sie einen Text zur Beschreibung des Bedienfelds hinzufügen (oder bearbeiten). |
| Bereichslink abrufen | Sie können Personen zu einem bestimmten Bereich innerhalb eines Projekts leiten. Wenn auf den Link geklickt wird, muss sich der Empfänger anmelden, bevor er zu genau dem Bedienfeld weitergeleitet wird, mit dem er verknüpft ist. |
