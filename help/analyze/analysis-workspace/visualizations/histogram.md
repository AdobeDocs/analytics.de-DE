---
description: Erfahren Sie, wie Sie ein Histogramm verwenden, das einem Balkendiagramm ähnelt, aber Zahlen in Bereichen (Buckets) gruppiert.
title: Histogramm
uuid: 8a6bd2c4-da15-4f64-b889-ab9add685046
feature: Visualizations
role: User, Admin
exl-id: f3dd7507-db2c-495c-b6b9-6c770c7c7ddc
source-git-commit: 035723a8a1dcdee96c9be9a2ee7a0b2e98a8f56e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 66%

---

# Histogramm {#histogram}

>[!CONTEXTUALHELP]
>id="workspace_histogram_button"
>title="Histogramm"
>abstract="Erstellen Sie eine Histogrammvisualisierung, um die Verteilung numerischer Daten in Bereichsgruppen darzustellen."


>[!BEGINSHADEBOX]

_In diesem Artikel wird die Histogrammvisualisierung in_![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_Siehe [Histogramm](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/visualizations/histogram) für die ![_ CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics** Version dieses Artikels._

>[!ENDSHADEBOX]


Die Visualisierung ![Histogram](/help/assets/icons/Histogram.svg) **[!UICONTROL Histogramm]** ähnelt einer Visualisierung [!UICONTROL Balken], fasst jedoch Zahlen zu Bereichen (Buckets) zusammen. Analytics automatisiert diese Zusammenfassung von Zahlen zu Bereichen, wobei Sie jedoch die Einstellungen unter [Erweiterte Einstellungen](#advanced-settings) ändern können.

## Verwenden

So erstellen Sie ein Histogramm:

1. Fügen Sie eine Visualisierung ![Histogram](/help/assets/icons/Histogram.svg) **[!UICONTROL Histogramm]** hinzu. Siehe [Hinzufügen einer Visualisierung zu einem Panel](freeform-analysis-visualizations.md#add-visualizations-to-a-panel).
1. Ziehen Sie eine Metrik aus **[!UICONTROL Komponentenliste]** Metriken“ oder wählen Sie eine Metrik aus dem [!UICONTROL *Metrik hinzufügen*] Dropdown-Menü aus.
1. (Optional) Wählen Sie **[!UICONTROL Erweiterte Einstellungen einblenden]** aus. Weitere Informationen finden Sie unter [Erweiterte Einstellungen](#advanced-settings).
1. Wählen Sie **[!UICONTROL Erstellen]** aus.

>[!NOTE]
>
>Histogramme unterstützen nur Standardmetriken, keine berechneten Metriken.

Im folgenden Beispiel wird ein Histogramm für das Bucketing von Sitzungen für die Anzahl der Personen verwendet. Das Histogramm zeigt, dass für die meisten Personen für den ausgewählten Datumsbereich zwischen 16 und 21 Sitzungen vorliegen.

![](assets/histogram.png)

## Erweiterte Einstellungen

Im Rahmen der Visualisierung sind bestimmte Histogrammeinstellungen verfügbar.

| Histogrammeinstellungen | Beschreibung |
|---|---|
| **[!UICONTROL Anfangs-Bucket]** | Bestimmt, mit welchem Bucket das Histogramm beginnt. „1“ ist der Standardwert. Sie können Anfangszahlen von 0 bis unendlich festlegen (keine negativen Zahlen). |
| **[!UICONTROL Metrik-Buckets]** | Ermöglicht das Erhöhen/Verringern der Anzahl der Datenbereiche (Buckets). Maximal 50 Buckets sind möglich. |
| **[!UICONTROL Metrik-Bucket-Größe]** | Hier können Sie die Größe der einzelnen Behälter festlegen. Sie können beispielsweise die Größe des Buckets von einer Seitenansicht in zwei Seitenansichten ändern. |
| **[!UICONTROL Zählmethode]** | Treffen Sie eine Auswahl aus **[!UICONTROL Person]**, **[!UICONTROL Sitzung]** oder **[!UICONTROL Ereignis]**, z. B. Seitenansichten pro Sitzung, Seitenansichten pro Person oder Seitenansichten pro Ereignis. |

<!--Russ or Meike - Check Hit Type link above. -->

**Beispiele**:

| Anfangs-Bucket | Metrik-Buckets | Metrik-Bucket-Größe | Ergebnis |
|:----:|:--:|:--:|:--|
| 1 | 5 | 2 | ![Histogramm, Anfangs-Bucket 1, Metrik-Buckets 5, Metrik-Bucket-Größe 2](assets/histogram-1-5-2.png) |
| 0 | 3 | 5 | ![Histogramm, Anfangs-Bucket 0, Metrik-Buckets 3, Metrik-Bucket-Größe 5](assets/histogram-0-3-5.png) |

>[!MORELIKETHIS]
>
>[Hinzufügen einer Visualisierung zu einem Bedienfeld](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>[Einstellungen der Visualisierung](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>[Kontextmenü der Visualisierung](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>[Verwenden von Histogrammen zur Identifizierung unerwarteter Datenwerte](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/using-histograms-to-identify-unexpected-data-values/ba-p/596168)

