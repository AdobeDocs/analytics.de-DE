---
title: Metriken für Streaming-Medien-Videometadaten
description: Verfügbare Metriken, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren.
feature: Metrics
exl-id: b2f60a34-e139-4498-bf71-74d291759ef2
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# Metriken für Streaming-Medien-Videometadaten

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren. Siehe [Dimensionen für Streaming-Medien-Videometadaten](../dimensions/sm-video-metadata.md) für verfügbare Dimensionen.*

Metadaten von Streaming-Medien-Videos bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Metriken ist die Sammlung **[!UICONTROL Adobe-Streaming-Medien erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Videometadaten]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, ist die folgende Metrik verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Autorisiert | Ein boolescher Wert, der Trigger wird, wenn der Benutzer über die Adobe-Authentifizierung autorisiert wird. | Medienstart, Medienschluss | `a.media.pass.auth` |

{style="table-layout:auto"}
