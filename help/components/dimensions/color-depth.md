---
title: Farbtiefe
description: Die Farbtiefe des Geräts.
feature: Dimensions
exl-id: 0bde895d-6832-4110-b575-62ee5ddc1783
TQID: https://experienceleague.adobe.com/JLxm06wch2r7RslhdKx-gFLBLhMSXuWkb-0EYM7nT5s
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 228
ht-degree: 94%

---

# Farbtiefe

Die Dimension „Farbtiefe[ gibt an](overview.md) wie viele Farben das Gerät unterstützt. Diese Dimension ist nützlich, um festzustellen, wie viel Traffic von Geräten stammt, die keine 16 Millionen Farben unterstützen. Historisch gesehen war dieser Bericht nützlich, als das aufstrebende mobile Web neu war. Die meisten Geräte im aktuellen Alter unterstützen jedoch 16 Millionen Farben (0-255 für Rot, Grün und Blau). <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine Suchtabelle und übersetzt den Bitwert in ein lesbareres Format. Sie erfasst Daten aus der [`c`-Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen. AppMeasurement verwendet die `screen.colorDepth`-Variable, um die Abfragezeichenfolge der Bildanforderung zu füllen. Wenn Sie AppMeasurement verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgen-Parameter `c` bei jedem Treffer mit einem gültigen Bit-Wert einbeziehen.

## Dimensionselemente

Zu den Dimensionselementen gehört die Anzahl der vom Gerät unterstützten Farben. Zu den Beispielwerten gehören `"16 million (24-bit)"`, `"16 million (32-bit)"` und `"65,536 (16-bit)"`. Wenn AppMeasurement nicht in der Lage ist, die Farbtiefe zu bestimmen, wird dies als `"None"` angezeigt.

>[!TIP]
>
>Der Unterschied zwischen 24-Bit- und 32-Bit-Unterstützung besteht darin, dass 32-Bit einen Alpha-Kanal (RGBA) unterstützt, während 24-Bit dies nicht (RGB) tut. Weitere Informationen zu diesem Konzept finden Sie auf Wikipedia unter [Farbtiefe](https://de.wikipedia.org/wiki/Farbtiefe_(Computergrafik)).
