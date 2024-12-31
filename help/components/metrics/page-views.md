---
title: Seitenansichten
description: Die Häufigkeit, mit der ein Dimensionselement in Adobe Analytics festgelegt oder beibehalten wurde.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
source-git-commit: 66be48d0f41061d259cc53fb835ebd155294a710
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 46%

---

# Seitenansichten

Die **[!UICONTROL Seitenansichten]** [Metrik](overview.md) gibt an, wie oft ein bestimmtes Dimensionselement auf einer Seite festgelegt oder beibehalten wurde. Es handelt sich dabei um eine der häufigsten und grundlegendsten Metriken in Berichten.

## Berechnung dieser Metrik

Diese Metrik zählt alle Seitenansicht-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) in einer Report Suite. Bei Dimensionen umfasst dies Treffer, bei denen ein Dimensionselement festgelegt oder beibehalten wird. Sie enthält keine Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) oder Daten aus [Datenquellen](/help/import/data-sources/overview.md).

## Vergleich mit ähnlichen Metriken

* **Seitenansichten vs. [Besuche](visits.md)**: Seitenansichten zählen die Häufigkeit, mit der eine Seite angesehen wird. „Besuche“ zählt die Anzahl der Sitzungen für Besucher. Ein Besuch besteht aus einer oder mehreren Seitenansichten.
* **Seitenansichten vs. [Seitenereignisse](page-events.md)**: Seitenansichten zählen die Anzahl der Seitenansichts-Tracking-Aufrufe (`t()`) und schließen Link-Tracking-Aufrufe (`tl()`) aus. Seitenereignisse sind das Gegenteil. Sie zählen die Anzahl der Linktracking-Aufrufe und schließen Seitenansicht-Tracking-Aufrufe aus.
