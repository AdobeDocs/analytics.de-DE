---
title: Dimensionen für Audio-Metadaten von Streaming-Mediendiensten
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Audio-Metadaten] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: 2e4dc1e9-267b-47a2-b791-23d1e754a2c1
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 6%

---

# Dimensionen für Audio-Metadaten von Streaming-Mediendiensten

Streaming-Mediendienste und -Dimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediendienste-Bibliotheken. Für die Verwendung dieser Dimensionen ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Audio-Metadaten]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Album]** | Der Name des Albums. | Medienstart, Medienschluss | `a.media.album` | `xdm.mediaCollection.`<br>`sessionDetails.album`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.album` |
| **[!UICONTROL Künstler]** | Der Name des Künstlers. | Medienstart, Medienschluss | `a.media.artist` | `xdm.mediaCollection.`<br>`sessionDetails.artist`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.artist` |
| **[!UICONTROL author]** | Der Name des Hörbuchautors. | Medienstart, Medienschluss | `a.media.author` | `xdm.mediaCollection.`<br>`sessionDetails.author`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.author` |
| **[!UICONTROL Beschriftung]** | Der Name der Datensatzkennzeichnung. | Medienstart, Medienschluss | `a.media.label` | `xdm.mediaCollection.`<br>`sessionDetails.label`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.label` |
| **[!UICONTROL Veröffentlicher]** | Der Name des Herausgebers des Audioinhalts. | Medienstart, Medienschluss | `a.media.publisher` | `xdm.mediaCollection.`<br>`sessionDetails.publisher`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.publisher` |
| **[!UICONTROL Station]** | Der Name oder die ID des Radiosenders. | Medienstart, Medienschluss | `a.media.station` | `xdm.mediaCollection.`<br>`sessionDetails.station`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.station` |
