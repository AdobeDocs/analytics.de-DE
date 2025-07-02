---
description: Sie können Anomalien in einer Tabelle oder einem Liniendiagramm anzeigen.
title: Anomalien in Analysis Workspace anzeigen
feature: Anomaly Detection
role: User, Admin
exl-id: 32edc7f4-c9b9-472a-b328-246ea5b54d07
source-git-commit: d37fa0aff0b1bbe196b943bc26e86b1e79936184
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 52%

---

# Anzeigen von Anomalien

Sie können Anomalien in Analysis Workspace in einer Tabelle oder einem Liniendiagramm anzeigen.

## Anzeigen von Anomalien in einer Tabelle {#section_869A87B92B574A38B017A980ED8A29C5}

Sie können Anomalien in einer Freiformtabelle für Zeitreihen anzeigen.

1. Wählen Sie ![ Spaltenüberschrift ](/help/assets/icons/Setting.svg)Einstellung“ aus und stellen Sie sicher, dass die Option **[!UICONTROL Anomalien]** in der Optionsliste ausgewählt ist. Weitere Informationen finden Sie unter [Spalteneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md).

1. Anomalien werden in der Tabelle wie folgt angezeigt:

   ![Anomalien erkannt](assets/anomaly-detected.png)

   Ein ◥ wird in der oberen rechten Ecke jeder Zeile angezeigt, in der eine Datenanomalie erkannt wird.

   Die **farbige senkrechte Linie** in jeder Zeile zeigt ➋ den erwarteten Wert an. Der **farbig schattierte Bereich** in jeder Zeile zeigt ➊ den tatsächlichen Wert an. Der Vergleich der Linie (erwarteter Wert) mit dem schattierten Bereich (tatsächlicher Wert) bestimmt, ob eine Anomalie vorliegt. (Eine Anomalie wird durch die fortschrittlichen statistischen Verfahren festgestellt, die im Abschnitt [In der Anomalieerkennung verwendete statistische Verfahren“ beschrieben ](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md).)

1. Wählen Sie ◥ in der oberen rechten Ecke einer Zeile aus, um Details zur Anomalie anzuzeigen. Angezeigt wird das Ausmaß (in Prozent), in dem der tatsächliche Wert über oder unter dem erwarteten Wert liegt.
1. Wählen [Beitragsanalyse öffnen](run-contribution-analysis.md), um die Beitragsanalyse zu starten.

## Darstellen von Anomalien in einem Liniendiagramm

Anomalien können ausschließlich in Liniendiagrammen visuell dargestellt werden.

So stellen Sie Anomalien in einem Liniendiagramm dar:

1. Wählen Sie ![Einstellung](/help/assets/icons/Setting.svg) in der Visualisierungskopfzeile aus und stellen Sie sicher, dass die Option [!UICONTROL **Anomalien anzeigen**] in der Optionsliste ausgewählt ist. Weitere Informationen finden Sie im Abschnitt [Linie](/help/analyze/analysis-workspace/visualizations/line.md).

1. (Optional) Damit das Diagramm anhand des Konfidenzintervalls skaliert werden kann, wählen Sie in der Visualisierungskopfzeile ![Einstellung](/help/assets/icons/Setting.svg) und dann die Option „Skalierung der Y-Achse durch Anomalien **[!UICONTROL &quot;]**.

   Diese Option ist nicht standardmäßig aktiviert, da das Diagramm dadurch unübersichtlicher werden kann.

   Anomalien werden im Liniendiagramm wie folgt dargestellt:

   ![Anomalieerkennung für Linienvisualisierung](assets/anomaly-detected-line.gif)

   Ein **weißer Punkt** auf der Linie bedeutet, dass an dieser Stelle eine Datenanomalie erkannt wurde. (Eine Anomalie wird durch die fortschrittlichen statistischen Verfahren festgestellt, die im Abschnitt [In der Anomalieerkennung verwendete statistische Verfahren“ beschrieben ](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md).)

   Der **hell schattierte Bereich** ist das Konfidenzband bzw. der erwartete Bereich, in dem Werte auftreten sollten. Jeder Wert, der außerhalb dieses erwarteten Bereichs liegt, ist eine Anomalie.

   Wenn das Liniendiagramm mehrere Metriken enthält, werden nur die Anomalien angezeigt. Bewegen Sie in diesem Fall den Mauszeiger über jede einzelne Anomalie, damit das Konfidenzband für diese Metrik eingeblendet wird.

   Die **gepunktete Linie** ist der erwartete Wert.

1. Wählen Sie eine Anomalie (weißer Punkt) aus, um die folgenden Informationen anzuzeigen:

   * Das Datum, an dem die Anomalie aufgetreten ist.

   * Der Rohwert der Anomalie.

   * Der Prozentwert über oder unter dem erwarteten Wert, der durch eine durchgezogene grüne Linie dargestellt wird.

   * Der **[!UICONTROL Analysieren]**-Link, um die Beitragsanalyse zu starten






