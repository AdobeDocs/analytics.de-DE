---
title: Kapitelmetriken für Streaming-Mediendienste
description: Verfügbare Metriken bei Aktivierung [!UICONTROL Medienkapiteln] für eine Report Suite.
feature: Metrics
exl-id: bef379d5-9dc9-404f-8197-1ba66d11299d
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 5%

---

# Kapitelmetriken für Streaming-Mediendienste

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren. Siehe [Dimensionen im Kapitel zu Streaming](../dimensions/sm-chapters.md)Mediendiensten“ für verfügbare Dimensionen.*

Die Kapitelmetriken zu Streaming-Mediendiensten bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Sammlungsbibliotheken von Streaming-Mediendiensten. Für die Verwendung dieser Metriken ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Medienkapitel]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Kapitel abgeschlossen | Ein boolescher Wert, der nach Abschluss eines Kapitels Trigger wird. | Kapitelschluss | `a.media.chapter.complete` |
| Kapitelstarts | Ein boolescher Wert, der beim Start eines Kapitels Trigger wird. | Chapter Start | `a.media.chapter.view` |
| Besuchszeit für Kapitel | Die für das Kapitel aufgewendete Zeit in Sekunden. | Kapitelschluss | `a.media.chapter.timePlayed` |

{style="table-layout:auto"}
