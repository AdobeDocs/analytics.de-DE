---
title: Seiten nicht gefunden (Metriken)
description: Die Anzahl der Treffer, die einen Fehler enthalten.
feature: Metrics
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
TQID: https://experienceleague.adobe.com/V5jVT8wh71qMrchQmmM6c4EMofHPUEI388TmAf7Zf6M
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 35%

---

# Seiten nicht gefunden

*Auf dieser Hilfeseite wird beschrieben, wie „Seiten nicht gefunden“ als Metrik funktioniert. Weitere Informationen zur Funktionsweise als Dimension finden [&#x200B; auf &#x200B;](../dimensions/pages-not-found.md) Dimensionsseite „Seiten nicht gefunden“*

Die Metrik „Seiten nicht gefunden[&#x200B; &#x200B;](overview.md) gibt die Anzahl der Treffer an, bei denen eine Dimension zum Zeitpunkt des Fehlers eines Besuchers festgelegt oder beibehalten wurde. Diese Metrik ist nützlich, wenn Sie sehen möchten, welche Seiten oder URLs Fehlermeldungen enthalten (z. B. eine 404). Sie können diese Informationen dann an Ihr Web-Entwicklungs-Team weitergeben, das die Fehlerursache ermitteln und beheben kann.

## Berechnung dieser Metrik

Diese Metrik zählt alle Treffer, bei denen die [`pageType`](/help/implement/vars/page-vars/pagetype.md)-Variable dem Wert von `"errorPage"` entspricht. Dies ist das Metrik-Äquivalent der Dimension [Seiten nicht gefunden](../dimensions/pages-not-found.md).
