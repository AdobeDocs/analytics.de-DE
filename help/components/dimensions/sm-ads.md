---
title: Anzeigendimensionen für Streaming-Medien
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Media Ads] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: 3f17bacc-8c36-499a-a863-9298e2d54370
source-git-commit: fdd66c9558f070cd760f37a39e5911f0dac22612
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 15%

---

# Anzeigendimensionen für Streaming-Medien

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Media Ads] für eine Report Suite aktivieren. Unter [Metriken für Streaming-](../metrics/sm-ads.md)-Anzeigen“ finden Sie verfügbare Metriken.*

Streaming-Medien und -Dimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediensammlungsbibliotheken. Für die Verwendung dieser Dimensionen ist die Sammlung **[!UICONTROL Adobe-Streaming-Medien erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

Wenn Sie **[!UICONTROL Media Ads]** unter [Media-Reporting](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable |
| --- | --- | --- | --- |
| Anzeige | Die eindeutige Kennung der Anzeige. | Anzeigenstart, Anzeigenschluss | `a.media.ad.name` |
| Anzeigename (Variable) | Der Anzeigename der Anzeige. Eine Klassifizierungsdimension mit dem Namen „Anzeigename“ ist ebenfalls verfügbar und hat einen ähnlichen Zweck. Diese Dimension und die Klassifizierung werden als zwei verschiedene Dimensionen behandelt. | Anzeigenstart, Anzeigenschluss | `a.media.ad.friendlyName` |
| Player-Namen hinzufügen | Der Name des Players, der die Anzeige rendert. | Anzeigenstart, Anzeigenschluss | `a.media.ad.playerName` |
| Anzeigenlänge (variabel) | Die Länge der Videoanzeige in Sekunden. | Anzeigenstart, Anzeigenschluss | `a.media.ad.length` |
| Anzeigen-Pod | Die eindeutige Kennung für den Anzeigen-Pod. | Anzeigenstart, Anzeigenschluss | `a.media.ad.pod` |
| Anzeigenposition im Pod | Die Indexposition der Anzeige innerhalb der übergeordneten Anzeigenunterbrechung (0-indiziert). | Anzeigenstart, Anzeigenschluss | `a.media.ad.podPosition` |
| Advertiser | Das Unternehmen oder die Marke, die in der Anzeige zu sehen ist. | Anzeigenstart, Anzeigenschluss | `a.media.ad.advertiser` |
| Kampagnen-ID | Die ID der Anzeigenkampagne | Anzeigenstart, Anzeigenschluss | `a.media.ad.campaign` |

{style="table-layout:auto"}

Zusätzlich zu den oben genannten Dimensionen erstellt Adobe automatisch die folgenden Klassifizierungsdimensionen. Sie müssen Klassifizierungsdaten hochladen, um Berichte anzuzeigen, die diese Dimensionen verwenden.

| Klassifizierungsname | Übergeordnete Dimension | Beschreibung |
| --- | --- | --- |
| Element-ID | [Inhalt](sm-core.md) | Die eindeutige Kennung für den Inhalt des Medien-Assets. Beispiele sind die Kennung der Fernsehserie, die Kennung des Film-Assets oder die Kennung des Live-Ereignisses. Diese IDs werden normalerweise von Metadatenbehörden wie EIDR, TMS/Gracenote, Rovi oder von anderen proprietären oder internen Systemen abgeleitet. |
| Bewertung des Inhalts | [Inhalt](sm-core.md) | Die Bewertung gemäß den Richtlinien für Eltern von TV. |
| Erstes Sendedatum | [Inhalt](sm-core.md) | Das Datum der Erstausstrahlung des Inhalts im Fernsehen. Da es sich bei dieser Klassifizierungsdimension um eine Zeichenfolge handelt, ist jedes Datumsformat zulässig. Adobe empfiehlt die Verwendung eines konsistenten Datumsformats, z. B. `YYYY-MM-DD`. |
| Erstes digitales Veröffentlichungsdatum | [Inhalt](sm-core.md) | Das Datum der Erstausstrahlung des Inhalts in einem digitalen Kanal oder auf einer digitalen Plattform. Da es sich bei dieser Klassifizierungsdimension um eine Zeichenfolge handelt, ist jedes Datumsformat zulässig. Adobe empfiehlt die Verwendung eines konsistenten Datumsformats, z. B. `YYYY-MM-DD`. |
| Anzeigenlänge | Anzeige | Die Länge der Videoanzeige in Sekunden. |
| Anzeigenname | Anzeige | Der Anzeigename der Anzeige. Dies entspricht der Klassifizierung von „Anzeigename (Variable)“. |
| Creative-ID | Anzeige | Die ID des Kreativinhalts der Anzeige. |
| Pod-Name | Anzeigen-Pod | Der Anzeigename des Anzeigen-Pods. |
| Pod-Position | Anzeigen-Pod | Der Versatz der Werbeunterbrechung innerhalb des Inhalts in Sekunden. |

{style="table-layout:auto"}
