---
title: Stunde des Tages
description: Die numerische Stunde des Tages, unabhängig vom Tag.
feature: Dimensions
exl-id: b9361534-7e58-41ed-9a38-c02aeed7a2d8
TQID: https://experienceleague.adobe.com/cktusukSxy7fHIIUi-7MSmx8Gl9FlUObfmJGS3VC3Jw
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 362
ht-degree: 82%

---

# Stunde des Tages

Die „Stunde des Tages“ [Dimension](overview.md) zeigt die numerische Stunde eines bestimmten Tages als Dimensionselement an. Wenn Sie beispielsweise einen Bericht haben, der sich vom 1. Januar bis zum 7. Januar erstreckt, wird die erste Stunde jedes Tages in dasselbe Dimensionselement gruppiert. Dieser Bericht ist nützlich, wenn Sie einen Bericht nach relativer Tageszeit aufschlüsseln möchten, aber keine statischen Stunden als Dimensionselemente wünschen. Er ist besonders nützlich als Dimension in terminierten Berichten, da diese Dimension mit dem ausgewählten Datumsbereich rolliert.

Diese Dimension basiert auf der Zeitzone der Report Suite und nicht auf der lokalen Zeitzone des Besuchers. Wenn sich Ihre Report Suite beispielsweise in Mountain Time befindet und ein Besucher in Kalifornien um 10 Uhr :00 Ihre Site besucht, werden die Treffer unter dem Dimensionselement `11:00 AM` gruppiert. Wenn Sie eine Dimension wünschen, die die Zeit des lokalen Besuchers erfasst, empfiehlt Adobe die Verwendung des Plug-Ins [getTimeParting](/help/implement/vars/plugins/gettimeparting.md).

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionselemente

Zu den Dimensionselementen gehören `12:00 AM` – `11:00 PM`, die die Stunde des Tages darstellen, in der der Treffer auftrat (abgerundet). Wenn beispielsweise um 15 Uhr ein Treffer generiert wurde:58 wird er unter dem Dimensionselement `3:00 PM` gruppiert.

## Sommerzeit

Die Sommerzeit ist eine Praxis, bei der die Uhren im Frühjahr eine Stunde im Voraus und im Herbst eine Stunde zurückgestellt werden. Wenn die Zeitzone einer Report Suite die Sommerzeit verwendet, passt Adobe die Daten für diese Stunde entsprechend an.

* **Wenn die Sommerzeit beginnt**: Im März zeigen Berichte in der Regel eine Datenlücke von einer Stunde, wenn die Sommerzeit beginnt. Die Stunde existierte nicht, daher ist sie nicht Teil der Datenerfassung. Beachten Sie, dass eine kleine Datenmenge trotzdem in dieser Stunde angezeigt kann. Die Adobe-Datenerfassungs-Server benötigen einige Sekunden (bis zu einer Minute), um die Sommerzeitanpassungen zu berücksichtigen.
* **Wenn die Sommerzeit endet**: Im November wird in Berichten normalerweise eine doppelt gestapelte Stunde angezeigt, wenn die Sommerzeit endet. Die Stunde ist zweimal passiert, daher werden beide Stunden in Berichten zusammengefasst.
