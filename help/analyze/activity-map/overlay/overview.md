---
description: Erfahren Sie mehr über die Activity Map-Erweiterung und das Navigieren in ihrer Benutzeroberfläche.
title: Activity Map-Erweiterungsschnittstelle
uuid: f6734b60-0b77-4f50-a45a-6a6936d1524e
feature: Activity Map
role: User, Admin
exl-id: 461abda1-3238-4a32-b9d3-5a57b00cf0d3
source-git-commit: 19c2c1abd7f1799598597c0e696d0b001c1ef0ea
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%

---

# Activity Map-Erweiterungsschnittstelle

Die Activity Map-Erweiterungsschnittstelle besteht aus zwei Teilen:

* Ein oberes Bedienfeld, in dem Sie die Erweiterung und Berichte konfigurieren können
* Eine Überlagerung, die die beliebtesten Links anzeigt
* Ein unteres Bedienfeld mit Metriken zu den beliebtesten Links

## Oberes Bedienfeld

Das obere Bedienfeld enthält die grundlegenden Steuerelemente für die Activity Map-Überlagerung.

![Überlagerung](../assets/overlay.png)

Es bietet die folgenden Einstellungen:

* **Standard-/Live-**: Schaltet zwischen Standard- und Live-Ansicht um.
   * Standardansicht: Zeigt die Überlagerung basierend auf historischen Daten an.
   * Live-Ansicht: Zeigt die Überlagerung basierend auf Live-Daten an. Die Datumsauswahl wird zu einem Dropdown-Menü, über das Sie die Granularität von Live-Daten ändern können.
* **Metrikauswahl**: Ermöglicht das Ändern der Metrik, die von der Überlagerung gemeldet wird. Wenn [!UICONTROL  Live-Ansicht ausgewählt ], sind nur Link-Klicks verfügbar.
* **Segmentauswahl**: Ermöglicht die Auswahl eines [Segments](/help/components/segmentation/seg-overview.md), wobei eine Teilmenge der Daten in Ihrer Überlagerung angezeigt wird. Segmente sind in der Live-Ansicht nicht verfügbar.
* **Visualisierungstyp „Überlagerung**: Ermöglicht es Ihnen zu ändern, wie die Überlagerung das Ranking von Links visualisiert.
   * **[!UICONTROL Bubble]**: Top-Links erhalten eine grüne Blase, die ihren numerischen Rang während des Berichtszeitraums anzeigt. Sie können die Sprechblasenfarbe in „Einstellungen[ ändern](settings.md).
   * **[!UICONTROL Verlauf]**: Top-Links werden schattiert in transparentem Rot angezeigt. Die beliebtesten Links sind die dunkelsten rot. Sie können die Farbe des Farbverlaufs in [Einstellungen](settings.md) ändern.
   * **[!UICONTROL Aus]**: Deaktivieren von Linküberlagerungen.
* **Datumsauswahl**: Ermöglicht die Änderung des Berichtszeitraums.

Die Kopfzeile dieses Bedienfelds enthält die folgenden Einstellungen:

