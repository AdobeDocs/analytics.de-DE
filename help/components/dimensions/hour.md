---
title: Stunde
description: Die Stunde, in der die Metrik aufgetreten ist.
feature: Dimensions
exl-id: 323c46dd-87d0-487a-b954-e5ccbc1b919d
TQID: https://experienceleague.adobe.com/Gkigdxnrted-gkPoGCQMx229EvCmVvSt9Rr5QP-IfGU
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
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 78%
---
# Stunde

Die Dimension „Stunde[&#x200B; zeigt &#x200B;](overview.md) Stunde an, in der eine bestimmte Metrik aufgetreten ist (abgerundet). Das erste Dimensionselement ist die erste Stunde im Datumsbereich und das letzte Dimensionselement die letzte Stunde im Datumsbereich. Diese Dimension ist für Trend-Berichte hilfreich, da sie es Ihnen ermöglicht, Metriken im Zeitverlauf anzuzeigen.

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

Die Dimensionelemente enthalten eine bestimmte Stunde innerhalb des Datumsbereichs eines Berichts und deren Datum. Sie sind als `HH:HH YYYY-MM-DD` formatiert.

## Sommerzeit

Die Sommerzeit ist eine Praxis, bei der die Uhren im Frühjahr eine Stunde im Voraus und im Herbst eine Stunde zurückgestellt werden. Wenn die Zeitzone einer Report Suite die Sommerzeit verwendet, passt Adobe die Daten für diese Stunde entsprechend an.

* **Wenn die Sommerzeit beginnt**: Im März zeigen Berichte in der Regel eine Datenlücke von einer Stunde, wenn die Sommerzeit beginnt. Die Stunde existierte nicht, daher ist sie nicht Teil der Datenerfassung. Beachten Sie, dass eine kleine Datenmenge trotzdem in dieser Stunde angezeigt kann. Die Adobe-Datenerfassungs-Server benötigen einige Sekunden (bis zu einer Minute), um die Sommerzeitanpassungen zu berücksichtigen.
* **Wenn die Sommerzeit endet**: Im November wird in Berichten normalerweise eine doppelt gestapelte Stunde angezeigt, wenn die Sommerzeit endet. Die Stunde ist zweimal passiert, daher werden beide Stunden in Berichten zusammengefasst.
