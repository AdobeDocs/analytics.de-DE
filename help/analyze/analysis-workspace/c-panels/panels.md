---
description: Ein Bedienfeld ist eine Sammlung von Tabellen und Visualisierungen
title: Übersicht über Bedienfelder
feature: Panels
role: User, Admin
exl-id: dd1a3c40-8b5b-47dd-86d9-da766575ee46
source-git-commit: aacba26d0eb612146a9e0bf6386f9e755a9e8f07
workflow-type: tm+mt
source-wordcount: '1582'
ht-degree: 54%

---

# Übersicht über Bedienfelder

Ein [!UICONTROL Bedienfeld] ist eine Sammlung von Tabellen und Visualisierungen. Sie können über das Symbol oben links in Arbeitsbereich oder über ein [leeres Bedienfeld](blank-panel.md) auf Bedienfelder zugreifen. Panels sind hilfreich, wenn Sie Ihre Projekte nach Zeiträumen, Report Suites oder Analysen ordnen möchten. 

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
| [Bedienfeld „Mit Medienwiedergabe verbrachte Zeit“](/help/analyze/analysis-workspace/c-panels/media-playback-time-spent.md) | Analysieren Sie gleichzeitige Betrachter über einen längeren Zeitraum. Sie erhalten Details zum maximalen gleichzeitigen Zugriff und die Möglichkeit, aufzuschlüsseln und zu vergleichen. |
| [Bedienfeld „Segmentvergleich“](c-segment-comparison/segment-comparison.md) | Vergleichen Sie schnell zwei Segmente über alle Datenpunkte hinweg, um automatisch relevante Unterschiede zu ermitteln. |

![](assets/panel-overview.png)

Die Bedienfelder [!UICONTROL Quick Insights], [!UICONTROL Blank] und [!UICONTROL Freiform] eignen sich hervorragend als Ausgangspunkt für Ihre Analyse, während sich die Bedienfelder [!UICONTROL Analytics for Target], [!UICONTROL Attribution], [!UICONTROL Gleichzeitige Medienbetrachter] und [!UICONTROL Segmentvergleich] für erweiterte Analysen eignen. In Projekten steht eine `"+"`-Schaltfläche zur Verfügung, mit der Sie jederzeit leere Bedienfelder hinzufügen können.

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

Mit dem Ablegebereich eines Panels können Sie Segment- und Dropdown-Filter auf alle Tabellen und Visualisierungen innerhalb des Panels anwenden. Sie können einen oder mehrere Filter auf ein Bedienfeld anwenden.

### Segmentfilter

Ziehen Sie alle Segmente aus der linken Leiste in die Dropzone des Bedienfelds, um mit dem Filtern Ihres Bedienfelds zu beginnen. Wiederholen Sie diesen Vorgang, um dem Bedienfeld weitere Filter hinzuzufügen. Filter werden oben im Bedienfeld nebeneinander angezeigt.

![Filter](assets/segment-filter.png)

### Ad-hoc-Segmentfilter

Komponenten, die keine Segmente sind, können auch direkt in die Dropzone gezogen werden, um Ad-hoc-Segmente zu erstellen. So sparen Sie Zeit und Mühe beim Aufrufen von Segment Builder. Auf diese Weise erstellte Segmente werden automatisch als Segmente auf Trefferebene definiert. Diese Definition kann geändert werden, indem Sie auf das Informationssymbol (i) neben dem Segment und dann auf das stiftförmige Bearbeitungssymbol klicken und sie in Segment Builder bearbeiten.

Ad-hoc-Segmente sind eine Art Schnellsegment und für das Projekt lokal verfügbar. Sie werden nicht in der linken Leiste angezeigt, es sei denn, Sie machen sie öffentlich.

Weitere Informationen finden Sie unter [Schnellsegmente](/help/analyze/analysis-workspace/components/segments/quick-segments.md).

### Statische Dropdown-Segmente

Statische Dropdown-Segmente ermöglichen Ihnen eine kontrollierte Interaktion mit den Daten. Sie können beispielsweise ein Dropdown-Segment für Mobilgerätetypen hinzufügen, damit Sie das Bedienfeld nach Tablet, Mobiltelefon oder Desktop segmentieren können.

Statische Dropdown-Segmente können auch verwendet werden, um viele Projekte zu einem zusammenzufassen. Wenn Sie beispielsweise über viele Versionen desselben Projekts mit verschiedenen Ländersegmenten verfügen, können Sie alle Versionen in einem Projekt zusammenfassen und ein Dropdown-Segment &quot;Land&quot;hinzufügen.

