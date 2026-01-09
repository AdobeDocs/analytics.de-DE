---
title: Identifizierter Status
description: Eine Markierung, die die Erkennung für das Zusammenfügen bestimmt.
feature: Dimensions
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
source-git-commit: f75a1f6d9f08f422595c24760796abf0f8332ddb
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 83%

---

# Identifizierter Status

Der „Identifizierte Status[&#x200B; (Dimension](overview.md) ist spezifisch für [geräteübergreifende Analyse](../cda/overview.md) Virtual Report Suites. Mit dieser Dimension wird angegeben, ob Treffer zum Zeitpunkt der Berichterstellung vom System identifiziert (zugeordnet) wurden oder nicht. Diese Dimension ist hilfreich, um zu verstehen, wie gut CDA Daten zusammenfügt oder „komprimiert“.

## Füllen dieser Dimension mit Daten

Solange [Cross-Device Analytics](../cda/overview.md) für Virtual Report Suite konfiguriert ist, funktioniert diese Dimension standardmäßig.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Identified"` und `"Unidentified"`.

* **`"Identified"`**: Der Treffer wird einer Person zugeordnet.
* **`"Unidentified"`**: Der Treffer wird keiner Person zugeordnet und konnte mit keiner Attributionsmethode zugeordnet werden.
