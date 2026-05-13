---
title: Seitenansichten
description: Die Häufigkeit, mit der ein Dimensionselement in Adobe Analytics festgelegt oder beibehalten wurde.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
TQID: https://experienceleague.adobe.com/ZJOoxc3imuMfVTa7caV5eQ6-XJh0amCRq65ByuANFq0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 100%

---

# Seitenansichten

Die [Metrik](overview.md) **[!UICONTROL Seitenansichten]** zeigt an, wie oft ein bestimmtes Dimensionselement auf einer Seite festgelegt oder beibehalten wurde. Es handelt sich dabei um eine der häufigsten und grundlegendsten Metriken in Berichten.

## Berechnung dieser Metrik

Diese Metrik zählt alle Seitenansicht-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) in einer Report Suite. Bei Dimensionen sind auch Treffer enthalten, bei denen ein Dimensionselement festgelegt oder persistiert wird. Sie enthält keine Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) oder Daten aus [Datenquellen](/help/import/data-sources/overview.md).

## Vergleich mit ähnlichen Metriken

* **Seitenansichten im Vergleich zu [Besuchen](visits.md)**: „Seitenansichten“ zählt, wie oft eine Seite angezeigt wird. „Besuche“ zählt die Anzahl der Sitzungen für Besuchende. Ein Besuch besteht aus einer oder mehreren Seitenansichten.
* **Seitenansichten im Vergleich zu [Seitenereignissen](page-events.md)**: „Seitenansichten“ zählt die Anzahl der Tracking-Aufrufe für Seitenansichten (`t()`) und schließt Linktracking-Aufrufe (`tl()`) aus. „Seitenereignisse“ sind das Gegenteil. Sie zählen die Anzahl der Linktracking-Aufrufe und schließen Seitenansichts-Tracking-Aufrufe aus.
