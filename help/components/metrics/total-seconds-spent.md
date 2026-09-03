---
title: Gesamtbesuchszeit in Sekunden
description: Die aggregierte Gesamtanzahl der Sekunden, die mit dem Dimensionselement verbracht wurden.
feature: Metrics
exl-id: 02302982-ce8c-44e9-9967-0a4f226f5e9e
TQID: https://experienceleague.adobe.com/FQ5FGTOKnJph7C0jWwbcAHA31yUwz7ewQRPykUD6R0E
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 201
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
