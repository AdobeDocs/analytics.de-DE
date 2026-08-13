---
title: Paid Search
description: Unterscheidet Metriken von gebührenpflichtiger und kostenloser Suche.
feature: Dimensions
exl-id: b12665a3-e92f-4fc1-acd3-ea17a316e5e5
TQID: https://experienceleague.adobe.com/s9jhjGeXaOCo-Wz-Jyof951NZdRWfz-9tjrVrjHvTS0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 87%

---

# Paid Search

Mit der Dimension [Paid Search](overview.md) können Sie eine beliebige Metrik betrachten und sie zwischen Paid Search und natürlicher Suche vergleichen. Alle anderen Treffer außerhalb der Suchmaschinen werden weggelassen. Diese Dimension ist hilfreich, um zu verstehen, wie sich Ihre gebührenpflichtigen Suchbemühungen mit der kostenlosen Suche vergleichen.

## Füllen dieser Dimension mit Daten

Die einzige Voraussetzung für die ordnungsgemäße Funktion dieser Dimension ist, dass die [gebührenpflichtige Sucherkennung](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md) in den Einstellungen der Report Suite korrekt konfiguriert ist. Wenn die gebührenpflichtige Sucherkennung korrekt konfiguriert ist und eine Report Suite Daten enthält, funktioniert diese Dimension immer.

## Dimensionselemente

Zu den Dimensionselementen gehören zwei statische Werte: `"Natural"` und `"Paid"`. Wenn ein Besuch die Kriterien für eine Suchmaschine erfüllt und auch mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum Dimensionselement `"Paid"`. Wenn ein Besuch die Kriterien für eine Suchmaschine erfüllt und *nicht* mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum Dimensionselement `"Natural"`.
