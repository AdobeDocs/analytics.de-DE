---
title: Kapitelmetriken für Streaming-Medien
description: Verfügbare Metriken, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren.
feature: Metrics
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---

# Kapitelmetriken für Streaming-Medien

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Medienkapitel] für eine Report Suite aktivieren. Verfügbare Dimensionen finden Sie unter [Kapiteldimensionen der Streaming-Medien](../dimensions/sm-chapters.md) .*

Die Kapitelmetriken für Streaming-Medien bieten zusätzliche Berichtsfunktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Metriken ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medienkapitel]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Metriken verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Kapitelbeendigungen | Ein boolescher Wert, der beim Abschluss eines Kapitels Trigger wird. | Chapter Close | `a.media.chapter.complete` |
| Kapitelstarts | Ein boolescher Wert, der beim Beginn eines Kapitels Trigger wird. | Chapter Start | `a.media.chapter.view` |
| Besuchszeit für Kapitel | Die mit dem Kapitel verbrachte Zeit in Sekunden. | Chapter Close | `a.media.chapter.timePlayed` |

{style="table-layout:auto"}
