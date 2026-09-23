---
title: Seiten nicht gefunden (Metriken)
description: Die Anzahl der Treffer, die einen Fehler enthalten.
feature: Metrics
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
TQID: https://experienceleague.adobe.com/V5jVT8wh71qMrchQmmM6c4EMofHPUEI388TmAf7Zf6M
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 35%
---
# Seiten nicht gefunden

>[!BEGINSHADEBOX]

*Auf dieser Hilfeseite wird beschrieben, wie „Seiten nicht gefunden“ als Metrik funktioniert. Weitere Informationen zur Funktionsweise als Dimension finden [&#x200B; auf &#x200B;](../dimensions/pages-not-found.md) Dimensionsseite „Seiten nicht gefunden“*

>[!ENDSHADEBOX]

Die Metrik „Seiten nicht gefunden[&#x200B; &#x200B;](overview.md) gibt die Anzahl der Treffer an, bei denen eine Dimension zum Zeitpunkt des Fehlers eines Besuchers festgelegt oder beibehalten wurde. Diese Metrik ist nützlich, wenn Sie sehen möchten, welche Seiten oder URLs Fehlermeldungen enthalten (z. B. eine 404). Sie können diese Informationen dann an Ihr Web-Entwicklungs-Team weitergeben, das die Fehlerursache ermitteln und beheben kann.

## Berechnung dieser Metrik

Diese Metrik zählt alle Treffer, bei denen die [`pageType`](/help/implement/vars/page-vars/pagetype.md)-Variable dem Wert von `"errorPage"` entspricht. Dies ist das Metrik-Äquivalent der Dimension [Seiten nicht gefunden](../dimensions/pages-not-found.md).
