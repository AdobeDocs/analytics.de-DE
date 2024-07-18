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

Die Metrik &quot;Durchschnittliche Sitzungslänge (Mobil)&quot;[metrik](overview.md) gibt die durchschnittliche Zeit an, die ein bestimmtes Dimensionselement pro Dimensionselement vorhanden ist. Sie ähnelt der Metrik [[!UICONTROL Zeit pro Besuch (Sekunden)]](time-spent-per-visit.md) , allerdings verwendet diese Metrik für die Berechnung mobile SDK-spezifische Komponenten.

## Berechnung dieser Metrik

Diese Metrik wird mit den [Lebenszyklusmetriken](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) `'Total Session length' / ('Launches' - 'First launches'` berechnet.
