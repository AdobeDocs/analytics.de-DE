---
description: Berechnete und erweiterte berechnete Metriken sind benutzerdefinierte Metriken, die Sie über vorhandene Metriken erstellen können.
keywords: Berechnete Metriken;erweiterte berechnete Metriken
title: Berechnete und erweiterte berechnete Metriken
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 9714863374052e257e1d6349c442fc74182a0a2f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 100%

---

# Berechnete und erweiterte berechnete Metriken

Berechnete und erweiterte berechnete Metriken sind benutzerdefinierte Metriken, die Sie über vorhandene Metriken erstellen können. 

Mit unseren Tools für berechnete Metriken können Sie Metriken auf flexiblere Weise erstellen, verwalten und kuratieren. Damit können Marketingexperten, Produktmanager und Analytiker Fragen zu den Daten beantworten, ohne die [!DNL Analytics]-Implementierung ändern zu müssen. Dies sind die benutzerdefinierten Metriken, die in den einzelnen [!DNL Analytics]-Paketen verfügbar sind:

* Adobe [!DNL Analytics] Foundation: Berechnet
* [Adobe Analytics Select](https://www.adobe.com/de/data-analytics-cloud/analytics/select.html): Berechnet + erweitert berechnet
* [Adobe Analytics Prime](https://www.adobe.com/de/data-analytics-cloud/analytics/prime.html): Berechnet + erweitert berechnet
* [Adobe Analytics Ultimate](https://www.adobe.com/de/data-analytics-cloud/analytics/ultimate.html): Berechnet + erweitert berechnet

Hier sehen Sie einen Vergleich zwischen den jeweiligen Möglichkeiten, die berechnete und erweiterte berechnete Metriken bieten:

| Builder-Optionen | Berechnete Metriken | Erweiterte berechnete Metriken |
|---|---|---|
| [Formatarten (Dezimal, Zeit, Prozent, Währung)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) | Ja | Ja |
| [Attributionsänderung (Standard, Linear, Teilnahme etc.)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| [Metriktypen (Standard, Total)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | Ja | Ja |
| Grundrechenarten (Addieren, Subtrahieren, Multiplizieren, Dividieren) | Ja | Ja |
| [Segmente anwenden](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) | Nein | Ja |
| [Allgemeine Funktionen (Zählen, Anzeigenwert, Mittel etc.)](/help/components/c-calcmetrics/cm-reference/cm-functions.md) | Nein | Ja |
| [Erweiterte Funktionen (Regression, Wenn-Dann, T-Transformation etc.)](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) | Nein | Ja |

## Funktionen {#section_A0A5C275B68A4D628950BBB0B1EE631F}

Sie können

* Metriken für [!UICONTROL Analysis Workspace], [!UICONTROL Report Builder], [!UICONTROL Anomalieerkennung] und [!UICONTROL Beitragsanalyse] erstellen.
* Erstellen Sie segmentierte Metriken, die zur Berichtslaufzeit abgeleitet werden, ohne die Implementierung ändern zu müssen. Diese Metriken können historisch angezeigt werden, da sie auf Segmenten basieren.

>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Berechnete Metriken](https://video.tv.adobe.com/v/37931?quality=12&learn=on&captions=ger){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

* Metriken über Report Suites hinweg freigeben. Das bedeutet, dass alle neu erstellten Metriken für alle Report Suites in demselben Anmeldeunternehmen gelten.
* (Nur erweiterte berechnete Metriken) Segmentieren Sie Metriken. Sie können beispielsweise eine Metrik für „Neue Besuchende“ erstellen, mit der die Personen gezählt werden, für die dies die erste Sitzung ist.

* (Nur erweiterte berechnete Metriken) Beziehen Sie statistische Funktionen mit ein, um Daten besser beschreiben zu können. Sie könnten beispielsweise die Elemente in einem Bericht zählen oder die Anzahl der Standardabweichungen für jedes Element addieren.


## Einschränkungen

Bei einigen [!DNL Analytics]-Funktionen können Sie Ereignisse, aber keine berechneten Metriken verwenden:

* [!UICONTROL Fallout] in [!UICONTROL Analysis Workspace]
* [!UICONTROL Kohortenanalyse] in Analysis Workspace
* [!UICONTROL Data Warehouse]
* [!UICONTROL Segmente]
* [!DNL Analytics] für [!DNL Target]


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Berechnete Metriken](https://video.tv.adobe.com/v/37931?quality=12&learn=on&captions=ger){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Segmentierte berechnete Metriken in Segmenten](https://video.tv.adobe.com/v/37930?quality=12&learn=on&captions=ger){target="_blank"} finden Sie ein Demovideo.

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