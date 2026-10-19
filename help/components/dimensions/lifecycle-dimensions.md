---
title: Lebenszyklusdimensionen für Mobile
description: Dimensionen, die auf Daten basieren, die mit der Mobile SDK erfasst werden.
feature: Dimensions
exl-id: b7ba45d7-7d30-48a3-a747-ea9fbb253abb
TQID: 'https://experienceleague.adobe.com/VUN8x5eMzIfJ9VGw76v2pWfKWU7b-ct-kI6liwWTObw'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
  - id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
    internal-label: Dimensions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 6fd4400b33fcfc8bc3cd3ffc54fa738fef3441ef
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 8%
---
# Lebenszyklusdimensionen für Mobile

>[!BEGINSHADEBOX]

*Diese Seite verweist auf Daten, die häufig über die Adobe Experience Platform Mobile SDK verfolgt werden. Informationen zu Mobilgeräten mit dem Benutzeragenten finden Sie unter [Dimensionen für die mobile Suche](mobile-dimensions.md). Metriken, die mit der Mobile SDK verfolgt werden, finden Sie unter [Mobile Lebenszyklusmetriken](../metrics/lifecycle-metrics.md).*

>[!ENDSHADEBOX]

| Name der Lebenszyklusdimension | Beschreibung | Kontextdatenvariable |
| --- | --- | --- |
| **[!UICONTROL Erstes Startdatum]** | Das Datum, an dem die App zum ersten Mal ausgeführt wurde, nachdem sie installiert oder neu installiert wurde, `M/d/yyyy` im -Format. | `a.InstallDate` |
| **[!UICONTROL Gerätename (SDK)]** | Der Gerätename, den die SDK erfasst. | `a.DeviceName` |
| **[!UICONTROL Betriebssystemversion (SDK)]** | Der Betriebssystemname und die Version, die von SDK erfasst werden. | `a.OSVersion` |
| **[!UICONTROL Resolution (SDK)]** | Die Bildschirmauflösung des Geräts in Pixeln, als Breite x Höhe. | `a.Resolution` |
| **[!UICONTROL Akquise-Source]** | Der ursprüngliche Referrer für eine App-Akquise-Kampagne, z. B. ein Newsletter oder ein Social-Media-Netzwerk. | `a.referrer.campaign.source` |
| **[!UICONTROL App-ID]** | Der App-Name und die Version im Format `AppName BundleVersion (app version code)`. Beispiel: `MyAppName 1.1(1)`. | `a.AppID` |
| **[!UICONTROL Akquise-Medium]** | Das Marketing-Medium für eine App-Akquise-Kampagne, z. B. ein Banner oder eine E-Mail. | `a.referrer.campaign.medium` |
| **[!UICONTROL Akquisitionsbedingung]** | Kostenpflichtige Keywords oder andere Begriffe, die mit einer App-Akquise-Kampagne verbunden sind. | `a.referrer.campaign.term` |
| **[!UICONTROL Akquise-Inhalte]** | Der Name oder die ID des Inhalts, der den App-Akquise-Link angezeigt hat. | `a.referrer.campaign.content` |
| **[!UICONTROL Akquise-Name]** | Der Name der App-Akquise-Kampagne. | `a.referrer.campaign.name` |
| **[!UICONTROL Standort (bis 10 km)]** | Breiten- und Längengrad des Besuchers, genau bis zur ersten Dezimalstelle. Beispiel: `040.9` `-111.9`. | `a.loc.lat.a` + `a.loc.lon.a` |
| **[!UICONTROL Standort (bis 100 m)]** | Breiten- und Längengrad des Besuchers, genau bis zur dritten Dezimalstelle. Beispiel: `040.932` `-111.931`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lon.a` + `a.loc.lon.b` |
| **[!UICONTROL Standort (bis 1 m)]** | Breiten- und Längengrad des Besuchers, genau bis zur fünften Dezimalstelle. Beispiel: `040.93231` `-111.93152`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lat.c` + `a.loc.lon.a` + `a.loc.lon.b` + `a.loc.lon.c` |
| **[!UICONTROL Zielpunkt-Bezeichnung]** | Der Name des Points of Interest (POI), in dem sich das Gerät befindet. Wenn Sie die Erweiterung [Places](https://developer.adobe.com/client-sdks/solution/places/) verwenden, ist dieser Wert der Name der Region Places . | `a.loc.poi` |
| **[!UICONTROL Entfernung zum Zentrum des Zielpunkts]** | Der Abstand zwischen dem Gerät und dem Mittelpunkt des Zielpunkts, an dem sich das Gerät befindet. | `a.loc.dist` |
| **[!UICONTROL Startanzahl]** | Die Häufigkeit, mit der die App gestartet oder aus dem Hintergrund gebracht wurde. | `a.Launches` |
| **[!UICONTROL Tage seit der ersten Verwendung]** | Die Anzahl der Tage seit der ersten Ausführung der App. | `a.DaysSinceFirstUse` |
| **[!UICONTROL Aktionsname]** | Der Name der Aktion, die in einem `trackAction`-Aufruf gesendet wird. | `a.action` |
| **[!UICONTROL Lebenszeitwert (eVar)]** | Der Lebenszeitwert eines Benutzers, z. B. Käufe über die gesamte Lebensdauer, Anzeigen-Ansichten, abgeschlossene Videos oder Social Shares. | `a.ltv.amount` |
| **[!UICONTROL Beacon Major]** | Die Haupt-ID des Beacons, in dessen Nähe sich das Gerät befindet. | `a.beacon.major` |
| **[!UICONTROL Beacon-Minor]** | Die kleinere ID des Beacons, in dessen Nähe sich das Gerät befindet. | `a.beacon.minor` |
| **[!UICONTROL Beacon-UUID]** | Die UUID des Beacons, in dessen Nähe sich das Gerät befindet. | `a.beacon.uuid` |
| **[!UICONTROL Beacon-Nähe]** | Die Nähe des Geräts zum Beacon: `0` (unbekannt), `1` (unmittelbar), `2` (nah) oder `3` (fern). | `a.beacon.prox` |
| **[!UICONTROL Tage seit der letzten Verwendung]** | Die Anzahl der Tage seit der letzten Verwendung der App. | `a.DaysSinceLastUse` |
| **[!UICONTROL Stunde des Tages (SDK)]** | Die Stunde, in der die App gestartet wurde, im 24-Stunden-Format. Nützlich für die Zeitunterteilung, um Spitzenauslastungszeiten zu ermitteln. | `a.HourOfDay` |
| **[!UICONTROL Wochentag (SDK)]** | Der Wochentag, an dem die App gestartet wurde. | `a.DayOfWeek` |
| **[!UICONTROL Point of Interest-ID]** | Die ID des Points of Interest, an dem sich das Gerät befindet. Wenn Sie die Erweiterung [Places](https://developer.adobe.com/client-sdks/solution/places/) verwenden, ist dieser Wert die Regions-ID für die Orte. | `a.loc.poi.id` |

>[!NOTE]
>
>Einige dieser Dimensionen werden mit Methoden aus der veralteten Mobile Services SDK (4.x) gefüllt, die nicht mehr unterstützt wird. Adobe Experience Platform Mobile SDK füllt sie nicht automatisch:
>
>* **Akquise-Dimensionen** ([!UICONTROL Akquise-Source], [!UICONTROL Medium], [!UICONTROL Term], [!UICONTROL Content] und [!UICONTROL Name]): Ausgefüllt durch die Akquise von Mobile Apps, die die Mobile-SDK [nicht unterstützt](https://developer.adobe.com/client-sdks/resources/upgrade-platform-sdks/comparison/).
>* **[!UICONTROL Standort] Abmessungen und [!UICONTROL Entfernung zum Point of Interest Center]**: Wird mit der `trackLocation`-Methode 4.x ausgefüllt. Mobile SDK ersetzt diese Methode durch die [Places-Erweiterung](https://developer.adobe.com/client-sdks/solution/places/) mit den Ausfüllungen [!UICONTROL Point of Interest Name] und [!UICONTROL Point of Interest ID].
>* **[!UICONTROL Lebenszeitwert (eVar)]**: Wird mit der `trackLifetimeValueIncrease`-Methode 4.x aufgefüllt.
>* **Beacon-Dimensionen** ([!UICONTROL Beacon Major], [!UICONTROL Minor], [!UICONTROL UUID] und [!UICONTROL Proximity]): Wird mit der 4.x `trackBeacon`-Methode aufgefüllt. Informationen zum Senden von Beacon-Daten mit Mobile SDK finden Sie unter [Tracking von Beacons](https://developer.adobe.com/client-sdks/solution/adobe-analytics/track-beacon/).
>
>Weitere Informationen finden Sie unter Migration von [Adobe Mobile Library (v4](https://developer.adobe.com/client-sdks/resources/upgrade-platform-sdks/analytics/) zu Experience Platform Analytics .
