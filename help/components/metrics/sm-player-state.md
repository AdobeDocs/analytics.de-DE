---
title: 'Streaming-Mediendienste: Player-Statusverfolgungsmetriken'
description: Verfügbare Metriken, wenn Sie [!UICONTROL Player-Statusverfolgung] für eine Report Suite aktivieren.
feature: Metrics
exl-id: 324936cc-0c7a-4710-a618-b24cc6a2c2cf
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 2%

---

# Streaming-Mediendienste: Player-Statusverfolgungsmetriken

Streaming-Mediendienste und Player-Statusverfolgungsmetriken bieten zusätzliche Berichtsfunktionen für die Datenerfassung über Streaming-Mediendienste-Bibliotheken. Für die Verwendung dieser Metriken ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Player-Status-Tracking]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Von verdeckten Untertiteln betroffene Streams]** | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein Untertitelstatus aufgetreten ist. | Schließen von Medien | `a.media.states.`<br>`closedcaptioning.set` | `mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL Geschlossene Untertitelanzahl]** | Die Häufigkeit, mit der das Video in einen Untertitelstatus übergegangen ist. | Schließen von Medien | `a.media.states.`<br>`closedcaptioning.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL Gesamtdauer für verdeckte Untertitel]** | Die Zeit in Sekunden, die sich das Video im Zustand „Untertitel“ befand. | Schließen von Medien | `a.media.states.`<br>`closedcaptioning.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL Vom Vollbildmodus betroffene Streams]** | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein Vollbildstatus aufgetreten ist. | Schließen von Medien | `a.media.states.`<br>`fullscreen.set` | `xdm.mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL Anzahl der Vollbilder]** | Die Häufigkeit, mit der das Video in einen Vollbildmodus übergegangen ist. | Schließen von Medien | `a.media.states.`<br>`fullscreen.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL Gesamtdauer im Vollbildmodus]** | Die Zeit in Sekunden, die das Video im Vollbildmodus angezeigt wurde. | Schließen von Medien | `a.media.states.`<br>`fullscreen.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL Von im Fokus betroffene Streams]** | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein Fokusstatus aufgetreten ist. | Schließen von Medien | `a.media.states.`<br>`infocus.set` | `mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL Anzahl der Fokussierungen]** | Die Häufigkeit, mit der das Video in den Fokusstatus übergegangen ist. | Schließen von Medien | `a.media.states.`<br>`infocus.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL Gesamtdauer des Fokus]** | Die Zeit in Sekunden, die sich das Video im Fokusstatus befand. | Schließen von Medien | `a.media.states.`<br>`infocus.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL Von Stummschaltung betroffene Streams]** | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein Stummschaltungsstatus aufgetreten ist. | Schließen von Medien | `a.media.states.`<br>`mute.set` | `xdm.mediaReporting.`<br>`states.[*].isSet` |
| **[!UICONTROL Anzahl der Stummschaltungen]** | Die Häufigkeit, mit der das Video in einen Stummschaltungsstatus übergegangen ist. | Schließen von Medien | `a.media.states.`<br>`mute.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL Gesamtdauer der Stummschaltung]** | Die Zeit in Sekunden, die das Video im Stummschaltungsstatus war. | Schließen von Medien | `a.media.states.`<br>`mute.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
| **[!UICONTROL Vom Bild betroffene Ströme in Bild]** | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein „Bild im Bild“-Status aufgetreten ist. | Schließen von Medien | `a.media.states.`<br>`pictureinpicture.set` | `mediaReporting.states.`<br>`[*].isSet` |
| **[!UICONTROL Anzahl der Bilder im Bild]** | Die Häufigkeit, mit der das Video in den Status „Bild in Bild“ wechselt. | Schließen von Medien | `a.media.states.`<br>`pictureinpicture.count` | `xdm.mediaReporting.`<br>`states.[*].count` |
| **[!UICONTROL Gesamtdauer des Bildes]** | Die Zeit in Sekunden, während der sich das Video im Bildstatus befand. | Schließen von Medien | `a.media.states.`<br>`pictureinpicture.time` | `xdm.mediaReporting.`<br>`states.[*].time` |
