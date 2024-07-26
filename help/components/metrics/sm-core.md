---
title: Hauptmetriken der Streaming-Medien
description: Verfügbare Metriken, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren.
feature: Metrics
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 1%

---

# Hauptmetriken der Streaming-Medien

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren. Verfügbare Dimensionen finden Sie unter [ Core-Dimensionen für Streaming-Medien](../dimensions/sm-core.md) .*

Die Kernmetriken von Streaming-Medien bieten grundlegende Berichtsfunktionen für Daten, die über Streaming-Mediensammlungsbibliotheken erfasst werden. Für die Verwendung dieser Metriken ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medien-Core]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Durchschnittliche Minutenzielgruppe | Die Gesamtdauer, die für ein bestimmtes Inhaltselement verbracht wurde, dividiert durch seine Länge für alle zugehörigen Wiedergabesitzungen.<br>`[Time spent] / [Media length]` | Media Close | `a.media.averageMinuteAudience` |
| Inhalt abgeschlossen | Trigger, wenn ein Inhaltselement abgeschlossen ist. Diese Metrik bedeutet nicht unbedingt, dass sie die Gesamtheit des Inhalts angesehen hat; sie hätte vorausspringen können. Das bedeutet nur, dass sie das Ende des Inhalts erreicht haben. | `a.media.complete` |
| Betroffene Streams pausiert | Ein boolescher Wert, der Trigger, wenn eine oder mehrere Pausen während der Wiedergabe des Inhalts aufgetreten sind. | Media Close | `a.media.pause` |
| Pausierung - Ereignisse | Die Anzahl der Pausen, die während einer Wiedergabesitzung aufgetreten sind. | Media Close | `a.media.pauseCount` |
| Pausierung - Gesamtdauer | Die Gesamtdauer aller Pausenereignisse in Sekunden. | Media Close | `a.media.pauseTime` |
| Inhaltsstarts | Der erste Frame des Mediums wird wiedergegeben. Wenn ein Benutzer während einer Anzeige oder während der Pufferung abbricht, wird dieses Ereignis nicht Trigger. | Media Close | `a.media.play` |
| Fortschrittsmarkierung von 10 % | Die Abspielleiste überspringt die 10%-Markierung basierend auf der Länge des Inhalts. Diese Markierung wird nur einmal gezählt, auch wenn eine rückwärts gerichtete Suche stattfindet. Bei der Suche nach vorn werden übersprungene Markierungen nicht gezählt. | Media Close | `a.media.progress10` |
| Fortschrittsmarkierung von 25 % | Die Abspielleiste überspringt die 25%-Markierung basierend auf der Länge des Inhalts. Diese Markierung wird nur einmal gezählt, auch wenn eine rückwärts gerichtete Suche stattfindet. Bei der Suche nach vorn werden übersprungene Markierungen nicht gezählt. | Media Close | `a.media.progress25` |
| Fortschrittsmarkierung von 50 % | Die Abspielleiste überspringt die 50%-Markierung basierend auf der Länge des Inhalts. Diese Markierung wird nur einmal gezählt, auch wenn eine rückwärts gerichtete Suche stattfindet. Bei der Suche nach vorn werden übersprungene Markierungen nicht gezählt. | Media Close | `a.media.progress50` |
| 75 % Fortschrittsmarkierung | Die Abspielleiste überspringt die 75%-Markierung basierend auf der Länge des Inhalts. Diese Markierung wird nur einmal gezählt, auch wenn eine rückwärts gerichtete Suche stattfindet. Bei der Suche nach vorn werden übersprungene Markierungen nicht gezählt. | Media Close | `a.media.progress75` |
| 95% Fortschrittsmarkierung | Die Abspielleiste überspringt die 95%-Markierung basierend auf der Länge des Inhalts. Diese Markierung wird nur einmal gezählt, auch wenn eine rückwärts gerichtete Suche stattfindet. Bei der Suche nach vorn werden übersprungene Markierungen nicht gezählt. | Media Close | `a.media.progress95` |
| Wiederaufnahme von Inhalten | Ein boolescher Wert, der Trigger, wenn der Inhalt nach mehr als 30 Minuten Pufferzeit, Pausierung oder Unterbrechung wieder aufgenommen wird. Auch Trigger, wenn sie vom Player auf der VideoInfo trackPlay festgelegt werden. | Media Close | `a.media.resume` |
| Ansichten von Inhaltssegmenten | Ein boolescher Wert, der im ersten Frame des angezeigten Segments Trigger wird. | Media Close | `a.media.segmentView` |
| Medienstarts | Ein boolescher Wert, der beim ersten Laden des Mediums Trigger wird. Dieses Ereignis umfasst Anzeigen, Pufferung und Fehler. | Medienstart | `a.media.view` |
| Inhaltsdauer | Die Gesamtdauer des Ereignisses für alle Ereignisse des Typs &quot;PLAY&quot;im Hauptinhalt in Sekunden. | Media Close | `a.media.timePlayed` |
| Eindeutige Wiedergabedauer | Die Gesamtdauer der Wiedergabe des eindeutigen Inhalts in Sekunden. Diese Metrik schließt die Zeit aus, die bei der Anzeige von wiederholten Inhalten, z. B. der rückwärts gerichteten Suche, abgespielt wird. | Media Close | `a.media.uniqueTimePlayed` |

{style="table-layout:auto"}
