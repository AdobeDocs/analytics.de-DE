---
description: Erfahren Sie, wie Sie einen Beitragsanalysebericht in Analysis Workspace ausführen.
title: Ausführen einer Beitragsanalyse
role: User, Admin
exl-id: 20d1ba8d-3e4e-4702-ae28-5eb6bf00847b
feature: Anomaly Detection
TQID: https://experienceleague.adobe.com/gRnQxBkxEqtDdZ-zbgeg4Oe0MweTmqKwtThl3NYPpgs
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: dcae653e-62c6-4cc8-84e6-ee110b848296id: e38cbddc-1633-4cd5-bed5-9f289f2a6029
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 554
ht-degree: 9%

---

# Ausführen einer Beitragsanalyse

[Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, der helfen soll, Aspekte zu erkennen, die zu einer in Adobe Analytics festgestellten Anomalie mit beigetragen haben. ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis) Damit soll Benutzenden geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysen viel schneller zu identifizieren.

>[!NOTE]
>
>Die Beitragsanalyse wird nur für Daten mit täglicher Granularität unterstützt.

Die Schritte zum Ausführen der Beitragsanalyse sind:

1. Aufrufen der Beitragsanalyse in einem Projekt

   ![Ausführen der Beitragsanalyse](assets/run-contribution-analysis.png)

   1. Wählen Sie in einer Linienvisualisierung, die auf einer Freiformtabelle mit täglicher Granularität basiert, einen Anomalie-Datenpunkt aus. Wählen Sie im Popup die Option **[!UICONTROL Analysieren]** aus.
   1. Wählen Sie in einer Freiformtabelle mit täglicher Granularität im Kontextmenü in einer beliebigen Zeile die Option **[!UICONTROL Beitragsanalyse ausführen]** aus. Sie können die Analyse auch für Zeilen ausführen, die keine Anomalie anzeigen.
   1. In einer Freiformtabelle mit täglicher Granularität in einer Zeile, die eine Anomalie anzeigt:
      1. Wählen Sie die ◥ aus.
      1. Wählen Sie im Dialogfeld ![Warnhinweis](/help/assets/icons/Alert.svg) **[!UICONTROL Anomalie]**) die Option **[!UICONTROL Beitragsanalyse öffnen]**.



1. (Optional) Sie können den Umfang der Analyse einschränken (und somit die Analyse beschleunigen), indem Sie [Dimensionen ausschließen](#exclude-dimensions).

   ![Ausschließen von Dimensionen aus der Beitragsanalyse](assets/excluding-dimensions.png)

1. Wählen **[!UICONTROL Beitragsanalyse ausführen]** aus.

1. Warten Sie, während die Beitragsanalyse verarbeitet wird. Die Verarbeitung kann je nach Größe der Report Suite und der Anzahl der Dimensionen erheblich dauern. Die Beitragsanalyse führt eine Analyse der wichtigsten 50.000 Elemente pro Dimension durch. Sie werden auch über die Anzahl der verbleibenden [Beitragsanalyse-Token](anomaly-detection.md#contribution-analysis-tokens) benachrichtigt.

   ![Beitragsanalyse wird ausgeführt](assets/contribution-analysis-executing.png)

1. Analysis Workspace lädt ein neues **[!UICONTROL Beitragsanalyse]**-Bedienfeld direkt in diesem Projekt.

   ![Bedienfeld Beitragsanalyse](assets/contribution-analysis.png)

   * Visualisierung [Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md).
   * Eine monatliche Trend[Linien](/help/analyze/analysis-workspace/visualizations/line.md)Visualisierung.
   * Eine **[!UICONTROL Top-Elemente]**[Freiformtabelle), ](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) anzeigt, welche Top-Elemente zu dieser Anomalie beitragen, sortiert nach [Beitragsbewertung](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md#contribution-analysis). Die zusätzlichen Spalten zeigen die betreffende Metrik und eine **[!UICONTROL Unique Visitors]**-Metrik zur Bereitstellung des Kontexts.

   * Die **[!UICONTROL Generierte Segmente (Cluster der obersten Elemente]** [Freiformtabelle) ](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) Zuordnungen der obersten Elemente basierend auf dem Beitragswert, Anomalievorfällen und dem Gesamtprozentsatz, der zur anormalen Metrik beiträgt. Diese Zuordnung wird dann als Zielgruppensegment (Beitragssegment 1, Beitragssegment 2 usw.) erfasst. Wählen Sie ![Info](/help/assets/icons/Info.svg) aus, um die Segmentdefinition anzuzeigen, einschließlich der Elemente, aus denen die Segmente am häufigsten bestehen:


1. Da die Beitragsanalyse jetzt Teil von Analysis Workspace ist, können Sie eine Reihe seiner Funktionen aus einem Freiformtabellen-Kontextmenü nutzen, um Ihre Analyse noch aussagekräftiger zu gestalten, z. B.:

   * [Schlüsseln Sie jedes Dimensionselement nach einer anderen Dimension auf](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md)
   * [Trending einer oder mehrerer Zeilen](/help/analyze/analysis-workspace/home.md#section_34930C967C104C2B9092BA8DCF2BF81A)
   * [Neue Visualisierungen hinzufügen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)
   * [Warnhinweise erstellen](/help/components/alerts/alerts-overview.md)
   * [Erstellen oder vergleichen Sie Segmente.](/help/analyze/analysis-workspace/c-panels/c-segment-comparison/segment-comparison.md)

>[!NOTE]
>
>Die analysierte Anomalie wird in der Beitragsanalyse und den zugehörigen Projekten für intelligente Warnhinweise mit einem blauen Punkt hervorgehoben. Diese Hervorhebung bietet einen deutlicheren Hinweis auf die zu analysierende Anomalie.


## Dimensionen ausschließen

Möglicherweise möchten Sie einige Dimensionen aus der Beitragsanalyse ausschließen. Beispielsweise sind Ihnen möglicherweise Browser- oder hardwarebezogene Dimensionen völlig egal, und Sie möchten die Analyse beschleunigen, indem Sie sie entfernen.

So verwalten Sie die ausgeschlossene Dimension:

* Ziehen Sie unerwünschte Dimensionen in das Bedienfeld **[!UICONTROL Ausgeschlossene Dimensionen]** und speichern Sie dann die Liste, indem Sie auf **[!UICONTROL Als Standard festlegen]** klicken.

* Wählen Sie **[!UICONTROL Alle löschen]**, um von vorne zu beginnen.

* Wählen Sie ![Dimensionen](/help/assets/icons/Dimensions.svg) aus, um ein Kontextmenü anzuzeigen, und verwenden Sie ![CrossSize400](/help/assets/icons/CrossSize400.svg), um ausgewählte ausgeschlossene Dimensionen aus der Liste zu entfernen.

  ![](assets/excluded-dimensions-list.png)

Nachdem Sie auszuschließende Dimensionen geändert haben, wählen Sie erneut **[!UICONTROL Beitragsanalyse]**.

