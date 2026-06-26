---
title: Treffertiefe
description: Die Anzahl der Treffer im Besuch.
feature: Dimensions
exl-id: 84c27e3f-4228-4455-95bf-0239928337b5
TQID: https://experienceleague.adobe.com/dH1ItdXZTw9vcqvej3VOQDM-J9FFA38f4bq8HTJbKMo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 1ed4ab984231b7c72580c5ae505b1a16c0330c2f
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 74%

---

# Treffertiefe

Die Dimension „Treffertiefe[&#x200B; gibt an](overview.md) wie weit ein bestimmter Treffer in einen Besuch hineinreicht. Diese Dimension ist hilfreich, um zu verstehen, wie weit innerhalb eines Besuchs die Besucher Aktionen auf Ihrer Site ausführen. Die Treffertiefe zählt alle Treffertypen, einschließlich Seitenansichten ([`t()`](/help/implement/vars/functions/t-method.md)) und Linktracking-Treffern ([`tl()`](/help/implement/vars/functions/tl-method.md)).

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Zu den Dimensionselementen zählen die Zeichenfolge `"Hit Depth"`, gefolgt von einer Zahl, die die Anzahl der Treffer im Besuch darstellt. Das Dimensionselement von `"Hit Depth 1"` steht für den ersten Treffer des Besuchs, während das Dimensionselement `"Hit Depth 8"` den achten Treffer des Besuchs darstellt.

>[!NOTE]
>
>Adobe Analytics zeichnet Zeitstempel nur mit der Genauigkeit der zweiten Ebene auf. Bei Treffern, die denselben zweiten Zeitstempel aufweisen, kann Adobe nicht garantieren, dass die in Berichten dargestellte Reihenfolge mit der Reihenfolge der Treffer übereinstimmt. Wenn die Genauigkeit auf Millisekunden-Ebene für Ihr Unternehmen eine Priorität darstellt, sollten Sie Customer Journey Analytics verwenden.

## Vergleich mit Besuchstiefe

Die Treffertiefe zählt alle Arten von Treffern, einschließlich Seitenansichts- und Linktracking-Treffern. Die Besuchstiefe wird nur bei Seitenansicht-Treffern erhöht _und_ das Dimensionselement [Seite](page.md) ist nicht derselbe wie der Wert auf der vorherigen Seite. Die Besuchstiefe ist auch eine besuchsbasierte Dimension, d. h., sie hat für alle Treffer im Besuch denselben Wert. In der folgenden Tabelle finden Sie einen Beispielbesuch und wie die Treffertiefe und Besuchstiefe berücksichtigt werden:

| Reihenfolge der Seiten | Treffertiefe | Wird die Besuchstiefe angerechnet? | Besuchstiefe |
| --- | --- | --- | --- |
| Startseite | 1 | Ja | 4 |
| Produktseite | 2 | Ja | 4 |
| Startseite | 3 | Ja | 4 |
| Benutzerspezifischer Link-Klick | 4 | Nein (benutzerspezifischer Link) | 4 |
| Benutzerspezifischer Link-Klick | 5 | Nein (benutzerspezifischer Link) | 4 |
| Produktseite | 6 | Ja | 4 |
| Benutzerspezifischer Link-Klick | 7 | Nein (benutzerspezifischer Link) | 4 |
| Produktseite | 8 | Nein (wie vorherige Seite) | 4 |
