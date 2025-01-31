---
description: Verwenden Sie die Map-Visualisierung in einem Workspace-Projekt.
title: Zuordnung
uuid: 6038f336-62a3-4efa-8316-4d7792468db3
feature: Visualizations
role: User, Admin
exl-id: a60544b4-27b6-413a-96ce-ab9487594422
source-git-commit: e0d14f6dd7be438f3dad979abcfc279e710873e7
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 60%

---

# Zuordnung {#map}

<!-- markdownlint-disable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_button"
>title="Zuordnung"
>abstract="Diese Visualisierung stellt Metriken dar, indem sie sie auf einer Karte überlagert. Diese Visualisierung ist nützlich, um Daten über verschiedene geografische Regionen hinweg zu identifizieren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_bubbles"
>title="Blasen"
>abstract="Plotten Sie Ereignisse mithilfe von Blasen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_map_heatmap"
>title="Heatmap"
>abstract="Plotten Sie Ereignisse mithilfe einer Heatmap."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_In diesem Artikel wird die Zuordnungsvisualisierung in {_} ![Adobe Analytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**._<br/>_Derzeit ist keine Zuordnungsvisualisierung in {_}![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**._

>[!ENDSHADEBOX]



Die ![Globe](/help/assets/icons/Globe.svg)**[!UICONTROL Map]** Visualisierung in Analysis Workspace

* Ermöglicht die Erstellung einer visuellen Zuordnung zu einer beliebigen Metrik (einschließlich berechneter Metriken),
* ist nützlich für die Identifizierung und den Vergleich von Metrikdaten über verschiedene geografische Regionen hinweg,
* kann zwei Datenquellen unterstützen: Breitengrad/Längengrad der mobilen Nutzung oder geografische Dimension für die Web-Nutzung,
* unterstützt den PDF-Export und
* nutzt WebGL für die Grafikanzeige. Wenn Ihre Grafiktreiber die WebGL-Ausgabe nicht unterstützen, müssen Sie Ihre Treiber unter Umständen aktualisieren.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Kartenvisualisierung in Analysis Workspace](https://video.tv.adobe.com/v/23559/?quality=12){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


## Verwenden

1. Fügen Sie eine Visualisierung ![Map](/help/assets/icons/Globe.svg) [!UICONTROL Map] hinzu. Siehe [Hinzufügen einer Visualisierung zu einem Bedienfeld](freeform-analysis-visualizations.md#add-visualizations-to-a-panel). Sie können eine Kartenvisualisierung nur auf eine Freiformtabelle ziehen.

   ![Konfiguration zuordnen](assets/map-configuration.png){width="50%"}

1. Wählen Sie aus den Dropdown-Listen eine Metrik aus. Oder ziehen Sie eine Metrik aus der Liste der Metriken (einschließlich berechneter Metriken).
1. Geben Sie die Datenquelle an, aus der Sie zeichnen möchten. Dieses Dialogfeld wird nur angezeigt, wenn das Standorttracking für Mobile-App-Daten aktiviert ist.

   | Quelle | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Mobiler Breitengrad/Längengrad]** | Diese Option stellt die Daten der Mobile App dar. Diese Option wird Ihnen nur angezeigt, wenn Sie sie für Ihre Report Suite unter [!UICONTROL Analytics] > [!UICONTROL Admin] > [!UICONTROL Report Suites] > (gewünschte Report Suite) > [!UICONTROL Einstellungen bearbeiten] >  [!UICONTROL Mobile Management] > [!UICONTROL Standortverfolgung aktivieren] aktiviert haben. Diese Einstellung ist die Standardeinstellung (wenn die Standortverfolgung aktiviert ist). |
   | **[!UICONTROL Geographische Dimension]** | Diese Option stellt anhand der IP-Adresse eines Besuchers gewonnene Geosegmentierungsdaten über seinen Standort dar. Diese Daten werden in [!UICONTROL Land], [!UICONTROL Region] und [!UICONTROL Stadt] umgewandelt. Beachten Sie, dass dies nicht bis zu den Ebenen „DMA“ oder „Postleitzahl“ reicht. Diese Dimension ist für beinahe alle Report Suites aktiviert. Wenn das bei Ihrer Report Suite nicht der Fall ist, bitten Sie die Adobe-Kundenunterstützung um Hilfe bei der Aktivierung geographischer Berichte. |

1. Wählen Sie **[!UICONTROL Erstellen]** aus.

   Es wird eine Weltkartenvisualisierung mit Blasen generiert.

   ![](assets/bubble-world-view.png)

1. Sie können jetzt:

   * die Landkarte **heranzoomen**, um bestimmte Bereiche zu vergrößern. Klicken Sie dazu doppelt auf die Landkarte oder nutzen Sie das Scrollrad. Die Landkarte wird an der Stelle herangezoomt, an der Sie den Cursor platziert haben. Durch die Zoom-Interaktion wird die erforderliche Dimension (Land > Bundesland > Stadt) basierend auf dem Zoomfaktor aktualisiert.
   * zwei oder mehr Map Visualizations im selben Projekt **vergleichen**. Platzieren Sie sie dazu nebeneinander.
   * **Zeitraumsvergleiche anzeigen (beispielsweise Jahresvergleiche)**:

      * Negative Zahlen anzeigen: Wenn Sie beispielsweise eine Metrik zum Jahresvergleich plotten, kann auf der Karte für New York -33 % angezeigt werden.
      * Bei Metriken vom Typ *Prozent* errechnet sich der Durchschnitt der Prozentsätze durch Clustering.
      * Grünes/rotes Farbschema: Positiv/negativ

   * die Landkarte in 2D oder 3D **drehen**. Halten Sie dazu die Taste [!UICONTROL Strg] gedrückt und verschieben Sie die Landkarte.

   * **Umschalten** auf eine andere Ansicht wie die Heatmap. Nehmen Sie dazu die unten beschriebenen [Einstellungen](/help/analyze/analysis-workspace/visualizations/map-visualization.md#section_5F89C620A6AA42BC8E0955478B3A427E) vor. Beachten Sie, dass die Blasendiagramm-Ansicht die Standardeinstellung ist.

1. **Speichern** Sie das Projekt, um alle Einstellungen an der Landkarte zu speichern (Koordinaten, Zoom, Drehung).
1. Die Freiformtabelle unterhalb der Visualisierung kann ausgefüllt werden, indem Standortdimensionen und Metriken aus der linken Leiste gezogen werden.



## Konfigurieren

Um die Kartenvisualisierung neu zu konfigurieren, wählen Sie ![Bearbeiten](/help/assets/icons/Edit.svg) aus.


## Einstellungen

Um Einstellungen für die Visualisierung zu definieren, wählen Sie ![Einstellung](/help/assets/icons/Setting.svg) aus.

| Einstellung | Beschreibung |
|--- |--- |
| **[!UICONTROL Zuordnungstyp]** | |
| [!UICONTROL Blasen] | Plottet Ereignisse mithilfe von Blasen. Ein Blasendiagramm ist ein multivariables Diagramm, das eine Kreuzung aus Streudiagramm und proportionalem Flächendiagramm darstellt. Diese Ansicht ist die Standardansicht. |
| Heatmap | Plottet Ereignisse mithilfe einer Heatmap. Eine Heatmap ist eine graphische Darstellung von Daten, bei der die individuellen Werte in einer Matrix als Farben dargestellt werden. |
| **[!UICONTROL Stile]** | |
| [!UICONTROL Farbschema] | Zeigt das Farbschema für die Heatmap und die Blasen. Sie können zwischen Korallenrot, Rot, Grün oder Blau auswählen. Die Standardeinstellung ist Coral. |
| [!UICONTROL Zuordnungsstil] | Sie können zwischen Basic, Streets, Bright, Light, Dark und Satellite wählen. |
| **[!UICONTROL Cluster-Radius]** | Gruppiert Datenpunkte, die sich innerhalb der festgelegten Pixelanzahl befinden. Die Standardeinstellung ist „50“. |
| **[!UICONTROL Benutzerdefinierter Maximalwert]** | Ermöglicht es Ihnen, die Schwelle für den Maximalwert für die Zuordnung zu verändern. Wird dieser Wert angepasst, ändert sich auch die Skala für die Werte der Blasen/Heatmap (Farbe und Größe) relativ zum festgelegten Maximalwert. |

<!--
## Build a time-parting heatmap

Here is a video on the topic:

>[!VIDEO](https://video.tv.adobe.com/v/26991/?quality=12)

-->

