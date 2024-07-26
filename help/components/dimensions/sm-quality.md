---
title: Qualitätsdimensionen der Streaming-Medien
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren.
feature: Dimensions
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%

---

# Qualitätsdimensionen der Streaming-Medien

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Medienqualität] für eine Report Suite aktivieren. Verfügbare Metriken finden Sie unter [Metriken zur Qualität von Streaming-Medien](../metrics/sm-quality.md) .*

Die Qualitätsdimensionen der Streaming-Medien bieten Berichte, die sich auf die Qualität der Inhalte beziehen, die der Besucher konsumiert. Für die Verwendung dieser Dimensionen ist das [!UICONTROL Adobe Streaming-Mediensammlungs-Add-on] erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medienqualität]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimensionen | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Durchschnittliche Bitrate | Die durchschnittliche Bitrate in 100-KBPS-Bucket-Intervallen. Sie wird als gewichteter Durchschnitt aller Bitratenwerte im Verhältnis zur Wiedergabedauer für eine bestimmte Wiedergabesitzung berechnet. | Media Close | `a.media.qoe.bitrateAverageBucket` |
| Bitratenänderungen | Die Anzahl der Bitratenänderungen, die während einer Wiedergabesitzung aufgetreten sind. | Media Close | `a.media.qoe.bitrateChangeCount` |
| Pufferereignisse | Die Häufigkeit, mit der der Medienplayer während einer Wiedergabesitzung einen Pufferstatus erreicht hat. | Media Close | `a.media.qoe.bufferCount` |
| Gesamtpufferdauer | Die insgesamt mit Pufferung verbrachte Zeit in Sekunden. | Media Close | `a.media.qoe.bufferTime` |
| Dropped Frames | Die Gesamtzahl der Dropped Frames, die während einer Wiedergabesitzung aufgetreten sind. | Media Close | `a.media.qoe.droppedFrameCount` |
| Fehler | Die Gesamtzahl der Fehler, die während einer Wiedergabesitzung aufgetreten sind. | Media Close | `a.media.qoe.errorCount` |
| Externe Fehler-IDs | Alle eindeutigen Fehler-IDs aus einer beliebigen externen Quelle, z. B. CDN-Fehler. Sie müssen die gewünschten Fehlercodes oder -IDs angeben. Mehrere Fehler-IDs sind zulässig. | Media Close | `a.media.qoe.externalErrors` |
| Player-SDK-Fehler-IDs | Alle eindeutigen Fehler-IDs, die vom Content Player SDK generiert werden. Sie müssen die gewünschten Fehlercodes oder -IDs angeben. Mehrere Fehler-IDs sind zulässig. | Media Close | `a.media.qoe.playerSdkErrors` |
| Startzeit | Dieser Wert wird standardmäßig auf `0` gesetzt, wenn er nicht über das QoSObject festgelegt wird. Legen Sie den Wert in Millisekunden fest. Analysis Workspace meldet diese Dimension in Sekunden. | Media Start, Media Close | `a.media.qoe.timeToStart` |

{style="table-layout:auto"}