![](assets/dropdown-filter-intro.png)

#### Erstellen von statischen Dropdown-Segmenten

* Wählen Sie für Dropdown-Segmente, die Dimensionselemente verwenden, eine einzelne Dimension aus der linken Leiste aus und legen Sie sie in der Dropzone des Bedienfelds ab **, während Sie`[Shift]`** gedrückt halten. Dadurch wird ein Dropdown-Segment mit allen Dimensionselementen erstellt, die mit dieser Dimension verknüpft sind.

  Wenn Sie auch möchten, dass das Dropdown-Segment nur bestimmte Dimensionselemente enthält, die mit einer Dimension verknüpft sind, klicken Sie in der linken Leiste auf das Pfeilsymbol neben der gewünschten Dimension. Diese Aktion legt alle verfügbaren Dimensionselemente offen. Wählen Sie mithilfe von `[Shift + Click]` oder `[Ctrl + Click]` mehrere Dimensionselemente aus dieser Liste aus und legen Sie sie dann im Ablegebereich des Bedienfelds ab, **während** Sie `[Shift]` gedrückt halten.

* Wählen Sie für Dropdown-Segmente, die einen einzelnen Komponententyp verwenden (z. B. nur Dimensionen oder nur Segmente oder nur Metriken), mehrere Elemente desselben Typs in der linken Leiste mit `[Shift + Click]` oder `[Ctrl + Click]` aus und legen Sie sie dann in der Dropzone **ab, während Sie`[Shift]`** gedrückt halten.

  Ein einzelnes Dropdown-Segment wird mit den von Ihnen ausgewählten Komponenten erstellt.

* Wählen Sie für Dropdown-Segmente mit einer Mischung aus Komponententypen (z. B. 2 Metriken und 3 Filter) mehrere Komponenten mit `[Shift + Click]` oder `[Ctrl + Click]` aus. Legen Sie die Auswahl im Ablegebereich des Bedienfelds ab, **während Sie`[Shift]`** gedrückt halten. In diesem Kontext werden alle Komponententypen als separate Dropdown-Segmente behandelt. Wenn Sie beispielsweise sowohl Metriken als auch Dimensionselemente in Ihre Auswahl aufnehmen, werden zwei separate Dropdown-Segmente erstellt: eines enthält Dimensionselemente, das andere wiederum Metriken.

  ![Das Fenster Bedienfeld mit dem Feld Mobilkundensegment , das zum Ablegen eines statischen Dropdown-Segments verfügbar ist. ](assets/create-dropdown.png)

Wenn Sie mit der rechten Maustaste auf ein Dropdown-Segment klicken, stehen folgende Optionen zur Verfügung:

* **[!UICONTROL Dropdown-Liste löschen]**: Entfernt das Dropdown-Segment aus dem Bereich.
* **[!UICONTROL Titel löschen]**: Entfernen Sie den Text über einem Dropdown-Segment. Wählen Sie zum Ändern des Labels das Stiftsymbol aus.
* **[!UICONTROL Titel hinzufügen]**: Wenn Sie ein Dropdown-Segment zu einem Projekt hinzufügen, wird für eine Beschriftung automatisch der Komponentenname festgelegt. Wenn Sie den Titel löschen, können Sie ihn mit dieser Option erneut hinzufügen.
* **[!UICONTROL Auswahl erforderlich]**: Erfordert, dass ein Segment im Bereich festgelegt wird.

[Sehen Sie sich das Video an](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-panels-to-organize-your-analysis-workspace-projects.html?lang=de), um mehr über das Hinzufügen von Dropdown-Filtern zu Ihrem Projekt zu erfahren.

#### Verwenden von statischen Dropdown-Segmenten

Verwenden Sie das Dropdown-Menü für Segmente auf eine der folgenden Arten, um den Bereich zu filtern:

* Wenden Sie ein einzelnes Segment auf das Bedienfeld an, indem Sie das Segment aus dem Dropdown-Menü auswählen.

* Wenden Sie mehrere Segmente auf das Bedienfeld an, indem Sie mehr als ein Segment aus dem Dropdown-Menü auswählen. Das Bedienfeld wird gefiltert, um eines der ausgewählten Segmente einzuschließen.

  Um ein Segment aus der Liste zu entfernen, wählen Sie es erneut im Dropdown-Menü aus.

  ![Mehrere Segmente auswählen](assets/dropdown-filter-multiselect.png)

### Dynamische Dropdown-Segmente

