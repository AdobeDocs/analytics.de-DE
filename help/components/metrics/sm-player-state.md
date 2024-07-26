---
title: Tracking-Metriken zum Status von Streaming-Medien-Playern
description: Verfügbare Metriken, wenn Sie [!UICONTROL Player-Status-Tracking] für eine Report Suite aktivieren.
feature: Metrics
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---

# Tracking-Metriken zum Status von Streaming-Medien-Playern

Die Statusverfolgungsmetriken des Streaming-Medien-Players bieten zusätzliche Berichtsfunktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Metriken ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Player-Status-Tracking]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Von Untertiteln betroffene Streams | Wird ausgelöst, wenn mindestens ein Status mit verdeckten Untertiteln während einer Wiedergabesitzung aufgetreten ist. | Media Close | `a.media.states.closedcaptioning.set` |
| Anzahl verdeckter Untertitel | Gibt an, wie oft das Video in den Status &quot;Verdeckte Untertitel&quot;gelangt ist. | Media Close | `a.media.states.closedcaptioning.count` |
| Gesamtdauer der verdeckten Untertitel | Die Zeit, die das Video in einem verdeckten Untertitelstatus in Sekunden war. | Media Close | `a.media.states.closedcaptioning.time` |
| Vom Vollbildmodus betroffene Streams | Wird ausgelöst, wenn mindestens ein Vollbildstatus während einer Wiedergabesitzung aufgetreten ist. | Media Close | `a.media.states.fullscreen.set` |
| Vollbildzählung | Gibt an, wie oft das Video in den Vollbildstatus gelangt ist. | Media Close | `a.media.states.fullscreen.count` |
| Gesamtdauer der Vollbildmodi | Die Dauer, über die das Video im Vollbildmodus war (in Sekunden). | Media Close | `a.media.states.fullscreen.time` |
| Vom Fokusmodus betroffene Streams | Wird ausgelöst, wenn mindestens ein Status mit Fokusmodus während einer Wiedergabesitzung aufgetreten ist. | Media Close | `a.media.states.infocus.set` |
| Anzahl der Fokusmodi | Die Häufigkeit, mit der das Video in den Status &quot;Im Fokus&quot;wechselte. | Media Close | `a.media.states.infocus.count` |
| Gesamtdauer des Fokus | Die Zeit, die das Video im Fokusmodus war (in Sekunden). | Media Close | `a.media.states.infocus.time` |
| Von Stummschaltung betroffene Streams | Wird ausgelöst, wenn mindestens ein Stummschaltstatus während einer Wiedergabesitzung aufgetreten ist. | Media Close | `a.media.states.mute.set` |
| Stummschaltungen | Die Häufigkeit, mit der das Video in den Status &quot;Stummschaltung&quot;wechselte. | Media Close | `a.media.states.mute.count` |
| Gesamtdauer der Stummschaltung | Die Zeit, die das Video in einem Stummschaltstatus in Sekunden war. | Media Close | `a.media.states.mute.time` |
| Vom Bild im Bild betroffene Streams | Wird ausgelöst, wenn mindestens ein Bild-im-Bild-Status während einer Wiedergabesitzung aufgetreten ist. | Media Close | `a.media.states.pictureinpicture.set` |
| Bildanzahl | Die Häufigkeit, mit der das Video in den Status Bild-im-Bild gelangt ist. | Media Close | `a.media.states.pictureinpicture.count` |
| Gesamtdauer des Bildes im Bild | Die Zeit, die das Video im Status Bild-im-Bild verbracht hat, in Sekunden. | Media Close | `a.media.states.pictureinpicture.time` |

{style="table-layout:auto"}
