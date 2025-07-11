---
description: Erfahren Sie, wie Sie einen Datumsvergleich in Analysis Workspace verwenden, mit dem Sie eine beliebige Spalte mit einem Datumsbereich verwenden und einen allgemeinen Datumsvergleich erstellen können.
title: Datumsvergleich
feature: Date Ranges
role: User, Admin
exl-id: ea7a42ef-89de-4f70-b468-8a5cf69fea05
source-git-commit: 3d15bd941cb8eaf20b8ae9f1ffa1dbfd403b2bfa
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 35%

---

# Datumsvergleich

Mit dem Datumsvergleich in Analysis Workspace können Sie eine beliebige Spalte mit einem Datumsbereich verwenden und einen allgemeinen Datumsvergleich erstellen, z. B. Jahres-, Quartals- oder Monatsvergleich.

## Zeiträume vergleichen

Für Analysen wird Kontext benötigt, der oft durch einen vorherigen Zeitraum geliefert wird. Zum Beispiel die Frage *Wie viel besser oder schlechter geht es Ihnen jetzt im Vergleich zu dieser Zeit im letzten Jahr?* ist für das Verständnis Ihres Unternehmens von grundlegender Bedeutung. Der Datumsvergleich enthält automatisch *Spalte &quot;*&quot;, die die prozentuale Änderung im Vergleich zu einem bestimmten Zeitraum anzeigt.

1. Erstellen Sie [Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) mit allen Dimensionen und Metriken, die Sie über einen bestimmten Zeitraum vergleichen möchten.
1. Öffnen Sie das Kontextmenü für eine Tabellenzeile und wählen Sie **[!UICONTROL Zeiträume vergleichen]** aus.

   ![Tabellenzeile mit ausgewählten Zeiträumen vergleichen](assets/compare-time.png)

   >[!NOTE]
   >
   >Diese Kontextmenüoption ist für Metrik -Zeilen, Datumsbereichszeilen und Zeitdimensionszeilen deaktiviert.

1. Je nachdem, wie Sie den Datumsbereich der Tabelle festgelegt haben, stehen die folgenden Optionen zum Vergleich zur Verfügung:

   | Option | Beschreibung |
   |---|---|
   | **[!UICONTROL Vorherige *x* Wochen/Monate/Quartale/Jahre bis zu diesem Datumsbereich]** | Mit dem ausgewählten Datumsbereich unmittelbar vor diesem Datumsbereich vergleichen. |
   | **[!UICONTROL Diese x Wochen/Monate/Quartale/Jahre sind im letzten Jahr bis zu diesem Datumsbereich aufgetreten]** | Mit demselben Datumsbereich vor einem Jahr vergleichen. |
   | **[!UICONTROL Benutzerdefinierter Datumsbereich vor diesem Datumsbereich]** | Sie können einen benutzerdefinierten Datumsbereich definieren. |

   >[!NOTE]
   >
   >Wenn Sie eine benutzerdefinierte Anzahl an Tagen auswählen, z. B. 7.–20. Oktober (ein Zeitraum von 14 Tagen), stehen nur zwei Optionen zur Verfügung: **[!UICONTROL Vorhergehende 14 Tage vor diesem Datumsbereich]** und **[!UICONTROL Benutzerdefinierter Datumsbereich vor diesem Datumsbereich]**.

1. Der resultierende Vergleich sieht wie folgt aus:

   ![Freiformtabelle mit einem Vergleich der Datumsbereiche und der prozentualen Änderung.](assets/compare-time-result.png)

   Zeilen in der Spalte „Prozentuale Änderung“ werden für negative Werte rot und für positive Werte grün angezeigt.

## Eine Zeitraumspalte zum Vergleich hinzufügen

Sie können jeder Spalte in einer Tabelle jetzt einen Zeitraum hinzufügen, sodass Sie einen anderen Zeitraum hinzufügen können als den, für den Ihr Kalender festgelegt ist.

