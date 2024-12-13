---
title: Kernmetriken für Streaming-Medien
description: Verfügbare Metriken bei Aktivierung von [!UICONTROL Media Core] für eine Report Suite.
feature: Metrics
exl-id: f4ff5f84-18b6-4e67-b808-133faeaf8605
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 1%

---

# Kernmetriken für Streaming-Medien

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren. Siehe [Kerndimensionen von Streaming-Medien](../dimensions/sm-core.md) für verfügbare Dimensionen.*

Kernmetriken für Streaming-Medien bieten grundlegende Reporting-Funktionen für Daten, die über Streaming-Mediensammlungsbibliotheken erfasst werden. Für die Verwendung dieser Metriken ist die Sammlung **[!UICONTROL Adobe-Streaming-Medien erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Media Core]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Zielgruppendurchschnitt pro Minute | Die Gesamtdauer, die mit einem bestimmten Inhaltselement verbracht wurde, dividiert durch die Länge seiner gesamten Wiedergabesitzungen.<br>`[Time spent] / [Media length]` | Schließen von Medien | `a.media.averageMinuteAudience` |
| Inhalt abgeschlossen | Trigger, wenn ein Teil des Inhalts abgeschlossen ist. Diese Metrik bedeutet nicht unbedingt, dass sie den gesamten Inhalt angezeigt haben. Sie hätten auch vorgesprungen sein können. Das bedeutet nur, dass sie das Ende des Inhalts erreicht haben. | `a.media.complete` |
| Betroffene Streams angehalten | Ein boolescher Wert, der einen Trigger erzeugt, wenn während der Wiedergabe von Inhalten eine oder mehrere Pausen aufgetreten sind. | Schließen von Medien | `a.media.pause` |
| Ereignisse anhalten | Die Anzahl der Pausen, die während einer Wiedergabesitzung aufgetreten sind. | Schließen von Medien | `a.media.pauseCount` |
| Gesamte Pausendauer | Die Gesamtdauer aller Pausenereignisse in Sekunden. | Schließen von Medien | `a.media.pauseTime` |
| Inhaltsstarts | Der erste Frame von Medien wird genutzt. Wenn ein(e) Benutzende(r) während einer Anzeige oder während der Pufferung abfällt, tritt bei diesem Ereignis kein Trigger auf. | Schließen von Medien | `a.media.play` |
| 10%-Fortschrittsmarkierung | Der Abspielkopf übergibt die 10-%-Markierung des Inhalts basierend auf der Länge. Diese Markierung wird nur einmal gezählt, auch wenn rückwärts gesucht wird. Bei der Suche nach vorwärts werden übersprungene Markierungen nicht gezählt. | Schließen von Medien | `a.media.progress10` |
| 25%-Fortschrittsmarkierung | Der Abspielkopf übergibt die 25-%-Markierung des Inhalts basierend auf der Länge. Diese Markierung wird nur einmal gezählt, auch wenn rückwärts gesucht wird. Bei der Suche nach vorwärts werden übersprungene Markierungen nicht gezählt. | Schließen von Medien | `a.media.progress25` |
| 50%-Fortschrittsmarkierung | Der Abspielkopf übergibt die 50-%-Markierung des Inhalts basierend auf der Länge. Diese Markierung wird nur einmal gezählt, auch wenn rückwärts gesucht wird. Bei der Suche nach vorwärts werden übersprungene Markierungen nicht gezählt. | Schließen von Medien | `a.media.progress50` |
| 75%-Fortschrittsmarkierung | Der Abspielkopf übergibt die 75-%-Markierung des Inhalts basierend auf der Länge. Diese Markierung wird nur einmal gezählt, auch wenn rückwärts gesucht wird. Bei der Suche nach vorwärts werden übersprungene Markierungen nicht gezählt. | Schließen von Medien | `a.media.progress75` |
| 95%-Fortschrittsmarkierung | Der Abspielkopf übergibt die 95-%-Markierung des Inhalts basierend auf der Länge. Diese Markierung wird nur einmal gezählt, auch wenn rückwärts gesucht wird. Bei der Suche nach vorwärts werden übersprungene Markierungen nicht gezählt. | Schließen von Medien | `a.media.progress95` |
| Inhaltswiederaufnahmen | Ein boolescher Wert, der beim Fortsetzen von Inhalten nach mehr als 30 Minuten Puffer-, Pause- oder Anhaltezeit Trigger wird. Auch Trigger, wenn vom Player auf dem VideoInfo-TrackPlay festgelegt. | Schließen von Medien | `a.media.resume` |
| Ansichten des Inhaltssegments | Ein boolescher Wert, der beim ersten Frame des angezeigten Segments Trigger wird. | Schließen von Medien | `a.media.segmentView` |
| Medienstarts | Ein boolescher Wert, der beim ersten Laden des Mediums Trigger wird. Dieses Ereignis umfasst Anzeigen, Pufferung und Fehler. | Medienstart | `a.media.view` |
| Besuchszeit für Inhalt | Die gesamte Ereignisdauer für alle Ereignisse des Typs WIEDERGABE im Hauptinhalt in Sekunden. | Schließen von Medien | `a.media.timePlayed` |
| Eindeutige Wiedergabedauer | Die Gesamtdauer, wie lange der eindeutige Inhalt wiedergegeben wird, in Sekunden. Diese Metrik schließt die Zeit aus, die bei der Anzeige wiederholter Inhalte wiedergegeben wird, z. B. bei der Rückwärtssuche. | Schließen von Medien | `a.media.uniqueTimePlayed` |

{style="table-layout:auto"}
