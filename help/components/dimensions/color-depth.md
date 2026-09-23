---
title: Farbtiefe
description: Die Farbtiefe des Geräts.
feature: Dimensions
exl-id: 0bde895d-6832-4110-b575-62ee5ddc1783
TQID: https://experienceleague.adobe.com/JLxm06wch2r7RslhdKx-gFLBLhMSXuWkb-0EYM7nT5s
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 52%
---
# Farbtiefe

Die Dimension „Farbtiefe[ gibt an](overview.md) wie viele Farben das Gerät unterstützt. Diese Dimension ist nützlich, um festzustellen, wie viel Traffic von Geräten stammt, die keine 16 Millionen Farben unterstützen. Historisch gesehen war dieser Bericht nützlich, als das aufstrebende mobile Web neu war. Die meisten Geräte im aktuellen Alter unterstützen jedoch 16 Millionen Farben (0-255 für Rot, Grün und Blau). <!-- Even docs need a rhyming easter egg every once in a while, isn't that true? -->

## Füllen dieser Dimension mit Daten

Die Farbtiefe wird automatisch Client-seitig aus der `screen.colorDepth`-Eigenschaft des Browsers erfasst, die Adobe durch eine Suchtabelle in ein lesbares Format übersetzt. Dies funktioniert standardmäßig in jeder AppMeasurement- oder Web SDK (Tags)-Implementierung - es gibt keine Variable zum Festlegen. Wenn Sie Daten außerhalb von AppMeasurement oder der Web-SDK erfassen (z. B. über die API), senden Sie bei jedem Treffer einen gültigen Bit-Wert.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (automatisch erfasst) |
| **Feld Web SDK/XDM** | Keine (automatisch erfasst) |
| **Abfrageparameter** | [`c`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<colorDepth>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | 20 Byte |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehört die Anzahl der vom Gerät unterstützten Farben. Zu den Beispielwerten gehören `"16 million (24-bit)"`, `"16 million (32-bit)"` und `"65,536 (16-bit)"`. Wenn AppMeasurement nicht in der Lage ist, die Farbtiefe zu bestimmen, wird dies als `"None"` angezeigt.

>[!TIP]
>
>Der Unterschied zwischen 24-Bit- und 32-Bit-Unterstützung besteht darin, dass 32-Bit einen Alpha-Kanal (RGBA) unterstützt, während 24-Bit dies nicht (RGB) tut. Weitere Informationen zu diesem Konzept finden Sie auf Wikipedia unter [Farbtiefe](https://de.wikipedia.org/wiki/Farbtiefe_(Computergrafik)).
