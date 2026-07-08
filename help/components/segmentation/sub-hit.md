---
title: Analyse der untergeordneten Treffer
description: Erfahren Sie, wie Sie mit der Analyse von Teiltreffern einzelne Produkte innerhalb eines Treffers in Adobe Analytics filtern können, wodurch der Attributionsblutungen in Produktberichten vermieden wird.
feature: Segmentation
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: a544b409-2610-410d-a842-474ac1d0d54e
source-git-commit: 0168cf33d647c5edb367094d57ad9ea3ee253844
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 0%

---

# Analyse der untergeordneten Treffer

{{release-limited-testing}}

Mit der Analyse untergeordneter Treffer können Sie Produktdaten auf einer Ebene analysieren, die detaillierter ist als die Trefferebene. Anstatt nach ganzen Treffern zu filtern, können Sie innerhalb von Treffern nach einzelnen Produkten segmentieren. Beispielsweise die Segmentierung nach einer bestimmten Produktkategorie ohne Einbeziehung aller anderen in derselben Bestellung gekauften Produkte.

In Adobe Analytics gilt die Analyse von Untertreffern speziell für die Variable **[!UICONTROL Products]**. Die **[!UICONTROL products]**-Variable ist das einzige Objekt mit mehreren Werten in Adobe Analytics, das die Analyse von Untertreffern unterstützt.

In Adobe Analytics kann die [Variable „Produkte](/help/components/dimensions/product.md) mehrere Produkte in einem Treffer erfassen. Ohne Analyse von Untertreffern gibt die Segmentierung nach einem Produktattribut alle Treffer zurück, bei denen ein beliebiges Produkt innerhalb eines Treffers mit dem Produktattribut übereinstimmt. Das Ergebnis ist eine falsche Attribution und überhöhte Umsatzmetriken. Die Analyse untergeordneter Treffer erfasst den Filter auf einzelne Produktzeilen innerhalb eines Treffers und löst diese Probleme.

In der Analyse von Untertreffern verhält sich die Ausschlusslogik anders als der standardmäßige Ausschluss auf Trefferebene bei der Variablen „products“. Wenn Sie Produktattribute im [!UICONTROL Produkte]-Container ausschließen, gibt das Segment Treffer zurück, die **Produkte haben** aber nicht Ihren Ausschlusskriterien entsprechen. Das Segment gibt keine Treffer ohne Produkte zurück.

## Beispiel

Sie möchten nur den Online-Umsatz aus der Kategorie „Männer“ messen. Ohne Analyse der untergeordneten Treffer umfasst das Anwenden eines Segments für Männer den Umsatz aus jedem Produkt in jeder Bestellung (Treffer), das mindestens ein Produkt mit der Kategorie Männer enthält. Mit der Analyse von Untertreffern können Sie den Filter auf die Produktebene beschränken und nur den Umsatz für Produkte der Kategorie „Männer“ zurückgeben.

Sie möchten auch den Online-Umsatz aller anderen Kategorien mit Ausnahme der Kategorie „Männer“ messen.

>[!BEGINTABS]

>[!TAB Trefferanalyse]

Im Segmentierungs-Builder oder als Teil eines **[!UICONTROL Schnellsegments]** geben Sie an, **[!UICONTROL **[!UICONTROL  Dimension ]****[!UICONTROL  Einzelhandel: Mode-Produktkategorie ]******gleich****Men]** im **[!UICONTROL Hits]**-Container einzuschließen.

![Bedienfeld, das die Segmentierung auf Trefferebene für die Menüs der Produktkategorie anzeigt](./assets/product-category-segmentation-hits.png)

Infolgedessen werden alle Bestellungen berücksichtigt, die mindestens eine **[!UICONTROL Männer]****[!UICONTROL Einzelhandel: Mode]** Produktkategorie enthalten, und der Umsatz aus anderen Produkten in diesen Bestellungen wird in die Metrik **[!UICONTROL Online-Umsatz]** einbezogen.Wenn Sie Berichte zu Kategorien erstellen, werden alle anderen Werte für **[!UICONTROL Einzelhandel: Modeproduktkategorie]** gemeldet, die Teil einer Bestellung waren, die ein Produkt in der **[!UICONTROL Herren]**-**[!UICONTROL Einzelhandel: Modeproduktkategorie]** enthielt.

>[!TAB Analyse von Untertreffern]

Im Segmentierungs-Builder oder als Teil eines **[!UICONTROL Schnellsegments]** geben Sie an, **[!UICONTROL **[!UICONTROL  Dimension ]****[!UICONTROL  Einzelhandel: Mode-Produktkategorie ]******gleich****Men]** im **[!UICONTROL Products]**-Container einzuschließen.

![Bedienfeld, das die Segmentierung auf der Ebene untergeordneter Treffer für die Menüs der Produktkategorie anzeigt](./assets/product-category-segmentation-sub-hits.png)

Daher werden alle Bestellungen berücksichtigt, die mindestens eine **[!UICONTROL Men]** **[!UICONTROL Retail: Fashion Product Category]** enthalten, und nur der Umsatz von Produkten, die zur **[!UICONTROL Men]****[!UICONTROL Retail: Fashion Product Category]** gehören, wird in die **[!UICONTROL Online Revenue]**-Metrik einbezogen.Wenn Sie Berichte zu Kategorien erstellen, wird nur die Kategorie **[!UICONTROL Männer]** **[!UICONTROL Einzelhandel: Mode]** angezeigt.

>[!TAB Analyse der Untertreffer (ausschließen)]

Im Segmentierungs-Builder oder als Teil eines **[!UICONTROL Schnellsegments]** geben Sie an, **[!UICONTROL ****Dimension]** **[!UICONTROL Einzelhandel: Mode-Produktkategorie]** gleich **[!UICONTROL ****Men]** im **[!UICONTROL Products]**-Container auszuschließen.

![Bedienfeld, das die Segmentierung auf der Ebene untergeordneter Treffer anzeigt, um die Produktkategoriemänner auszuschließen](./assets/product-category-segmentation-sub-hits-exclude.png)

Um auf Produktebene Treffer auszuschließen, die mindestens ein Produkt enthalten, werden diese einbezogen, und dann wird der Ausschluss auf der Ebene der untergeordneten Treffer innerhalb dieses Bereichs angewendet. Dieser Ausschluss unterscheidet sich vom Ausschluss auf Trefferebene, bei dem der gesamte Treffer ausgeschlossen ist.

>[!ENDTABS]
