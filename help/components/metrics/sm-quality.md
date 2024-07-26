---
title: Qualitätsmetriken für Streaming-Medien
description: Verfügbare Metriken, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren.
feature: Metrics
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# Qualitätsmetriken für Streaming-Medien

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren. Verfügbare Dimensionen finden Sie unter [Qualitätsdimensionen der Streaming-Medien](../dimensions/sm-quality.md) .*

Metriken zur Qualität von Streaming-Medien bieten zusätzliche Berichtsfunktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Metriken ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medienqualität]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Durchschnittliche Bitrate | Ein gewichteter Durchschnitt aller Bitratenwerte für die Wiedergabedauer einer Wiedergabesitzung. | Media Close | `a.media.qoe.bitrateAverage` |
| Von Bitratenänderungen betroffene Streams | Ein boolescher Wert, der Trigger, wenn sich die Bitrate während einer Wiedergabesitzung mindestens einmal ändert. | Media Close | `a.media.qoe.bitrateChange` |
| Bitratenänderungen | Die Häufigkeit, mit der sich die Bitrate geändert hat. | Media Close | `a.media.qoe.bitrateChangeCount` |
| Von Puffer betroffene Streams | Ein boolescher Wert, der Trigger, wenn das Video mindestens einmal in den Pufferstatus wechselt. | Media Close | `a.media.qoe.buffer` |
| Pufferereignisse | Die Häufigkeit, mit der das Video während einer Wiedergabesitzung gepuffert wurde. | Media Close | `a.media.qoe.bufferCount` |
| Gesamtpufferdauer | Die Zeit, die ein Video über alle Pufferereignisse hinweg gepuffert hat, in Sekunden. | Media Close | `a.media.qoe.bufferTime` |
| Drops vor Start | Ein boolescher Wert, der Trigger, wenn ein Anwender den Vorgang beendet, bevor der Hauptinhalt eines Videos beginnt. | Media Close | `a.media.qoe.dropBeforeStart` |
| Dropped Frames | Eine Ganzzahl, die die Gesamtzahl der Frames darstellt, die während einer Wiedergabesitzung abgelegt wurden. | Media Close | `a.media.qoe.droppedFrameCount` |
| Von Dropped Frames betroffene Streams | Ein boolescher Wert, der Trigger, wenn Frames während einer Wiedergabesitzung abgelegt werden. | Media Close | `a.media.qoe.droppedFrames` |
| Von Fehlern betroffene Streams | Ein boolescher Wert, der Trigger, wenn ein Video während einer Wiedergabesitzung jederzeit einen Fehler auftritt. | Media Close | `a.media.qoe.error` |
| Fehlerereignisse | Eine Ganzzahl, die die Gesamtzahl der während einer Wiedergabesitzung aufgetretenen Fehler darstellt. | Media Close | `a.media.qoe.errorCount` |
| Startzeit | Die zum Starten eines Videos benötigte Zeit in Millisekunden. Adobe konvertiert diesen Wert und speichert ihn in Sekunden. | Media Close | `a.media.qoe.timeToStart` |
