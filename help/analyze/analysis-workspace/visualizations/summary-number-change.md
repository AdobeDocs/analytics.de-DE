---
description: Verwenden Sie die Visualisierungen „Zusammenfassungsnummer“ und „Zusammenfassungsänderung“, um wichtige Datenpunkte in einem Projekt anzuzeigen.
title: Zusammenfassungsnummer und Zusammenfassungsänderung
uuid: 177c1b89-6d98-473d-8447-6b4cdc479565
feature: Visualizations
role: User, Admin
exl-id: d6a08201-ca3a-48ff-983a-3ec6b989deda
source-git-commit: 978bd8642011dd2c8e43564c90303f194689a64e
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 98%

---

# [!UICONTROL Zusammenfassungszahl] und [!UICONTROL Zusammenfassungsänderung]

_In diesem Artikel werden die Visualisierungen von Zusammenfassungszahlen und Zusammenfassungsänderungen in_ ![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics** beschrieben._<br/>_Unter [Zusammenfassungszahl und Zusammenfassungsänderung](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/visualizations/summary-number-change) finden Sie die Version dieses Artikels für_ ![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics**._


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Visualisierungen von Zusammenfassungszahlen und Zusammenfassungsänderungen](https://video.tv.adobe.com/v/335564/?quality=12){target=&#34;_blank&#34;} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


## Visualisierung der [!UICONTROL Zusammenfassungszahl] {#summary-number}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_summarynumber_button"
>title="Zusammenfassungszahl"
>abstract="Erstellen Sie eine Visualisierung, die die Summen und Zwischensummen anzeigt."

<!-- markdownlint-enable MD034 -->


Verwenden Sie die Visualisierung der ![MoveUpDown](/help/assets/icons/MoveUpDown.svg) **[!UICONTROL Zusammenfassungsänderung]**, um das Delta (die Änderung) zwischen zwei Zahlen anzuzeigen. <!-- This is applicable for AA, not CJA: The green and red color of the Summary Change can be controlled through [custom event polarity](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/success-events/success-event.html) or a calculated metric's [Show Upward Trend As](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html) option.-->

<!--
The green and red color of the Summary Change can be controlled through [custom event polarity](https://experienceleague.adobe.com/docs/analytics/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) or a calculated metric's [Show Upward Trend As](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html) option.
-->

Diese Visualisierung verhält sich folgendermaßen:

* Wenn keine Zelle ausgewählt ist, werden die ersten beiden Zellenwerte in der Spalte verglichen.
* Wenn eine Zelle ausgewählt ist, wird 0 angezeigt, weil der Zellenwert mit sich selbst verglichen wird.
* Wenn zwei Zellen ausgewählt sind, wird die erste ausgewählte Zelle als Numerator und die zweite als Denominator verwendet.
* Wenn mehr als zwei Zellen ausgewählt sind, werden nur die ersten beiden Zellen für den Vergleich berücksichtigt.
* Wenn ein Zellbereich ausgewählt ist, wird die erste Zelle mit den letzten im Bereich ausgewählten Zellen verglichen.
* Wenn die Spalte ausgewählt ist, wird der erste Wert mit sich selbst verglichen, sodass eine Änderung von 0 angezeigt wird.


![Visualisierung „Zusammenfassungsänderung“ mit dem Delta zwischen zwei Zahlen.](assets/summary-change.png)


Im Rahmen der Visualisierungseinstellungen sind bestimmte **[!UICONTROL Optionen für die Zusammenfassungsänderung]** verfügbar.

| Option | Definition |
|--- |--- |
| **[!UICONTROL Prozentänderung zeigen]** | Zeigen Sie die prozentuale Änderung zwischen den beiden Zahlen an. |
| **[!UICONTROL Rohdifferenz anzeigen]** | Zeigen Sie die Rohdifferenz zwischen den beiden Zahlen an. Mit dieser Option können Sie auch Werte kürzen und bis zu 3 Dezimalstellen anzeigen. |
| **[!UICONTROL Wert kürzen]** | Wählen Sie **[!UICONTROL Wert abkürzen]**, um den geänderten Wert intelligent zu kürzen. Wenn diese Option ausgewählt ist, geben Sie eine Zahl ein, um den Umfang der Abkürzung zu definieren. Beispiel:<br/><table><tr><td>**Originalwert**</td><td>**Abgekürzter Wert**</td><td>**Ergebnis**</td></tr><tr><td>12.011.141,25 USD</td><td>Nicht ausgewählt</td><td  align="right">12.011.141,25 USD</td></tr><tr><td>12.011.141,25 USD</td><td>Ausgewählt, auf `0` gesetzt</td><td align="right">12 Mio. USD</td></tr><tr><td>12.011.141,25 USD</td><td> Ausgewählt, auf `1` gesetzt</td><td  align="right">12,0 Mio. USD</td></tr><tr><td>12.011.141,25 USD</td><td>Ausgewählt, auf `2` gesetzt</td><td align="right">12,01 Mio. USD</td></tr><tr><td>12.011.141,25 USD</td><td>Ausgewählt, auf `3` gesetzt</td><td align="right">12,01 Mio. USD</td></tr></table> |

>[!MORELIKETHIS]
>
>[Hinzufügen einer Visualisierung zu einem Panel](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>&#x200B;>[Visualisierungseinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>&#x200B;>[Kontextmenü der Visualisierung](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>
