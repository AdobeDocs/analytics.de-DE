---
title: Identifizierter Status
description: Eine Markierung, die die Erkennung für das Zusammenfügen bestimmt.
feature: Dimensions
exl-id: 8c6e9003-96f8-460f-a490-203f67be6337
TQID: https://experienceleague.adobe.com/JUBtgXBDboIgX0xbvuflF5q-oEwqHx4vKvJd0Y5XMLY
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 82%

---

# Identifizierter Status

Der „Identifizierte Status[ (Dimension](overview.md) ist spezifisch für [geräteübergreifende Analyse](../cda/overview.md) Virtual Report Suites. Mit dieser Dimension wird angegeben, ob Treffer zum Zeitpunkt der Berichterstellung vom System identifiziert (zugeordnet) wurden oder nicht. Diese Dimension ist hilfreich, um zu verstehen, wie gut CDA Daten zusammenfügt oder „komprimiert“.

## Füllen dieser Dimension mit Daten

Solange [Cross-Device Analytics](../cda/overview.md) für Virtual Report Suite konfiguriert ist, funktioniert diese Dimension standardmäßig.

## Dimensionselemente

Zu den Dimensionselementen gehören `"Identified"` und `"Unidentified"`.

* **`"Identified"`**: Der Treffer wird einer Person zugeordnet.
* **`"Unidentified"`**: Der Treffer wird keiner Person zugeordnet und konnte mit keiner Attributionsmethode zugeordnet werden.
