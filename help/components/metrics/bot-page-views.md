---
title: Bot-Seitenansichten
description: Die Anzahl der Seitenansichten, die mit Bot-Regeln übereinstimmen.
feature: Metrics
exl-id: d6699880-3faa-4df9-ad49-c7998f6ce45b
TQID: https://experienceleague.adobe.com/Y0r2fzF87dep4NsrbJGCC9OnqBHrZozCh2DovNc90KQ
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 11%

---

# Bot-Seitenansichten

Die Metrik „Bot[Seitenansichten“ ](overview.md) die Anzahl der Seitentreffer an, die mit [Bot-Regeln“ ](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md).

Da beide Berichte vom Rest der Report Suite-Daten getrennt sind, funktioniert diese Metrik nur mit den folgenden Dimensionen:

* [Bot-Name](../dimensions/bot-name.md)
* [Seite](../dimensions/page.md)
* Zeitbasierte Dimensionen (z. B. [Tag](../dimensions/day.md), [Woche](../dimensions/week.md) oder [Monat](../dimensions/month.md))

Die Verwendung einer anderen Dimension mit dieser Metrik gibt keine Daten zurück.

## Berechnung dieser Metrik

Adobe prüft jeden Seitenaufruf, um festzustellen, ob er mit den von Ihrem Unternehmen konfigurierten Bot-Regeln übereinstimmt. Wenn ein bestimmter Treffer mit einer Bot-Regel übereinstimmt, wird der Seitentreffer aus dem Reporting ausgeschlossen und diese Metrik erhöht sich um eins. Diese Metrik umfasst keine Linktracking-Treffer ([`tl()`](/help/implement/vars/functions/tl-method.md)).
