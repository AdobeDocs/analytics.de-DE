---
description: Erfahren Sie, wie Sie einzelne Metriken segmentieren, sodass Sie Metriken innerhalb derselben Visualisierung vergleichen können.
title: Segmentierte Metriken
feature: Calculated Metrics
exl-id: 1e7e048b-9d90-49aa-adcc-15876c864e04
TQID: https://experienceleague.adobe.com/t1HtjinGP02YSBQk1Z95t6wIQ0OhuFb14GKfpd8Y9Eg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: a544b409-2610-410d-a842-474ac1d0d54eid: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 463
ht-degree: 1%

---

# Segmentierte Metriken

Im [Generator für berechnete Metriken](cm-build-metrics.md#definition-builder) können Sie Segmente innerhalb Ihrer Metrikdefinition anwenden. Das Anwenden von Segmenten ist hilfreich, wenn Sie Metriken für eine Teilmenge Ihrer Daten in Ihrer Analyse verwenden möchten.

>[!NOTE]
>
>Segmentdefinitionen werden über den [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-build.md) aktualisiert. Wenn Sie eine Änderung an einem Segment vornehmen, wird das Segment automatisch aktualisiert, wo immer es verwendet wird, auch wenn das Segment Teil einer Definition für berechnete Metriken ist.
>

Sie möchten Metriken für deutsche Personen, die mit Ihrer Marke interagieren, mit denen für Personen außerhalb Deutschlands vergleichen. Sie können also Fragen beantworten wie:

1. Wie viele Deutsche bzw. internationale Personen besuchen Ihre beliebtesten [Seiten](#popular-pages).
1. Wie viele Deutsche bzw. internationale Personen [total](#totals) haben in diesem Monat online mit Ihrer Marke interagiert.
1. Was sind [Prozent](#percentages) der Deutschen und internationalen Menschen, die Ihre beliebten Seiten besucht haben?

In den folgenden Abschnitten erfahren Sie, wie Sie mithilfe segmentierter Metriken diese Fragen beantworten können. Gegebenenfalls wird auf eine ausführlichere Dokumentation verwiesen.

## Beliebte Seiten

1. [Erstellen Sie eine berechnete ](../cm-workflow.md) aus einem Workspace-Projekt namens `Germany`.
1. Erstellen Sie im [Generator für berechnete ](cm-build-metrics.md)[ ein Segment](/help/components/segmentation/segmentation-workflow/seg-build.md) mit dem Titel &quot;`Germany`&quot;, das das Feld „Länder“ verwendet.

   >[!TIP]
   >
   >Im Generator für berechnete Metriken können Sie ein Segment direkt mithilfe des Bedienfelds Komponenten erstellen.
   >   

   Ihr Segment könnte wie folgt aussehen.

   ![Segment Deutschland](assets/segment-germany.png)

1. Zurück im Generator für berechnete Metriken verwenden Sie das Segment , um die berechnete Metrik zu aktualisieren.

   ![Berechnete Metrik Deutschland](assets/germany-visits.png)

Wiederholen Sie die obigen Schritte für die internationale Version Ihrer berechneten Metrik.

1. Erstellen Sie aus Ihrem Workspace-Projekt eine berechnete Metrik mit dem Titel `Non Germany visits`.
1. Erstellen Sie im Generator für berechnete Metriken ein Segment mit dem Titel &quot;`Not Germany`&quot;, das das Feld „CRM-Land“ aus Ihren CRM-Daten verwendet, um zu bestimmen, woher eine Person kommt.

   Ihr Segment sollte wie folgt aussehen.

   ![Segment Deutschland](assets/segment-not-germany.png)

1. Zurück im Generator für berechnete Metriken verwenden Sie das Segment , um die berechnete Metrik zu aktualisieren.

   ![Berechnete Metrik Deutschland](assets/non-germany-visits.png)


1. Erstellen Sie ein Projekt in Analysis Workspace, in dem Sie sich die Seiten ansehen, die von deutschen und nichtdeutschen Besuchern besucht werden.

   ![Workspace-Freiformtabellen-Visualisierung, die deutsche und internationale Personen zeigt](assets/workspace-german-vs-international.png)


## Gesamt

1. Erstellen Sie zwei neue berechnete Metriken basierend auf der Gesamtsumme. Öffnen Sie jedes der zuvor erstellten Segmente, benennen Sie das Segment um, legen Sie **[!UICONTROL Metriktyp]** für **[!UICONTROL Personen]** auf **[!UICONTROL Gesamtsumme]** fest und verwenden Sie **[!UICONTROL Speichern unter]**, um das Segment unter dem neuen Namen zu speichern. Zum Beispiel:

   ![Gesamtmetrik für Deutschland](assets/calculated-metric-germany-total.png)

1. Fügen Sie Ihrem Workspace-Projekt eine neue Freiformtabellen-Visualisierung hinzu, die die Gesamtseiten für dieses Jahr anzeigt.

   ![Workspace-Freiformtabellen-Visualisierung, die Deutsche im Vergleich zu internationalen Personen zeigt](assets/workspace-german-vs-international-totals.png)


## Prozentsatz

1. Erstellen Sie zwei neue berechnete Metriken, die einen Prozentsatz aus den zuvor erstellten berechneten Metriken berechnen.

   ![Workspace-Freiformtabellen-Visualisierung, die den prozentualen Anteil deutscher vs. internationaler Personen anzeigt](assets/calculated-metric-germany-total-percentage.png)


1. Aktualisieren Sie Ihr Workspace-Projekt.

   ![Workspace-Freiformtabellen-Visualisierung, die Deutsche im Vergleich zu internationalen Personen zeigt](assets/workspace-german-vs-international-totals-percentage.png)

