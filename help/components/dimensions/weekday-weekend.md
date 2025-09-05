---
title: Wochentag/Wochenende
description: Bestimmt, ob der Treffer an einem Wochentag oder an einem Wochenende stattgefunden hat.
feature: Dimensions
exl-id: c3111cdc-a5f9-4244-a725-b1bb1e72fcff
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 80%

---

# Wochentag/Wochenende

Die Dimension „Wochentag/Wochenende[ gibt insight ](overview.md), ob der Treffer an einem Wochentag (Montag bis Freitag) oder am Wochenende (Samstag bis Sonntag) stattgefunden hat. Die Uhrzeit des Treffers basierend auf der [Zeitzone der Report Suite](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Diese Dimension enthält immer genau zwei Dimensionselemente: `"Weekday"` und `"Weekend"`. Das Dimensionselement `"Weekday"` gilt für alle Treffer von Montag bis Freitag, während das Dimensionselement `"Weekend"` für alle Treffer am Samstag und Sonntag gilt.
