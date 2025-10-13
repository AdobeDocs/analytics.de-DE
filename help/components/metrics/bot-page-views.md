---
title: Bot-Seitenansichten
description: Die Anzahl der Seitenansichten, die mit Bot-Regeln übereinstimmen.
feature: Metrics
exl-id: d6699880-3faa-4df9-ad49-c7998f6ce45b
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 11%

---

# Bot-Seitenansichten

Die Metrik „Bot[Seitenansichten“ &#x200B;](overview.md) die Anzahl der Seitentreffer an, die mit [Bot-Regeln“ &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md).

Da beide Berichte vom Rest der Report Suite-Daten getrennt sind, funktioniert diese Metrik nur mit den folgenden Dimensionen:

* [Bot-Name](../dimensions/bot-name.md)
* [Seite](../dimensions/page.md)
* Zeitbasierte Dimensionen (z. B. [Tag](../dimensions/day.md), [Woche](../dimensions/week.md) oder [Monat](../dimensions/month.md))

Die Verwendung einer anderen Dimension mit dieser Metrik gibt keine Daten zurück.

## Berechnung dieser Metrik

Adobe prüft jeden Seitenaufruf, um festzustellen, ob er mit den von Ihrem Unternehmen konfigurierten Bot-Regeln übereinstimmt. Wenn ein bestimmter Treffer mit einer Bot-Regel übereinstimmt, wird der Seitentreffer aus dem Reporting ausgeschlossen und diese Metrik erhöht sich um eins. Diese Metrik umfasst keine Linktracking-Treffer ([`tl()`](/help/implement/vars/functions/tl-method.md)).
