---
title: Seiten nicht gefunden (Metriken)
description: Die Anzahl der Treffer, die einen Fehler enthalten.
feature: Metrics
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
source-git-commit: a15d2b596c1e8b70e91efb49dd607fdbb0ceec3c
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 35%

---

# Seiten nicht gefunden

*Auf dieser Hilfeseite wird beschrieben, wie „Seiten nicht gefunden“ als Metrik funktioniert. Weitere Informationen zur Funktionsweise als Dimension finden [ auf ](../dimensions/pages-not-found.md) Dimensionsseite „Seiten nicht gefunden“*

Die Metrik „Seiten nicht gefunden[ ](overview.md) gibt die Anzahl der Treffer an, bei denen eine Dimension zum Zeitpunkt des Fehlers eines Besuchers festgelegt oder beibehalten wurde. Diese Metrik ist nützlich, wenn Sie sehen möchten, welche Seiten oder URLs Fehlermeldungen enthalten (z. B. eine 404). Sie können diese Informationen dann an Ihr Web-Entwicklungs-Team weitergeben, das die Fehlerursache ermitteln und beheben kann.

## Berechnung dieser Metrik

Diese Metrik zählt alle Treffer, bei denen die [`pageType`](/help/implement/vars/page-vars/pagetype.md)-Variable dem Wert von `"errorPage"` entspricht. Dies ist das Metrik-Äquivalent der Dimension [Seiten nicht gefunden](../dimensions/pages-not-found.md).
