---
description: Durch die Segmentierung einzelner Metriken können Sie Metriken innerhalb eines Berichts vergleichen.
title: Segmentierte Metriken
feature: Calculated Metrics
exl-id: 1e7e048b-9d90-49aa-adcc-15876c864e04
source-git-commit: 1dc0325f1a8b4fc1888895ee18570effb34e6208
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 69%

---

# Segmentierte Metriken

Im Generator für berechnete Metriken können Sie Segmente innerhalb Ihrer Metrikdefinition anwenden. Dies ist hilfreich, wenn Sie neue Metriken für Ihre Analyse ableiten möchten. Beachten Sie, dass Segmentdefinitionen über den Segment Builder aktualisiert werden können. Wenn Änderungen vorgenommen werden, wird das Segment automatisch überall dort aktualisiert, wo es angewendet wurde, auch wenn es Teil einer Definition für berechnete Metriken ist.

![](assets/german-visitors.png)

## Erstellen einer segmentierten Metrik {#create}

Beispiel: Sie möchten unterschiedliche Aspekte des Segments „Deutsche Besucher“ mit denen des Segments „Internationale Besucher“ vergleichen. Dazu können Sie Metriken erstellen, die Einblick in Folgendes ermöglichen:

* Wie sieht das Browsingverhalten im Vergleich zwischen den beiden Gruppen aus? (Ein weiteres Beispiel wäre: Wie sieht die Konversionsrate im Vergleich zwischen den beiden Segmenten aus?)
* Wie viele Besucher aus Deutschland navigieren im Vergleich mit internationalen Besuchern zu bestimmten Seiten (als Prozentsatz der Gesamtbesucher)?
* Wo liegen die größten Unterschiede in Bezug darauf, welcher Inhalt von den verschiedenen Segmenten aufgerufen wird?

Erstellen und speichern Sie eine Metrik namens „Deutsche Besucher“ und eine Metrik namens „Internationale Besucher“:

1. Erstellen Sie im Generator für berechnete Metriken ein Ad-hoc-Segment namens „Deutsche Besucher“, bei dem Sie für „Länder“ den Wert „Deutschland“ angeben.

   Ziehen Sie die Dimension Länder in die Arbeitsfläche Definition und wählen Sie [!UICONTROL **Deutschland**] als Wert aus:

   ![](assets/segment-from-dimension.png)

   >[!NOTE]
   >
   >Sie können diesen Vorgang auch im [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-build.md) durchführen, aber wir haben den Arbeitsablauf vereinfacht. Daher stehen Dimensionen auch im Generator für berechnete Metriken zur Verfügung. „Ad hoc“ bedeutet, dass das Segment nicht in der Liste der **[!UICONTROL Segmente]** in der linken Leiste angezeigt wird. Sie können es aber auch veröffentlichen, indem Sie über das „i“ daneben fahren und auf **[!UICONTROL Als öffentlich einstellen klicken]**.

1. Ziehen Sie das Segment Deutschland in die Arbeitsfläche Definition und ziehen Sie die Metrik Unique Visitors hinein:

   ![](assets/german-visitors.png)

1. Wählen [!UICONTROL **Speichern**], um die berechnete Metrik zu speichern.

1. Erstellen Sie im Generator für berechnete Metriken ein Ad-hoc-Segment namens „Internationale Besucher“, bei dem „Länder“ nicht „Deutschland“ entspricht.

   Ziehen Sie die Dimension Länder in die Arbeitsfläche „Definition“, wählen Sie [!UICONTROL **Deutschland**] als Wert aus und wählen Sie dann [!UICONTROL **Ist nicht gleich**] als Operator aus.

1. Ziehen Sie die Metrik Unique Visitors hinein.

1. Wählen [!UICONTROL **Speichern**], um die berechnete Metrik zu speichern.

1. Ziehen Sie in Analysis Workspace die Dimension **[!UICONTROL Seite]** in eine Freiform-Tabelle und dann die zwei neuen berechneten Metriken nebeneinander oben in die Tabelle:

   ![](assets/workspace-pages.png)

Im Folgenden finden Sie eine Videoübersicht:

>[!VIDEO](https://video.tv.adobe.com/v/25409/?quality=12&learn=on)

## Prozent der Gesamtmetriken {#percent-total}

Sie können das obige Beispiel weiter ausführen, indem Sie Ihr Segment mit der Gesamtpopulation vergleichen. Erstellen Sie dazu zwei neue Metriken: „% aller deutschen Besucher“ und „% der Gesamtzahl internationaler Besucher“:

1. Ziehen Sie das Segment „Deutsche Besucher“ (oder „Internationale Besucher“) in die Arbeitsfläche.
1. Legen Sie darunter ein weiteres Segment „Deutsche Besucher“ (oder „Internationale Besucher“) ab. Klicken Sie dieses Mal aber auf das zugehörige Konfigurationssymbol (Zahnrad), um den Metriktyp „Gesamt“ auszuwählen. Das Format sollte „Prozent“ lauten. Der Operator sollte „Geteilt durch“ lauten. Dadurch erhalten Sie die folgende Metrikdefinition:

   ![](assets/cm_metric_total.png)

1. Wenden Sie diese Metrik auf das Projekt an:

   ![](assets/cm_percent_total.png)