Mit dynamischen Dropdown-Segmenten können Sie verfügbare Werte basierend auf Daten innerhalb des Berichtsbereichs des Bedienfelds und Werte in anderen Dropdown-Segmenten bestimmen. Sie können beispielsweise mithilfe der Dimension [Länder](/help/components/dimensions/countries.md) und der Dimension [Städte](/help/components/dimensions/cities.md) zwei dynamische Dropdown-Listen erstellen. Wenn Sie ein Land aus der Dropdownliste [!UICONTROL Länder] auswählen, wird die Dropdownliste [!UICONTROL Städte] dynamisch angepasst, um nur Städte in diesem Land anzuzeigen.

Dieses Konzept gilt für alle Dimensionen. Es sind nur Dimensionselemente sichtbar, die innerhalb des Datumsbereichs des Bedienfelds angezeigt werden, sowie ausgewählte Segmente. In statischen Dropdown-Dimensionen ausgewählte Elemente wirken sich auf verfügbare Werte in dynamischen Dropdown-Segmenten aus. Das Gegenteil ist jedoch nicht der Fall. In dynamischen Dropdown-Dimensionen ausgewählte Elemente wirken sich nicht auf verfügbare Werte in statischen Dropdown-Segmenten aus.

Eine manuelle Auswahl von Dimensionselementen ist verfügbar, wenn Sie erwarten, dass ein bestimmtes Dimensionselement in Zukunft erfasst wird. Sie können auch ein dynamisches Dropdown-Segment löschen, sodass es keinen Wert enthält, sodass andere dynamische Dropdown-Segmente mehr Werte enthalten können. Wählen Sie **[!UICONTROL Alle zurücksetzen]** aus, um die Auswahl aus allen Dropdown-Segmenten für dieses Bedienfeld zu löschen.

So erstellen Sie ein dynamisches Dropdown-Segment:

* Ziehen Sie eine einzelne Dimension in den Ablegebereich des Bedienfelds, **während Sie`[Shift]`** gedrückt halten.
* Dynamische Dropdown-Segmente sind nicht für Metriken, Segmente oder Datumsbereiche verfügbar.
* Klicken Sie mit der rechten Maustaste auf ein Dropdown-Segment und wählen Sie **[!UICONTROL Dropdown-Liste löschen]** aus, um es zu löschen.

Wenn Sie mit der rechten Maustaste auf einen dynamischen Dropdown-Filter klicken, stehen dieselben Optionen zur Verfügung wie für statische Dropdown-Filter.

## Rechtsklickmenü {#right-click}

Weitere Funktionen für ein Bedienfeld sind verfügbar, wenn Sie mit der rechten Maustaste auf die Bedienfeldüberschrift klicken.

![ Rechtsklick auf Menü](assets/right-click-menu.png)

Folgende Einstellungen sind verfügbar:

| Einstellung | Beschreibung |
| --- | --- |
| Kopiertes Bedienfeld/kopierte Visualisierung einfügen | Ermöglicht es Ihnen, das kopierte Bedienfeld oder die kopierte Visualisierung an einer anderen Stelle innerhalb des Projekts oder in ein ganz anderes Projekt einzufügen. |
| Bedienfeld kopieren | Ermöglicht es Ihnen, mit der rechten Maustaste auf ein Bedienfeld zu klicken und es zu kopieren, sodass Sie es an einer anderen Stelle innerhalb des Projekts oder in ein anderes Projekt einfügen können. |
| Anwenden einer Report Suite auf alle Panels | Damit können Sie die Report Suite des aktiven Bedienfelds auf alle Bedienfelder im Projekt anwenden. |
| Bedienfeld duplizieren | Fertigt ein exaktes Duplikat des aktuellen Bedienfelds an, das Sie dann bearbeiten können. |
| Alle Bedienfelder reduzieren/erweitern | Reduziert und erweitert alle Projektbedienfelder. |
| Alle Visualisierungen im Bedienfeld reduzieren/erweitern | Reduziert bzw. erweitert alle Visualisierungen im aktuellen Bedienfeld. |
| Beschreibung bearbeiten | Hiermit können Sie einen Text zur Beschreibung des Bedienfelds hinzufügen (oder bearbeiten). |
| Bereichslink abrufen | Sie können Personen zu einem bestimmten Bereich innerhalb eines Projekts leiten. Wenn auf den Link geklickt wird, muss sich der Empfänger anmelden, bevor er zu genau dem Bedienfeld weitergeleitet wird, mit dem er verknüpft ist. |
