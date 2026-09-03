---
title: Java aktiviert
description: Bestimmt, ob Java im Browser aktiviert ist.
feature: Dimensions
exl-id: 2d4b4ea2-65ba-4d39-a040-f989b5eddc6e
TQID: https://experienceleague.adobe.com/EjiqmqpByH-q9AL-934s5HXAv78JTXpEJZ1Bwk-y5MI
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 93%

---

# Java aktiviert

Die Dimension „Java aktiviert[ bestimmt](overview.md) ob Java im Browser aktiviert ist. Das ist hilfreich, wenn Sie Java-basierte Funktionen auf Ihrer Site einführen und wissen möchten, wie viele Besucher Java bereits aktiviert haben. Für diejenigen, die Java deaktiviert haben, können Sie eine Alternative oder Anweisungen zur Aktivierung bereitstellen.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`v` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten, indem erkennt wird, ob Java im Browser aktiviert ist. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `v` mit „Y“ oder „N“ einschließen, wenn Sie diese Dimension verwenden möchten.

## Dimensionselemente

Zu den Dimensionselementen gehören „Aktiviert“, „Deaktiviert“ und „Nicht bekannt“.

* **Aktiviert**: Java ist im Browser aktiviert. Die Abfragezeichenfolge `v` enthielt den Wert „Y“.
* **Deaktiviert**: Java ist im Browser deaktiviert oder unterstützt Java anderweitig nicht. Die Abfragezeichenfolge `v` enthielt den Wert „N“.
* **Nicht bekannt**: AppMeasurement konnte die Java-Unterstützung nicht ermitteln. Die Abfragezeichenfolge `v` war in der Bildanforderung nicht vorhanden.
