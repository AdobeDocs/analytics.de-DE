---
title: Durchschnittliche Seitenansichten pro Besuch
description: Die durchschnittliche Häufigkeit, mit der ein bestimmtes Dimensionselement bei einem Besuch angezeigt wurde.
feature: Metrics
exl-id: fef6e803-e819-4f0f-8cb0-c565328a8bea
TQID: https://experienceleague.adobe.com/sospsPhk77O5qOLcMLmu7gB7rvlxbp8rGqB39LCnQ5g
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 216
ht-degree: 92%

---

# Durchschnittliche Seitenansichten pro Besuch

Die Dimension „Durchschnittliche Seitenansichten pro Besuch“ gibt an, wie viele Seitenansichten durchschnittlich in Ihrer gewünschten Dimension aufgetreten sind. Bei zeitbasierten Dimensionen können Sie sehen, wie sich die durchschnittliche Anzahl der Seitenansichten innerhalb eines Besuchs im Zeitverlauf entwickelt. Diese [Metrik](overview.md) ist hilfreich, wenn Sie verstehen möchten, wie oft Dimensionselemente bei einem Besuch angezeigt werden.

>[!TIP]
>
>Verwenden Sie diese Metrik zusammen mit einer anderen Metrik (z. B. [Besuche](visits.md)), um bessere Einblicke zu erhalten. Wenn Sie diese Metrik allein verwenden, erhalten Sie Dimensionselemente mit anomalen Seitenansichten pro Besuch, was normalerweise nicht nützlich ist.

## Berechnung dieser Metrik

Diese Metrik wird mit der Formel [`Page views`](page-views.md)` divided by `[`Visits`](visits.md) berechnet.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Im Nenner sind die durchschnittlichen Seitenansichten pro Besuch der gesamten Dimension und im Zähler die durchschnittlichen Seitenansichten pro Besuch des Dimensionselements. Wenn die durchschnittlichen Seitenansichten pro Besuch der gesamten Dimension geringer sind als die durchschnittlichen Seitenansichten pro Besuch eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für durchschnittlichen Seitenansichten pro Besuch angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.
