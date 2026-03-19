---
title: Einzelseitenbesuche (Metriken)
description: Die Häufigkeit, mit der sich das Dimensionselement „Seite“ bei einem Besuch nicht geändert hat.
feature: Metrics
exl-id: 086235d0-4542-4e82-96ab-28c47c842ecf
source-git-commit: 6d2c278c5525c89b73c39bbfcedbe644806bf989
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 33%

---

# Einzelseitenbesuche

*Auf dieser Hilfeseite wird beschrieben, wie „Einzelseitenbesuche“ als Metrik funktioniert. Weitere Informationen finden Sie unter der Dimension [Einzelseitenbesuche](../dimensions/single-page-visits.md).*

Die Metrik **[!UICONTROL Einzelseitenbesuche]** [&#x200B; gibt &#x200B;](overview.md) Anzahl der Besuche an, bei denen das Dimensionselement [Seite](../dimensions/page.md) nur einen einzigen Wert für den gesamten Besuch enthält. Diese Metrik ist hilfreich bei Dimensionen, in denen Sie kurze Besuche anzeigen, aber keine so strengen Regeln wie bei [[!UICONTROL Absprüngen]](bounces.md) verwenden möchten.

## Berechnung dieser Metrik

Die Definition dieser Metrik hängt von der Projekteinstellung von „Wiederholte Instanzen zählen[[!UICONTROL &#x200B; ab]](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md#project-info-settings):

* **[!UICONTROL Wiederholte Instanzen zählen] aktiviert**: Zählt die Anzahl der Besuche, bei denen die Dimension [!UICONTROL Seite] einen einzelnen Wert für den Besuch enthält. Wenn ein Besucher die Seite neu lädt, wird sie als einzelner Seitenbesuch disqualifiziert.
* **[!UICONTROL Wiederholte Instanzen zählen] deaktiviert**: Zählt die Anzahl der Besuche, bei denen die Dimension [!UICONTROL Seite] einen einzelnen eindeutigen Wert für den gesamten Besuch enthält.

Unabhängig von der Projekteinstellung [!UICONTROL Wiederholte Instanzen zählen] hält diese Metrik die folgenden Regeln ein:

* Ein Besuch gilt auch dann als Einzelseitenbesuch, wenn ein Besucher Linktracking-Aufrufe auslöst (die Dimension [!UICONTROL Seite] wird aus allen Linktracking-Aufrufen entfernt).
* Sobald sich die Dimension [!UICONTROL Seite] in einen zweiten eindeutigen Wert ändert, gilt der Besuch nicht mehr als einzelner Seitenbesuch.

Einen Vergleich der Metriken finden Sie unter [Einzelzugriff](single-access.md).
