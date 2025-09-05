---
description: Erfahren Sie mehr über Metriktyp und Attribution.
title: Metriktyp und Attribution
feature: Calculated Metrics
exl-id: 3fb98227-e2ef-4829-ae84-812f845470ee
source-git-commit: 665319bdfc4c1599292c2e7aea45622d77a291a7
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 100%

---

# Metriktyp und Attribution {#metric-type-attribution}

Sie können den Metriktyp und das [Attributionsmodell](#attribution-models) für eine Metrik in der Definition einer berechneten Metrik konfigurieren.

1. Wählen Sie in der Metrikkomponente ![Einstellung](/help/assets/icons/Setting.svg) aus.
1. Im Popup-Dialogfeld:

   ![Metriktyp und Attribution](assets/cm-type-alloc.png)

   * Geben Sie den **[!UICONTROL Metriktyp]** an:

     | Metriktyp | Definition |
     |---|---|
     | **[!UICONTROL Standard]** | Wenn eine Formel aus einer einzelnen Standardmetrik besteht, zeigt sie die gleichen Daten wie das nicht berechnete Metrikgegenstück an. Standardmetriken eignen sich zum Erstellen berechneter Metriken, die speziell für die einzelnen Zeileneinträge gelten. <p>Zum Beispiel teilt ![Ereignis](/help/assets/icons/Event.svg) **[!UICONTROL Bestellungen]** ![Geteilt durch](/help/assets/icons/Divide.svg) ![Ereignis](/help/assets/icons/Event.svg) **[!UICONTROL Besuche]** die Bestellungen für diesen spezifischen Zeileneintrag durch die Anzahl der Besuche für diesen spezifischen Zeileneintrag. |
     | **[!UICONTROL Gesamtsumme]** | Verwenden Sie die **[!UICONTROL Gesamtsumme]** für den Berichtszeitraum in jedem Zeileneintrag. Wenn eine Formel aus einer einzelnen Gesamtsummenmetrik besteht, zeigt sie dieselbe Gesamtsummenzahl für jeden Zeileneintrag an. Gesamtsummenmetriken sind hilfreich, wenn Sie berechnete Metriken erstellen möchten, die mit den Gesamtdaten verglichen werden. <p>Zum Beispiel zeigt ![Ereignis](/help/assets/icons/Event.svg) **[!UICONTROL Bestellungen]** ![Geteilt durch](/help/assets/icons/Divide.svg) ![Ereignis](/help/assets/icons/Event.svg) **[!UICONTROL Gesamtbesuche]** den Anteil der Bestellungen im Verhältnis zu allen Besuchen und nicht nur die Besuche für den spezifischen Zeileneintrag an. In diesem Beispiel geben Sie die **[!UICONTROL Gesamtsumme]** für die Metrik ![Ereignis](/help/assets/icons/Event.svg) **[!UICONTROL Besuche]** in Ihrer berechneten Metrik an, die sie automatisch in ![Ereignis](/help/assets/icons/Event.svg) **[!UICONTROL Gesamtbesuche]** umwandelt. |

   * Geben Sie die **[!UICONTROL Attribution]** an.

      1. Sie haben folgende Möglichkeiten:

         * Deaktivieren Sie **[!UICONTROL Nicht standardmäßiges Zuordnungsmodell verwenden]**, um das standardmäßige Spalten-Attributionsmodell Letztkontakt mit einem Lookback-Fenster von 30 Tagen zu verwenden.
         * Aktivieren Sie **[!UICONTROL Nicht standardmäßiges Zuordnungsmodell verwenden]**. Im Dialogfeld **[!UICONTROL Attributionsmodell mit Spalten]**

            * Wählen Sie ein **[!UICONTROL Modell]** aus den [Attributionsmodellen](#attribution-models) aus.
            * Wählen Sie einen **[!UICONTROL Container]** aus den Optionen für [Container](#container) aus.
            * Wählen Sie ein **[!UICONTROL Lookback-Fenster]** aus den Optionen für [Lookback-Fenster](#lookback-window) aus. Wenn Sie **[!UICONTROL Benutzerdefinierte Zeit]** auswählen, können Sie den Zeitraum in **[!UICONTROL Minuten]** bis zu **[!UICONTROL Quartalen]** festlegen. 

      1. Wählen Sie **[!UICONTROL Anwenden]**, um das nicht standardmäßige Attributionsmodell anzuwenden. Wählen Sie zum Abbrechen die Option „Abbrechen“ aus.

     Wenn Sie bereits ein nicht standardmäßiges Attributionsmodell definiert haben, wählen Sie **[!UICONTROL Bearbeiten]** aus, um die Auswahl zu ändern.

Unter [Beispiel](#example) finden Sie ein Beispiel für die Verwendung von Attributionsmodellen, Containern und Lookback-Fenstern.


## Attributionsmodelle {#attribution-models}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_nondefaultattributionmodel"
>title="Nicht standardmäßiges Attributionsmodell verwenden"
>abstract="Aktivieren Sie ein nicht standardmäßiges Attributionsmodell für die ausgewählte Metrik."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attributionmodel"
>title="Modell"
>abstract="Wählen Sie ein Attributionsmodell für die Metrik aus."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lasttouch"
>title="Letztkontakt"
>abstract="Die Credits gehen zu 100 % an den letzten Dimensionswert, den eine Besucherin bzw. ein Besucher gesehen hat."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_firsttouch"
>title="Erstkontakt"
>abstract="Die Credits gehen zu 100 % an den ersten Dimensionswert, den eine Besucherin bzw. ein Besucher gesehen hat."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_linear"
>title="Linear"
>abstract="Die Credits werden gleichmäßig auf alle Dimensionswerte verteilt."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_participation"
>title="Beitrag"
>abstract="Die Credits gehen zu 100 % an jeden Dimensionswert, der von einer Besucherin oder einem Besucher gesehen wird.<br/>Spaltensummen werden erhöht."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_sametouch"
>title="Selber Kontakt"
>abstract="Die Credits werden nur für Dimensionswerte erteilt, die bei demselben Ereignis wie die Konversion auftreten."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_instance"
>title="Selber Kontakt"
>abstract="Die Credits werden nur für Dimensionswerte erteilt, die bei demselben Ereignis wie die Konversion auftreten."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_ushaped"
>title="U-Form"
>abstract="Die Credits gehen zu zu 40 % an die erste Dimension, zu 40 % an die letzte und zu 20 % an die mittlere."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_jcurve"
>title="J-Kurve"
>abstract="Die Credits gehen zu zu 60 % an den letzten Dimensionswert, zu 20 % an den ersten und zu 20 % an den mittleren."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_jshaped"
>title="J-Kurve"
>abstract="Die Credits gehen zu zu 60 % an den letzten Dimensionswert, zu 20 % an den ersten und zu 20 % an den mittleren."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_inversej"
>title="Umgekehrtes J"
>abstract="Die Credits gehen zu 60 % an den ersten Dimensionswert, zu 20 % an den letzten und zu 20 % an den mittleren."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_reversejshaped"
>title="Umgekehrtes J"
>abstract="Die Credits gehen zu 60 % an den ersten Dimensionswert, zu 20 % an den letzten und zu 20 % an den mittleren."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_timedecay"
>title="Zeitverfall"
>abstract="Die Dimensionswerte, die einer Konversion zeitlich am nächsten sind, erhalten die meisten Credits."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_custom"
>title="Anpassen"
>abstract="Definieren Sie Ihre eigene positionsbasierte Attributionsgewichtung."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_positionbased"
>title="Anpassen"
>abstract="Definieren Sie Ihre eigene positionsbasierte Attributionsgewichtung."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_algorithmic"
>title="Algorithmisch"
>abstract="Die Credits werden anhand eines statistischen Algorithmus dynamisch bestimmt."

{{attribution-models-details}}


## Container {#container}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_container"
>title="Container"
>abstract="Wählen Sie einen Container aus, um den gewünschten Umfang für die Attribution festzulegen."

{{attribution-container}}


## Lookback-Fenster {#lookback-winwow}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lookbackwindow"
>title="Lookback-Fenster"
>abstract="Diese Einstellung bestimmt das Fenster der Datenattribution, das für jede Konversion angewendet wird."

{{attribution-lookback-window}}

## Beispiel

{{attribution-example}}


<!--
When [building a calculated metric](/help/components/calculated-metrics/workflow/c-build-metrics/cm-build-metrics.md), you can specify the metric type and the attribution model.

## Metric type

To specify the metric type when building a calculated metric:

1. Select the gear icon next to the metric whose type you want to select.

   ![](assets/cm-type-alloc.png) 

1. Choose from the following options:

   |  Metric Type  | Definition  |
   |---|---|
   |  Standard  | These metrics are the same metrics used in standard [!DNL Analytics] reporting. If a formula consisted of a single standard metric, it displays identical data to its non-calculated-metric counterpart. Standard metrics are useful for creating calculated metrics specific to each individual line item. For example, [Orders] / [Visits] takes orders for that specific line item and divides it by the number of visits for that specific line item.  |
   |  Grand total  | Use Grand total for the reporting period in every line item. If a formula consisted of a single Grand total metric, it displays the same total number on every line item. Grand total metrics are useful for creating calculated metrics that compare against site total data. For example, [Orders] / [Total Visits] shows the proportion of orders against ALL visits to your site, not just the visits to the specific line item.  |

## How linear allocation works

[Attribution](/help/analyze/analysis-workspace/attribution/overview.md) is how allocation models in calculated metrics are evaluated.

For a full list of non-default attribution models and lookback windows supported, see [Attribution models and lookback windows](/help/analyze/analysis-workspace/attribution/models.md).

The following example illustrates how calculated metrics with linear allocations work in reporting: 

| | Hit 1 | Hit 2 | Hit 3 | Hit 4 | Hit 5 | Hit 6 | Hit 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
|Data Sent In|PROMO A|-|PROMO A|PROMO B|-|PROMO C|$10|
|Last Touch eVar|PROMO A|PROMO A|PROMO A|PROMO B|PROMO B|PROMO C|$10|
|First Touch eVar|PROMO A|PROMO A|PROMO A|PROMO A|PROMO A|PROMO A|$10|
|Example prop|PROMO A|-|PROMO A|PROMO B|-|PROMO C|$10|

In this example, the values A, B, and C were sent into a variable on hits 1, 3, 4, and 6 before a $10 purchase was made on hit 7. In the second row, those values persist across hits on a last touch visit basis. The third row illustrates a first-touch visit persistence. Finally, the last row illustrates how data would be recorded for a prop which does not have persistence.

-->