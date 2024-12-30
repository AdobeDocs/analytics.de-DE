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

Die Bedienfelder [!UICONTROL Quick Insights], [!UICONTROL Leer] und [!UICONTROL Freiform] eignen sich hervorragend als Ausgangspunkt für Ihre Analyse. [!UICONTROL Analytics for Target], [!UICONTROL Attribution], [!UICONTROL Media Concurrent Viewers] und [!UICONTROL Segmentvergleich] eignen sich für erweiterte Analysen. In Projekten steht eine `"+"`-Schaltfläche zur Verfügung, mit der Sie jederzeit leere Bedienfelder hinzufügen können.

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

Ziehen Sie beliebige Segmente aus der linken Leiste in den Ablagebereich des Bedienfelds, um mit dem Filtern des Bedienfelds zu beginnen. Wiederholen Sie diesen Vorgang, um dem Bedienfeld weitere Filter hinzuzufügen. Filter werden oben im Bedienfeld nebeneinander angezeigt.

![Filter](assets/segment-filter.png)

### Ad-hoc-Segmentfilter

Komponenten, die keine Segmente sind, können auch direkt in den Ablagebereich gezogen werden, um Ad-hoc-Segmente zu erstellen, sodass Sie sich das mühsame Aufrufen von Segment Builder ersparen. Auf diese Weise erstellte Segmente werden automatisch als Segmente auf Trefferebene definiert. Diese Definition kann geändert werden, indem Sie auf das Informationssymbol (i) neben dem Segment und dann auf das stiftförmige Bearbeitungssymbol klicken und sie in Segment Builder bearbeiten.

Ad-hoc-Segmente sind eine Art von Schnellsegmenten und lokal im Projekt verfügbar. Sie werden nicht in der linken Leiste angezeigt, es sei denn, Sie machen sie öffentlich.

Weitere Informationen finden Sie unter [Schnellsegmente](/help/analyze/analysis-workspace/components/segments/quick-segments.md).

### Statische Dropdown-Segmente

Statische Dropdown-Segmente ermöglichen eine kontrollierte Interaktion mit den Daten. Sie können beispielsweise ein Dropdown-Segment für Typen von Mobilgeräten hinzufügen, damit Sie das Bedienfeld nach Tablet, Mobiltelefon oder Desktop segmentieren können.

Statische Dropdown-Segmente können auch verwendet werden, um viele Projekte zu einem zusammenzufassen. Wenn Sie beispielsweise viele Versionen desselben Projekts mit unterschiedlichen Ländersegmenten angewendet haben, können Sie alle Versionen in einem Projekt zusammenfassen und ein Dropdown-Segment Land hinzufügen.

![](assets/dropdown-filter-intro.png)

#### Erstellen statischer Dropdown-Segmente

* Bei Dropdown-Segmenten, die Dimensionselemente verwenden, wählen Sie eine einzelne Dimension aus der linken Leiste aus und legen Sie sie im Ablagebereich des Bedienfelds ab **während Sie`[Shift]`** gedrückt halten. Dadurch wird ein Dropdown-Segment mit allen Dimensionselementen erstellt, die mit dieser Dimension verknüpft sind.

  Wenn das Dropdown-Segment nur bestimmte Dimensionselemente enthalten soll, die mit einer Dimension verknüpft sind, klicken Sie auf das Pfeil-nach-rechts-Symbol neben der gewünschten Dimension in der linken Leiste. Diese Aktion legt alle verfügbaren Dimensionselemente offen. Wählen Sie mithilfe von `[Shift + Click]` oder `[Ctrl + Click]` mehrere Dimensionselemente aus dieser Liste aus und legen Sie sie dann im Ablegebereich des Bedienfelds ab, **während** Sie `[Shift]` gedrückt halten.

* Wählen Sie für Dropdown-Segmente, die einen einzelnen Komponententyp verwenden (z. B. nur Dimensionen oder nur Segmente oder nur Metriken), in der linken Leiste mithilfe von `[Shift + Click]` oder `[Ctrl + Click]` mehrere Elemente desselben Typs aus und legen Sie sie dann im Ablagebereich des Bedienfelds ab **während Sie`[Shift]`** gedrückt halten.

  Ein einzelnes Dropdown-Segment wird mit ausgewählten Komponenten erstellt.

* Wählen Sie für Dropdown-Segmente, die einen Mix aus Komponententypen verwenden (z. B. zwei Metriken und drei Filter), mehrere Komponenten mit `[Shift + Click]` oder `[Ctrl + Click]` aus. Legen Sie die Auswahl im Ablegebereich des Bedienfelds ab, **während Sie`[Shift]`** gedrückt halten. In diesem Kontext werden alle Komponententypen als separate Dropdown-Segmente behandelt. Wenn Sie beispielsweise sowohl Metriken als auch Dimensionselemente in Ihre Auswahl einbeziehen, werden zwei separate Dropdown-Segmente erstellt: eines der Dropdown-Segmente enthält Dimensionselemente und das andere enthält Metriken.

  ![Das Bedienfeldfenster mit dem Feld Mobile-Kundensegment , das zum Ablegen eines statischen Dropdown-Segments verfügbar ist. ](assets/create-dropdown.png)

