---
title: Anzeigendimensionen für Streaming-Medien
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Medienanzeigen] für eine Report Suite aktivieren.
feature: Dimensions
source-git-commit: 26c131a37fa1f30c83fd99b290523a97d3c954db
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 15%

---

# Anzeigendimensionen für Streaming-Medien

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Medienanzeigen] für eine Report Suite aktivieren. Verfügbare Metriken finden Sie unter [ Streaming-Medien-Anzeigenmetriken](../metrics/sm-ads.md) .*

Streaming-Medien-Anzeigendimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Dimensionen ist das **[!UICONTROL Adobe Streaming Media Collection Add-on]** erforderlich. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Medienanzeigen]** unter [Medienberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Anzeige | Die eindeutige Kennung für die Anzeige. | Ad Start, Ad Close | `a.media.ad.name` |
| Anzeigenname (Variable) | Der Anzeigename der Anzeige. Es ist auch eine Classification-Dimension mit dem Namen &quot;Anzeigenname&quot;verfügbar, die einen ähnlichen Zweck bietet. Diese Dimension und die Classification werden als zwei unterschiedliche Dimensionen behandelt. | Ad Start, Ad Close | `a.media.ad.friendlyName` |
| Name des Anzeigenplayers | Der Name des Players, der die Anzeige rendert. | Ad Start, Ad Close | `a.media.ad.playerName` |
| Anzeigenlänge (Variable) | Die Länge der Videoanzeige in Sekunden. | Ad Start, Ad Close | `a.media.ad.length` |
| Anzeigen-Pod | Die eindeutige Kennung für den Anzeigen-Pod. | Ad Start, Ad Close | `a.media.ad.pod` |
| Anzeige in Position der Werbeunterbrechung | Die Indexposition der Anzeige innerhalb der übergeordneten Werbeunterbrechung (0-indiziert). | Ad Start, Ad Close | `a.media.ad.podPosition` |
| Advertiser | Das Unternehmen oder die Marke der Anzeige. | Ad Start, Ad Close | `a.media.ad.advertiser` |
| Kampagnen-ID | Die ID der Anzeigenkampagne | Ad Start, Ad Close | `a.media.ad.campaign` |

{style="table-layout:auto"}

Zusätzlich zu den oben genannten Dimensionen erstellt Adobe automatisch die folgenden Classification-Dimensionen. Sie müssen Classification-Daten hochladen, um Berichte anzuzeigen, die diese Dimensionen verwenden.

| Klassifizierungsname | Übergeordnete Dimension | Beschreibung |
| --- | --- | --- |
| Element-ID | [Inhalt](sm-core.md) | Die eindeutige Kennung für den Inhalt des Medien-Assets. Beispiele sind die Kennung einer Serienfolge, ein Film-Asset oder eine Live-Ereigniskennung. Diese IDs werden normalerweise von Metadatenbehörden wie EIDR, TMS/Gracenote, Rovi oder anderen proprietären oder internen Systemen abgeleitet. |
| Inhaltsbewertung | [Inhalt](sm-core.md) | Die Alterseinstufung nach Definition von TV Parental Guidelines. |
| Erstes Sendedatum | [Inhalt](sm-core.md) | Das Datum der Erstausstrahlung des Inhalts im Fernsehen. Da diese Classification-Dimension eine Zeichenfolge ist, ist jedes Datumsformat zulässig. Adobe empfiehlt die Verwendung eines einheitlichen Datumsformats, z. B. `YYYY-MM-DD`. |
| Erstes digitales Veröffentlichungsdatum | [Inhalt](sm-core.md) | Das Datum der Erstausstrahlung des Inhalts in einem digitalen Kanal oder auf einer digitalen Plattform. Da diese Classification-Dimension eine Zeichenfolge ist, ist jedes Datumsformat zulässig. Adobe empfiehlt die Verwendung eines einheitlichen Datumsformats, z. B. `YYYY-MM-DD`. |
| Anzeigenlänge | Anzeige | Die Länge der Videoanzeige in Sekunden. |
| Anzeigenname | Anzeige | Der Anzeigename der Anzeige. Dies ist das Classification-Äquivalent zu &quot;Anzeigenname (Variable)&quot;. |
| Creative-ID | Anzeige | Die ID des Anzeigenmotivs. |
| Name der Werbeunterbrechung | Anzeigen-Pod | Der Anzeigename der Anzeigen-Pod. |
| Position der Werbeunterbrechung | Anzeigen-Pod | Der Versatz der Werbeunterbrechung innerhalb des Inhalts in Sekunden. |

{style="table-layout:auto"}
