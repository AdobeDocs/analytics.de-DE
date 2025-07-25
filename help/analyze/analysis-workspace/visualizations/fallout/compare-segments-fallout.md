---
description: Erfahren Sie, wie Sie in einer Fallout-Analyse in Analysis Workspace Segmente aus einem Touchpoint erstellen, Segmente als Touchpoint hinzufügen und wichtige Workflows über verschiedene Segmente hinweg vergleichen können.
keywords: Fallout und Segmentierung;Segmente in Fallout-Analyse;Segmente in Fallout vergleichen
title: Segmente in Fallout-Analyse anwenden
feature: Visualizations
role: User, Admin
exl-id: 2177cd09-5a27-4295-8414-580cf53062cb
source-git-commit: bf8bc40e3ec325e8e70081955fb533eee66a1734
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 42%

---

# Segmente in der Fallout-Analyse anwenden

Sie können in Analysis Workspace Segmente aus einem Touchpoint erstellen, Segmente als Touchpoints hinzufügen und wichtige Workflows über verschiedene Segmente hinweg vergleichen.

>[!IMPORTANT]
>
>Segmente, die als Checkpoints in Fallout verwendet werden, müssen einen Container verwenden, der auf einer niedrigeren Ebene liegt als der Gesamtkontext der Fallout-Visualisierung. Bei einem Besucherkontext-Fallout müssen Segmente, die als Checkpoints verwendet werden, besuchsbasierte oder Hit-basierte Segmente sein. Bei einem besuchskontextbezogenen Fallout müssen Segmente, die als Checkpoint verwendet werden, Hit-basierte Segmente sein. Wenn Sie eine ungültige Kombination verwenden, beträgt der Fallout 100 %. In der Fallout-Visualisierung wird eine Warnung angezeigt, wenn Sie ein inkompatibles Segment als Touchpoint hinzufügen. Bestimmte ungültige Segment-Container-Kombinationen führen zu ungültigen Fallout-Diagrammen, z. B.:
>
>* Verwenden eines besucherbasierten Segments als Touchpoint innerhalb einer auf den Besucherkontext bezogenen Fallout-Visualisierung.
>* Verwenden eines besucherbasierten Segments als Touchpoint innerhalb einer auf den Besuchskontext bezogenen Fallout-Visualisierung
>* Verwenden eines besuchsbasierten Segments als Touchpoint innerhalb einer auf den Besuchskontext bezogenen Fallout-Visualisierung
>

## Erstellen eines Segments aus einem Touchpoint

1. Als Erstes erstellen Sie ein Segment aus einem bestimmten Touchpoint, an dem Sie interessiert sind und der sich möglicherweise lohnt, auch in andere Berichte übernommen zu werden. Klicken Sie dazu mit der rechten Maustaste auf den Touchpoint und wählen Sie dann **[!UICONTROL Segment aus Touchpoint erstellen aus]**.

   ![](assets/fallout-createsegment.png)

   Der Segment Builder wird geöffnet und enthält das vorab erstellte sequenzielle Segment, das zu dem von Ihnen ausgewählten Touchpoint passt:

   ![](assets/fallout-definesegment.png)

1. Geben Sie einen Titel und eine Beschreibung für das Segment ein, und speichern Sie es.

   Dieses Segment kann jetzt in jedem gewünschten Projekt verwendet werden.

## Hinzufügen eines Segments als Touchpoint

Wenn Sie beispielsweise sehen möchten, wie sich die Mobile-App-Treffer im Trend auswirken und wie sich dies auf den Fallout auswirkt, ziehen Sie einfach das Segment Mobile-App-Treffer in den Fallout:

![](assets/segment-touchpoint.png)

Sie können auch einen UND-Touchpoint erstellen, indem Sie das Segment Mobile-App-Treffer auf einen anderen Checkpoint ziehen.

## Vergleichen von Segmenten im Fallout

In der Fallout-Visualisierung können Sie eine unbegrenzte Anzahl von Segmenten vergleichen. (Beachten Sie, dass Sie im folgenden Video bis zu drei Segmente vergleichen können, was falsch ist.)


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Segmente in einer Fallout-Visualisierung vergleichen](https://video.tv.adobe.com/v/328032?quality=12&learn=on&captions=ger){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


1. Wählen Sie die zu vergleichenden Segmente aus dem Bedienfeld [!UICONTROL Segment] auf der linken Seite aus. Im Beispiel sind zwei Segmente ausgewählt: **[!UICONTROL iOS]** und **[!UICONTROL Android]**.
1. Ziehen Sie die drei Segmente in den Ablegebereich für Segmente am oberen Rand der Visualisierung.

   ![](assets/segment-compare.png)

1. Optional: Sie können *Alle Personen* als Standard-Container beibehalten oder den Container löschen.

1. Sie können jetzt den Fallout über die drei Segmente hinweg vergleichen, z. B. wo ein Segment eine bessere Leistung als das andere erzielt, oder andere Einblicke erhalten.
