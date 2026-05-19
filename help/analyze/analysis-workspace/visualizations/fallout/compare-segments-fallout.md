---
description: Erfahren Sie, wie Sie in einer Fallout-Analyse in Analysis Workspace Segmente aus einem Touchpoint erstellen, Segmente als Touchpoint hinzufügen und wichtige Workflows über verschiedene Segmente hinweg vergleichen können.
keywords: Fallout und Segmentierung;Segmente in Fallout-Analyse;Segmente in Fallout vergleichen
title: Segmente in Fallout-Analyse anwenden
feature: Visualizations
role: User, Admin
exl-id: 2177cd09-5a27-4295-8414-580cf53062cb
TQID: https://experienceleague.adobe.com/LZiLhy8ufqzxHyxjqWy1XLv5uU7JgB5eqzPm6wbXF6s
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: a544b409-2610-410d-a842-474ac1d0d54e
  - id: dcae653e-62c6-4cc8-84e6-ee110b848296
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 449
ht-degree: 40%

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

   Der Segment Builder wird geöffnet und enthält bereits das vorkonfigurierte sequenzielle Segment, das dem von Ihnen ausgewählten Touchpoint entspricht:

   ![](assets/fallout-definesegment.png)

1. Geben Sie dem Segment einen Titel und eine Beschreibung und speichern Sie es.

   Dieses Segment kann jetzt in jedem gewünschten Projekt verwendet werden.

## Hinzufügen eines Segments als Touchpoint

Wenn Sie beispielsweise sehen möchten, wie sich die Mobile-App-Treffer im Trend auswirken und wie sich dies auf den Fallout auswirkt, ziehen Sie einfach das Segment Mobile-App-Treffer in den Fallout:

![](assets/segment-touchpoint.png)

Sie können auch einen UND-Touchpoint erstellen, indem Sie das Segment Mobile-App-Treffer auf einen anderen Checkpoint ziehen.

## Vergleichen von Segmenten im Fallout

In der Fallout-Visualisierung können Sie eine unbegrenzte Anzahl von Segmenten miteinander vergleichen. (Beachten Sie, dass Sie im folgenden Video bis zu drei Segmente vergleichen können, was falsch ist.)



1. Wählen Sie die zu vergleichenden Segmente aus dem Bedienfeld [!UICONTROL Segment] auf der linken Seite aus. Im Beispiel sind zwei Segmente ausgewählt: **[!UICONTROL iOS]** und **[!UICONTROL Android]**.
1. Ziehen Sie die drei Segmente in den Ablegebereich für Segmente am oberen Rand der Visualisierung.

   ![](assets/segment-compare.png)

1. Optional: Sie können *Alle Personen* als Standard-Container beibehalten oder den Container löschen.

1. Sie können jetzt den Fallout über die drei Segmente hinweg vergleichen, z. B. wo ein Segment eine bessere Leistung als das andere erzielt, oder andere Einblicke erhalten.
