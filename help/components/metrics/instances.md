---
title: Instanzen
description: Die Anzahl der Treffer, für die eine Variable festgelegt (und nicht beibehalten) wurde.
feature: Metrics
exl-id: 9d1a66b5-46f9-4834-87a1-5f63e386e61d
TQID: https://experienceleague.adobe.com/a6Ycw6CVzeSKuOCHezQtLNIZZo6vbkVneVWO0C2QfxQ
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 263
ht-degree: 50%

---

# Instanzen

Die [Metrik „Instanzen](overview.md) gibt an, wie oft eine Dimension in einer Bildanforderung explizit definiert wurde. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), behalten ihre Dimensionselemente über den Treffer hinaus bei, für den sie festgelegt wurden. Diese Metrik ist nützlich, wenn Sie sehen möchten, wie oft ein Dimensionselement ohne die Treffer festgelegt wurde, bei denen dieser Wert beibehalten wurde.

## Berechnung dieser Metrik

Schließen Sie von allen Treffern in einer Report Suite nur Treffer ein, die explizit ein Dimensionselement in der Bildanforderung festlegen. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), bleiben über den Treffer hinaus bestehen, für den sie festgelegt wurden. Metriken, wie [Seitenansichten](page-views.md) und [Vorfälle](occurrences.md), zählen sowohl Anfangswerte als auch beibehaltene Werte. Diese Metrik zählt keine persistenten Werte.

Ein Besucher gelangt beispielsweise auf Ihre Site und verwendet die interne Suche. Sie verfolgen die interne Suche in eVar1. Nachdem sie die interne Suche einmal verwendet haben, besuchen sie fünf weitere Seiten, bevor sie gehen.

Wenn Sie einen Bericht in Workspace anzeigen, werden eine eVar1-Instanz und sechs Vorfälle angezeigt. Eine Instanz zählt auf der Suchergebnisseite, während die Metrik Vorfälle den Anfangswert und die nachfolgenden persistierten Werte zählt.

## Vergleich mit ähnlichen Metriken

* **Instanzen vs. [Vorfälle](occurrences.md)**: Instanzen enthalten keine Treffer, bei denen ein Dimensionselement persistent ist. Anzahl von Vorfällen Treffer, bei denen ein Dimensionselement festgelegt oder beibehalten wurde.
* **Instanzen vs. [Seitenansichten](page-views.md)**: Instanzen umfassen alle Treffertypen, einschließlich Seitenansichts-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)), Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) und Daten aus [ (Datenquellen](/help/import/data-sources/overview.md). Die Metrik „Seitenansichten“ umfasst nur Seitenansichts-Tracking-Aufrufe, aber keine Linktracking-Aufrufe und Datenquellen auf Zusammenfassungsebene.
