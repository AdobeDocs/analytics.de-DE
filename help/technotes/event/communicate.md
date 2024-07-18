---
title: Auswirkungen an Benutzer kommunizieren
description: Erfahren Sie, wie Sie die Wirkung eines Ereignisses in Ihrer Organisation effektiv kommunizieren können.
exl-id: 9ba83f3f-2eea-44c2-80b2-a0a9111d51cf
feature: Event
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 1%

---

# Ereignisauswirkungen an Benutzer kommunizieren

Wenn von einem Ereignis ](overview.md) Daten [betroffen sind, ist es wichtig, dieses Ereignis Benutzern in Ihrer Organisation mitzuteilen.

* Entwickeln eines häufigen Haftungsausschlusses, den Sie für die Konsistenz in der Kommunikation verwenden können
* Bereitstellung laufender Kommunikation für Analytics-Benutzer und wichtige Interessengruppen während und nach der Veranstaltung
* Fügen Sie eine Kalendererinnerung für nachfolgende Meilensteine ein, z. B. für den folgenden Monat oder das folgende Jahr. Diese Mitteilung in der Zukunft hilft Benutzern, die Berichte anzeigen, daran zu erinnern, wie sich diese in Monatsberichten oder Jahresberichten auswirken.

Die folgenden Abschnitte in Adobe Analytics zeigen verschiedene Möglichkeiten, mit Benutzern in Ihrem Unternehmen zu kommunizieren. Sie können auch andere Methoden außerhalb von Adobe Analytics verwenden, z. B. E-Mail, um mit Benutzern zu kommunizieren.

## Kommunikation über Bedienfeld- oder Visualisierungsbeschreibungen

Wenn Sie ein Workspace-Projekt unter Benutzern in Ihrem Unternehmen freigegeben haben, können Sie die Auswirkungen eines Ereignisses über Bedienfeld- oder Visualisierungsbeschreibungen kommunizieren. Klicken Sie mit der rechten Maustaste auf einen Bereich oder eine Visualisierungs-Kopfzeile und wählen Sie dann **[!UICONTROL Beschreibung bearbeiten]** aus.

![Bereichsbeschreibung](assets/panel_description.png)

## Kommunikation über Textvisualisierungen

Sie können die Auswirkungen eines Ereignisses auch über spezielle Textvisualisierungen kommunizieren. Siehe [Textvisualisierungen](/help/analyze/analysis-workspace/visualizations/text.md) im Benutzerhandbuch zu Analysen.

![Textvisualisierung](assets/text_visualization.png)

## Hinzufügen benutzerdefinierter Kalenderereignisse zu Trends in Workspace

Für jede Trend-Visualisierung in Workspace können Sie eine Reihe hinzufügen, die Ihren betroffenen Datumsbereich darstellt.

1. Erstellen Sie eine berechnete Metrik mit dem Segment &quot;Betroffene Tage&quot;, indem Sie den Schritten folgen: [Bestimmte Daten in der Analyse ausschließen](segments.md).
1. Fügen Sie die gewünschte Metrik der Arbeitsfläche für berechnete Metriken hinzu.

   ![Metrik](assets/calcmetric_event.png)

1. Fügen Sie einen Titel und eine Beschreibung hinzu, die Benutzer über die Auswirkungen informieren. Sie können diese Metrik bei Bedarf auch als Kalenderanmerkung taggen.

   ![Titel und Beschreibung](assets/calcmetric_title_description.png)

1. Fügen Sie in einer Freiformtabelle die Dimension &quot;Tag&quot;hinzu. Fügen Sie &quot;Besuche&quot;und Ihre berechnete Metrik als Spalten nebeneinander hinzu.

   ![Freiformtabelle](assets/calcmetric_freeform.png)

1. Klicken Sie auf das Zahnradsymbol für die Spalteneinstellungen für die berechnete Metrik und aktivieren Sie die Option **[!UICONTROL Null als keinen Wert auffassen]**.

   ![Einstellungen für berechnete Metriken](assets/calcmetric_zero_no_value.png)

1. Eine Linienvisualisierung hinzufügen. Betroffene Tage werden mit einer anderen Farbe dargestellt. Benutzer können auch auf das Symbol &quot;Info&quot;in der berechneten Metrik klicken, um weitere Informationen zu erhalten.

   ![Infosymbol](assets/calcmetric_infoicon.png)

