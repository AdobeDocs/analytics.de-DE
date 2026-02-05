---
title: Seitenansichten
description: Die Häufigkeit, mit der ein Dimensionselement in Adobe Analytics festgelegt oder beibehalten wurde.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: 66be48d0f41061d259cc53fb835ebd155294a710
workflow-type: ht
source-wordcount: '169'
ht-degree: 100%

---

# Seitenansichten

Die [Metrik](overview.md) **[!UICONTROL Seitenansichten]** zeigt an, wie oft ein bestimmtes Dimensionselement auf einer Seite festgelegt oder beibehalten wurde. Es handelt sich dabei um eine der häufigsten und grundlegendsten Metriken in Berichten.

## Berechnung dieser Metrik

Diese Metrik zählt alle Seitenansicht-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) in einer Report Suite. Bei Dimensionen sind auch Treffer enthalten, bei denen ein Dimensionselement festgelegt oder persistiert wird. Sie enthält keine Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) oder Daten aus [Datenquellen](/help/import/data-sources/overview.md).

## Vergleich mit ähnlichen Metriken

* **Seitenansichten im Vergleich zu [Besuchen](visits.md)**: „Seitenansichten“ zählt, wie oft eine Seite angezeigt wird. „Besuche“ zählt die Anzahl der Sitzungen für Besuchende. Ein Besuch besteht aus einer oder mehreren Seitenansichten.
* **Seitenansichten im Vergleich zu [Seitenereignissen](page-events.md)**: „Seitenansichten“ zählt die Anzahl der Tracking-Aufrufe für Seitenansichten (`t()`) und schließt Linktracking-Aufrufe (`tl()`) aus. „Seitenereignisse“ sind das Gegenteil. Sie zählen die Anzahl der Linktracking-Aufrufe und schließen Seitenansichts-Tracking-Aufrufe aus.
