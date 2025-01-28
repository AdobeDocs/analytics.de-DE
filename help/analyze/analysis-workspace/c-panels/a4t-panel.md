---
description: Im Bedienfeld „Analytics for Target“ können Sie Ihre Adobe Target-Aktivitäten und -Erlebnisse in Analysis Workspace analysieren.
title: Bedienfeld „Analytics for Target“ (A4T)
feature: Panels
role: User, Admin
exl-id: 36bca104-37b8-43c6-b8d0-b607a9a333cc
source-git-commit: 2aaa8c0d13755b40ec701ca6342ab773103a0422
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 46%

---

# Analytics for Target-Bedienfeld {#analyze-for-target-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_a4t_button"
>title="Analytics for Target"
>abstract="Target-Aktivitäten und Erlebnisse in Analysis Workspace analysieren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_a4t_panel"
>title="Analytics for Target-Bedienfeld"
>abstract="Target-Aktivitäten und Erlebnisse in Analysis Workspace analysieren.<br/><br>**Parameter **<br/>**Target-Aktivität**: Die analysierte Target-Aktivität.<br/>**Kontrollerlebnis**: Das Kontrollerlebnis für die ausgewählte Target-Aktivität.<br/>**Normalisierungsmetrik**: Besuchende, Besuche oder Impressions. Diese Metrik (auch als Zählmethodik bezeichnet) wird zum Nenner der Steigerungsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird.<br/>**Erfolgsmetrik**: Bis zu 3 standardmäßige (nicht berechnete) Erfolgsmetriken zur Analyse der Target-Aktivität."

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

