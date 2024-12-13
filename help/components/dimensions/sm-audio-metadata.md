---
title: Dimensionen für Audio-Metadaten von Streaming-Medien
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Audio-Metadaten] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: 2e4dc1e9-267b-47a2-b791-23d1e754a2c1
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 8%

---

# Dimensionen für Audio-Metadaten von Streaming-Medien

Streaming-Medien und -Dimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Dimensionen ist die Sammlung **[!UICONTROL Adobe-Streaming-Medien erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Audio-Metadaten]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Album | Der Name des Albums. | Medienstart, Medienschluss | `a.media.album` |
| Künstler | Der Name des Künstlers. | Medienstart, Medienschluss | `a.media.artist` |
| Autor | Der Name des Hörbuchautors. | Medienstart, Medienschluss | `a.media.author` |
| Beschriftung | Der Name der Datensatzkennzeichnung. | Medienstart, Medienschluss | `a.media.label` |
| Publisher | Der Name des Herausgebers des Audioinhalts. | Medienstart, Medienschluss | `a.media.publisher` |
| Station | Der Name oder die ID des Radiosenders. | Medienstart, Medienschluss | `a.media.station` |

{style="table-layout:auto"}
