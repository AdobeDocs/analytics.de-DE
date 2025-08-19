---
title: Streaming-Mediendienste und -metriken
description: Verfügbare Metriken bei Aktivierung von [!UICONTROL Media Ads] für eine Report Suite.
feature: Metrics
exl-id: f0ddf3e0-ab55-4a05-a8ae-f040ba26e704
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 5%

---

# Streaming-Mediendienste und -metriken

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Media Ads] für eine Report Suite aktivieren. Verfügbare Dimensionen finden [ unter &quot;](../dimensions/sm-ads.md)-Dimensionen für Streaming-Mediendienste“*

Streaming-Mediendienste und -Metriken bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediendienste-Bibliotheken. Für die Verwendung dieser Metriken ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Media Ads]** unter [Media-Reporting](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Anzeige abgeschlossen | Wird ausgelöst, wenn eine Videoanzeige abgeschlossen wird. | Schließen hinzufügen | `a.media.ad.complete` |
| Anzeigenstarts | Wird ausgelöst, wenn eine Videoanzeige beginnt. | Werbung gestartet | `a.media.ad.view` |
| Besuchszeit für die Anzeige | Die Gesamtzeit in Sekunden, die mit dem Ansehen der Anzeige verbracht wurde. | Schließen hinzufügen | `a.media.ad.timePlayed` |
| Besuchszeit für Medien | Addiert die Ereignisdauer für alle PLAY-Ereignisse (Haupt- und Anzeigeninhalte) in Sekunden. | Schließen von Medien | `a.media.totalTimePlayed` |

{style="table-layout:auto"}
