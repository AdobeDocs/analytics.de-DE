---
description: Linienvisualisierung zur Darstellung von (zeitbasierten) Trend-Datensätzen verwenden
title: Linie
uuid: 0508ff29-43fe-4f3a-a5f7-051869271b55
feature: Visualisierungen
role: User, Admin
exl-id: d177b39f-add7-4011-977a-1bdf3a9368cb
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: ht
source-wordcount: '512'
ht-degree: 100%

---

# Linie

Die Linienvisualisierung stellt Metriken anhand einer Linie dar, die den Wertverlauf über einen bestimmten Zeitraum hinweg zeigt. Ein Liniendiagramm kann nur verwendet werden, wenn die Zeit als Dimension verwendet wird.

![Linienvisualisierung](assets/line-viz.png)

Klicken Sie auf das Zahnradsymbol oben rechts in der Linienvisualisierung, um auf die verfügbaren [**Visualisierungseinstellungen**](freeform-analysis-visualizations.md) zuzugreifen. Die Einstellungen sind in folgende Kategorien unterteilt:

* **Allgemein**: Einstellungen, die für verschiedene Visualisierungstypen gelten
* **Achse**: Einstellungen, die sich auf die x- oder y-Achse der Linienvisualisierung auswirken
* **Überlagerungen**: Optionen zum Hinzufügen von zusätzlichem Kontext zu den in Ihrer Linienvisualisierung angezeigten Serien.

![Visualisierungseinstellungen](assets/viz-settings-modal.png)

## Granularität ändern

In den [Visualisierungseinstellungen](freeform-analysis-visualizations.md) können Sie über ein Dropdown-Menü für die Granularität eine Trend-Visualisierung (z. B. Linie, Balken) von täglich zu wöchentlich zu monatlich usw. ändern. Die Granularität wird auch in der Datenquellentabelle aktualisiert.

## Min. oder Max. anzeigen

Unter **[!UICONTROL Visualisierungseinstellungen]** > **[!UICONTROL Überlagerungen]** > **[!UICONTROL Min/Max anzeigen]** können Sie eine Beschriftung für Minimal- und Maximalwerte überlagern, um die Spitzen und Täler schnell in einer Metrik hervorzuheben. Hinweis: Die Minimal bzw. Maximalwerte werden aus den sichtbaren Datenpunkten in der Visualisierung abgeleitet, nicht aus dem vollständigen Satz von Werten innerhalb einer Dimension.

![Min./Max. anzeigen](assets/min-max-labels.png)

## Trendzeilenüberlagerung anzeigen

Unter **[!UICONTROL Visualisierungseinstellungen]** > **[!UICONTROL Überlagerungen]** > **[!UICONTROL Trendlinie anzeigen]** können Sie Ihrer Linienserie eine Regressionstrendlinie hinzufügen oder die Durchschnittstrendlinie in Ihre Linienserie verschieben. Trendlinien helfen, ein Muster in den Daten besser darzustellen.

>[!TIP]
>
>Es wird empfohlen, Trendlinien auf Daten anzuwenden, die weder das aktuelle Datum (partielle Daten) noch zukünftige Datumsangaben enthalten, da diese die Trendlinie verfälschen. Wenn Sie jedoch zukünftige Datumsangaben einbeziehen müssen, entfernen Sie Nullen aus den Daten, um eine Verfälschung für diese Tage zu vermeiden. Gehen Sie dazu zur Datenquellenabelle der Visualisierung, wählen Sie Ihre Metrikspalte aus und aktivieren Sie dann **[!UICONTROL Spalteneinstellungen]** > **[!UICONTROL Null als keinen Wert interpretieren]**.

![Lineare Trendlinie](assets/show-linear-trendline.png)

Alle Trendlinien des Regressionsmodells werden über die reguläre Kleinstquadrat-Methode angepasst:

| Modell | Beschreibung |
| --- | --- |
| Linear | Erstellt eine am besten passende gerade Linie für einfache lineare Datensätze und ist nützlich, wenn die Daten stetig zunehmen oder abnehmen. Gleichung: `y = a + b * x` |
| Logarithmisch | Erstellt eine am besten passende gekrümmte Linie und ist nützlich, wenn die Änderungsrate der Daten schnell zunimmt oder abnimmt und dann abflacht. Eine logarithmische Trendlinie kann negative und positive Werte verwenden. Gleichung: `y = a + b * log(x)` |
| Exponentiell | Erstellt eine gekrümmte Linie und ist nützlich, wenn Daten mit ständig steigenden Raten steigen oder fallen. Diese Option sollte nicht verwendet werden, wenn Ihre Daten Null oder negative Werte enthalten. Gleichung: `y = a + e^(b * x)` |
| Potenzfunktion | Erstellt eine gekrümmte Linie und ist nützlich für Datensätze, die Messungen vergleichen, die mit einer bestimmten Rate ansteigen. Diese Option sollte nicht verwendet werden, wenn Ihre Daten Null oder negative Werte enthalten. Gleichung: `y = a * x^b` |
| Quadratisch | Findet die beste Anpassung für einen Datensatz in Form einer Parabel (konkav nach oben oder unten). Gleichung: `y = a + b * x + c * x^2` |
| Gleitender Mittelwert | Erstellt eine glatte Trendlinie basierend auf einer Reihe von Durchschnittswerten. Ein gleitender Durchschnittswert, der auch als rollierender Durchschnitt bezeichnet wird, nutzt eine bestimmte Anzahl von Datenpunkten (bestimmt durch Auswahl eines Zeitraums), errechnet einen Durchschnittswert und verwendet den Durchschnittswert als Punkt auf der Linie. Beispiele sind der gleitende Durchschnitt für 7 Tage oder der gleitende Durchschnitt für 4 Wochen. |
