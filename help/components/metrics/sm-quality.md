---
title: Qualitätsmetriken für Streaming-Mediendienste
description: Verfügbare Metriken, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren.
feature: Metrics
exl-id: a64829b5-d45b-44c6-80c3-5acf1a6d9919
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 2%

---

# Qualitätsmetriken für Streaming-Mediendienste

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren. Siehe [Qualitätsdimensionen von Streaming-](../dimensions/sm-quality.md)-Services“ für verfügbare Dimensionen.*

Qualitätsmetriken für Streaming-Mediendienste bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Bibliotheken für Streaming-Mediendienste. Für die Verwendung dieser Metriken ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Medienqualität]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Durchschnittliche Bitrate]** | Ein gewichteter Durchschnitt aller Bitratenwerte für die Wiedergabedauer einer Wiedergabesitzung. | Schließen von Medien | `a.media.qoe.`<br>`bitrateAverage` | `xdm.mediaReporting.`<br>`qoeDataDetails.bitrateAverage` |
| **[!UICONTROL Von Bitratenänderung betroffene Streams]** | Ein boolescher Wert, der Trigger wird, wenn sich die Bitrate während einer Wiedergabesitzung mindestens einmal ändert. | Schließen von Medien | `a.media.qoe.`<br>`bitrateChange` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`hasBitrateChangeImpactedStreams` |
| **[!UICONTROL Bitratenänderungen]** | Die Häufigkeit, mit der die Bitrate geändert wurde. | Schließen von Medien | `a.media.qoe.`<br>`bitrateChangeCount` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`bitrateChangeCount`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bitrateChangeCount` |
| **[!UICONTROL Vom Puffer betroffene Streams]** | Ein boolescher Wert, der Trigger wird, wenn das Video mindestens einmal in einen Pufferstatus übergeht. | Schließen von Medien | `a.media.qoe.`<br>`buffer` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`hasBufferImpactedStreams` |
| **[!UICONTROL Pufferereignisse]** | Die Häufigkeit, mit der das Video während einer Wiedergabesitzung gepuffert wurde. | Schließen von Medien | `a.media.qoe.`<br>`bufferCount` | `xdm.mediaReporting.`<br>`qoeDataDetails.bufferCount` |
| **[!UICONTROL Gesamtdauer des Puffers]** | Die Zeit in Sekunden, die ein Video mit der Pufferung aller Pufferereignisse verbracht hat. | Schließen von Medien | `a.media.qoe.`<br>`bufferTime` | `xdm.mediaReporting.`<br>`qoeDataDetails.bufferTime` |
| **[!UICONTROL Drops vor dem Start]** | Ein boolescher Wert, der den Trigger hat, wenn ein Benutzer beendet wird, bevor der Hauptinhalt eines Videos beginnt. | Schließen von Medien | `a.media.qoe.`<br>`dropBeforeStart` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`isDroppedBeforeStart` |
| **[!UICONTROL Dropped Frames]** | Eine Ganzzahl, die die Gesamtzahl der Frames angibt, die während einer Wiedergabesitzung gelöscht wurden. | Schließen von Medien | `a.media.qoe.`<br>`droppedFrameCount` | `xdm.mediaCollection.`<br>`qoeDataDetails.droppedFrames`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.droppedFrames` |
| **[!UICONTROL Von Dropped Frames betroffene Streams]** | Ein boolescher Wert, der beim Ablegen von Frames während einer Wiedergabesitzung Trigger erzeugt. | Schließen von Medien | `a.media.qoe.`<br>`droppedFrames` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`hasDroppedFrameImpactedStreams` |
| **[!UICONTROL Von Fehlern betroffene Streams]** | Ein boolescher Wert, der Trigger wird, wenn ein Video während einer Wiedergabesitzung zu einem beliebigen Zeitpunkt einen Fehler aufweist. | Schließen von Medien | `a.media.qoe.`<br>`error` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`hasErrorImpactedStreams` |
| **[!UICONTROL Fehlerereignisse]** | Eine Ganzzahl, die die Gesamtzahl der während einer Wiedergabesitzung aufgetretenen Fehler darstellt. | Schließen von Medien | `a.media.qoe.`<br>`errorCount` | `xdm.mediaReporting.`<br>`qoeDataDetails.errorCount` |
| **[!UICONTROL Zeit bis zum Start]** | Die Zeit in Millisekunden, die zum Starten eines Videos benötigt wird. Adobe konvertiert diesen Wert und speichert ihn in Sekunden. | Schließen von Medien | `a.media.qoe.`<br>`timeToStart` | `xdm.mediaCollection.`<br>`qoeDataDetails.timeToStart`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.timeToStart` |
