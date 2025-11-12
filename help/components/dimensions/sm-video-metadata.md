---
title: Dimensionen für Videometadaten von Streaming-Mediendiensten
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: e476c19a-9542-4a6f-9b79-5f801e2a7bf8
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 3%

---

# Dimensionen für Videometadaten von Streaming-Mediendiensten

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren. Unter [Metriken zu Videometadaten von Streaming](../metrics/sm-video-metadata.md)Mediendiensten finden Sie verfügbare Metriken.*

Streaming-Mediendienste und -Dimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Sammlungsbibliotheken von Streaming-Mediendiensten. Für die Verwendung dieser Dimensionen ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Videometadaten]** unter [Medienberichte](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Anzeigenladevorgänge]** | Der Typ der geladenen Anzeige. | | `a.media.adLoad` | `xdm.mediaCollection.`<br>`sessionDetails.adLoad` |
| **[!UICONTROL Teil des Tages]** | Die Tageszeit, zu der der Inhalt gesendet oder wiedergegeben wurde. Jeder Zeichenfolgenwert wird unterstützt. | Medienstart, Medienschluss | `a.media.dayPart` | `xdm.mediaCollection.`<br>`sessionDetails.dayPart`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.dayPart` |
| **[!UICONTROL Folge]** | Die Nummer der Folge. | Medienstart, Medienschluss | `a.media.episode` | `xdm.mediaCollection.`<br>`sessionDetails.episode`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.episode` |
| **[!UICONTROL Medien-Feed-Typ]** | Die Art des Feeds. | Medienstart, Medienschluss | `a.media.feed` | `xdm.mediaCollection.`<br>`sessionDetails.feed`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.feed` |
| **[!UICONTROL Genre]** | Der Typ oder die Gruppierung des Inhalts, wie vom Inhaltsersteller definiert. Diese Dimension unterstützt mehrere Werte, durch Kommas getrennt. | Medienstart, Medienschluss | `a.media.genre` | `xdm.mediaCollection.`<br>`sessionDetails.genre`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.genreList` |
| **[!UICONTROL MVPD]** | Die MVPD, wie sie von der Adobe-Authentifizierung bereitgestellt wird. | Medienstart, Medienschluss | `a.media.pass.mvpd` | `xdm.mediaCollection.`<br>`sessionDetails.mvpd`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.mvpd` |
| **[!UICONTROL Netzwerk]** | Der Netzwerk- oder Kanalname. | Medienstart, Medienschluss | `a.media.network` | `xdm.mediaCollection.`<br>`sessionDetails.network`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.network` |
| **[!UICONTROL Staffel]** | Die Staffelnummer, zu der die Sendung gehört. | Medienstart, Medienschluss | `a.media.season` | `xdm.mediaCollection.`<br>`sessionDetails.season`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.season` |
| **[!UICONTROL Anzeigen]** | Der Name des Programms oder der Serie. | Medienstart, Medienschluss | `a.media.show` | `xdm.mediaCollection.`<br>`sessionDetails.show`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.show` |
| **[!UICONTROL Typ anzeigen]** | Eine Ganzzahl, die den Inhaltstyp darstellt.<br>`0`: Full Episode<br>`1`: Vorschau oder Trailer<br>`2`: Clip<br>`3`: Sonstiges | Medienstart, Medienschluss | `a.media.type` | `xdm.mediaCollection.`<br>`sessionDetails.showType`<br><br>`xdm.mediaReporting.`<br>`sessionDetails.showType` |

