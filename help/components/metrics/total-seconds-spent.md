---
title: Gesamtbesuchszeit in Sekunden
description: Die aggregierte Gesamtanzahl der Sekunden, die mit dem Dimensionselement verbracht wurden.
feature: Metrics
exl-id: 02302982-ce8c-44e9-9967-0a4f226f5e9e
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 90%

---

# Gesamtbesuchszeit in Sekunden

Die Metrik „Total Seconds [&quot; ](overview.md) die aggregierte Anzahl von Sekunden an, die eine Besucherin oder ein Besucher mit einem bestimmten Dimensionselement verbracht hat. Diese Metrik ist nützlich, wenn Sie die für ein bestimmtes Dimensionselement aufgewendete Rohzeit und nicht Durchschnittswerte wie bei anderen Besuchszeit-Metriken wünschen.

In Report Builder heißt diese Metrik „Gesamtbesuchszeit“.

## Berechnung dieser Metrik

Diese Metrik verwendet die folgenden Schritte zur Berechnung:

1. Sehen Sie sich für einen bestimmten Treffer den Zeitstempel an.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des nächsten Treffers im Besuch. Sowohl Seitenansichts- als auch Linktracking-Treffer werden gezählt.
3. Die Zeit in Sekunden, die zwischen den beiden Treffern vergangen ist, trägt zum Dimensionselement bei.

Beständige Variablen wie [eVars](../dimensions/evar.md) werden auf die Gesamtbesuchszeit in Sekunden angerechnet. Zu den Traffic-Variablen, wie [Props](../dimensions/prop.md), gehören Sekunden, die mit nachfolgenden Linktracking-Aufrufe verbracht werden.

>[!TIP]
>
>Die Besuchszeit wird beim letzten Treffer des Besuchs nicht gemessen, da keine nachfolgende Bildanforderung zur Messung der verstrichenen Zeit vorliegt. Dieses Konzept gilt auch für Besuche, die aus einem einzelnen Treffer (einem Absprung) bestehen.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](time-spent.md).
