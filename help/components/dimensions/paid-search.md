---
title: Paid Search
description: Unterscheidet Metriken aus Paid Search und natürlicher Suche.
feature: Dimensions
exl-id: b12665a3-e92f-4fc1-acd3-ea17a316e5e5
TQID: https://experienceleague.adobe.com/s9jhjGeXaOCo-Wz-Jyof951NZdRWfz-9tjrVrjHvTS0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 59%
---
# Paid Search

Mit der Dimension [Paid Search](overview.md) können Sie eine beliebige Metrik betrachten und sie zwischen Paid Search und natürlicher Suche vergleichen. Alle anderen Treffer außerhalb von Suchmaschinen werden weggelassen. Diese Dimension ist hilfreich, um zu verstehen, wie sich Ihre gebührenpflichtigen Suchbemühungen mit der kostenlosen Suche vergleichen.

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension durch die Paid-Search-Erkennung ab, die den Suchmaschinen-Traffic als „Paid“ oder „Natural“ klassifiziert. Es gibt keine Variable zum Festlegen. Die einzige Voraussetzung ist, dass die [Paid-Search-Erkennung](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md) in den Report Suite-Einstellungen korrekt konfiguriert ist. Wenn die Paid-Search-Erkennung korrekt konfiguriert ist und eine Report Suite Daten enthält, funktioniert diese Dimension immer.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet durch Erkennung von Paid Search) |
| **Feld Web SDK/XDM** | Keine (abgeleitet durch Erkennung von Paid Search) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehören zwei statische Werte: `"Natural"` und `"Paid"`. Wenn ein Besuch die Kriterien für eine Suchmaschine erfüllt und auch mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum Dimensionselement `"Paid"`. Wenn ein Besuch die Kriterien für eine Suchmaschine erfüllt und *nicht* mit der gebührenpflichtigen Sucherkennung übereinstimmt, gehört er zum Dimensionselement `"Natural"`.
