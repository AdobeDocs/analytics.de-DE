---
title: Hierarchie
description: (Eingestellt) Eine benutzerdefinierte Dimension, die Sie in Berichten verwenden können.
feature: Dimensions
exl-id: f9bd3ae1-3578-44c5-a540-ea93feac5bef
TQID: https://experienceleague.adobe.com/7WnYvaE3qCfYGWcX6IuvMZiF0MJq50Izz6i2LNg4h6c
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 167
ht-degree: 86%

---

# Hierarchie

>[!IMPORTANT]
>
>Diese Dimension wurde eingestellt und ist keine verfügbare [Dimension](overview.md) in Analysis Workspace. Adobe empfiehlt stattdessen die Verwendung von [eVars](evar.md) und Klassifizierungen.

Hierarchien sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie bleiben nicht über den von ihnen festgelegten Treffer hinaus bestehen. Es sind bis zu 5 Hierarchien verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Füllen von Hierarchien mit Daten

Jede Hierarchie erfasst Daten aus der [`h1` - `h5` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen. Beispielsweise erfasst der Abfragezeichenfolgenparameter `h1` Daten für Hierarchie 1, während der Abfragezeichenfolgenparameter `h4` Daten für Hierarchie 4 erfasst.

AppMeasurement, das JavaScript-Variablen in eine Bildanforderung für die Datenerfassung kompiliert, verwendet die Variablen `hier1` – `hier5`. Die Implementierungsrichtlinien finden Sie [hier](/help/implement/vars/page-vars/hier.md) im Benutzerhandbuch zu Implementierungen.

## Dimensionselemente

Da Hierarchien benutzerdefinierte Zeichenfolgen in Ihrer Implementierung enthalten, bestimmt Ihre Organisation, welche Dimensionselemente für jede Hierarchie gelten. Stellen Sie sicher, dass Sie den Zweck jeder Hierarchie und die typischen Dimensionselemente in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.
