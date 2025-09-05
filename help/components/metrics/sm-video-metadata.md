---
title: Metadatenmetriken für Streaming-Mediendienste
description: Verfügbare Metriken, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren.
feature: Metrics
exl-id: b2f60a34-e139-4498-bf71-74d291759ef2
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

---

# Metadatenmetriken für Streaming-Mediendienste

*Auf dieser Seite werden die verfügbaren Metriken beschrieben, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren. Siehe [Dimensionen für Streaming-Medien-Services](../dimensions/sm-video-metadata.md) für Videometadaten für verfügbare Dimensionen.*

Metadaten von Streaming-Mediendiensten bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediendienstbibliotheken. Für die Verwendung dieser Metriken ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Videometadaten]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, ist die folgende Metrik verfügbar:

| Metrikname | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Autorisiert | Ein boolescher Wert, der Trigger wird, wenn der Benutzer über die Adobe-Authentifizierung autorisiert wird. | Medienstart, Medienschluss | `a.media.pass.auth` |

{style="table-layout:auto"}
