---
title: Seiten nicht gefunden (Metriken)
description: Die Anzahl der Treffer, die einen Fehler enthalten.
feature: Metrics
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 45%

---

# Seiten nicht gefunden

*Auf dieser Hilfeseite wird beschrieben, wie „Seiten nicht gefunden“ als Metrik funktioniert. Weitere Informationen finden Sie unter der Dimension [Seiten nicht gefunden](../dimensions/pages-not-found.md).*

Die Metrik „Seiten nicht gefunden[ ](overview.md) gibt die Anzahl der Treffer an, bei denen eine Dimension zum Zeitpunkt des Fehlers eines Besuchers festgelegt oder beibehalten wurde. Diese Metrik ist nützlich, wenn Sie sehen möchten, welche Seiten oder URLs Fehlermeldungen enthalten (z. B. eine 404). Sie können diese Informationen dann an Ihr Web-Entwicklungs-Team weitergeben, das die Fehlerursache ermitteln und beheben kann.

## Berechnung dieser Metrik

Diese Metrik zählt alle Treffer, bei denen die [`pageType`](/help/implement/vars/page-vars/pagetype.md)-Variable dem Wert von `"errorPage"` entspricht. Dies ist das Metrik-Äquivalent der Dimension [Seiten nicht gefunden](../dimensions/pages-not-found.md).
