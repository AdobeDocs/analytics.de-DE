---
description: Ein Histogramm ist ein neuer Visualisierungstyp in Analysis Workspace.
title: Histogramm
uuid: 8a6bd2c4-da15-4f64-b889-ab9add685046
feature: Visualizations
role: User, Admin
exl-id: f3dd7507-db2c-495c-b6b9-6c770c7c7ddc
source-git-commit: fe1d4a87157a125f6065a6d827e4266d4ddefd4e
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 90%

---

# Histogramm {#histogram}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_histogram_button"
>title="Histogramm"
>abstract="Erstellen Sie eine Histogrammvisualisierung, um die Verteilung numerischer Daten in Bereichsgruppen darzustellen."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_In diesem Artikel wird die Histogrammvisualisierung in {_}![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_Siehe [Histogramm](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/histogram) für die_![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**-Version dieses Artikels._

>[!ENDSHADEBOX]


Ein Histogramm ähnelt einem Balkendiagramm, fasst jedoch Zahlen zu Bereichen (Behältern) zusammen. Analytics automatisiert diese Zusammenfassung von Zahlen zu Bereichen, wobei Sie jedoch die Einstellungen unter [Erweiterte Einstellungen](#section_09D774C584864D4CA6B5672DC2927477) ändern können.

Im Folgenden finden Sie ein Video zur Verwendung von Histogrammen:

>[!VIDEO](https://video.tv.adobe.com/v/23725/?quality=12)

## Erstellen eines Histogramms {#section_74647707CC984A1CB6D3097F43A30B45}

So erstellen Sie ein Histogramm:

1. Klicken Sie in der linken Leiste auf **[!UICONTROL Visualisierungen]**.
1. Ziehen Sie **[!UICONTROL Histogramm]** in das Bedienfeld.
1. Wählen Sie eine Metrik zum Ziehen der Visualisierung „Histogramm“ aus und klicken Sie dann auf **[!UICONTROL Erstellen]**.

![](assets/histogram.png)

>[!NOTE]
>
>Histogramme unterstützen nur Standardmetriken, keine berechneten Metriken.

Hier haben wir die Metrik „Seitenansichten pro Unique Visitors“ verwendet. Das erste Paket (links) bezieht sich auf 1 Seitenansicht pro Unique Visitor, das zweite auf 2 Seitenansichten usw.

![](assets/histogram2.png)

## Erweiterte Einstellungen {#section_09D774C584864D4CA6B5672DC2927477}

Wenn Sie die Einstellungen für Ihr Histogramm ändern möchten, klicken Sie auf das Einstellungssymbol (Zahnrad) in der Ecke oben rechts. Die folgenden Einstellungen können Sie ändern:

| Histogramm-Einstellungen | Dient dem folgenden Zweck |
|---|---|
| Startpaket | Bestimmt, mit welchem Paket das Histogramm beginnt. Die Standardeinstellung lautet 1. Sie können Startwerte von null bis unendlich festlegen, jedoch keine negativen Zahlen. |
| Metrische Behälter | Ermöglicht das Erhöhen/Verringern der Anzahl der Datenbereiche (Buckets). Die maximale Anzahl von Buckets ist 50. |
| Metrische Behältergröße | Hiermit können Sie die Größe der einzelnen Behälter festlegen. So könnten Sie zum Beispiel die Behältergröße von 1 Seitenansicht zu 2 Seitenansichten ändern. |
| Zählmethode | Sie können [Besucher](/help/components/metrics/unique-visitors.md), [Besuch](/help/components/metrics/visits.md) oder [Treffertyp](/help/components/dimensions/hit-type.md) auswählen, z. B. Seitenansichten pro Besuch, Seitenansichten pro Besucher oder Seitenansichten pro Hit. Für Hits wird „Vorkommen“ in der Freiformtabelle als Metrik der Y-Achse verwendet. |

<!--Russ or Meike - Check Hit Type link above. -->

**Beispiele**:

* Startpaket: 1; Metrische Behälter: 5; Metrische Behältergröße: 2 – Diese Werte würden zu dem folgenden Histogramm führen: 1-2, 3-4, 5-6, 7-8, 9-10.
* Startpaket: 0; Metrische Behälter: 3; Metrische Behältergröße: 5 – Diese Werte würden zu dem folgenden Histogramm führen: 0-4, 5-9, 10-14.

## Anzeigen und Bearbeiten von Histogrammdaten {#section_B2CD7CDF0F6B432F928103AE7AAA3617}

Wenn Sie die Datenquelle für das Histogramm anzeigen oder ändern möchten, klicken Sie auf den Punkt neben der Histogramm-Überschrift und navigieren Sie zu **[!UICONTROL Datenquelleneinstellungen]** > **[!UICONTROL Datenquelle anzeigen]**.

![](assets/manage-data-source.png)

Vorab erstellte Segmente, die in der Tabelle angezeigt werden, sind interne Segmente und werden in der Segmentauswahl nicht angezeigt. Klicken Sie auf das Symbol „i“ neben dem Segmentnamen und klicken Sie dann auf **[!UICONTROL Veröffentlichen]**, um das Segment öffentlich zu machen.

![](assets/prebuilt_segments.png)

Weitere Möglichkeiten zum Verwalten von Freiform-Datentabellen und anderen Visualisierungen (wie zum Beispiel Datenaufschlüsselungen) finden Sie [hier](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=de).
