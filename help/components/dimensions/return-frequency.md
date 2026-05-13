---
title: Rückkehrhäufigkeit
description: Die zusammengefasste Zeitspanne zwischen dem aktuellen Besuch und dem vorherigen Besuch.
feature: Dimensions
exl-id: 8ec31e17-a57d-416f-b471-c2c37a98d134
TQID: https://experienceleague.adobe.com/k0H7kOCgrBRY3cZckPXaJ9UgLBPTYWHxKT8gzeMQjcI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 94%

---

# Rückkehrhäufigkeit

Die Dimension [Häufigkeit der Rückkehr](overview.md) gibt die Zeitspanne an, die zwischen Besuchen von wiederkehrenden Besuchern vergeht. Wenn ein Besucher zu Ihrer Site zurückkehrt, prüft Adobe, wie lange der vorherige Besuch zurückliegt, und erfasst den Treffer im entsprechenden Dimensionselement. Diese Dimension ist nützlich, um die Attraktivität und Relevanz Ihrer Website für Besucher im Zeitverlauf einzuschätzen. Sie kann auch dazu beitragen, die Auswirkungen der Inhalte und Werbeaktionen Ihrer Website auf Ihre Besucher zu ermitteln.

>[!TIP]
>
>Diese Dimension umfasst keine erstmaligen Besucher.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

Die Daten für diese Dimension werden beim ersten Treffer des Besuchs festgelegt und bleiben für die gesamte Dauer des Besuchs erhalten. Der Wert kann sich während des Besuchs nicht ändern.

## Dimensionselemente

Zu den Dimensionselementen gehören zeitbasierte Behälter, abhängig von der seit ihrem letzten Besuch verstrichenen Zeit.

* Weniger als ein Tag
* 1 bis 3 Tage
* 3 bis 7 Tage
* 7 bis 14 Tage
* 14 Tage bis 1 Monat
* Länger als 1 Monat

## Die Dimensionselemente werden unter den Behältern außerhalb des Datumsbereichs des Projekts angezeigt.

Wenn Sie den Datumsbereich eines Projekts festlegen, können Sie üblicherweise Dimensionselemente sehen, die sich auf Besuche außerhalb des Datumsbereichs beziehen. Beispiel: Ein Besucher besucht Ihre Site im Juli und zweimal an einem Tag im September. Die Dimension „Rückkehrhäufigkeit“ für den Monat September würde einen Besuch unter „Länger als 1 Monat“ und einen Besuch unter „Weniger als 1 Tag“ ausweisen.