1. Klicken Sie mit der rechten Maustaste auf eine Spalte in der Tabelle und wählen Sie **[!UICONTROL Spalte für Zeitraum hinzufügen]** aus

   ![](assets/add-time-period-column.png)

1. Je nachdem, wie Sie den Datumsbereich der Tabelle festgelegt haben, stehen die folgenden Optionen zum Vergleich zur Verfügung:

   | Option | Beschreibung |
   |---|---|
   | **[!UICONTROL Vorherige *x* Wochen/Monate/Quartale/Jahre bis zu diesem Datumsbereich]** | Fügen Sie eine Spalte mit dem Wochentag/Monat usw. hinzu. unmittelbar vor diesem Datumsbereich. |
   | **[!UICONTROL Diese *x* Wochen/Monate/Quartale/Jahre letzten Jahres bis zu diesem Datumsbereich]** | Fügen Sie denselben Datumsbereich wie vor einem Jahr hinzu. |
   | **[!UICONTROL Benutzerdefinierter Datumsbereich vor diesem Datumsbereich]** | Sie können einen benutzerdefinierten Datumsbereich erstellen. |

   >[!NOTE]
   >
   >Wenn Sie eine benutzerdefinierte Anzahl an Tagen auswählen, z. B. 7.–20. Oktober (ein Zeitraum von 14 Tagen), stehen nur zwei Optionen zur Verfügung: **[!UICONTROL Vorhergehende 14 Tage vor diesem Datumsbereich]** und **[!UICONTROL Benutzerdefinierter Datumsbereich vor diesem Datumsbereich]**.

1. Der Zeitraum wird über der ausgewählten Spalte eingefügt:

   ![Freiformtabelle mit Vorkommnissen für den aktuellen Kalenderzeitraum und den vorherigen Kalendermonat.](assets/add-time-period-column2.png)

1. Sie können so viele Zeitspalten hinzufügen, wie Sie möchten, sowie verschiedene Datumsbereiche kombinieren:

1. Darüber hinaus können Sie nach jeder Spalte sortieren. Dadurch ändert sich die Reihenfolge der Tage in Abhängigkeit von der Spalte, nach der Sie sortieren.

## Beginn der Spaltendaten an derselben Zeile ausrichten

Sie können die Daten in den einzelnen Spalten so ausrichten, dass sie alle in derselben Zeile beginnen.

Sie führen beispielsweise einen Tagesvergleich für die letzte Woche (bis zum 5. Oktober 2024) und die vorherige Woche durch. Standardmäßig beginnt die linke Spalte am 22. September und die rechte Spalte am 29. September.

![Nicht abgestimmte Daten](assets/not-align-dates.png)

