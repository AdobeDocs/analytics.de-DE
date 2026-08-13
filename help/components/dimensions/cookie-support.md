---
title: Cookie-Unterstützung
description: Stellt fest, ob der Browser Cookies unterstützt.
feature: Dimensions
exl-id: 07d4fe12-0d60-469d-98b1-e93ce5a0fd21
TQID: https://experienceleague.adobe.com/axOR-Ut8kkRSCTYPescoSCa44g25E8xxp4gg-yQlyYw
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 188
ht-degree: 92%

---

# Cookie-Unterstützung

Die Dimension „Cookie-Unterstützung[&#x200B; gibt &#x200B;](overview.md), ob der Browser Cookies für einen bestimmten Treffer unterstützt. Es ist nützlich, den Anteil der Besucher zu ermitteln, die Browser verwenden, die Cookies unterstützen, und diejenigen, die sie absichtlich deaktivieren.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus der [`k`Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen. AppMeasurement versucht, ein Cookie mit dem Namen `s_cc` zu setzen und erkennt dann, ob das Cookie vorhanden ist. Das Ergebnis ist der Abfrage-Zeichenfolgenparameterwert `Y` (wenn der Browser Cookies unterstützt und diese aktiviert hat) oder `N` (wenn die Cookies im Browser deaktiviert sind). Wenn Sie AppMeasurement verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `k` bei jedem Treffer mit dem Wert `Y` oder `N` einbeziehen.

## Dimensionselemente

Zu den Dimensionselementen gehören `Enabled`, `Disabled` und `Unknown`.

* **`Enabled`**: Der Browser unterstützt Cookies und hat diese aktiviert.
* **`Disabled`**: Cookies werden vom Browser nicht unterstützt oder sie wurden vom Besucher deaktiviert.
* **`Unknown`**: AppMeasurement konnte die Cookie-Unterstützung nicht ermitteln. Die Abfragezeichenfolge `k` war in der Bildanforderung nicht vorhanden.
