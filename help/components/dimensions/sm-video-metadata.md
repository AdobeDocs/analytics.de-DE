---
title: Dimensionen für Streaming-Medien-Metadaten
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren.
feature: Dimensions
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 7%

---

# Dimensionen für Streaming-Medien-Metadaten

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Videometadaten] für eine Report Suite aktivieren. Verfügbare Metriken finden Sie unter [ Metriken zu Streaming-Medien-Videometadaten](../metrics/sm-video-metadata.md) .*

Streaming-Medien-Anzeigendimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Dimensionen ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Videometadaten]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Anzeigenladevorgänge | Der Typ der geladenen Anzeige. | TBD | `a.media.adLoad` |
| Tagesteil | Die Tageszeit, zu der der Inhalt ausgestrahlt oder wiedergegeben wurde. Jeder Zeichenfolgenwert wird unterstützt. | Media Start, Media Close | `a.media.dayPart` |
| Folge | Die Nummer der Folge. | Media Start, Media Close | `a.media.episode` |
| Medien-Feed-Typ | Der Feed-Typ. | Media Start, Media Close | `a.media.feed` |
| Genre | Der Typ oder die Gruppierung des Inhalts entsprechend der Definition des Inhaltserstellers. Diese Dimension unterstützt mehrere Werte, die durch Kommas getrennt sind. | Media Start, Media Close | `a.media.genre` |
| MVPD | Der MVPD, wie durch Adobe-Authentifizierung bereitgestellt. | Media Start, Media Close | `a.media.pass.mvpd` |
| Netzwerk | Name des Netzwerks oder Kanals | Media Start, Media Close | `a.media.network` |
| Staffel | Die Staffelnummer, zu der die Sendung gehört. | Media Start, Media Close | `a.media.season` |
| Serie | Der Name des Programms oder der Serie. | Media Start, Media Close | `a.media.show` |
| Serientyp | Eine Ganzzahl, die den Inhaltstyp darstellt.<br>`0`: Vollständige Folge<br>`1`: Vorschau oder Trailer<br>`2`: Clip<br>`3`: Sonstige | Media Start, Media Close | `a.media.type` |

{style="table-layout:auto"}
