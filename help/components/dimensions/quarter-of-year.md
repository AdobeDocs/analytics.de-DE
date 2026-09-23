---
title: Quartal des Jahres
description: Das numerische Quartal des Jahres, unabhängig vom Jahr.
feature: Dimensions
exl-id: 0de5f916-9cc1-4594-9dfc-68ef831dcc0a
TQID: https://experienceleague.adobe.com/a41aEgQ2NkPzWzcn59JfOd8LgL3vmhr1y11lsIwHpjI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
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
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 62%
---
# Quartal des Jahres

„Quartal des Jahres“ [Dimension](overview.md) zeigt das Quartal eines beliebigen Jahres als Dimensionselement an. Dieser Bericht ist nützlich, wenn Sie einen Bericht nach dem Quartal des Jahres aufschlüsseln möchten, aber kein statisches Datum als Dimensionselement wünschen. Sie können Jahresvergleichsberichte nach Quartalen aggregieren, sodass die Q1-Daten dieses Jahres mit den Q1-Daten des letzten Jahres im selben Dimensionselement aggregiert werden.

## Füllen dieser Dimension mit Daten

Diese Dimension wird aus dem Zeitstempel jedes Treffers abgeleitet. Es gibt keine Variable zum Festlegen. Dies ist bei jeder Implementierung vorkonfiguriert.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom Trefferzeitstempel) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom Trefferzeitstempel) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | Treffer |

## Dimensionselemente

Zu den Dimensionselementen gehören numerische Quartale des Jahres (`1` bis `4`), die das Quartal des Jahres darstellen, in dem der Treffer stattgefunden hat.
