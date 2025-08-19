---
title: Qualitätsmetriken für Streaming-Mediendienste
description: Verfügbare Metriken, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren.
feature: Metrics
exl-id: a64829b5-d45b-44c6-80c3-5acf1a6d9919
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 1%

---

# Qualitätsmetriken für Streaming-Mediendienste

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren. Siehe [Qualitätsdimensionen von Streaming-](../dimensions/sm-quality.md)-Services“ für verfügbare Dimensionen.*

Qualitätsmetriken für Streaming-Mediendienste bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Bibliotheken für Streaming-Mediendienste. Für die Verwendung dieser Metriken ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Medienqualität]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Durchschnittliche Bitrate | Ein gewichteter Durchschnitt aller Bitratenwerte für die Wiedergabedauer einer Wiedergabesitzung. | Schließen von Medien | `a.media.qoe.bitrateAverage` |
| Von Bitratenänderung betroffene Streams | Ein boolescher Wert, der Trigger wird, wenn sich die Bitrate während einer Wiedergabesitzung mindestens einmal ändert. | Schließen von Medien | `a.media.qoe.bitrateChange` |
| Änderungen der Bitrate | Die Häufigkeit, mit der die Bitrate geändert wurde. | Schließen von Medien | `a.media.qoe.bitrateChangeCount` |
| Vom Puffer betroffene Streams | Ein boolescher Wert, der Trigger wird, wenn das Video mindestens einmal in einen Pufferstatus übergeht. | Schließen von Medien | `a.media.qoe.buffer` |
| Pufferereignisse | Die Häufigkeit, mit der das Video während einer Wiedergabesitzung gepuffert wurde. | Schließen von Medien | `a.media.qoe.bufferCount` |
| Gesamtdauer des Puffers | Die Zeit in Sekunden, die ein Video mit der Pufferung aller Pufferereignisse verbracht hat. | Schließen von Medien | `a.media.qoe.bufferTime` |
| Drops vor dem Start | Ein boolescher Wert, der den Trigger hat, wenn ein Benutzer beendet wird, bevor der Hauptinhalt eines Videos beginnt. | Schließen von Medien | `a.media.qoe.dropBeforeStart` |
| Abgelegte Frames | Eine Ganzzahl, die die Gesamtzahl der Frames angibt, die während einer Wiedergabesitzung gelöscht wurden. | Schließen von Medien | `a.media.qoe.droppedFrameCount` |
| Von Dropped Frames betroffene Streams | Ein boolescher Wert, der beim Ablegen von Frames während einer Wiedergabesitzung Trigger erzeugt. | Schließen von Medien | `a.media.qoe.droppedFrames` |
| Von Fehlern betroffene Streams | Ein boolescher Wert, der Trigger wird, wenn ein Video während einer Wiedergabesitzung zu einem beliebigen Zeitpunkt einen Fehler aufweist. | Schließen von Medien | `a.media.qoe.error` |
| Fehlerereignisse | Eine Ganzzahl, die die Gesamtzahl der während einer Wiedergabesitzung aufgetretenen Fehler darstellt. | Schließen von Medien | `a.media.qoe.errorCount` |
| Zeit bis zum Start | Die Zeit in Millisekunden, die zum Starten eines Videos benötigt wird. Adobe konvertiert diesen Wert und speichert ihn in Sekunden. | Schließen von Medien | `a.media.qoe.timeToStart` |
