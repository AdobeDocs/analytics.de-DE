---
title: Suchvorgänge
description: Die Häufigkeit, mit der ein Treffer externen Suchkriterien entsprach.
feature: Metrics
exl-id: b84c895d-e678-47a1-9e41-500970e0a80c
TQID: https://experienceleague.adobe.com/bcK-h9tkOKRHFoZ5EbX05ppNtV5S8Kok8dhMJZxf-ao
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 88%

---

# Suchvorgänge

Die [Metrik „Suchen](overview.md) gibt die Anzahl der Treffer an, die mit der externen Sucherkennung von Adobe übereinstimmen. Diese Metrik ist nützlich, wenn Sie nicht suchbezogene Dimensionselemente betrachten und sehen möchten, wie sie zum Traffic von Suchmaschinen beigetragen haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, die mit der externen Sucherkennung von Adobe übereinstimmen. Sie muss mit beiden der folgenden Kriterien übereinstimmen:

* Der Referrer-Wert des Treffers ist eine von Adobe anerkannte Suchdomäne.
* Die Referrer-URL des Treffers enthält einen Abfragezeichenfolgenparameter für Suchbegriffe. Aufgrund moderner Datenschutzpraktiken ist dieser Abfragezeichenfolgenwert in der Regel leer. Adobe erkennt leere Schlüsselwort-Abfragezeichenfolgen als Teil der Sucherkennung.
