---
description: Berechnete und erweiterte berechnete Metriken sind benutzerdefinierte Metriken, die Sie über vorhandene Metriken erstellen können.
keywords: Berechnete Metriken;erweiterte berechnete Metriken
title: Berechnete und erweiterte berechnete Metriken
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: ht
source-wordcount: '552'
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

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Berechnete Metriken](https://video.tv.adobe.com/v/25407?quality=12&learn=on){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

* Metriken über Report Suites hinweg freigeben. Das bedeutet, dass alle neu erstellten Metriken für alle Report Suites in demselben Anmeldeunternehmen gelten.
* (Nur erweiterte berechnete Metriken) Segmentieren Sie Metriken. Sie können beispielsweise eine Metrik für „Neue Besuchende“ erstellen, mit der die Personen gezählt werden, für die dies die erste Sitzung ist.

* (Nur erweiterte berechnete Metriken) Beziehen Sie statistische Funktionen mit ein, um Daten besser beschreiben zu können. Sie könnten beispielsweise die Elemente in einem Bericht zählen oder die Anzahl der Standardabweichungen für jedes Element addieren.


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Segmentierte berechnete Metriken in Segmenten](https://video.tv.adobe.com/v/25409?quality=12&learn=on){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


## Einschränkungen {#section_CB878B02451541D68A68B508D4DBD19A}

Bei einigen [!DNL Analytics]-Funktionen können Sie Ereignisse, aber keine berechneten Metriken verwenden:

* [!UICONTROL Fallout] in [!UICONTROL Analysis Workspace]
* [!UICONTROL Kohortenanalyse] in Analysis Workspace
* [!UICONTROL Data Warehouse]
* [!UICONTROL Segmente]
* [!DNL Analytics] für [!DNL Target]

## Tools {#section_D65E9C067E9C45E1A50DD30F50561BB2}

Im Folgenden erhalten Sie einen kurzen Überblick über die Tools für [!UICONTROL berechnete Metriken]:

| Tool | Funktionen |
|--- |--- |
| Generator für berechnete Metriken | <ul><li>Erstellen Sie einfache berechnete Metriken oder erweiterte berechnete Metriken mit erweiterten Zuordnungsmodellen.</li><li>Segmente inline zu Metrikformeln hinzufügen</li><li>Segmente in einem Bericht vergleichen (beispielsweise lokale Besucher mit internationalen Besuchern vergleichen.)</li><li>Statistische Funktionen verwenden</li><li>Detaillierte Metrikbeschreibungen angeben (was die Metrik macht, wo sie verwendet werden sollte, wo sie NICHT verwendet werden sollte)</li><li>Definitionen in neue Metriken kopieren</li><li>Eine Inline-Metrikvorschau bereitstellen</li><li>Die Metrikpolarität festlegen, die angibt, ob es gut oder schlecht ist, wenn ein bestimmtes benutzerspezifisches Ereignis (eine Metrik) steigt</li><li>Metriken taggen</li></ul> |
| Manager für berechnete Metriken | <ul><li>Metriken für andere freigeben<li>Metriken genehmigen und kuratieren</li><li>Metriken organisieren (taggen), damit sie von Personen gefunden werden können</li><li>Metriken löschen</li><li>Metriken umbenennen</li></ul> |
| Leiste „Metrikauswahl“ | Mit dieser Funktion können Sie Metriken suchen und diese dem Bericht hinzufügen bzw. darauf anwenden. Sie können auch die Sortierreihenfolge ändern (Optionen sind: „Alphabetisch“, „Empfohlen“, „Häufig verwendet“, „Zuletzt verwendet“). Darüber hinaus können Sie nach Report Suites filtern, um nur Metriken anzuzeigen, die in einer bestimmten Report Suite erstellt wurden.  Um auf diese Metrikauswahl zuzugreifen, klicken Sie auf das Metriksymbol auf der linken Seite eines Berichts.  |
| API für berechnete Metriken | Teil des Adobe Analytics 2.0-API-Sets. |
