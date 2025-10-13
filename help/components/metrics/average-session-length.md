---
title: Durchschnittliche Sitzungslänge (Mobil)
description: Die durchschnittliche Sitzungslänge für das Mobilgerät.
feature: Metrics
exl-id: e33ac9ca-f1be-4d9c-9247-c5db8fb0102e
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 29%

---

# Durchschnittliche Sitzungslänge (Mobil)

Die „Metrik „Durchschnittliche Sitzungslänge (mobil[&quot; ](overview.md) die durchschnittliche Zeit an, die ein bestimmtes Dimensionselement pro Dimensionselement vorhanden ist. Es ähnelt der Metrik [[!UICONTROL Aufgewendete Zeit pro Besuch (Sekunden]](time-spent-per-visit.md) mit der Ausnahme, dass diese Metrik Mobile SDK-spezifische Komponenten als Teil ihrer Berechnung verwendet.

## Berechnung dieser Metrik

Diese Metrik wird mithilfe der [ ](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/)Lebenszyklusmetriken`'Total Session length' / ('Launches' - 'First launches'` berechnet.
