---
title: Besuchsdauer pro Besucher (Sekunden)
description: Die Metrik „Besuchsdauer pro Besucher (Sekunden)“ gibt die durchschnittliche Zeit an, die Besucher während der gesamten Lebensdauer eines Besuchers mit einem bestimmten Dimensionselement interagieren.
feature: Metrics
exl-id: 80f38bab-2ee1-4d0d-ba53-9b2c7c85e481
TQID: https://experienceleague.adobe.com/NFmA2Q80h2WOTRwoJ882aFMG60y2HKngR0Ew0qnxb8o
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
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 85%

---

# Besuchsdauer pro Besucher (Sekunden)

Die [!UICONTROL Metrik Besuchszeit pro Besucher (Sekunden] [&#x200B; zeigt &#x200B;](overview.md) durchschnittliche Zeit an, die Besucherinnen und Besucher während ihrer gesamten Lebensdauer mit einem bestimmten Dimensionselement interagieren.

Diese Metrik ist aufgrund ihrer unterschiedlichen Verarbeitungsarchitektur nicht in Data Warehouse verfügbar.

## Berechnung dieser Metrik

Diese Metrik verwendet die Formel [`Total seconds spent`](total-seconds-spent.md) `divided by` [`Unique visitors`](unique-visitors.md).

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die Besuchsdauer pro Besucher der gesamten Dimension und der Zähler ist die Besuchsdauer pro Besucher des Dimensionselements. Wenn die Besuchsdauer pro Besucher der gesamten Dimension kürzer ist als die Besuchsdauer pro Besucher eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für die Besuchszeit pro Besucher angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](time-spent.md).
