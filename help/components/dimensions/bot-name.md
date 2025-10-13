---
title: Bot-Name
description: Der Name des Bots, der den Bot-Regeln entspricht.
exl-id: 034dce46-e83c-4053-a062-3998231f8d6b
feature: Dimensions
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%

---

# Bot-Name

Die Dimension „Bot-[&quot; &#x200B;](overview.md) die Namen von Bots an, die mithilfe von [Bot-Regeln“ &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md) wurden. Bei diesen Regeln kann es sich um standardmäßige IAB-Regeln oder benutzerdefinierte Bot-Regeln handeln, die von Ihrem Unternehmen konfiguriert werden. Dies ist hilfreich, wenn Sie mehr darüber erfahren möchten, welche Bots Ihre Site besuchen oder welche Bots den meisten Traffic generieren.

Treffer, die mit [!UICONTROL Bot-Regeln] übereinstimmen, werden automatisch aus allen Analytics-Berichten gefiltert, mit Ausnahme dieser Dimension, [Bot-Vorfälle](../metrics/bot-occurrences.md) und [Bot-Seitenansichten](../metrics/bot-page-views.md). Sie können diese Dimension und diese beiden Metriken verwenden, um zu sehen, welche Bot-Daten aus dem Rest Ihrer Berichte ausgeschlossen sind.

Da beide Berichte vom Rest Ihrer Report Suite-Daten getrennt sind, werden mit dieser Dimension nur die folgenden Dimensionen und Metriken unterstützt:

* [Seite](page.md)
* Zeitbasierte Dimensionen (z. B. [Tag](day.md), [Woche](week.md) oder [Monat](month.md))
* [Bot-Vorfälle](../metrics/bot-occurrences.md)
* [Bot-Seitenansichten](../metrics/bot-page-views.md)

Die Verwendung einer anderen Dimension oder Metrik mit dieser Dimension gibt keine Daten zurück.

## Füllen dieser Dimension mit Daten

Wenn Sie „Bot[Regeln“ aktiviert haben](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md) erfasst diese Dimension automatisch Daten. Wenn Sie „Bot[!UICONTROL Regeln“ noch nicht &#x200B;] haben, wird diese Dimension in Analysis Workspace nicht angezeigt.

## Dimensionselemente

Jedes Dimensionselement listet den Namen des Bots auf, der den IAB- oder benutzerdefinierten Bot-Regelkriterien entsprach.
