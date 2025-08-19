---
description: Erfahren Sie, wie Sie mit dem Bedienfeld „Analytics for Target“ Ihre Adobe Target-Aktivitäten und -Erlebnisse in Analysis Workspace analysieren können.
title: Bedienfeld „Analytics for Target“
feature: Panels
role: User, Admin
exl-id: 36bca104-37b8-43c6-b8d0-b607a9a333cc
source-git-commit: 978bd8642011dd2c8e43564c90303f194689a64e
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 97%

---

# Analytics for Target-Bedienfeld {#analyze-for-target-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_a4t_button"
>title="Analytics for Target"
>abstract="Analysieren Sie Target-Aktivitäten und Erlebnisse in Analysis Workspace."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_a4t_panel"
>title="Analytics for Target-Bedienfeld"
>abstract="Analysieren Sie Target-Aktivitäten und Erlebnisse in Analysis Workspace.<br/><br>**Parameter **<br/>**Target-Aktivität**: Die Target-Aktivität, die analysiert wird.<br/>**Kontrollerlebnis**: Das Kontrollerlebnis für die ausgewählte Target-Aktivität.<br/>**Normalisierungsmetrik**: Besuchende, Besuche oder Impressions. Diese Metrik (auch als Zählmethodik bezeichnet) wird zum Nenner der Steigerungsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird.<br/>**Erfolgsmetrik**: Bis zu 3 standardmäßige (nicht berechnete) Erfolgsmetriken zur Analyse der Target-Aktivität."

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

