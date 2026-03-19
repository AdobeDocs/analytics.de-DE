---
title: Einzelzugriff
description: Die Häufigkeit, mit der sich ein Dimensionselement bei einem Besuch nicht geändert hat.
feature: Metrics
exl-id: 973ce835-9d6f-4ead-90c9-0b80aac82cc0
source-git-commit: 6d2c278c5525c89b73c39bbfcedbe644806bf989
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 15%

---

# Einzelzugriff

Die **[!UICONTROL Einzelzugriff]** [Metrik) &#x200B;](overview.md) die Anzahl der Besuche an, bei denen die entsprechende Berichtsdimension nur einen einzigen Wert für einen gesamten Besuch enthielt. Es handelt sich um die breitere, dimensionsspezifische Version von [[!UICONTROL Einzelseitenbesuche]](single-page-visits.md). Diese Metrik ist hilfreich im Kontext jeder Dimension, bei der Sie den Wert einer Dimension sehen möchten, wenn er während eines Besuchs nur einmal festgelegt wurde.

## Berechnung dieser Metrik

Die Definition dieser Metrik hängt von der Projekteinstellung von „Wiederholte Instanzen zählen[[!UICONTROL &#x200B; ab]](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md#project-info-settings):

* **Wiederholte Instanzen zählen aktiviert**: Zählt Besuche, bei denen die Dimension genau einen Wert pro Besuch enthält. Wenn die Dimension bestehen bleibt, wird sie nicht mehr als einzelner Zugriff qualifiziert.
* **Wiederholte Instanzen zählen deaktiviert**: Zählt Besuche, bei denen die Dimension einen einzelnen eindeutigen Wert enthält. Sie können das Dimensionselement mehrmals auf denselben Wert setzen oder ihn beibehalten lassen, sodass er weiterhin als einzelner Zugriff gezählt wird.

Unabhängig von &quot;[!UICONTROL &#x200B; wiederholte Instanzen zählen] ist der Besuch nicht mehr als einzelner Zugriff qualifiziert, wenn die Dimension in einen zweiten eindeutigen Wert geändert wird. Linktracking-Aufrufe sind in dieser Berechnung enthalten, wenn die Dimension in ihnen festgelegt ist.

## Unterschied zwischen &quot;[!UICONTROL Einzelzugriff] und &quot;[!UICONTROL Einzelseitenbesuch]&quot;

Im Kontext der Dimension [[!UICONTROL Seite]](../dimensions/page.md) sind [!UICONTROL Einzelzugriff] und [!UICONTROL Einzelseitenbesuche] unabhängig von der Projekteinstellung [!UICONTROL Wiederholungsinstanzen zählen] immer genau identisch. Die Unterschiede treten auf, wenn Sie andere Dimensionen verwenden.

* **[!UICONTROL Einzelzugriff]**: Zeigt die Anzahl der Besuche an, bei denen das angegebene Dimensionselement für einen einzelnen Treffer vorhanden war. Sie ist kontextabhängig von der Dimension, die Sie in Ihrem Projekt verwenden.
* **[!UICONTROL Einzelseitenbesuch]**: Zeigt die Anzahl der Besuche an, bei denen die Dimension [!UICONTROL Seite] für einen einzelnen Treffer vorhanden war. Obwohl Sie in Ihrem Bericht eine andere Dimension verwenden, werden dennoch Besuche gezählt, die ein einzelnes eindeutiges Dimensionselement [!UICONTROL Seite] enthalten.

Wenn [[!UICONTROL Wiederholte Instanzen zählen]](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md#project-info-settings) deaktiviert ist, ändern sich die Metrikdefinitionen geringfügig:

* **Einzelzugriff**: Zeigt die Anzahl der Besuche an, bei denen sich das angegebene Dimensionselement während des gesamten Besuchs nicht geändert hat.
* **Einzelseitenbesuch**: Zeigt die Anzahl der Besuche an, bei denen sich die Dimension [!UICONTROL Seite] nicht für den gesamten Besuch geändert hat.

Betrachten Sie beispielsweise das folgende Beispiel für Besuche mit zwei Treffern. Die Dimension in Ihrem Bericht lautet [[!UICONTROL Site-]](../dimensions/site-section.md)) und [!UICONTROL Wiederholte Instanzen zählen] ist deaktiviert.

* Ein Besucher ruft zwei Seiten auf, die sich jedoch beide im gleichen Website-Bereich befinden. Da der Site-Bereich während des Besuchs unverändert blieb, zählt er als einzelner Zugriff. Er zählt nicht als Einzelseitenbesuch, da der Besuch mehr als ein eindeutiges Dimensionselement [!UICONTROL Seite] enthält.
* Ein Besucher ruft zwei Seiten in verschiedenen Website-Bereichen auf, aber beide Seiten haben zufällig den gleichen Namen. Der Besuch zählt nicht als Einzelzugriff, da es zwei eindeutige Site-Abschnittswerte gab. Dies zählt als einzelner Seitenbesuch, da es nur ein einziges eindeutiges [!UICONTROL Seite] Dimensionselement gab.