Sie können in **[!UICONTROL Einstellungen“ für die Freiformtabellen-Visualisierung die Option „Datum]** jeder Spalte so ausrichten[ dass alle Spalten in derselben Zeile beginnen, aktivieren](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md#settings-1) um Spaltendaten so auszurichten, dass sie in derselben Zeile beginnen.

![](assets/align-dates.png)

Beachten Sie beim Verwenden dieser Option Folgendes:

* Diese Einstellung ist standardmäßig für alle neuen Projekte aktiviert.

* Diese Einstellung gilt für die gesamte Tabelle. Wenn Sie diese Einstellung beispielsweise für eine Aufschlüsselung innerhalb der Tabelle ändern, wird die Einstellung auf die gesamte Tabelle angewendet.


<!--
# Date comparison

Date comparison in Analysis Workspace lets you take any column containing a date range and create a common date comparison, such as: year-over-year, quarter-over-quarter, month-over-month, etc.


>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Date comparison](https://video.tv.adobe.com/v/33712?quality=12&learn=on&captions=ger){target="_blank"} for a demo video.

>[!ENDSHADEBOX]



## Compare time periods {#section_C4E36BFE0F5C4378A74E705747C9DEE4}

>[!NOTE]
>[!UICONTROL Compare Time Periods] leverages advanced Calculated Metrics. As a result, it is available only to customers with Analytics Select, Prime, and Ultimate SKUs. 

Analysis requires context, and often that context is provided by a previous time period. For example, the question "How much better or worse are we doing than at this time last year?" is fundamental to understanding your business. Date Comparison automatically include a "difference" column, which shows the percentage change compared to a specified time period.

1. Create a Freeform table, with any dimensions and metrics you want to compare over a time period.
1. Right-click a table row and select **[!UICONTROL Compare time periods]**.

   ![](assets/compare-time.png)

   >[!NOTE]
   >
   >This right-click option is disabled for metric rows, date range rows, and time dimension rows.

1. Depending on how you have set the table's date range, you have these options for comparison: 

   |  Option  | Description  |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Compares to the week/month/etc. immediately before this date range.  |
   | **[!UICONTROL This week/month/quarter/year last year to this date range]** | Compares to the same date range a year ago.  |
   | **[!UICONTROL Custom date range to this date range]** | Lets you select a custom date range.  |

   >[!NOTE]
   >
   >When you select a custom number of days, for example October 7 - October 20 (a 14-day range), you will get only 2 options: **[!UICONTROL Prior 14 days before this date range]**, and **[!UICONTROL Custom date range to this date range]**.

1. The resulting comparison looks like this:

   ![](assets/compare-time-result.png)

   Rows in the Percent Change column appear red for negative values and green for positive values.

1. (Optional) As in any other Workspace projects, you can create visualizations based on these time comparisons. For example, here is a Bar graph:

   ![](assets/compare-time-barchart.png)

   Note that in order to show the percentage change in the bar chart, you have to have the [!UICONTROL Percentages] setting checked in the [!UICONTROL Visualization Settings].

## Add a time period column for comparison {#section_93CC2B4F48504125BEC104046A32EB93}

You can now add a time period to each column in a table, enabling you to add a time period that is different from the one your calendar is set to. This is another way you can compare dates.

1. Right-click a column in the table and select **[!UICONTROL Add time period column]**. 

   ![](assets/add-time-period-column.png)

1. Depending on how you have set the table's date range, you have these options for comparison: 

   |  Option  | Description  |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Adds a column with the week/month/etc. immediately before this date range.  |
   | **[!UICONTROL This week/month/quarter/year last year to this date range]** | Adds the same date range a year ago.  |
   | **[!UICONTROL Custom date range to this date range]** | Lets you select a custom date range.  |

   >[!NOTE]
   >
   >When you select a custom number of days, for example October 7 - October 20 (a 14-day range), you will get only 2 options: **[!UICONTROL Prior 14 days before this date range]**, and **[!UICONTROL Custom date range to this date range]**.

1. The time period will be inserted on top of the column you selected:

   ![](assets/add-time-period-column2.png)

1. You can add as many time columns as you want, as well as mix and match different date ranges:

   ![](assets/add-time-period-column4.png)

1. In addition, you can sort on each column, which will change the order of days depending on the column you are sorting on.

## Align column dates to start on the same row {#section_5085E200082048CB899C3F355062A733}

You can align the dates from each column to all start on the same row. 

For example, when you choose to align the dates, if you do a month-over-month comparison between October and September 2016, the left column will start with October 1 and the right column will start with September 1:

![](assets/add-time-period-column3.png)

>[!NOTE]
>
>Consider the following when using this option:
>
>* This setting is enabled by default for all new projects.
>
>* This setting applies to the entire table. For example, if you change this setting for a breakdown within the table, it will change the setting for the entire table.
>

To enable this setting, if it is not already enabled:

1. In the table where you want to align column dates, select the **Settings** icon in the table header.

1. On the [!UICONTROL **Settings**] tab, select **[!UICONTROL Align Dates from each column to all start on the same row (applies to entire table)]**.

![](assets/date-comparison-setting.png)


-->