Wenn Sie mit der rechten Maustaste auf ein Dropdown-Segment klicken, erhalten Sie die folgenden Optionen:

* **[!UICONTROL Dropdown löschen]**: Entfernt das Dropdown-Segment aus dem Bedienfeld.
* **[!UICONTROL Bezeichnung löschen]**: Entfernen des Textes über einem Dropdown-Segment. Wählen Sie zum Ändern des Labels das Stiftsymbol aus.
* **[!UICONTROL Beschriftung hinzufügen]**: Wenn Sie einem Projekt ein Dropdown-Segment hinzufügen, wird eine Beschriftung automatisch auf den Komponentennamen festgelegt. Wenn Sie den Titel löschen, können Sie ihn mit dieser Option erneut hinzufügen.
* **[!UICONTROL Auswahl erforderlich]**: Erfordert, dass ein Segment im Bedienfeld festgelegt wird.

[Sehen Sie sich das Video an](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-panels-to-organize-your-analysis-workspace-projects.html?lang=de), um mehr über das Hinzufügen von Dropdown-Filtern zu Ihrem Projekt zu erfahren.

#### Verwenden von statischen Dropdown-Segmenten

Verwenden Sie das Dropdown-Menü Segmente auf eine der folgenden Arten, um das Bedienfeld zu filtern:

* Wenden Sie ein einzelnes Segment auf das Bedienfeld an, indem Sie das Segment aus dem Dropdown-Menü auswählen.

* Wenden Sie mehrere Segmente auf das Bedienfeld an, indem Sie mehr als ein Segment aus dem Dropdown-Menü auswählen. Das Bedienfeld wird so gefiltert, dass es jedes der ausgewählten Segmente enthält.

  Um ein Segment aus der Liste zu entfernen, wählen Sie es im Dropdownmenü erneut aus.

  ![Mehrere Segmente auswählen](assets/dropdown-filter-multiselect.png)

### Dynamische Dropdown-Segmente

Mit dynamischen Dropdown-Segmenten können Sie verfügbare Werte auf der Grundlage von Daten innerhalb des Berichtsbereichs des Bedienfelds und Werte in anderen Dropdown-Segmenten bestimmen. Sie können beispielsweise zwei dynamische Dropdown-Listen mit den Dimensionen &quot;[&quot; ](/help/components/dimensions/countries.md) &quot;[&quot; ](/help/components/dimensions/cities.md). Wenn Sie ein Land aus der Dropdownliste [!UICONTROL Länder] auswählen, wird die Dropdownliste [!UICONTROL Städte] dynamisch angepasst, sodass nur Städte innerhalb dieses Landes angezeigt werden.

Dasselbe Konzept gilt für alle Dimensionen. Nur Dimensionselemente, die innerhalb des Datumsbereichs und der ausgewählten Segmente des Bedienfelds angezeigt werden, sind sichtbar. In statischen Dropdown-Segmenten ausgewählte Segmentelemente wirken sich auf verfügbare Werte in dynamischen Dropdown-Dimensionen aus. Das Gegenteil trifft jedoch nicht zu. In der Dropdown-Liste Dynamische Segmente ausgewählte Segmentelemente wirken sich nicht auf verfügbare Werte in statischen Dropdown-Dimensionen aus.

Eine manuelle Auswahl von Dimensionselementen ist verfügbar, wenn Sie erwarten, dass ein bestimmtes Dimensionselement in Zukunft erfasst wird. Sie können ein dynamisches Dropdown-Segment auch löschen, sodass es keinen Wert enthält, sodass andere dynamische Dropdown-Segmente weitere Werte enthalten können. Wählen Sie **[!UICONTROL Alle zurücksetzen]** aus, um die Auswahl aus allen Dropdown-Segmenten für dieses Bedienfeld zu löschen.

So erstellen Sie ein dynamisches Dropdown-Segment:

* Ziehen Sie eine einzelne Dimension in den Ablegebereich des Bedienfelds, **während Sie`[Shift]`** gedrückt halten.
* Dynamische Dropdown-Segmente sind für Metriken, Segmente oder Datumsbereiche nicht verfügbar.
* Klicken Sie mit der rechten Maustaste auf ein Dropdown-Segment und wählen Sie **[!UICONTROL Dropdown löschen]**, um es zu löschen.

Wenn Sie mit der rechten Maustaste auf einen dynamischen Dropdown-Filter klicken, stehen dieselben Optionen zur Verfügung wie für statische Dropdown-Filter.

## Rechtsklickmenü {#right-click}

Weitere Funktionen für ein Bedienfeld sind verfügbar, wenn Sie mit der rechten Maustaste auf die Bedienfeldüberschrift klicken.

![Kontextmenü](assets/right-click-menu.png)

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
