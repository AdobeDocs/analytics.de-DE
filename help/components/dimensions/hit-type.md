---
title: Treffertyp
description: Bestimmt, ob es sich bei dem Treffer um einen Vordergrund- oder Hintergrundtreffer handelt.
feature: Dimensions
exl-id: b922adbb-fe36-46c7-aab2-b9471de07d2f
TQID: https://experienceleague.adobe.com/6G-XpOMMZGum9LAQzKn0zGdeNRmHFPpmYizqRrbKuUE
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2
  - id: c77ba355-6681-41fe-b719-563d3f507fdb
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 84%

---

# Treffertyp

Der „Treffertyp“ [Dimension](overview.md) bestimmt, ob sich eine Mobile App im Vorder- oder Hintergrund befand, als der Treffer an die Datenerfassungs-Server von Adobe gesendet wurde. Diese Dimension ist nur für Report Suites relevant, die Daten für mobile Apps enthalten. Über AppMeasurement erfasste Browser-Daten melden den Treffer immer als „Vordergrund“.

## Füllen dieser Dimension mit Daten

Diese Dimension funktioniert bei allen Mobile SDK-Implementierungen ab Version 4.13.6 standardmäßig. Wenn Sie das Mobile SDK nicht verwenden, werden alle Treffer unter dem Dimensionselement „Vordergrund“ aufgelistet. Wenn „Ältere Berichterstellung und Attribution deaktivieren, um Hintergrundtreffer zu erhalten“ ausgewählt wird, werden Hintergrundtreffer nur in [Virtual Report Suites](../vrs/vrs-mobile-visit-processing.md) angezeigt.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Foreground"` und `"Background"`. Jeder Treffer, der nicht im Hintergrund einer mobilen App gesendet wurde, gehört zum Dimensionselement `"Foreground"`. Jeder Treffer, der gesendet wird, wenn die mobile App im Hintergrund war, gehört zum Dimensionselement `"Background"`.
