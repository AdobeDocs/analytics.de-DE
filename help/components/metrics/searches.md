---
title: Suchvorgänge
description: Die Häufigkeit, mit der ein Treffer externen Suchkriterien entsprach.
feature: Metrics
exl-id: b84c895d-e678-47a1-9e41-500970e0a80c
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 88%

---

# Suchvorgänge

Die [Metrik „Suchen](overview.md) gibt die Anzahl der Treffer an, die mit der externen Sucherkennung von Adobe übereinstimmen. Diese Metrik ist nützlich, wenn Sie nicht suchbezogene Dimensionselemente betrachten und sehen möchten, wie sie zum Traffic von Suchmaschinen beigetragen haben.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, die mit der externen Sucherkennung von Adobe übereinstimmen. Sie muss mit beiden der folgenden Kriterien übereinstimmen:

* Der Referrer-Wert des Treffers ist eine von Adobe anerkannte Suchdomäne.
* Die Referrer-URL des Treffers enthält einen Abfragezeichenfolgenparameter für Suchbegriffe. Aufgrund moderner Datenschutzpraktiken ist dieser Abfragezeichenfolgenwert in der Regel leer. Adobe erkennt leere Schlüsselwort-Abfragezeichenfolgen als Teil der Sucherkennung.
