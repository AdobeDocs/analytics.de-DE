---
title: Streaming-Mediendienste und -Dimensionen
description: Verfügbare Dimensionen, wenn Sie [!UICONTROL Media Ads] für eine Report Suite aktivieren.
feature: Dimensions
exl-id: 3f17bacc-8c36-499a-a863-9298e2d54370
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 4%

---

# Streaming-Mediendienste und -Dimensionen

*Auf dieser Seite werden die verfügbaren Dimensionen beschrieben, wenn Sie [!UICONTROL Media Ads] für eine Report Suite aktivieren. Unter [Metriken für Streaming-](../metrics/sm-ads.md)-Anzeigen“ finden Sie verfügbare Metriken.*

Streaming-Mediendienste und -Dimensionen bieten zusätzliche Reporting-Funktionen für die Datenerfassung über Streaming-Mediendienste-Bibliotheken. Für die Verwendung dieser Dimensionen ist das Add **[!UICONTROL on Adobe Analytics for Streaming Media erforderlich]**. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

Wenn Sie **[!UICONTROL Media Ads]** unter [Media-Reporting](/help/admin/tools/manage-rs/edit-settings/media-management.md) aktivieren, sind die folgenden Dimensionen verfügbar:

| Name der Dimension | Beschreibung | Gesendet mit | Kontextdatenvariable | XDM-Feld |
| --- | --- | --- | --- | --- |
| **[!UICONTROL Anzeige]** | Die eindeutige Kennung der Anzeige. | Anzeigenstart, Anzeigenschluss | `a.media.ad.`<br>`name` | `xdm.mediaCollection.`<br>`advertisingDetails.name`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.name` |
| **[!UICONTROL Anzeigename (Variable)]** | Der Anzeigename der Anzeige. Eine Classification-Dimension mit dem Namen [!UICONTROL Anzeigename] ist ebenfalls verfügbar und hat einen ähnlichen Zweck. Diese Dimension und die Klassifizierung werden als zwei verschiedene Dimensionen behandelt. | Anzeigenstart, Anzeigenschluss | `a.media.ad.`<br>`friendlyName` | `xdm.mediaCollection.`<br>`advertisingDetails.friendlyName`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.friendlyName` |
| **[!UICONTROL Player-Namen hinzufügen]** | Der Name des Players, der die Anzeige rendert. | Anzeigenstart, Anzeigenschluss | `a.media.ad.`<br>`playerName` | `xdm.mediaCollection.`<br>`advertisingDetails.playerName`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.playerName` |
| **[!UICONTROL Anzeigenlänge (variabel)]** | Die Länge der Videoanzeige in Sekunden. | Anzeigenstart, Anzeigenschluss | `a.media.ad.`<br>`length` | `xdm.mediaCollection.`<br>`advertisingDetails.length`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.length` |
| **[!UICONTROL Anzeigen-Pod]** | Die eindeutige Kennung für den Anzeigen-Pod. | Anzeigenstart, Anzeigenschluss | `a.media.ad.`<br>`pod` | |
| **[!UICONTROL Anzeige in Pod-Position]** | Die Indexposition der Anzeige innerhalb der übergeordneten Anzeigenunterbrechung (0-indiziert). | Anzeigenstart, Anzeigenschluss | `a.media.ad.`<br>`podPosition` | `xdm.mediaCollection.`<br>`advertisingDetails.podPosition`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.podPosition` |
| **[!UICONTROL Advertiser]** | Das Unternehmen oder die Marke, die in der Anzeige zu sehen ist. | Anzeigenstart, Anzeigenschluss | `a.media.ad.`<br>`advertiser` | `xdm.mediaCollection.`<br>`advertisingDetails.advertiser`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.advertiser` |
| **[!UICONTROL Kampagnen-ID]** | Die ID der Anzeigenkampagne | Anzeigenstart, Anzeigenschluss | `a.media.ad.`<br>`campaign` | `xdm.mediaCollection.`<br>`advertisingDetails.campaignID`<br><br>`xdm.mediaReporting.`<br>`advertisingDetails.campaignID` |

Zusätzlich zu den oben genannten Dimensionen erstellt Adobe automatisch die folgenden Klassifizierungsdimensionen. Sie müssen Klassifizierungsdaten hochladen, um Berichte anzuzeigen, die diese Dimensionen verwenden.

| Klassifizierungsname | Übergeordnete Dimension | Beschreibung |
| --- | --- | --- |
| **[!UICONTROL Asset-ID]** | [[!UICONTROL Inhalt]](sm-core.md) | Die eindeutige Kennung für den Inhalt des Medien-Assets. Beispiele sind die Kennung der Fernsehserie, die Kennung des Film-Assets oder die Kennung des Live-Ereignisses. Diese IDs werden normalerweise von Metadatenbehörden wie EIDR, TMS/Gracenote, Rovi oder von anderen proprietären oder internen Systemen abgeleitet. |
| **[!UICONTROL Inhaltsbewertung]** | [[!UICONTROL Inhalt]](sm-core.md) | Die Bewertung gemäß den Richtlinien für Eltern von TV. |
| **[!UICONTROL Datum der Erstausstrahlung]** | [[!UICONTROL Inhalt]](sm-core.md) | Das Datum, an dem der Inhalt erstmals im Fernsehen ausgestrahlt wurde. Da es sich bei dieser Klassifizierungsdimension um eine Zeichenfolge handelt, ist jedes Datumsformat zulässig. Adobe empfiehlt die Verwendung eines konsistenten Datumsformats, z. B. `YYYY-MM-DD`. |
| **[!UICONTROL Erstes digitales Datum]** | [[!UICONTROL Inhalt]](sm-core.md) | Das Datum, an dem der Inhalt auf einem digitalen Kanal oder einer digitalen Plattform erstmals ausgestrahlt wurde. Da es sich bei dieser Klassifizierungsdimension um eine Zeichenfolge handelt, ist jedes Datumsformat zulässig. Adobe empfiehlt die Verwendung eines konsistenten Datumsformats, z. B. `YYYY-MM-DD`. |
| **[!UICONTROL Anzeigenlänge]** | [!UICONTROL Anzeige] | Die Länge der Videoanzeige in Sekunden. |
| **[!UICONTROL Anzeigename]** | [!UICONTROL Anzeige] | Der Anzeigename der Anzeige. Dies entspricht der Klassifizierung von &quot;[!UICONTROL Anzeigename (Variable)]. |
| **[!UICONTROL Creative-ID]** | [!UICONTROL Anzeige] | Die ID des Kreativinhalts der Anzeige. |
| **[!UICONTROL Pod-Name]** | [!UICONTROL Anzeigen-Pod] | Der Anzeigename des Anzeigen-Pods. |
| **[!UICONTROL Position des Pods]** | [!UICONTROL Anzeigen-Pod] | Der Versatz der Werbeunterbrechung innerhalb des Inhalts in Sekunden. |
