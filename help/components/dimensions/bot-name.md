---
title: Bot-Name
description: Der Name des Bots, der mit den Bot-Regeln übereinstimmte.
exl-id: 034dce46-e83c-4053-a062-3998231f8d6b
feature: Dimensions
source-git-commit: 9f70dbeb9dfe54897915213480f05cbdfaf920ef
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%

---

# Bot-Name

Die Dimension &quot;Bot name&quot;[Dimension](overview.md) zeigt die Namen von Bots an, die mit [Bot rules](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) erkannt wurden. Diese Regeln können standardmäßige IAB-Regeln oder benutzerdefinierte Bot-Regeln sein, die Ihr Unternehmen konfiguriert. Dies ist hilfreich, wenn Sie mehr darüber erfahren möchten, welche Bots Ihre Site besuchen oder welche Bots den meisten Traffic generieren.

Treffer, die mit [!UICONTROL Bot-Regeln] übereinstimmen, werden automatisch aus allen Analytics-Berichten mit Ausnahme dieser Dimension herausgefiltert: [Bot-Vorfälle](../metrics/bot-occurrences.md) und [Bot-Seitenansichten](../metrics/bot-page-views.md). Sie können diese Dimension und diese beiden Metriken verwenden, um zu sehen, welche Bot-Daten aus dem Rest Ihrer Berichte ausgeschlossen werden.

Da Bot-Berichte vom Rest Ihrer Report Suite-Daten getrennt sind, werden für diese Dimension nur die folgenden Dimensionen und Metriken unterstützt:

* [Seite](page.md)
* Zeitbasierte Dimensionen (z. B. [Tag](day.md), [Woche](week.md) oder [Monat](month.md))
* [Bot-Vorfälle](../metrics/bot-occurrences.md)
* [Bot-Seitenansichten](../metrics/bot-page-views.md)

Die Verwendung einer anderen Dimension oder Metrik mit dieser Dimension gibt keine Daten zurück.

## Füllen dieser Dimension mit Daten

Wenn Sie [Bot rules](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) aktiviert haben, erfasst diese Dimension automatisch Daten. Wenn Sie [!UICONTROL Bot rules] noch nicht aktiviert haben, wird diese Dimension nicht in Analysis Workspace angezeigt.

## Dimensionselemente

Jedes Dimensionselement listet den Namen des Bots auf, der den IAB- oder benutzerdefinierten Bot-Regelkriterien entsprach.
