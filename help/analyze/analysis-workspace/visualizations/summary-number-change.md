---
description: Verwenden Sie die Visualisierungen „Zusammenfassungsnummer“ und „Zusammenfassungsänderung“, um wichtige Datenpunkte in einem Projekt anzuzeigen.
title: Sammelnummer und Sammeländerung
uuid: 177c1b89-6d98-473d-8447-6b4cdc479565
feature: Visualizations
role: User, Admin
exl-id: d6a08201-ca3a-48ff-983a-3ec6b989deda
source-git-commit: c0855c6bed6a9762c0440e1a8e004ee11020808e
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 93%

---

# [!UICONTROL Zusammenfassungszahl] und [!UICONTROL Zusammenfassungsänderung]

*In diesem Artikel werden die Visualisierung der Zusammenfassungsnummer und der Zusammenfassungsänderung in **Adobe Analytics**.<br/>Siehe [Zusammenfassungsnummer und Zusammenfassungsänderung](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/summary-number-change) für die **Customer Journey Analytics**-Version dieses Artikels.*

Im Folgenden finden Sie ein Video zu diesen beiden Visualisierungen:

>[!VIDEO](https://video.tv.adobe.com/v/335564/?quality=12)

## Visualisierung der [!UICONTROL Zusammenfassungszahl] {#summary-number}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_summarynumber_button"
>title="Zusammenfassungszahl"
>abstract="Erstellen Sie eine Visualisierung, die die Summen und Zwischensummen anzeigt."

<!-- markdownlint-enable MD034 -->

Verwenden Sie die Visualisierung der [!UICONTROL Zusammenfassungszahl], um eine große Zahl hervorzuheben, die für ein Projekt wichtig ist. Diese Visualisierung verhält sich folgendermaßen:

* Wenn keine Zelle ausgewählt ist, wird die gesamte Spalte ausgewählt.
* Wenn eine einzelne Zelle ausgewählt ist, wird die Zusammenfassung für diese Zelle angezeigt.
* Wenn mehr als eine Zelle ausgewählt ist, wird die zuerst ausgewählte Zelle angezeigt.
* Wenn die Spalte ausgewählt ist, wird der erste Zellenwert in der Spalte verwendet.

Klicken Sie oben rechts auf den **Visualisierungseinstellungen**, um die Einstellungen für die Zusammenfassungsnummer zu konfigurieren:

| Einstellung | Definition |
|--- |--- |
| [!UICONTROL Prozentsätze] | Zeigt Prozentsätze anstatt von Rohdaten an. |
| [!UICONTROL Legende eingeblendet] | Zeigt Informationen zur angezeigten Metrik an. |
| [!UICONTROL Wert kürzen] | Wählen Sie diese Option, um Werte zu kürzen und bis zu 3 Dezimalstellen anzuzeigen. |
| [!UICONTROL Wert zusammenfassen nach] | Wählen Sie diese Option, um für ausgewählte Daten das Maximum, das Minimum, den Mittelwert, den Median oder die Summe anzuzeigen. |

## Visualisierung der [!UICONTROL Zusammenfassungsänderung:] {#summary-change}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_summarychange_button"
>title="Zusammenfassungsänderung"
>abstract="Erstellen Sie eine Visualisierung, die das Delta (die Änderung) zwischen zwei Zahlen anzeigt"

<!-- markdownlint-enable MD034 -->

Verwenden Sie die Visualisierung der [!UICONTROL Zusammenfassungsänderung], um das Delta (die Änderung) zwischen zwei Zahlen anzuzeigen. Die grüne und rote Farbe der [!UICONTROL Zusammenfassungsänderung] kann über die [benutzerdefinierte Ereignispolarität](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) oder die Option [Aufwärts-Trend anzeigen als](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html?lang=de) einer berechneten Metrik angepasst werden.

Diese Visualisierung verhält sich folgendermaßen:

* Wenn keine Zelle ausgewählt ist, werden die ersten beiden Zellenwerte in der Spalte verglichen.
* Wenn eine Zelle ausgewählt ist, wird 0 angezeigt, weil der Zellenwert mit sich selbst verglichen wird.
* Wenn zwei Zellen ausgewählt sind, wird die erste ausgewählte Zelle als Numerator und die zweite als Denominator verwendet.
* Wenn mehr als zwei Zellen ausgewählt sind, werden nur die ersten beiden Zellen für den Vergleich berücksichtigt.
* Wenn ein Zellbereich ausgewählt ist, wird die erste Zelle mit den letzten im Bereich ausgewählten Zellen verglichen.
* Wenn die Spalte ausgewählt ist, wird der erste Wert mit sich selbst verglichen, sodass eine Änderung von 0 angezeigt wird.


![](assets/summary-change.png)


Klicken Sie oben rechts auf den **Visualisierungseinstellungen**, um die Einstellungen für die Zusammenfassungsänderung zu konfigurieren:

| Einstellung | Definition |
| --- | --- |
| [!UICONTROL Prozentsätze] | Zeigt Prozentsätze anstatt von Rohdaten an. |
| [!UICONTROL Legende eingeblendet] | Zeigt Informationen zur angezeigten Metrik an. |
| [!UICONTROL Prozentuale Veränderung anzeigen] | Zeigt die prozentuale Änderung zwischen den beiden Zahlen an. |
| [!UICONTROL Rohdifferenz anzeigen] | Zeigt den tatsächlichen Unterschied zwischen den beiden Zahlen. Mit dieser Option können Sie auch Werte kürzen und bis zu 3 Dezimalstellen anzeigen. |
