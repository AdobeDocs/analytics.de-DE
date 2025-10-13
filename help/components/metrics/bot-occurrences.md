---
title: Bot-Vorfälle
description: Die Anzahl der Treffer, die mit Bot-Regeln übereinstimmen.
feature: Metrics
exl-id: 94cbbee4-8455-48b1-b804-534ed8fccdc9
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 9%

---

# Bot-Vorfälle

Die Metrik „Bot-[&quot; &#x200B;](overview.md) die Anzahl der Treffer an, die mit [Bot-Regeln“ &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md).

Da beide Berichte vom Rest der Report Suite-Daten getrennt sind, funktioniert diese Metrik nur mit den folgenden Dimensionen:

* [Bot-Name](../dimensions/bot-name.md)
* [Seite](../dimensions/page.md)
* Zeitbasierte Dimensionen (z. B. [Tag](../dimensions/day.md), [Woche](../dimensions/week.md) oder [Monat](../dimensions/month.md))

Die Verwendung einer anderen Dimension mit dieser Metrik gibt keine Daten zurück.

## Berechnung dieser Metrik

Adobe prüft jeden Treffer, um festzustellen, ob er mit den von Ihrem Unternehmen konfigurierten Bot-Regeln übereinstimmt. Wenn ein bestimmter Treffer mit einer Bot-Regel übereinstimmt, wird der Treffer vom Reporting ausgeschlossen und diese Metrik erhöht sich um eins. Diese Metrik umfasst sowohl Seitenansichten ([`t()`](/help/implement/vars/functions/t-method.md)) als auch Linktracking-Treffer ([`tl()`](/help/implement/vars/functions/tl-method.md)), während [Bot-Seitenansichten](bot-page-views.md) keine Linktracking-Treffer enthalten.
