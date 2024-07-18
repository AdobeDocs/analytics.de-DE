---
title: Bot-Seitenansichten
description: Die Anzahl der Seitenansichten, die mit Bot-Regeln übereinstimmten.
feature: Metrics
exl-id: d6699880-3faa-4df9-ad49-c7998f6ce45b
source-git-commit: 9f70dbeb9dfe54897915213480f05cbdfaf920ef
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 11%

---

# Bot-Seitenansichten

Die Metrik &quot;Bot page views&quot;[metric](overview.md) gibt die Anzahl der Seitentreffer an, die mit [Bot rules](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) übereinstimmten.

Da Bot-Berichte vom Rest Ihrer Report Suite-Daten getrennt sind, funktioniert diese Metrik nur mit den folgenden Dimensionen:

* [Bot-Name](../dimensions/bot-name.md)
* [Seite](../dimensions/page.md)
* Zeitbasierte Dimensionen (z. B. [Tag](../dimensions/day.md), [Woche](../dimensions/week.md) oder [Monat](../dimensions/month.md))

Die Verwendung einer anderen Dimension mit dieser Metrik gibt keine Daten zurück.

## Berechnung dieser Metrik

Adobe überprüft jeden Seitentreffer, um festzustellen, ob er mit den von Ihrem Unternehmen konfigurierten Bot-Regeln übereinstimmt. Wenn ein bestimmter Treffer mit einer Bot-Regel übereinstimmt, wird der Seitentreffer aus dem Bericht ausgeschlossen und diese Metrik erhöht sich um 1. Diese Metrik enthält keine Linktracking-Treffer ([`tl()`](/help/implement/vars/functions/tl-method.md)).
