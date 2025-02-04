---
title: Was ist eine Kohortenanalyse und wie funktioniert sie?
description: Informieren Sie sich genauer über die Daten rund um Ihre Zielgruppe und unterteilen Sie sie mit der Kohortenanalyse in die zugehörigen Gruppen. Erfahren Sie mehr über die Kohortenanalyse in Analysis Workspace.
feature: Cohort Analysis
role: User, Admin
exl-id: 6a46e76f-671e-4b1b-933a-6c2776c72d09
source-git-commit: 1ce002a513860ce15dc8a70825d26795fd93eb1d
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 33%

---

# Überblick über Kohortentabellen {#cohort-table-overview}


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_cohorttable_button"
>title="Kohortentabelle"
>abstract="Erstellen Sie eine Kohortenvisualisierung, um Benutzende bei Abschluss eines Ereignisses zu gruppieren und die anhaltende Interaktion und Abwanderung im Zeitverlauf zu analysieren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_cohorttable_panel"
>title="Kohortentabelle"
>abstract="Gruppieren Sie Benutzende bei Abschluss eines Ereignisses und analysieren Sie dann ihre anhaltenden Interaktionen und Abwanderungen im Zeitverlauf.<br/><br/>**Parameter **<br/>**Aufnahmekriterien**: Die Komponenten, die zur Definition der anfänglichen Besucherkohorten verwendet werden.<br/>**Rückkehrkriterien**: Die Komponenten, mit denen bestimmt wird, ob eine Besucherin bzw. ein Besucher zurückgekehrt ist."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_In diesem Artikel wird die Kohortentabelle in {_}![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_Siehe [Kohortentabelle](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/cohort-table/cohort-analysis) für die_![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**-Version dieses Artikels._

>[!ENDSHADEBOX]



Eine *Kohorte* ist eine Personengruppe mit gemeinsamen Merkmalen innerhalb eines bestimmten Zeitraums. Eine ![TextNumbered](/help/assets/icons/TextNumbered.svg)**[!UICONTROL Kohortentabelle]** Visualisierung ist beispielsweise nützlich, wenn Sie erfahren möchten, wie eine Kohorte mit einer Marke interagiert. Sie können problemlos Trend-Änderungen offenlegen und entsprechend reagieren. (Erläuterungen zur [!UICONTROL Kohortenanalyse] sind im Internet verfügbar, z. B. unter [Cohort Analysis 101](https://de.wikipedia.org/wiki/Cohort_analysis).)

Nachdem Sie einen Kohortenbericht erstellt haben, können Sie dessen Komponenten (bestimmte Dimensionen, Metriken und Filter) kuratieren und den Kohortenbericht dann für andere freigeben. Weitere Informationen finden Sie unter [Kuratieren und freigeben](/help/analyze/analysis-workspace/curate-share/curate.md).

Beispiele für Möglichkeiten einer „Kohortentabelle:

* Starten Sie Kampagnen, die dafür ausgelegt sind, eine erwünschte Aktion anzuregen.
* Erhöhen Sie das Marketingbudget genau zum richtigen Zeitpunkt im Kundenlebenszyklus.
* Erkennen Sie, wann Sie eine Testversion oder ein Angebot beenden müssen, um den Wert zu maximieren.
* Gewinnen Sie Ideen für A/B-Tests in Bereichen wie Preisstruktur, Upgrade-Pfad usw.

[!UICONTROL Kohortentabelle] ist für alle Customer Journey Analytics-Kunden mit Zugriffsrechten auf [!UICONTROL Analysis Workspace verfügbar].


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Kohortenanalyse in Analysis Workspace](https://video.tv.adobe.com/v/23990/?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


>[!IMPORTANT]
>
>[!UICONTROL Kohortenanalyse] unterstützt keine nicht filterbaren Metriken (einschließlich berechneter Metriken), Nicht-Ganzzahlmetriken (z. B. Umsatz) oder Vorfälle. In der Kohortenanalyse können nur Metriken verwendet werden[!UICONTROL  die in Filtern verwendet werden können] und sie können jeweils nur 1 inkrementiert werden.

Kohortentabellen in Customer Journey Analytics unterstützen doppelbasierte (oder beliebige numerische) Metriken. Beispielsweise kann „Purchase.Value“ (ein doppelter Wert) als Einschluss-/Rückgabe-Metrik verwendet werden. Darüber hinaus sind alle Metriken, die über den Analytics Source Connector an Adobe Experience Platform übergeben werden, ebenfalls doppelt vorhanden.

## Kohortentabellen-Funktionen

In den folgenden Abschnitten werden Funktionen zur Kohortenanalyse beschrieben, die eine Feinabstimmung der Kontrolle über die Kohorten ermöglichen, die Sie erstellen.

Weitere Informationen zum Erstellen einer Kohorte und zum Ausführen eines Berichts [!UICONTROL Kohortenanalyse] finden Sie unter [Konfigurieren einer Kohortentabelle](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).

### [!UICONTROL Beibehaltung] Tabelle

Eine [!UICONTROL Bindung] Kohortentabelle gibt Personen zurück: Jede Datenzelle zeigt die Rohanzahl und den Prozentsatz der Personen in der Kohorte an, die die Aktion während dieses Zeitraums ausgeführt haben. Sie können bis zu 3 Metriken und bis zu 10 Filter einschließen.

![Ein Kohortenbericht zur Rente, der die Einheiten und den Prozentsatz der Personen in der Kohorte ausgibt.](assets/retention-report.png)

### [!UICONTROL Abwanderung] Tabelle

Eine [!UICONTROL Abwanderungs]-Kohortentabelle ist das Gegenteil einer Bindungstabelle und zeigt die Personen, die im Laufe der Zeit ausgefallen sind oder die Rückkehrkriterien für Ihre Kohorte nie erfüllt haben. Sie können bis zu 3 Metriken und bis zu 10 Filter einschließen.

![Eine Tabelle mit den Einheiten und dem Prozentsatz der Menschen, die die Rückkehrkriterien für eine Kohorte nicht erfüllten.](assets/churn-report.png)

### [!UICONTROL Rollierende Berechnung]

Sie können die Beibehaltung oder Abwanderung basierend auf der vorherigen Spalte berechnen, nicht basierend auf der eingeschlossenen Spalte, die als rollierende Berechnung bezeichnet wird.

![Ein Kohortenbeibehaltungsbericht, der Berechnungen zeigt, die auf einer vorherigen Datenspalte basieren.](assets/retention-report-rolling.png)

### [!UICONTROL Latenz]-Tabelle

Eine Latenztabelle misst die Zeit, die vor und nach dem Einschlussereignis verstrichen ist. Die Latenzmessung ist ein hervorragendes Tool für Vor- und Nachanalysen. Die Spalte **[!UICONTROL Aufnahme]** befindet sich in der Mitte der Tabelle und die Zeiträume vor und nach dem Aufnahmeereignis werden auf beiden Seiten angezeigt.

![Ein Kohortenbericht, der die verstrichene Zeit vor und nach einem Ereignis zeigt.](assets/retention-report-latency.png)

### [!UICONTROL Benutzerdefinierte Dimension] Kohorte

Sie können Kohorten basierend auf einer ausgewählten Dimension und nicht auf zeitbasierten Kohorten erstellen (die der Standard sind). Verwenden Sie Dimensionen wie [!UICONTROL Stadt], [!UICONTROL Marketing-Kanal], [!UICONTROL Kampagne], [!UICONTROL Produkt], [!UICONTROL Seite], [!UICONTROL Region] oder jede andere Dimension, um Änderungen der Kundenbindung anzuzeigen. Basierend auf den verschiedenen Werten dieser Dimensionen.

![Ein Kohortenbericht, der benutzerdefinierte Berichte mit ausgewählten Dimensionen zeigt, nicht die standardmäßige zeitbasierte Kohorte.](assets/retention-dimensions.png)

>[!MORELIKETHIS]
>
>[Konfigurieren einer Kohortentabelle](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).
>



<!--
A *`cohort`* is a group of people sharing common characteristics over a specified period. [!UICONTROL Cohort Analysis] is useful, for example, when you want to learn how a cohort engages with a brand. You can easily spot changes in trends, then respond accordingly. (Explanations of [!UICONTROL Cohort Analysis] are available on the web, such as at [Cohort Analysis 101](https://en.wikipedia.org/wiki/Cohort_analysis).)

After creating a cohort report, you can curate its components (specific dimensions, metrics, and segments), then share the cohort report with anyone. See [Curate and Share](/help/analyze/analysis-workspace/curate-share/curate.md).

Examples of what you can do with [!UICONTROL Cohort Analysis]:

* Launch campaigns designed to spur a desired action.
* Shift marketing budget at exactly the right time in the customer lifecycle.
* Recognize when to end a trial or an offer, in order to maximize value.
* Gain ideas for A/B testing in areas such as pricing, upgrade path, and so on.

[!UICONTROL Cohort Analysis] is available for all Adobe Analytics customers with access rights to [!UICONTROL Analysis Workspace].


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Cohort analysis in Analysis Workspace](https://video.tv.adobe.com/v/25965?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>[!UICONTROL Cohort Analysis] does not support non-segmentable metrics (including calculated metrics), non-integer metrics (such as Revenue), or Occurrences. 
>
>Only metrics that can be used in segments can be used in [!UICONTROL Cohort Analysis], and they can only be incremented by >1 at a time. 

## Cohort Analysis capabilities

The following sections describe Cohort Analysis features that allow for fine-tuned control over the cohorts you are building.

For more detailed information about creating a cohort and running a [!UICONTROL Cohort Analysis] report, see [Configure a Cohort Analysis report](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md).

### [!UICONTROL Retention] Table

A [!UICONTROL Retention] cohort report returns visitors: each data cell shows the raw number and percentage of visitors in the cohort who did the action during that time period. You can include up to 3 metrics and up to 10 segments.

![](assets/retention-report.png)


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Calculate rolling retention](https://video.tv.adobe.com/v/25962?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]



### [!UICONTROL Churn] Table

A [!UICONTROL Churn] cohort is the inverse of a retention table and shows the visitors who fell out or never met the return criteria for your cohort over time. You can include up to 3 metrics and up to 10 segments.

![](assets/churn-report.png)

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Churn analysis](https://video.tv.adobe.com/v/25966?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]


### [!UICONTROL Rolling Calculation]

Lets you calculate retention or churn based on the previous column, not the included column.

![](assets/cohort-rolling-calculation.png)

### [!UICONTROL Latency] Table

Measures the time that has elapsed before and after the inclusion event occurred. This is an excellent tool for pre/post analysis. The **[!UICONTROL Included]** column is in the center of the table and time periods before and after the inclusion event are shown on both sides.

![](assets/cohort-latency.png)

### [!UICONTROL Custom Dimension] Cohort

Create cohorts based on a selected dimension, and not time-based cohorts, which are the default. Use dimensions such as [!UICONTROL marketing channel], [!UICONTROL campaign], [!UICONTROL product], [!UICONTROL page], [!UICONTROL region], or any other dimension in Adobe Analytics to show how retention changes based on the different values of these dimensions.

![](assets/cohort-customizable-cohort-row.png)

-->
