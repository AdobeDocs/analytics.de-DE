---
title: Streaming-Mediendienste und -metriken
description: Verfügbare Metriken bei Aktivierung von [!UICONTROL Media Ads] für eine Report Suite.
feature: Metrics
exl-id: f0ddf3e0-ab55-4a05-a8ae-f040ba26e704
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 6%

---

# Streaming-Mediendienste und -metriken

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Media Ads] für eine Report Suite aktivieren. Verfügbare Dimensionen finden [&#x200B; unter &quot;](../dimensions/sm-ads.md)-Dimensionen für Streaming-Mediendienste“*

Streaming-Mediendienste und -Metriken bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediendienste-Bibliotheken. Für die Verwendung dieser Metriken ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Media Ads]** unter [Media-Reporting](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Anzeige abgeschlossen]** | Wird ausgelöst, wenn eine Videoanzeige abgeschlossen wird. | Schließen hinzufügen | `a.media.ad.complete` | `xdm.mediaReporting.`<br>`advertisingDetails.isCompleted` |
| **[!UICONTROL Anzeigenstarts]** | Wird ausgelöst, wenn eine Videoanzeige beginnt. | Werbung gestartet | `a.media.ad.view` | `xdm.mediaReporting.`<br>`advertisingDetails.isStarted` |
| **[!UICONTROL Besuchszeit für Anzeige]** | Die Gesamtzeit in Sekunden, die mit dem Ansehen der Anzeige verbracht wurde. | Schließen hinzufügen | `a.media.ad.timePlayed` | `xdm.mediaReporting.`<br>`advertisingDetails.timePlayed` |
| **[!UICONTROL Besuchszeit für Medien]** | Addiert die Ereignisdauer für alle &quot;[!UICONTROL &quot;-] (Haupt- und Anzeigeninhalte) in Sekunden. | Schließen von Medien | `a.media.totalTimePlayed` | `xdm.mediaReporting.`<br>`sessionDetails.totalTimePlayed` |
