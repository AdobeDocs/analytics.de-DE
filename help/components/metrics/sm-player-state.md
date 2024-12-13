---
title: Statusverfolgungsmetriken des Streaming-Medien-Players
description: Verfügbare Metriken, wenn Sie [!UICONTROL Player-Statusverfolgung] für eine Report Suite aktivieren.
feature: Metrics
exl-id: 324936cc-0c7a-4710-a618-b24cc6a2c2cf
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 1%

---

# Statusverfolgungsmetriken des Streaming-Medien-Players

Statusverfolgungsmetriken für Streaming-Medien-Player bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Metriken ist die Sammlung **[!UICONTROL Adobe-Streaming-Medien erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Player-Status-Tracking]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Von verdeckten Untertiteln betroffene Streams | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein Untertitelstatus aufgetreten ist. | Schließen von Medien | `a.media.states.closedcaptioning.set` |
| Anzahl der verdeckten Untertitel | Die Häufigkeit, mit der das Video in einen Untertitelstatus übergegangen ist. | Schließen von Medien | `a.media.states.closedcaptioning.count` |
| Gesamtdauer für verdeckte Untertitel | Die Zeit in Sekunden, die sich das Video im Zustand „Untertitel“ befand. | Schließen von Medien | `a.media.states.closedcaptioning.time` |
| Vom Vollbildmodus betroffene Streams | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein Vollbildstatus aufgetreten ist. | Schließen von Medien | `a.media.states.fullscreen.set` |
| Anzahl der Vollbilder | Die Häufigkeit, mit der das Video in einen Vollbildmodus übergegangen ist. | Schließen von Medien | `a.media.states.fullscreen.count` |
| Gesamtdauer im Vollbildmodus | Die Zeit in Sekunden, die das Video im Vollbildmodus angezeigt wurde. | Schließen von Medien | `a.media.states.fullscreen.time` |
| Im Fokus befindliche Streams, die von betroffen sind | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein Fokusstatus aufgetreten ist. | Schließen von Medien | `a.media.states.infocus.set` |
| Anzahl der Fokussierungen | Die Häufigkeit, mit der das Video in den Fokusstatus übergegangen ist. | Schließen von Medien | `a.media.states.infocus.count` |
| Gesamtdauer des Fokus | Die Zeit in Sekunden, die sich das Video im Fokusstatus befand. | Schließen von Medien | `a.media.states.infocus.time` |
| Von Stummschaltung betroffene Streams | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein Stummschaltungsstatus aufgetreten ist. | Schließen von Medien | `a.media.states.mute.set` |
| Anzahl stummschalten | Die Häufigkeit, mit der das Video in einen Stummschaltungsstatus übergegangen ist. | Schließen von Medien | `a.media.states.mute.count` |
| Gesamtdauer der Stummschaltung | Die Zeit in Sekunden, die das Video im Stummschaltungsstatus war. | Schließen von Medien | `a.media.states.mute.time` |
| Von Bild in Bild betroffene Ströme | Wird ausgelöst, wenn während einer Wiedergabesitzung mindestens ein „Bild im Bild“-Status aufgetreten ist. | Schließen von Medien | `a.media.states.pictureinpicture.set` |
| Anzahl der Bilder im Bild | Die Häufigkeit, mit der das Video in den Status „Bild in Bild“ wechselt. | Schließen von Medien | `a.media.states.pictureinpicture.count` |
| Gesamtdauer des Bilds im Bild | Die Zeit in Sekunden, während der sich das Video im Bildstatus befand. | Schließen von Medien | `a.media.states.pictureinpicture.time` |

{style="table-layout:auto"}
