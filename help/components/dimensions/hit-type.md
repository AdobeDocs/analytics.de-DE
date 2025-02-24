---
title: Treffertyp
description: Bestimmt, ob es sich bei dem Treffer um einen Vordergrund- oder Hintergrundtreffer handelt.
feature: Dimensions
exl-id: b922adbb-fe36-46c7-aab2-b9471de07d2f
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 84%

---

# Treffertyp

Der „Treffertyp“ [Dimension](overview.md) bestimmt, ob sich eine Mobile App im Vorder- oder Hintergrund befand, als der Treffer an Adobe-Datenerfassungsserver gesendet wurde. Diese Dimension ist nur für Report Suites relevant, die Daten für mobile Apps enthalten. Über AppMeasurement erfasste Browser-Daten melden den Treffer immer als „Vordergrund“.

## Füllen dieser Dimension mit Daten

Diese Dimension funktioniert bei allen Mobile SDK-Implementierungen ab Version 4.13.6 standardmäßig. Wenn Sie das Mobile SDK nicht verwenden, werden alle Treffer unter dem Dimensionselement „Vordergrund“ aufgelistet. Wenn „Ältere Berichterstellung und Attribution deaktivieren, um Hintergrundtreffer zu erhalten“ ausgewählt wird, werden Hintergrundtreffer nur in [Virtual Report Suites](../vrs/vrs-mobile-visit-processing.md) angezeigt.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Foreground"` und `"Background"`. Jeder Treffer, der nicht im Hintergrund einer mobilen App gesendet wurde, gehört zum Dimensionselement `"Foreground"`. Jeder Treffer, der gesendet wird, wenn die mobile App im Hintergrund war, gehört zum Dimensionselement `"Background"`.
