---
title: Lebenszyklusdimensionen für Mobile
description: Dimensionen, die auf Daten basieren, die mit der Mobile SDK erfasst werden.
feature: Dimensions
exl-id: b7ba45d7-7d30-48a3-a747-ea9fbb253abb
TQID: https://experienceleague.adobe.com/VUN8x5eMzIfJ9VGw76v2pWfKWU7b-ct-kI6liwWTObw
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 29%
---
# Lebenszyklusdimensionen für Mobile

>[!BEGINSHADEBOX]

*Diese Seite verweist auf Daten, die häufig über die Adobe Experience Platform Mobile SDK nachverfolgt werden. Informationen zu Mobilgeräten mit dem Benutzeragenten finden Sie unter [Dimensionen für die mobile Suche](mobile-dimensions.md). Metriken, die mit der Mobile SDK verfolgt werden, finden Sie unter [Mobile Lebenszyklusmetriken](../metrics/lifecycle-metrics.md).*

>[!ENDSHADEBOX]

| Name der Lebenszyklusdimension | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| [!UICONTROL Erstes Startdatum] | | |
| [!UICONTROL Gerätename (SDK)] | | `a.DeviceName` |
| [!UICONTROL Betriebssystemversion (SDK)] | | `a.OSVersion` |
| [!UICONTROL Resolution (SDK)] | | `a.Resolution` |
| [!UICONTROL Akquise-Source] | | `a.referrer.campaign.source` |
| [!UICONTROL App-ID] | | `a.AppID` |
| [!UICONTROL Akquise-Medium] | | `a.referrer.campaign.medium` |
| [!UICONTROL Akquisitionsbedingung] | | `a.referrer.campaign.term` |
| [!UICONTROL Akquise-Inhalte] | | `a.referrer.campaign.content` |
| [!UICONTROL Akquise-Name] | | `a.referrer.campaign.name` |
| [!UICONTROL Standort (bis 10 km)] | Breiten- und Längengrad des Besuchers, genau bis zur ersten Dezimalstelle. Beispiel: `040.9` `-111.9`. | `a.loc.lat.a` + `a.loc.lon.a` |
| [!UICONTROL Standort (bis 100 m)] | Breiten- und Längengrad des Besuchers, genau bis zur dritten Dezimalstelle. Beispiel: `040.932` `-111.931`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lon.a` + `a.loc.lon.b` |
| [!UICONTROL Standort (bis 1 m)] | Breiten- und Längengrad des Besuchers, genau bis zur fünften Dezimalstelle. Beispiel: `040.93231` `-111.93152`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lat.c` + `a.loc.lon.a` + `a.loc.lon.b` + `a.loc.lon.c` |
| [!UICONTROL Zielpunkt-Bezeichnung] | | `a.loc.poi` |
| [!UICONTROL Entfernung zum Zentrum des Zielpunkts] | | `a.loc.dist` |
| [!UICONTROL Startanzahl] | | `a.Launches` |
| [!UICONTROL Tage seit der ersten Verwendung] | | `a.DaysSinceFirstUse` |
| [!UICONTROL Aktionsname] | | |
| [!UICONTROL Lebenszeitwert (eVar)] | | `a.ltv.amount` |
| [!UICONTROL Beacon Major] | | |
| [!UICONTROL Beacon-Minor] | | |
| [!UICONTROL Beacon-UUID] | | |
| [!UICONTROL Beacon-Nähe] | | |
| [!UICONTROL Tage seit der letzten Verwendung] | | `a.DaysSinceFirstUse` |
| [!UICONTROL Stunde des Tages (SDK)] | | `a.HourOfDay` |
| [!UICONTROL Wochentag (SDK)] | | `a.DayOfWeek` |
| [!UICONTROL Point of Interest-ID] | | |

<!-- Missing: Install Date -->
