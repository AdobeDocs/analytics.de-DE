---
title: Kernmetriken für Streaming-Mediendienste
description: Verfügbare Metriken bei Aktivierung von [!UICONTROL Media Core] für eine Report Suite.
feature: Metrics
exl-id: f4ff5f84-18b6-4e67-b808-133faeaf8605
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# Kernmetriken für Streaming-Mediendienste

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Media Core] für eine Report Suite aktivieren. Verfügbare Dimensionen finden Sie [Kerndimensionen ](../dimensions/sm-core.md) Streaming-Mediendienste)*

Kernmetriken für Streaming-Mediendienste bieten grundlegende Reporting-Funktionen für Daten, die über Sammlungsbibliotheken von Streaming-Mediendiensten erfasst werden. Für die Verwendung dieser Metriken ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Media Core]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Zielgruppendurchschnitt pro Minute]** | Die Gesamtdauer, die mit einem bestimmten Inhaltselement verbracht wurde, dividiert durch die Länge seiner gesamten Wiedergabesitzungen.<br>`[Time spent] / [Media length]` | Schließen von Medien | `a.media.`<br>`averageMinuteAudience` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`averageMinuteAudience` |
| **[!UICONTROL Inhalt abgeschlossen]** | Trigger, wenn ein Teil des Inhalts abgeschlossen ist. Diese Metrik bedeutet nicht unbedingt, dass sie den gesamten Inhalt angezeigt haben. Sie hätten auch vorgesprungen sein können. Das bedeutet nur, dass sie das Ende des Inhalts erreicht haben. | | `a.media.complete` | `xdm.mediaReporting.`<br>`sessionDetails.isCompleted` |
| **[!UICONTROL Betroffene Streams angehalten]** | Ein boolescher Wert, der einen Trigger erzeugt, wenn während der Wiedergabe von Inhalten eine oder mehrere Pausen aufgetreten sind. | Schließen von Medien | `a.media.pause` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`hasPauseImpactedStreams` |
| **[!UICONTROL Ereignisse anhalten]** | Die Anzahl der Pausen, die während einer Wiedergabesitzung aufgetreten sind. | Schließen von Medien | `a.media.pauseCount` | `xdm.mediaReporting.`<br>`sessionDetails.pauseCount` |
| **[!UICONTROL Pausierung insgesamt]** | Die Gesamtdauer aller Pausenereignisse in Sekunden. | Schließen von Medien | `a.media.pauseTime` | `xdm.mediaReporting.`<br>`sessionDetails.pauseTime` |
| **[!UICONTROL Inhaltsstarts]** | Der erste Frame von Medien wird genutzt. Wenn ein(e) Benutzende(r) während einer Anzeige oder während der Pufferung abfällt, tritt bei diesem Ereignis kein Trigger auf. | Schließen von Medien | `a.media.play` | `xdm.mediaReporting.`<br>`sessionDetails.isPlayed` |
| **[!UICONTROL 10 % Fortschrittsmarkierung]**<br>**[!UICONTROL 25 % Fortschrittsmarkierung]**<br>**[!UICONTROL 50 % Fortschrittsmarkierung]**<br>**[!UICONTROL 75 % Fortschrittsmarkierung]**<br>**[!UICONTROL 95 % Fortschrittsmarkierung]** | Der Abspielkopf übergibt die angegebene Inhaltsmarkierung basierend auf der Länge. Jede Markierung wird nur einmal gezählt, auch wenn rückwärts gesucht wird. Bei der Suche nach vorwärts werden übersprungene Markierungen nicht gezählt. | Schließen von Medien | `a.media.progress10`<br>`a.media.progress25`<br>`a.media.progress50`<br>`a.media.progress75`<br>`a.media.progress95` | `xdm.mediaReporting.`<br>`sessionDetails.hasProgress10`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress25`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress50`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress75`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasProgress95` |
| **[!UICONTROL Inhaltswiederaufnahmen]** | Ein boolescher Wert, der beim Fortsetzen von Inhalten nach mehr als 30 Minuten Puffer-, Pause- oder Anhaltezeit Trigger wird. Auch Trigger, wenn vom Player auf dem VideoInfo-TrackPlay festgelegt. | Schließen von Medien | `a.media.resume` | `xdm.mediaCollection.`<br>`sessionDetails.hasResume`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.hasResume` |
| **[!UICONTROL Inhaltssegmentansichten]** | Ein boolescher Wert, der beim ersten Frame des angezeigten Segments Trigger wird. | Schließen von Medien | `a.media.segmentView` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`hasSegmentView` |
| **[!UICONTROL Medienstarts]** | Ein boolescher Wert, der beim ersten Laden des Mediums Trigger wird. Dieses Ereignis umfasst Anzeigen, Pufferung und Fehler. | Medienstart | `a.media.view` | `xdm.mediaReporting.`<br>`sessionDetails.isViewed` |
| **[!UICONTROL Besuchszeit für Inhalt]** | Die gesamte Ereignisdauer für alle Ereignisse des Typs WIEDERGABE im Hauptinhalt in Sekunden. | Schließen von Medien | `a.media.timePlayed` | `xdm.mediaReporting.`<br>`sessionDetails.timePlayed` |
| **[!UICONTROL Eindeutige Wiedergabezeit]** | Die Gesamtdauer, wie lange der eindeutige Inhalt wiedergegeben wird, in Sekunden. Diese Metrik schließt die Zeit aus, die bei der Anzeige wiederholter Inhalte wiedergegeben wird, z. B. bei der Rückwärtssuche. | Schließen von Medien | `a.media.`<br>`uniqueTimePlayed` | `xdm.mediaReporting.`<br>`sessionDetails.`<br>`uniqueTimePlayed` |
