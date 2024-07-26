---
title: Anzeigenmetriken für Streaming-Medien
description: Verfügbare Metriken, wenn Sie [!UICONTROL Medienanzeigen] für eine Report Suite aktivieren.
feature: Metrics
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---

# Anzeigenmetriken für Streaming-Medien

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Medienanzeigen] für eine Report Suite aktivieren. Verfügbare Dimensionen finden Sie unter [ Streaming-Medien-Anzeigendimensionen](../dimensions/sm-ads.md) .*

Die Anzeigenmetriken für Streaming-Medien bieten zusätzliche Berichtsfunktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Metriken ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medienanzeigen]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Anzeigenbeendigungen | Wird ausgelöst, wenn eine Videoanzeige abgeschlossen ist. | Ad Close | `a.media.ad.complete` |
| Anzeigenstarts | Wird ausgelöst, wenn eine Videoanzeige beginnt. | Werbung gestartet | `a.media.ad.view` |
| Besuchszeit für Anzeige | Die insgesamt mit der Wiedergabe der Anzeige verbrachte Zeit in Sekunden. | Ad Close | `a.media.ad.timePlayed` |
| Besuchszeit für Medien | Addiert die Ereignisdauer für alle PLAY-Ereignisse (Haupt- und Anzeigeninhalt) in Sekunden. | Media Close | `a.media.totalTimePlayed` |

{style="table-layout:auto"}
