---
title: Streaming Media-Kapitelmetriken
description: Verfügbare Metriken bei Aktivierung [!UICONTROL Medienkapiteln] für eine Report Suite.
feature: Metrics
exl-id: bef379d5-9dc9-404f-8197-1ba66d11299d
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 5%

---

# Streaming Media-Kapitelmetriken

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren. Siehe [Dimensionen des Streaming-](../dimensions/sm-chapters.md)-Kapitels*

Kapitelmetriken zu Streaming-Medien bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Metriken ist die Sammlung **[!UICONTROL Adobe-Streaming-Medien erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medienkapitel]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Kapitel abgeschlossen | Ein boolescher Wert, der nach Abschluss eines Kapitels Trigger wird. | Kapitelschluss | `a.media.chapter.complete` |
| Kapitelstarts | Ein boolescher Wert, der beim Start eines Kapitels Trigger wird. | Chapter Start | `a.media.chapter.view` |
| Besuchszeit für Kapitel | Die für das Kapitel aufgewendete Zeit in Sekunden. | Kapitelschluss | `a.media.chapter.timePlayed` |

{style="table-layout:auto"}
