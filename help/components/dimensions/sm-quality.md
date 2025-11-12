---
title: Qualitätsdimensionen der Streaming-Mediendienste
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: e3794d8c-3c03-425d-850c-a735b579324b
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 2%

---

# Qualitätsdimensionen der Streaming-Mediendienste

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren. Unter [Qualitätsmetriken für Streaming](../metrics/sm-quality.md)Mediendienste) finden Sie verfügbare Metriken.*

Qualitätsdimensionen von Streaming-Mediendiensten bieten Berichte in Bezug auf die Qualität der Inhalte, die der Besucher konsumiert. Für die Verwendung dieser Dimensionen ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Medienqualität]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Dimensionsname | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Durchschnittliche Bitrate]** | Die durchschnittliche Bitrate in Bucket-Intervallen von 100 Kbit/s. Er wird als gewichteter Durchschnitt aller Bitratenwerte in Bezug auf die Wiedergabedauer für eine bestimmte Wiedergabesitzung berechnet. | Schließen von Medien | `a.media.qoe.`<br>`bitrateAverageBucket` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`bitrate`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bitrateAverageBucket` |
| **[!UICONTROL Bitratenänderungen]** | Die Anzahl der Bitratenänderungen, die während einer Wiedergabesitzung aufgetreten sind. | Schließen von Medien | `a.media.qoe.`<br>`bitrateChangeCount` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`bitrateChangeCount`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bitrateChangeCount` |
| **[!UICONTROL Pufferereignisse]** | Die Häufigkeit, mit der der Media Player während einer Wiedergabesitzung in einen Pufferstatus übergegangen ist. | Schließen von Medien | `a.media.qoe.`<br>`bufferCount` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bufferCount` |
| **[!UICONTROL Gesamtdauer des Puffers]** | Die Gesamtdauer der Pufferung in Sekunden. | Schließen von Medien | `a.media.qoe.`<br>`bufferTime` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`bufferTime` |
| **[!UICONTROL Dropped Frames]** | Die Gesamtzahl der ausgelassenen Frames, die während einer Wiedergabesitzung aufgetreten sind. | Schließen von Medien | `a.media.qoe.`<br>`droppedFrameCount` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`droppedFrames`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`droppedFrames` |
| **[!UICONTROL Fehler]** | Die Gesamtzahl der Fehler, die während einer Wiedergabesitzung aufgetreten sind. | Schließen von Medien | `a.media.qoe.`<br>`errorCount` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`errorCount` |
| **[!UICONTROL Externe Fehler-IDs]** | Alle eindeutigen Fehler-IDs von einer externen Quelle, z. B. CDN-Fehler. Sie müssen die gewünschten Fehler-Codes oder IDs angeben. Mehrere Fehler-IDs sind zulässig. | Schließen von Medien | `a.media.qoe.`<br>`externalErrors` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`externalErrors` |
| **[!UICONTROL Player SDK-Fehler-IDs]** | Alle eindeutigen Fehler-IDs, die vom Content Player SDK generiert werden. Sie müssen die gewünschten Fehler-Codes oder IDs angeben. Mehrere Fehler-IDs sind zulässig. | Schließen von Medien | `a.media.qoe.`<br>`playerSdkErrors` | `xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`playerSdkErrors` |
| **[!UICONTROL Zeit bis zum Start]** | Dieser Wert ist standardmäßig auf `0` festgelegt, wenn er nicht über das QoSObject festgelegt wird. Legen Sie den Wert in Millisekunden fest. Analysis Workspace meldet diese Dimension in Sekunden. | Medienstart, Medienschluss | `a.media.qoe.`<br>`timeToStart` | `xdm.mediaCollection.`<br>`qoeDataDetails.`<br>`timeToStart`<br><br>`xdm.mediaReporting.`<br>`qoeDataDetails.`<br>`timeToStart` |
