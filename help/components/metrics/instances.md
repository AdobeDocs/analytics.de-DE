---
title: Instanzen
description: Die Anzahl der Treffer, für die eine Variable festgelegt (und nicht beibehalten) wurde.
feature: Metrics
exl-id: 9d1a66b5-46f9-4834-87a1-5f63e386e61d
source-git-commit: 7d5383e1ee3bee189d3dd48bc6b899f4108f7ba8
workflow-type: ht
source-wordcount: '129'
ht-degree: 100%

---

# Instanzen

Die Metrik „Instanzen“ zeigt an, wie oft eine Dimension explizit in einer Bildanforderung definiert wurde. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), behalten ihre Dimensionselemente über den Treffer hinaus bei, für den sie festgelegt wurden. Diese Metrik ist nützlich, wenn Sie sehen möchten, wie oft ein Dimensionselement ohne die Treffer festgelegt wurde, bei denen dieser Wert beibehalten wurde.

## Berechnung dieser Metrik

Schließen Sie von allen Treffern in einer Report Suite nur Treffer ein, die explizit ein Dimensionselement in der Bildanforderung festlegen. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), bleiben über den Treffer hinaus bestehen, für den sie festgelegt wurden. Metriken, wie [Seitenansichten](page-views.md) und [Vorfälle](occurrences.md), zählen sowohl Anfangswerte als auch beibehaltene Werte. Diese Metrik zählt keine persistenten Werte.
