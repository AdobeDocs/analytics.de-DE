---
title: Neuladungen
description: Die Häufigkeit, mit der die Seite neu geladen wurde.
feature: Metrics
exl-id: 9539a733-9e9f-48b3-b8ab-8d969de27f87
source-git-commit: c9b7c32adfb44a04ab792d12ca049106b3009710
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 21%

---

# Neuladungen

Die [Metrik „Neuladungen](overview.md) gibt an, wie oft ein Dimensionselement während eines Neuladens vorhanden war. Ein Besucher, der seinen Browser aktualisiert, stellt die häufigste Methode dar, eine Neuladung auszulösen.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der Treffer, bei denen die Dimension [Seite](../dimensions/page.md) denselben Wert wie der vorherige Treffer enthält.

Das Konzept des Neuladens gilt für die Dimension Seite, unabhängig davon, welche Dimension Sie im Reporting verwenden. Wenn Sie beispielsweise [eVar1](../dimensions/evar.md) als Dimension verwenden und als Metrik neu lädt, zeigt Ihnen die Tabelle an, wie oft jeder eVar-Wert während des Neuladens vorhanden war (zwei aufeinander folgende Seitenwerte). Es wird nicht angezeigt, wie oft zwei aufeinander folgende eVar1-Werte vorhanden waren.
