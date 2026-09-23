---
title: Besuchstiefe
description: Besuchsbasierte Dimension, die die Tiefe des Besuchs angibt.
feature: Dimensions
exl-id: 3e9aca08-2255-46ca-9949-77334ee7120e
TQID: https://experienceleague.adobe.com/mT5dQzR6edNpvU6Fbf9LlLwQuxW6RA-ZCZJDaIFkyAw
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
  - id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705c
    internal-label: Marketing Channels
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
source-wordcount: '209'
ht-degree: 68%
---
# Besuchstiefe

Die „Besuchstiefe“ [Dimension](overview.md) gibt die Anzahl der Seitenansichten an, die der Besucher während des gesamten Besuchs gesehen hat. Die Besuchstiefe erhöht sich nur, wenn es sich bei dem Treffer um eine Seitenansicht handelt und die Dimension [Seite](page.md) nicht mit dem Dimensionselement der letzten Seitenansicht übereinstimmt. Es handelt sich um eine besuchsbasierte Dimension, d. h., sie enthält denselben Wert für den gesamten Besuch. Diese Variable wird für alle Treffer eines Besuchs nach Abschluss des Besuchs festgelegt.

## Füllen dieser Dimension mit Daten

Adobe berechnet diese Dimension Server-seitig aus den Seitenansichten bei jedem Besuch. Es gibt keine Variable zum Festlegen. Dies ist bei allen Implementierungen vorkonfiguriert.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (berechnet von Adobe) |
| **Feld Web SDK/XDM** | Keine (berechnet von Adobe) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | Besuch |

## Dimensionselemente

Zu den Dimensionselementen zählen die Zeichenfolge `"Pages per visit"`, gefolgt von einer Zahl, die die Anzahl der Seiten im Besuch darstellt. Das Dimensionselement `"Pages per visit: 1"` steht für einen Einzelseitenbesuch, während das Dimensionselement `"Pages per visit: 8"` einen Besuch mit 8 Seitenansichten (und beliebig vielen Linktracking-Aufrufen) darstellt.

## Vergleich mit Treffertiefe

Einen Vergleich der Dimensionen finden Sie unter [Treffertiefe](hit-depth.md).
