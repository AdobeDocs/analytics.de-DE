---
title: Bot-Produktvorfälle
description: Die Metrik „Bot-Produktvorfälle“ zeigt die Anzahl der Untertreffer von Produktzeichenfolgen an, die mit Bot-Regeln übereinstimmten und aus dem Analytics-Reporting ausgeschlossen wurden.
feature: Metrics
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
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 7a99ecd99a9b1a639c8a2d48dc35d57fdfeb1a12
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 5%
---
# Bot-Produktvorfälle

Die Metrik „Bot-[&quot; ](overview.md) die Anzahl der Untertreffer an, die mit „Bot[Regeln“ ](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md).

Da beide Berichte vom Rest der Report Suite-Daten getrennt sind, funktioniert diese Metrik nur mit den folgenden Dimensionen:

* [Bot-Name](../dimensions/bot-name.md)
* Zeitbasierte Dimensionen (z. B. [Tag](../dimensions/day.md), [Woche](../dimensions/week.md) oder [Monat](../dimensions/month.md))

Die Verwendung einer anderen Dimension mit dieser Metrik gibt keine Daten zurück.

## Berechnung dieser Metrik

Adobe prüft jeden Untertreffer mit der [Produktzeichenfolge](/help/implement/vars/page-vars/products.md) um festzustellen, ob er mit den von Ihrem Unternehmen konfigurierten Bot-Regeln übereinstimmt. Wenn ein gegebener Untertreffer mit einer Bot-Regel übereinstimmt, wird der Untertreffer aus dem Reporting ausgeschlossen, und diese Metrik erhöht sich um eins.
