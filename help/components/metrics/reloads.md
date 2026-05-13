---
title: Neuladungen
description: Die Häufigkeit, mit der die Seite neu geladen wurde.
feature: Metrics
exl-id: 9539a733-9e9f-48b3-b8ab-8d969de27f87
TQID: https://experienceleague.adobe.com/Jhm8-usZH-SLOzUvNIC3hdoKDMkm9T5mnCUeeMRga7E
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 21%

---

# Neuladungen

Die [Metrik „Neuladungen](overview.md) gibt an, wie oft ein Dimensionselement während eines Neuladens vorhanden war. Ein Besucher, der seinen Browser aktualisiert, stellt die häufigste Methode dar, eine Neuladung auszulösen.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen die Dimension [Seite](../dimensions/page.md) denselben Wert wie der vorherige Treffer enthält.

Das Konzept des Neuladens gilt für die Dimension Seite, unabhängig davon, welche Dimension Sie im Reporting verwenden. Wenn Sie beispielsweise [eVar1](../dimensions/evar.md) als Dimension verwenden und als Metrik neu lädt, zeigt Ihnen die Tabelle an, wie oft jeder eVar-Wert während des Neuladens vorhanden war (zwei aufeinander folgende Seitenwerte). Es wird nicht angezeigt, wie oft zwei aufeinander folgende eVar1-Werte vorhanden waren.
