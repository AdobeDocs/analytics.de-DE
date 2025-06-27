---
description: Berechnete und erweiterte berechnete Metriken sind benutzerdefinierte Metriken, die Sie über vorhandene Metriken erstellen können.
keywords: Berechnete Metriken;erweiterte berechnete Metriken
title: Berechnete und erweiterte berechnete Metriken
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: d85e6990998e3c153ef969d8dc7f3a4835f683bf
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 36%

---

# Überblick über berechnete Metriken

Berechnete und benutzerdefinierte Metriken, die Sie aus vorhandenen Metriken erstellen können.

Berechnete Metriken bieten eine äußerst flexible Möglichkeit zum Erstellen, Verwalten und Kuratieren von Metriken. Mit berechneten Metriken können Sie als Marketing-Experten, Produkt-Manager und Analysten Fragen zu den Daten stellen, ohne Ihre [!DNL Analytics]-Implementierung ändern zu müssen.

Berechnete Metriken sind in jedem [!DNL Analytics] verfügbar, jedoch ist das Adobe Analytics Foundation Pack für Experience Cloud auf grundlegende berechnete Metriken beschränkt, einschließlich [Formattypen (Dezimal, Zeit, Prozent, Währung)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) ([Zuordnungsänderungen (Standard, linear, Teilnahme usw.)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md), [Metriktypen (Standard, Gesamt)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) und [Grundoperatoren](c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md#operators) (hinzufügen, subtrahieren, multiplizieren und teilen).


Weitere Informationen finden Sie in der &lbrace;0[&#128279;](https://helpx.adobe.com/de/legal/product-descriptions/adobe-analytics.html) Adobe Analytics-Produktbeschreibung.

<!--
Here is a comparison of calculated metrics and advanced calculated metrics capabilities: 

| [Format types (decimal, time, percent, currency)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
| [Attribution changes (default, linear, participation, etc.)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
| [Metric types (standard, total)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
|  Basic operators (add, subtract, multiply, divide)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  | ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)  |
| [Apply segments](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md)  | ![StopCircle](/help/assets/icons/StopCircle.svg)  | Yes  |
| [Basic functions (count, abs value, mean, etc)](/help/components/c-calcmetrics/cm-reference/cm-functions.md)  | No  | Yes  |
| [Advanced functions (regression, if/then, t-score, etc)](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md)  | No  | Yes  |

-->

## Funktionen {#section_A0A5C275B68A4D628950BBB0B1EE631F}

Sie können

* [Metriken erstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-workflow.md) für [!UICONTROL Analysis Workspace], [!UICONTROL Report Builder], [!UICONTROL Anomalieerkennung] und [!UICONTROL Beitragsanalyse].
* [Segmentierte Metriken erstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) die zur Berichtslaufzeit abgeleitet werden, ohne die Implementierung ändern zu müssen. Sie können beispielsweise eine Metrik für *Neue Besucher* mit der Anzahl der Personen erstellen, für die dies die erste Sitzung ist.

* [Metriken freigeben](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md) über Report Suites hinweg. Das bedeutet, dass alle neu erstellten Metriken für alle Report Suites in demselben Anmeldeunternehmen gelten.

* [Integrieren Sie statistische Funktionen](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) um Ihre Daten besser zu beschreiben. Sie könnten beispielsweise die Elemente in einem Bericht zählen oder die Anzahl der Standardabweichungen für jedes Element addieren.

## Einschränkungen

Einige [!DNL Analytics] Funktionen erlauben keine Verwendung von berechneten Metriken:

* [!UICONTROL Fallout] in [!UICONTROL Analysis Workspace]
* [!UICONTROL Kohortenanalyse] in Analysis Workspace
* [!UICONTROL Data Warehouse]
* [!UICONTROL Segmente]
* [!DNL Analytics] für [!DNL Target]


>[!BEGINSHADEBOX]

Unter ![Videosymbol](/help/assets/icons/VideoCheckedOut.svg) [Berechnete Metriken](https://video.tv.adobe.com/v/37931?quality=12&learn=on&captions=ger){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Unter ![Videosymbol](/help/assets/icons/VideoCheckedOut.svg) [Segmentierte berechnete Metriken in Segmenten](https://video.tv.adobe.com/v/37930?quality=12&learn=on&captions=ger){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

<!--

Here is a short overview of the [!UICONTROL Calculated metrics] tools: 

|Tool|Capabilities|
|--- |--- |
| [Calculated metric builder](c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)| The capabilities are: <ul><li>Create calculated and advanced calculated metrics using advancmd allocation models.</li><li>Add segments inline to metric formulas</li><li>Compare segments in the same report. For example, compare local visitors vs. international visitors.</li><li>Use statistical functions</li><li>Provide detailed metric descriptions (show what it does, where to use it, where NOT to use it)</li><li>Copy definitions into new metrics</li><li>Provide an inline metric preview</li><li>Set metric polarity, which indicates whether it's good or bad if a given custom event (metric) goes up</li><li>Tag metrics</li></ul>|
|Calculated Metric Manager|<ul><li>Share metrics with others</li<li>Approve and curate metrics</li><li>Organize (tag) your metrics so people can find them</li><li>Delete metrics</li><li>Rename metrics</li></ul>|
|Metric Selector rail|Lets you search for and add/apply metrics to the report. You can also change the  sort order (options are: alphabetical, recommended, frequently used, recently used.) In addition, you can filter on Report Suites to show only metrics created in a specific report suite.  To access this Metric Selector, click the Metrics icon  to the left of a report. |
|API for Calculated Metrics|Part of the Adobe Analytics 2.0 API set.|

-->

>[!MORELIKETHIS]
>
>[Metriken erstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-workflow.md)
>&#x200B;>[Metriken erstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)
>&#x200B;>[Verwenden Sie Funktionen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-using-functions.md)
>
