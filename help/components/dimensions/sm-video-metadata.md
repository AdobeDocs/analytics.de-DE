---
title: Metadatendimensionen von Streaming-Medien-Videos
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: e476c19a-9542-4a6f-9b79-5f801e2a7bf8
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 7%

---

# Metadatendimensionen von Streaming-Medien-Videos

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren. Unter [Metriken zu Streaming-Medien-Video](../metrics/sm-video-metadata.md) finden Sie verfügbare Metriken.*

Streaming-Medien und -Dimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Dimensionen ist die Sammlung **[!UICONTROL Adobe-Streaming-Medien erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Videometadaten]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Anzeigenladevorgänge | Der Typ der geladenen Anzeige. | TBD | `a.media.adLoad` |
| Tagesteil | Die Tageszeit, zu der der Inhalt gesendet oder wiedergegeben wurde. Jeder Zeichenfolgenwert wird unterstützt. | Medienstart, Medienschluss | `a.media.dayPart` |
| Folge | Die Nummer der Folge. | Medienstart, Medienschluss | `a.media.episode` |
| Medien-Feed-Typ | Die Art des Feeds. | Medienstart, Medienschluss | `a.media.feed` |
| Genre | Der Typ oder die Gruppierung des Inhalts, wie vom Inhaltsersteller definiert. Diese Dimension unterstützt mehrere Werte, durch Kommas getrennt. | Medienstart, Medienschluss | `a.media.genre` |
| MVPD | Die MVPD, wie sie von der Adobe-Authentifizierung bereitgestellt wird. | Medienstart, Medienschluss | `a.media.pass.mvpd` |
| Netzwerk | Der Netzwerk- oder Kanalname | Medienstart, Medienschluss | `a.media.network` |
| Staffel | Die Staffelnummer, zu der die Sendung gehört. | Medienstart, Medienschluss | `a.media.season` |
| Serie | Der Name des Programms oder der Serie. | Medienstart, Medienschluss | `a.media.show` |
| Serientyp | Eine Ganzzahl, die den Inhaltstyp darstellt.<br>`0`: Full Episode<br>`1`: Vorschau oder Trailer<br>`2`: Clip<br>`3`: Sonstiges | Medienstart, Medienschluss | `a.media.type` |

{style="table-layout:auto"}