* **Oberes Bedienfeld ein-/ausblenden**: Blendet das obere Bedienfeld ein oder aus, um Einstellungen horizontal oder vertikal anzuzeigen (Doppelpfeil-Symbol).
* **[!UICONTROL Seitendetails ein/]**: Unteres Bedienfeld ein- oder ausblenden (Augensymbol).
* **[!UICONTROL Einstellungen anzeigen]**: Öffnet ein Menü für Einstellungen, die Sie ändern können (Zahnradsymbol):
   * **[!UICONTROL Einstellungen]**: Öffnet die Erweiterung &quot;[Einstellungen](settings.md).
   * **[!UICONTROL Hilfe]**: Öffnet die Dokumentation zu Experience League (auf dieser Seite).
   * **[!UICONTROL Adobe-]**: Öffnet die [Experience League-](https://experienceleaguecommunities.adobe.com/?profile.language=de).
   * **[!UICONTROL Info]**: Zeigt die Erweiterungsversion an.
   * **[!UICONTROL Abmelden]**: Meldet Sie von der Erweiterung ab und muss sich erneut anmelden.
* **[!UICONTROL Activity Map beenden]**: Schließt alle Überlagerungen für die Erweiterung (Symbol X).

## Seitenüberlagerung

Die Seitenüberlagerung enthält Ihre Website-Inhalte mit einer Überlagerung, die Ihnen den Speicherort der beliebtesten Links anzeigt, auf die während des Berichtszeitraums geklickt wurde. Sie können diese Link-Überlagerungen so konfigurieren, dass sie als Blasen oder Verläufe im Visualisierungstyp „Überlagerung **[!UICONTROL des oberen Bedienfelds angezeigt]**.

Wenn Sie auf eine Blase oder einen Verlauf klicken, können Sie Details zu diesem bestimmten Link anzeigen.

![Link-Blase](../assets/link-bubble.png)

## Unteres Bedienfeld

Das untere Bedienfeld zeigt eine aggregierte Ansicht der Links an, die auf der Überlagerung angezeigt werden.

* **Berichtstyp**: Schalten Sie das untere Bedienfeld ein, um den Bericht **[!UICONTROL Links auf Seite]** oder den Bericht **[!UICONTROL Seitendetails]** anzuzeigen.
* **[!UICONTROL Seitenname]**: Der Name der aktuellen [Seite](/help/components/dimensions/page.md)-Dimension.
* **[!UICONTROL Suche]**: Filtern Sie den Bericht so, dass nur die Link-Namen angezeigt werden, die dem eingegebenen Text entsprechen.
* **[!UICONTROL Herunterladen]**: Exportiert den Bericht in CSV-Datei. Sie können den Bericht [!UICONTROL Links auf Seite], den Bericht [!UICONTROL Seite] und den Bericht [!UICONTROL Seitenfluss] in dieselbe Download-Datei aufnehmen.
* **[!UICONTROL Andockposition des Berichts ändern]**: Blendet die Position dieses Bedienfelds ein oder aus, sodass es am unteren oder oberen Teil des Browser-Fensters angezeigt wird.
* **[!UICONTROL Bericht schließen]**: Schließt dieses Bedienfeld. Sie können das Bedienfeld erneut über die Schaltfläche **[!UICONTROL Seitendetails umschalten]** im oberen Bedienfeld öffnen (Augensymbol).

Der **[!UICONTROL Links auf Seite]** Bericht zeigt einen grundlegenden Arbeitsbereichsbericht mit den folgenden Einstellungen:

* Die Dimension [Activity Map](/help/components/dimensions/activity-map-link.md)Link
* Die Metrik [Vorfälle](/help/components/metrics/occurrences.md) (beschriftet als **[!UICONTROL Link-Klicks]**)
* Der aktuelle [Page](/help/components/dimensions/page.md)-Wert, der als Segment angewendet wird

![Links im Seitenbedienfeld](../assets/links-on-page.png)

Der **[!UICONTROL Seitendetails]**-Bericht zeigt eine [Fluss](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)-Visualisierung mithilfe der Dimension [Seite](/help/components/dimensions/page.md) an, wobei der Fokus auf der aktuellen Seite liegt. Die folgenden Metriken für die aktuelle Seite werden auf der linken Seite angezeigt:

* [Seitenansichten](/help/components/metrics/page-views.md)
* [!UICONTROL  % aller Seitenansichten]
* [Eintritt](/help/components/metrics/entries.md) Anzahl
* [Beenden](/help/components/metrics/exits.md) Anzahl
* [Einzelseitenbesuche](/help/components/metrics/single-page-visits.md)
* [!UICONTROL Durchschn. Klicks auf Seite]
* Durchschn[Besuchszeit pro Seite](/help/components/metrics/time-spent.md)
* Anzahl der [Reloads](/help/components/metrics/reloads.md)
* [Absprungrate](/help/components/metrics/bounce-rate.md)
* [!UICONTROL Link-Klicks]

![Seitendetails](../assets/page-details.png)