_In diesem Artikel wird das Bedienfeld „Analytics for Target“ in_ ![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics** beschrieben._<br/>_Unter [Experimentier-Bedienfeld](https://experienceleague.adobe.com/de/docs/analytics/analyze/analysis-workspace/panels/a4t-panel) finden Sie weitere Informationen dazu, wie verschiedene Varianten von Anwendererlebnissen, Marketing oder Messaging in_ ![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics** miteinander verglichen werden können._

>[!ENDSHADEBOX]

Im Bedienfeld „Analytics for Target“ können Sie Ihre Adobe Target-Aktivitäten und -Erlebnisse in Analysis Workspace analysieren. Das Bedienfeld ermöglicht Ihnen außerdem, Steigerung und Konfidenz für bis zu drei Erfolgsmetriken zu sehen. Um auf das Bedienfeld „Analytics for Target“ zuzugreifen, navigieren Sie zu einer Report Suite, während Komponenten von Analytics for Target aktiviert sind. Wählen Sie dann das Bedienfeldsymbol ganz links und ziehen Sie das Bedienfeld „Analytics for Target“ in das Analysis Workspace-Projekt.


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Bedienfeld „Analytics for Target“](https://video.tv.adobe.com/v/37247?quality=12&learn=on){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]

## Verwenden

So verwenden Sie das Bedienfeld **[!UICONTROL Analytics for Target]**:

1. Erstellen Sie das Bedienfeld **[!UICONTROL Analytics for Target]**. Informationen zum Erstellen eines Bedienfelds finden Sie unter [Erstellen eines Bedienfelds](panels.md#create-a-panel).

1. Legen Sie die [Eingabe](#panel-input) für das Bedienfeld fest.

1. Sehen Sie sich die [Ausgabe](#panel-output) für das Bedienfeld an.

### Panel-Eingabe {#panel-nput}

Sie können das Bedienfeld „Analytics for Target“ mithilfe der folgenden Eingabeeinstellungen konfigurieren:

![A4T-Bedienfeld-Eingabe](assets/a4t-panel-input.png)

| Einstellung | Beschreibung |
|---|---|
| **[!UICONTROL Target-Aktivität]** | Treffen Sie Ihre Auswahl aus einer Liste mit Zielaktivitäten. Die Liste wird mit den Aktivitäten der letzten sechs Monate gefüllt, die mindestens einen Treffer hatten. Wenn Sie eine Aktivität nicht in der Liste sehen, ist sie möglicherweise älter als 6 Monate. Sie kann immer noch von der linken Leiste hinzugefügt werden, die einen Lookback-Zeitraum von bis zu 18 Monaten hat. |
| **[!UICONTROL Kontrollerlebnis]** | Wählen Sie das Kontrollerlebnis aus. |
| **[!UICONTROL Normalisierungsmetrik]** | Wählen Sie Besuchende, Besuche oder Impressionen aus. Für die meisten Anwendungsfälle der Analyse wird [!UICONTROL Besucher] empfohlen. Diese Metrik (auch als Zählmethodik bezeichnet) wird zum Nenner der Steigerungsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird. |
| **[!UICONTROL Erfolgsmetriken]** | Wählen Sie bis zu drei standardmäßige (nicht berechnete) Erfolgsereignisse aus dem Dropdown-Menü aus oder ziehen Sie Metriken per Drag-and-Drop aus „Metriken“ der Leiste „Komponenten“. Jede Metrik verfügt über eine eigene Tabelle und Visualisierung im gerenderten Bedienfeld. |

Wählen Sie **[!UICONTROL Erstellen]** aus, um das Bedienfeld zu erstellen.

### Bedienfeldausgabe {#panel-output}

Das Bedienfeld „Analytics for Target“ enthält umfangreiche Daten und Visualisierungen, die Ihnen helfen, die Leistung Ihrer Adobe Target-Aktivität und -Erlebnisse besser zu verstehen. Oben im Bedienfeld wird eine Zusammenfassungszeile angezeigt, die Sie an die ausgewählten Bedienfeldeinstellungen erinnert. Für jede ausgewählte Erfolgsmetrik wird eine [Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) und eine [Linienvisualisierung](/help/analyze/analysis-workspace/visualizations/line.md) mit dem Konversionsraten-Trend anzeigt:

![Gerendert](assets/a4t-panel-output.png)

Für jede Freiformtabelle werden die folgenden Metrikspalten angezeigt:

| Metrik | Beschreibung |
|---|---|
| **[!UICONTROL Normalisierungsmetriken]** | Die im Eingabebedienfeld ausgewählte Normalisierungsmetrik: Unique Visitors, Besuche oder Aktivitätsimpressionen. |
| **[!UICONTROL Erfolgsmetrik]** | Die im Eingabebedienfeld ausgewählte Erfolgsmetrik. |
| **[!UICONTROL Konversionsrate]** | Die Erfolgsmetrik/Normalisierungsmetrik. |
| **[!UICONTROL Steigerung]** | Vergleicht für jedes Erlebnis die Konversionsrate mit dem Kontrollerlebnis. Hinweis: Steigerung ist eine *gesperrte Metrik* für „Target-Erlebnisse“. Sie kann nicht aufgeschlüsselt oder mit anderen Dimensionen verwendet werden. |
| **[!UICONTROL Steigerung (Mindestwert)]** | Dieser Wert stellt die schlechteste Steigerung dar, die ein Variantenerlebnis bei einem Konfidenzintervall von 95 % im Vergleich zum Kontrollerlebnis aufweisen könnte.<br>Weitere Informationen finden Sie in den Excel-Dateien [Statistical calculations](https://experienceleague.adobe.com/de/docs/target/using/reports/statistical-methodology/statistical-calculations) und [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx). |
| **[!UICONTROL Steigerung (mittlerer Wert)]** | Dieser Wert stellt die mittlere Steigerung dar, die ein Variantenerlebnis bei einem Konfidenzintervall von 95 % im Vergleich zum Kontrollerlebnis aufweisen könnte. <br>Weitere Informationen finden Sie in den Excel-Dateien [Statistical calculations](https://experienceleague.adobe.com/de/docs/target/using/reports/statistical-methodology/statistical-calculations) und [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx). |
| **[!UICONTROL Steigerung (Maximalwert)]** | Dieser Wert stellt die beste Steigerung dar, die ein Variantenerlebnis bei einem Konfidenzintervall von 95 % im Vergleich zum Kontrollerlebnis aufweisen könnte.<br>Weitere Informationen finden Sie in den Excel-Dateien [Statistical calculations](https://experienceleague.adobe.com/de/docs/target/using/reports/statistical-methodology/statistical-calculations) und [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx). |
| **[!UICONTROL Konfidenz]** | Die Student-t-Verteilung berechnet das Konfidenzniveau, das die Wahrscheinlichkeit angibt, mit der ein Test bei seiner Wiederholung dieselben Ergebnisse liefert. Ein fester bedingter Formatierungsbereich von 75 %/85 %/95 % wurde auf die Metrik angewandt. Diese Formatierung kann bei Bedarf unter „Spalteneinstellungen“ angepasst werden. Hinweis: Konfidenz ist eine „gesperrte Metrik“ für Target-Erlebnisse. Sie kann nicht mit anderen Dimensionen aufgeschlüsselt oder verwendet werden.<br>Weitere Informationen finden Sie in den Excel-Dateien [Statistical calculations](https://experienceleague.adobe.com/de/docs/target/using/reports/statistical-methodology/statistical-calculations) und [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx). |

Wie bei allen Bedienfeldern in Analysis Workspace können Sie Ihre Analyse fortsetzen, indem Sie zusätzliche Tabellen und [Visualisierungen](https://experienceleague.adobe.com/de/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations) hinzufügen, die Ihnen bei der Analyse Ihrer Adobe Target-Aktivitäten helfen. Sie können ein Segment auch entweder auf Panel-Ebene oder innerhalb der Freiformtabelle anwenden. Beachten Sie, dass Sie beim Hinzufügen in der Freiformtabelle eine Überlagerung über die gesamte Tabelle durchführen müssen, um die Steigerungs- und Konfidenzberechnungen beizubehalten. Segmente auf Spaltenebene werden derzeit nicht unterstützt.

Verwenden Sie ![Bearbeiten](/help/assets/icons/Edit.svg), um das Bedienfeld neu zu konfigurieren und neu zu erstellen.

## Häufig gestellte Fragen (FAQ) {#FAQ}

| Frage | Antwort |
|---|---|
| Welche Aktivitätstypen werden in Analytics for Target unterstützt? | [Erfahren Sie mehr](https://experienceleague.adobe.com/de/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-activity-setup) darüber, welche Aktivitäten unterstützt werden. |
| Werden berechnete Metriken bei Steigerungs- und Konfidenzberechnungen unterstützt? | Nein. [Erfahren Sie mehr](https://experienceleague.adobe.com/de/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence) darüber, warum berechnete Metriken bei Steigerung und Konfidenz nicht unterstützt werden. Berechnete Metriken können jedoch außerhalb dieser Metriken in Analytics for Target-Berichten verwendet werden. |
| Warum unterscheiden sich Unique Visitors zwischen Target und Analytics? | [Erfahren Sie mehr](https://experienceleague.adobe.com/de/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports) über die Unterschiede zwischen Unique Visitors in den Produkten. |
| Warum werden nicht verwendete Erlebnisse zurückgegeben, wenn ich in meiner Analyse ein Hit-Segment für eine bestimmte Target-Aktivität anwende? | Die Analytics for Target-Dimension ist eine Listenvariable, d. h., sie kann mehrere Aktivitäten (und Erlebnisse) gleichzeitig enthalten. [Weitere Infos](https://experienceleague.adobe.com/de/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports) |
| Berücksichtigt die Konfidenzmetrik extreme Bestellungen oder wendet sie eine Bonferroni-Korrektur für mehrere Bestellungen an? | Nein. [Erfahren Sie mehr](https://experienceleague.adobe.com/de/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence) darüber, wie Analytics Konfidenz berechnet. |
| Können Steigerungs- und Konfidenzmetriken mit anderen Dimensionen oder Aufschlüsselungen verwendet werden? | Steigerung und Konfidenz sind „gesperrte Metriken“ für die Dimension „Target-Erlebnisse“, da sie ein Kontrollerlebnis und ein Variantenerlebnis für die Berechnung erfordern. Sie können daher nicht aufgeschlüsselt oder mit anderen Dimensionen verwendet werden. |
| Wann werden Steigerung und Konfidenz neu berechnet? | Steigerung und Konfidenz werden bei jeder Erstellung des Bedienfelds, bei einer Änderung des Datumsbereichs des Bedienfelds oder bei Anwendung eines Segments auf das Bedienfeld oder die Tabelle neu berechnet. Wenn Sie einen Segmentfilter auf die Freiformtabelle anwenden, muss das Segment über alle Spalten hinweg angewendet werden. Andernfalls wird die Steigerung oder Konfidenz nicht korrekt aktualisiert. Segmente auf Spaltenebene werden nicht unterstützt. |

Weitere Informationen zu Analytics for Target-Berichten finden Sie unter [Analytics for Target-Berichte](https://experienceleague.adobe.com/de/docs/target/using/integrate/a4t/reporting).
