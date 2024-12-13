---
title: Qualitätsdimensionen von Streaming-Medien
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: e3794d8c-3c03-425d-850c-a735b579324b
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---

# Qualitätsdimensionen von Streaming-Medien

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren. Unter [Qualitätsmetriken für Streaming-Medien](../metrics/sm-quality.md) finden Sie verfügbare Metriken.*

Qualitätsdimensionen von Streaming-Medien bieten Berichte in Bezug auf die Qualität der Inhalte, die der Besucher konsumiert. Für die Verwendung dieser Dimensionen ist die Sammlung [!UICONTROL Adobe-Streaming-Medien erforderlich]. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medienqualität]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Durchschnittliche Bitrate | Die durchschnittliche Bitrate in Bucket-Intervallen von 100 Kbit/s. Er wird als gewichteter Durchschnitt aller Bitratenwerte in Bezug auf die Wiedergabedauer für eine bestimmte Wiedergabesitzung berechnet. | Schließen von Medien | `a.media.qoe.bitrateAverageBucket` |
| Änderungen der Bitrate | Die Anzahl der Bitratenänderungen, die während einer Wiedergabesitzung aufgetreten sind. | Schließen von Medien | `a.media.qoe.bitrateChangeCount` |
| Pufferereignisse | Die Häufigkeit, mit der der Media Player während einer Wiedergabesitzung in einen Pufferstatus übergegangen ist. | Schließen von Medien | `a.media.qoe.bufferCount` |
| Gesamtdauer des Puffers | Die Gesamtdauer der Pufferung in Sekunden. | Schließen von Medien | `a.media.qoe.bufferTime` |
| Abgelegte Frames | Die Gesamtzahl der ausgelassenen Frames, die während einer Wiedergabesitzung aufgetreten sind. | Schließen von Medien | `a.media.qoe.droppedFrameCount` |
| Fehler | Die Gesamtzahl der Fehler, die während einer Wiedergabesitzung aufgetreten sind. | Schließen von Medien | `a.media.qoe.errorCount` |
| Externe Fehler-IDs | Alle eindeutigen Fehler-IDs von einer externen Quelle, z. B. CDN-Fehler. Sie müssen die gewünschten Fehler-Codes oder IDs angeben. Mehrere Fehler-IDs sind zulässig. | Schließen von Medien | `a.media.qoe.externalErrors` |
| Player SDK-Fehler-IDs | Alle eindeutigen Fehler-IDs, die vom Content Player SDK generiert werden. Sie müssen die gewünschten Fehler-Codes oder IDs angeben. Mehrere Fehler-IDs sind zulässig. | Schließen von Medien | `a.media.qoe.playerSdkErrors` |
| Zeit bis zum Start | Dieser Wert ist standardmäßig auf `0` festgelegt, wenn er nicht über das QoSObject festgelegt wird. Legen Sie den Wert in Millisekunden fest. Analysis Workspace meldet diese Dimension in Sekunden. | Medienstart, Medienschluss | `a.media.qoe.timeToStart` |

{style="table-layout:auto"}
