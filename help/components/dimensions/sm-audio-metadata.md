---
title: Abmessungen von Streaming Media-Audio-Metadaten
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Audio-Metadaten] für eine Report Suite aktivieren.
feature: Dimensions
source-git-commit: 45b371bd20223b86d0f17d9bdb48cffb2de15468
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 8%

---

# Abmessungen von Streaming Media-Audio-Metadaten

Streaming-Medien-Anzeigendimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Dimensionen ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Audio-Metadaten]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Album | Der Name des Albums. | Media Start, Media Close | `a.media.album` |
| Künstler | Der Name des Künstlers. | Media Start, Media Close | `a.media.artist` |
| Autor | Der Name des Hörbuchautors. | Media Start, Media Close | `a.media.author` |
| Beschriftung | Der Name der Datensatzbeschriftung. | Media Start, Media Close | `a.media.label` |
| Publisher | Der Name des Herausgebers des Audioinhalts. | Media Start, Media Close | `a.media.publisher` |
| Station | Name oder ID des Radiosenders. | Media Start, Media Close | `a.media.station` |

{style="table-layout:auto"}