_In diesem Artikel wird das Bedienfeld „Analytics for Target“ in_![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_Siehe [Experimentier-](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/a4t-panel)) für Informationen zum Vergleichen verschiedener Benutzererlebnisse, Marketing- oder Messaging-Variationen in_![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**._

>[!ENDSHADEBOX]

Im Bedienfeld „Analytics for Target“ können Sie Ihre Adobe Target-Aktivitäten und -Erlebnisse in Analysis Workspace analysieren. Im Bedienfeld können Sie außerdem Steigerung und Konfidenz für bis zu drei Erfolgsmetriken anzeigen. Um auf das Bedienfeld „Analytics for Target“ zuzugreifen, navigieren Sie zu einer Report Suite mit aktivierten Analytics for Target-Komponenten. Wählen Sie dann ganz links das Bedienfeldsymbol aus und ziehen Sie das Bedienfeld „Analytics for Target“ in Ihr Analysis Workspace-Projekt.

+++Im Folgenden finden Sie eine kurze Videoübersicht zum Bedienfeld „Analytics for Target“:

>[!VIDEO](https://video.tv.adobe.com/v/37247/?quality=12)

+++

## Verwenden

So verwenden Sie ein Bedienfeld **[!UICONTROL Analytics for Target]**:

1. Erstellen Sie ein Bedienfeld **[!UICONTROL Analytics for Target]**. Informationen zum Erstellen eines Bedienfelds finden Sie unter [Erstellen eines Bedienfelds](panels.md#create-a-panel).

1. Legen Sie die [Eingabe](#panel-input) für das Bedienfeld fest.

1. Sehen Sie sich die [Ausgabe](#panel-output) für das Bedienfeld an.

### Bedienfeldeingabe {#panel-nput}

Sie können das Bedienfeld „Analytics for Target“ mithilfe der folgenden Eingabeeinstellungen konfigurieren:

![A4T-Bedienfeld-Eingabe](assets/a4t-panel-input.png)

| Einstellung | Beschreibung |
|---|---|
| **[!UICONTROL Target-Aktivität]** | Auswahl aus einer Liste der Zielaktivitäten. Die Liste enthält die letzten 6 Monate der Aktivitäten, die mindestens einen Treffer erzielt haben. Wenn Sie eine Aktivität nicht in der Liste sehen, ist sie möglicherweise älter als 6 Monate. Sie kann immer noch von der linken Leiste hinzugefügt werden, die einen Lookback-Zeitraum von bis zu 18 Monaten hat. |
| **[!UICONTROL Kontrollerlebnis]** | Wählen Sie das Kontrollerlebnis aus. |
| **[!UICONTROL Normalisierungsmetrik]** | Besucher, Besuche oder Impressionen auswählen. [!UICONTROL Besucher] wird für die meisten Anwendungsfälle für Analysen empfohlen. Diese Metrik (auch als Zählmethodik bezeichnet) wird zum Nenner der Steigerungsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird. |
| **[!UICONTROL Erfolgsmetriken]** | Wählen Sie bis zu 3 standardmäßige (nicht berechnete) Erfolgsereignisse aus dem Dropdown-Menü aus oder ziehen Sie Metriken per Drag-and-Drop aus Metriken in die Komponentenleiste. Jede Metrik verfügt über eine dedizierte Tabelle und Visualisierung im gerenderten Bereich. |

Wählen Sie **[!UICONTROL Erstellen]** aus, um das Bedienfeld zu erstellen.

### Bedienfeldausgabe {#panel-output}

Das Bedienfeld „Analytics for Target“ enthält umfangreiche Daten und Visualisierungen, die Ihnen helfen, die Leistung Ihrer Adobe Target-Aktivität und -Erlebnisse besser zu verstehen. Oben im Bedienfeld wird eine Zusammenfassungszeile angezeigt, die Sie an die ausgewählten Bedienfeldeinstellungen erinnert. Für jede ausgewählte Erfolgsmetrik wird eine [Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) und eine [Linien](/help/analyze/analysis-workspace/visualizations/line.md)-Visualisierung angezeigt, die den Konversionsratentrend anzeigt:

![Gerendert](assets/a4t-panel-output.png)

Für jede Freiformtabelle werden die folgenden Metrikspalten angezeigt:

| Metrik | Beschreibung |
|---|---|
| **[!UICONTROL Normalisieren von Metriken]** | Die im Eingabefeld ausgewählte Normalisierungsmetrik: Unique Visitors, Besuche oder Aktivitätsimpressionen. |
| **[!UICONTROL Erfolgsmetrik]** | Die im Eingabebereich ausgewählte Erfolgsmetrik. |
| **[!UICONTROL Konversionsrate]** | Die Erfolgsmetrik/Normalisierungsmetrik. |
| **[!UICONTROL Steigerung]** | Vergleicht für jedes Erlebnis die Konversionsrate mit dem Kontrollerlebnis. Hinweis: Die Steigerung ist *gesperrte Metrik* auf Zielerlebnisse; sie kann nicht aufgeschlüsselt oder mit anderen Dimensionen verwendet werden. |
| **[!UICONTROL Hub (unten)]** | Dieser Wert stellt die schlechteste Steigerung dar, die eine Variantenerfahrung im Vergleich zur Kontrollvariante bei einem Konfidenzintervall von 95 % aufweisen könnte.<br>Siehe [Statistische Berechnungen](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) und [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) Excel-Datei für weitere Informationen. |
| **[!UICONTROL Anstieg (Mitte)]** | Dieser Wert stellt den mittleren Aufstieg dar, den ein Variantenerlebnis im Vergleich zum Kontrollerlebnis bei einem Konfidenzintervall von 95 % aufweisen könnte. <br>Siehe [Statistische Berechnungen](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) und [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) Excel-Datei für weitere Informationen. |
| **[!UICONTROL Anstieg (oben)]** | Dieser Wert stellt den besten Anstieg dar, den ein Variantenerlebnis im Vergleich zur Kontrollvariante bei einem Konfidenzintervall von 95 % aufweisen könnte.<br>Siehe [Statistische Berechnungen](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) und [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) Excel-Datei für weitere Informationen. |
| **[!UICONTROL Konfidenz]** | Die Student-t-Verteilung berechnet das Konfidenzniveau, das die Wahrscheinlichkeit angibt, mit der ein Test bei seiner Wiederholung dieselben Ergebnisse liefert. Ein fester bedingter Formatierungsbereich von 75 %/85 %/95 % wurde auf die Metrik angewandt. Diese Formatierung kann bei Bedarf unter „Spalteneinstellungen“ angepasst werden. Hinweis: Konfidenz ist eine „gesperrte Metrik“ für Target-Erlebnisse. Sie kann nicht mit anderen Dimensionen aufgeschlüsselt oder verwendet werden.<br>Siehe [Statistische Berechnungen](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) und [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) Excel-Datei für weitere Informationen. |

Wie bei jedem Bedienfeld in Analysis Workspace können Sie Ihre Analyse fortsetzen, indem Sie zusätzliche Tabellen und [Visualisierungen](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations) hinzufügen, mit denen Sie Ihre Adobe Target-Aktivitäten analysieren können. Sie können ein Segment auch entweder auf Panel-Ebene oder innerhalb der Freiformtabelle anwenden. Beachten Sie, dass Sie beim Hinzufügen in der Freiformtabelle eine Überlagerung über die gesamte Tabelle durchführen müssen, um die Steigerungs- und Konfidenzberechnungen beizubehalten. Segmente auf Spaltenebene werden derzeit nicht unterstützt.

Verwenden Sie ![Bearbeiten](/help/assets/icons/Edit.svg), um das Bedienfeld neu zu konfigurieren und neu zu erstellen.

## Häufig gestellte Fragen (FAQ) {#FAQ}

| Frage | Antwort |
|---|---|
| Welche Aktivitätstypen werden in Analytics for Target unterstützt? | [Erfahren Sie mehr](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-activity-setup) darüber, welche Aktivitäten unterstützt werden. |
| Werden berechnete Metriken bei Steigerungs- und Konfidenzberechnungen unterstützt? | Nein. [Erfahren Sie mehr](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence) darüber, warum berechnete Metriken bei Steigerung und Konfidenz nicht unterstützt werden. Berechnete Metriken können jedoch auch außerhalb dieser Metriken in Analytics for Target-Berichten verwendet werden. |
| Warum unterscheiden sich Unique Visitors zwischen Target und Analytics? | [Erfahren Sie mehr](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports) über die Varianzen von Unique Visitors zwischen Produkten. |
| Warum werden nicht verwendete Erlebnisse zurückgegeben, wenn ich in meiner Analyse ein Hit-Segement für eine bestimmte Target-Aktivität anwende? | Die Analytics for Target-Dimension ist eine Listenvariable, d. h. sie kann viele Aktivitäten (und Erlebnisse) gleichzeitig enthalten. [Weitere Infos](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports) |
| Berücksichtigt die Konfidenzmetrik extreme Bestellungen oder wendet sie eine Bonferroni-Korrektur für mehrere Bestellungen an? | Nein. [Erfahren Sie mehr](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence) darüber, wie Analytics Konfidenz berechnet. |
| Können Steigerungs- und Konfidenzmetriken mit anderen Dimensionen oder Aufschlüsselungen verwendet werden? | Steigerung und Konfidenz sind „gesperrte Metriken“ für die Dimension „Target-Erlebnisse“, da sie ein Kontrollerlebnis und ein Variantenerlebnis für die Berechnung erfordern. Sie können daher nicht aufgeschlüsselt oder mit anderen Dimensionen verwendet werden. |
| Wann werden Steigerung und Konfidenz neu berechnet? | Steigerung und Konfidenz werden jedes Mal neu berechnet, wenn das Bedienfeld erstellt wird, sich der Datumsbereich des Bedienfelds ändert oder ein Segment auf das Bedienfeld oder die Tabelle angewendet wird. Wenn Sie einen Segmentfilter auf die Freiformtabelle anwenden, muss das Segment auf alle Spalten angewendet werden, da sonst die Steigerung und Konfidenz nicht korrekt aktualisiert werden. Segmente auf Spaltenebene werden nicht unterstützt. |

Weitere Informationen zum Reporting in Analytics for Target finden Sie unter [Berichterstellung in Analytics for Target](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/reporting)
