---
title: Kompatibilität von Analytics-Dimensionen
description: Referenz zu Analytics-Dimensionen und -Berichten.
feature: Dimensions
exl-id: 1884bc20-b04d-4f9a-b057-2b2fbe53190d
TQID: https://experienceleague.adobe.com/WntN8KyUXgQUt8vvoHUZyQfTtEUSS3aPOF6pIDbJynk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705cid: c9bb7ea6-c04f-4262-b69c-fbb8d91e3559id: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 905
ht-degree: 48%

---

# Kompatibilität von Analytics-Dimensionen

Auf dieser Seite werden [Dimensionen](overview.md) aufgeführt, die in ihren jeweiligen Analytics-Funktionen unterstützt werden.

>[!NOTE]
>
>Benutzerdefinierte Variablennamen, Klassifizierungen und Besucherattribute werden in dieser Liste weggelassen. Diese Dimensionselemente sind spezifisch für einzelne Report Suites.

## In Analysis Workspace unterstützte Dimensionen

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|---|---|
| Analytics for Target | `targetraw` |
| Zielgruppen-ID | `mcaudiences` |
| [Browser](browser.md) | `browser` |
| [Browser-Typ](browser-type.md) | `browsertype` |
| [Kategorie](category.md) | `category` |
| [Städte](cities.md) | `geocity` |
| [Farbtiefe](color-depth.md) | `colordepth` |
| [Verbindungstyp](connection-type.md) | `connectiontype` |
| [Cookie-Unterstützung](cookie-support.md) | `cookie` |
| [Länder](countries.md) | `geocountry` |
| [Kundentreue](customer-loyalty.md) | `customerloyalty` |
| [Benutzerdefinierte Konversionsvariablen](evar.md) | `evar1`, `evar2` usw. |
| [Custom Insight-Vars](prop.md) | `prop1`, `prop2` usw. |
| [Anwenderspezifischer Link](custom-link.md) | `customlink` |
| [Tage bis Erstkauf](days-before-first-purchase.md) | `daysbeforefirstpurchase` |
| [Tage seit letztem Kauf](days-since-last-purchase.md) | `dayssincelastpurchase` |
| [Domain](domain.md) | `filtereddomain` |
| [Downloadlink](download-link.md) | `downloadlink` |
| [Einstiegsseite](entry-dimensions.md) | `entrypage` |
| [Einstiegsseite Original](entry-dimensions.md) | `entrypageoriginal` |
| [Exitlink](exit-link.md) | `exitlink` |
| [Erstkontakt-Kanal](first-touch-channel.md) | `firsttouchchannel` |
| [Detail des Erstkontaktkanals](first-touch-detail.md) | `firsttouchchanneldetail` |
| [Java aktiviert](java-enabled.md) | `javaenabled` |
| [Sprache](language.md) | `language` |
| [Letztkontakt-Kanal](last-touch-channel.md) | `lasttouchchannel` |
| [Detail des Letztkontaktkanals](last-touch-detail.md) | `lasttouchchanneldetail` |
| Listenvariablen | `listvariables` |
| [Marketing-](marketing-channel.md) | `marketingchannel` |
| [Mobile Audio-Unterstützung](mobile-dimensions.md) | `mobileaudiosupport` |
| [Mobilnetzbetreiber](mobile-dimensions.md) | `mobilecarrier` |
| [Mobile Farbtiefe](mobile-dimensions.md) | `mobilecolordepth` |
| [Unterstützung mobiler Cookies](mobile-dimensions.md) | `mobilecookiesupport` |
| [Mobilgerät](mobile-dimensions.md) | `mobiledevicename` |
| [Mobilgerätetyp](mobile-dimensions.md) | `mobiledevicetype` |
| [Maximale E-Mail-Länge für Mobilgeräte](mobile-dimensions.md) | `mobileemaillength` |
| [Unterstützung mobiler Bilder](mobile-dimensions.md) | `mobileimagesupport` |
| [Mobilgerätehersteller](mobile-dimensions.md) | `mobilemanufacturer` |
| [Betriebssystem für Mobilgeräte (veraltet)](mobile-dimensions.md) | `mobileos` |
| [Mobilgerät - Bildschirmhöhe](mobile-dimensions.md) | `mobilescreenheight` |
| [Mobilgerät - Bildschirmgröße](mobile-dimensions.md) | `mobilescreensize` |
| [Mobilgerät - Bildschirmbreite](mobile-dimensions.md) | `mobilescreenwidth` |
| [Maximale Browser-URL-Länge für Mobilgeräte](mobile-dimensions.md) | `mobileurllength` |
| [Unterstützung für Mobilgeräte](mobile-dimensions.md) | `mobilevideosupport` |
| [Bildschirmauflösung](monitor-resolution.md) | `monitorresolution` |
| [Betriebssysteme](operating-systems.md) | `operatingsystem` |
| [Ursprünglich verweisende Domain](original-referring-domain.md) | `referringdomainoriginal` |
| [Seite](page.md) | `page` |
| [Seiten nicht gefunden](pages-not-found.md) | `pagesnotfound` |
| [Produkt](product.md) | `product` |
| [Referrer](referrer.md) | `referrer` |
| [Typ der verweisenden Stelle](referrer-type.md) | `referrertype` |
| [Verweisende Domain](referring-domain.md) | `referringdomain` |
| [Regionen](regions.md) | `georegion` |
| [Rückkehrhäufigkeit](return-frequency.md) | `returnfrequency` |
| SC-TnT | `tntbase` |
| [Suchmaschine](search-engine.md) | `searchengine` |
| [Keywords](search-keyword.md) | `searchenginekeyword` |
| [Suchmaschine - Organisch](search-engine.md) | `searchenginenatural` |
| [Suchmaschine - Paid](search-engine.md) | `searchenginepaid` |
| [Suchbegriff - Organisch](search-keyword.md) | `searchenginenaturalkeyword` |
| [Suchbegriff - Paid](search-keyword.md) | `searchenginepaidkeyword` |
| [Ranking aller Suchseiten](all-search-page-rank.md) | `searchenginepagerank` |
| [Server](server.md) | `server` |
| [Einzelseitenbesuche](single-page-visits.md) | `singlepagevisits` |
| [Site-Bereich](site-section.md) | `sitesections` |
| [Besuchszeit pro Besuch - granular](time-spent-per-visit.md) | `sitetime` |
| [Trackingcode](tracking-code.md) | `campaign` |
| [US-DMA](us-dma.md) | `geodma` |
| [US-Bundesstaaten](us-states.md) | `state` |
| [Zeit vor Ereignis](time-prior-to-event.md) | `timeprior` |
| [Besuchszeit pro Besuch - in Buckets](time-spent-per-visit.md) | `timespent` |
| [Besuchstiefe](visit-depth.md) | `pathlength` |
| [Besuchnummer](visit-number.md) | `visitnumber` |
| [Postleitzahl](zip-code.md) | `zip` |
| [AM/PM](am-pm.md) | `timepartampm` |
| [Browser-Höhe - Behälter](browser-height.md) | `browserheightbucketed` |
| [Browser-Breite - Behälter](browser-width.md) | `browserwidthbucketed` |
| [Tag](day.md) | `daterangeday` |
| [Tag des Monats](day-of-month.md) | `timepartdayofmonth` |
| [Wochentag](day-of-week.md) | `dayofweek` |
| [Wochentag](day-of-week.md) | `timepartdayofweek` |
| [Tag des Jahres](day-of-year.md) | `timepartdayofyear` |
| [Tage seit dem letzten Besuch](days-since-last-visit.md) | `dayssincelastvisit` |
| [Benutzerdefinierte Einblicke eingeben](entry-dimensions.md) | `entryprops` |
| [Eintragslistenvariablen](entry-dimensions.md) | `entrylistvariables` |
| [Einstiegsserver](entry-dimensions.md) | `entryserver` |
| [Einstiegsbereich](entry-dimensions.md) | `entrysitesections` |
| [Benutzerdefinierte Einblicke beenden](exit-dimensions.md) | `exitprops` |
| [Listenvariablen beenden](exit-dimensions.md) | `exitlistvariables` |
| [Exitpage](exit-dimensions.md) | `exitpage` |
| [Server beenden](exit-dimensions.md) | `exitserver` |
| [Site-Bereich beenden](exit-dimensions.md) | `exitsitesections` |
| [Treffertiefe](hit-depth.md) | `hitdepth` |
| [Treffertyp](hit-type.md) | `customerperspective` |
| [Stunde](hour.md) | `daterangehour` |
| [Stunde des Tages](hour-of-day.md) | `timeparthourofday` |
| [Details zum Marketing-Kanal](marketing-detail.md) | `marketingchanneldetail` |
| [Minute](minute.md) | `daterangeminute` |
| [Maximale Lesezeichenlänge für Mobilgeräte](mobile-dimensions.md) | `mobilebookmarklength` |
| [Mobilgerätenummer](mobile-dimensions.md) | `mobiledevicenumber` |
| [Mobiler DRM](mobile-dimensions.md) | `mobiledrm` |
| [Mobile Informationsdienste](mobile-dimensions.md) | `mobileinformationservices` |
| [Mobile Java VM](mobile-dimensions.md) | `mobilejavavm` |
| [Mobile Mail Dekoration](mobile-dimensions.md) | `mobilemaildecoration` |
| [Mobile Net-Protokolle](mobile-dimensions.md) | `mobilenetprotocols` |
| [Mobiler Push zum Sprechen](mobile-dimensions.md) | `mobilepushtotalk` |
| [Monat](month.md) | `daterangemonth` |
| [Monat des Jahres](month-of-year.md) | `timepartmonthofyear` |
| [Betriebssystemtypen](operating-system-types.md) | `operatingsystemgroup` |
| [Paid Search](paid-search.md) | `paidsearch` |
| [Unterstützung persistenter Cookies](persistent-cookie-support.md) | `persistentcookie` |
| [Quartal](quarter.md) | `daterangequarter` |
| [Quartal des Jahres](quarter-of-year.md) | `timepartquarterofyear` |
| Umfrage | `surveybase` |
| [Besuchszeit pro Seite - Behälter](time-spent-on-page.md) | `averagepagetime` |
| [Besuchszeit pro Seite - Granular](time-spent-on-page.md) | `pagetimeseconds` |
| [Tracking des Abmeldegrundes](tracking-opt-out-reason.md) | `optoutreason` |
| [Wochentag / Wochenende](weekday-weekend.md) | `timepartweekdayweekend` |
| [Woche](week.md) | `daterangeweek` |
| [Jahr](year.md) | `daterangeyear` |

## Inhaltsorientierte Dimensionen, die nur in Analysis Workspace unterstützt werden

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|--- |--- |
| Activity Map – XY | `clickmapxy` |
| Mediensitzungs-ID | `videosessionid` |
| Nielsen-Zugriffsmethode | `nielsenaccmethod` |
| Nielsen-App-ID | `nielsenappid` |
| Nielsen-Kanal-Asset | `nielsenchannelasset` |
| Nielsen-Content-Typ | `nielsencontenttype` |

## Von Analysis Workspace unterstützte inhaltsbezogene Dimensionen

### Video (Streaming-Mediendienste)

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|--- |--- |
| [Inhalt](sm-core.md) | `video` |
| [Inhaltssegment](sm-core.md) | `videosegment` |
| [Content-Typ](sm-core.md) | `videocontenttype` |
| [Anzeigenplayer-Name](sm-ads.md) | `videoadplayername` |
| [Anzeige in Position Pod](sm-ads.md) | `videoadinpod` |
| [Dropped Frames](sm-quality.md) | `videoqoedroppedframecountevar` |
| [Fehler](sm-quality.md) | `videoqoeerrorcountevar` |
| [Durchschnittliche Bitrate](sm-quality.md) | `videoqoebitrateaverageevar` |
| [Bitratenänderungen](sm-quality.md) | `videoqoebitratechangecountevar` |
| [Gesamtdauer des Puffers](sm-quality.md) | `videoqoebuffertimeevar` |
| [Pufferereignisse](sm-quality.md) | `videoqoebuffercountevar` |
| [Zeit bis zum Start](sm-quality.md) | `videoqoetimetostartevar` |
| [Werbeblock](sm-ads.md) | `videoadpod` |
| [Medienpfad](sm-core.md) | `videopath` |
| [Anzeige](sm-ads.md) | `videoad` |
| [Name des Inhalts-Players](sm-core.md) | `videoplayername` |
| [Inhaltskanal](sm-core.md) | `videochannel` |
| [Kapitel](sm-chapters.md) | `videochapter` |
| [Inhaltsname (Variable)](sm-core.md) | `videoname` |
| [Inhaltslänge (variabel)](sm-core.md) | `videolength` |
| [Anzeigename (Variable)](sm-ads.md) | `videoadname` |
| [Anzeigenlänge (variabel)](sm-ads.md) | `videoadlength` |
| [Anzeigen](sm-video-metadata.md) | `videoshow` |
| [Staffel](sm-video-metadata.md) | `videoseason` |
| [Folge](sm-video-metadata.md) | `videoepisode` |
| [Netzwerk](sm-video-metadata.md) | `videonetwork` |
| [Sendungstyp](sm-video-metadata.md) | `videoshowtype` |
| [Anzeigenladevorgänge](sm-ads.md) | `videoadload` |
| [MVPD](sm-video-metadata.md) | `videomvpd` |
| [Day Part](sm-video-metadata.md) | `videodaypart` |
| [Advertiser](sm-ads.md) | `videoadadvertiser` |
| [Kampagnen-ID](sm-ads.md) | `videoadcampaign` |
| [Genre](sm-video-metadata.md) | `videogenre` |
| [Stream-Typ](sm-core.md) | `videostreamtype` |
| [Player SDK-Fehler-IDs](sm-quality.md) | `videoqoeplayersdkerrors` |
| [Externe Fehler-IDs](sm-quality.md) | `videoqoeextneralerrors` |
| [Medien-Feed-Typ](sm-video-metadata.md) | `videofeedtype` |
| [Medieneinstiegspfad](entry-dimensions.md) | `entryvideopath` |
| [Medienpfad beenden](exit-dimensions.md) | `exitvideopath` |
| [Einstiegsgenre](entry-dimensions.md) | `entryvideogenre` |
| [Genre beenden](exit-dimensions.md) | `exitvideogenre` |
| [Eintrags-Player SDK-Fehler-IDs](entry-dimensions.md) | `entryvideoqoeplayersdkerrors` |
| [Player-SDK-Fehler-IDs beenden](exit-dimensions.md) | `exitvideoqoeplayersdkerrors` |
| [Einstiegs-IDs für externe Fehler](entry-dimensions.md) | `entryvideoqoeextneralerrors` |
| [Externe Fehler-IDs beenden](exit-dimensions.md) | `exitvideoqoeextneralerrors` |

### Adobe Social

Adobe Social ist eingestellt.

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|--- |--- |
| Begriffe | `socialterm` |
| Soziale Plattformen/Eigenschaften | `socialcontentprovider` |
| Autoren | `socialauthor` |
| Sprache | `sociallanguage` |
| Breitengrad/Längengrad | `sociallatlong` |
| Asset-Trackingcodes | `socialassettrackingcode` |
| Eigene Social-Media-Präsenzen | `socialaccountandappids` |
| Eigene Post-IDs | `socialownedpostids` |
| Eigene Social-Media-Definitionen | `socialinteractiontype` |
| Eigene Eigenschafts-IDs | `socialownedpropertyid` |
| Eigene Eigenschaften vs. Anwendung | `socialownedpropertypropertyvsapp` |
| Eigener Eigenschaftsname | `socialownedpropertyname` |
| Eigene Definitionseigenschaft vs. Post | `socialowneddefinitionpropertyvspost` |
| Eigene Definition – Insight-Typ | `socialowneddefinitioninsighttype` |
| Eigene Definition – Insight-Wert | `socialowneddefinitioninsightvalue` |
| Eigene Definition – Metrik | `socialowneddefinitionmetric` |
| Asset | `socialmediaid` |

### Mobile SDK

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|--- |--- |
| [Erstes Startdatum](lifecycle-dimensions.md) | `mobileinstalldate` |
| [App-ID](lifecycle-dimensions.md) | `mobileappid` |
| [Startanzahl](lifecycle-dimensions.md) | `mobilelaunchnumber` |
| [Tage seit der ersten Verwendung](lifecycle-dimensions.md) | `mobiledayssincefirstuse` |
| [Tage seit der letzten Verwendung](lifecycle-dimensions.md) | `mobiledayssincelastuse` |
| [Stunde des Tages (SDK)](lifecycle-dimensions.md) | `mobilehourofday` |
| [Wochentag (SDK)](lifecycle-dimensions.md) | `mobiledayofweek` |
| [Betriebssystem (SDK)](lifecycle-dimensions.md) | `mobileosenvironment` |
| [Tage seit letztem Upgrade](lifecycle-dimensions.md) | `mobiledayssincelastupgrade` |
| [Starts seit letztem Upgrade](lifecycle-dimensions.md) | `mobilelaunchessincelastupgrade` |
| [Gerätename (SDK)](lifecycle-dimensions.md) | `mobiledevice` |
| [Betriebssystemversion (SDK)](lifecycle-dimensions.md) | `mobileosversion` |
| [Beacon Major](lifecycle-dimensions.md) | `mobilebeaconmajor` |
| [Beacon-Minor](lifecycle-dimensions.md) | `mobilebeaconminor` |
| [Beacon-UUID](lifecycle-dimensions.md) | `mobilebeaconuuid` |
| [Beacon-Nähe](lifecycle-dimensions.md) | `mobilebeaconproximity` |
| [Standort (bis 10 km)](lifecycle-dimensions.md) | `latlon1` |
| [Standort (bis 100 m)](lifecycle-dimensions.md) | `latlon23` |
| [Standort (bis 1 m)](lifecycle-dimensions.md) | `latlon45` |
| [Zielpunkt-Bezeichnung](lifecycle-dimensions.md) | `pointofinterest` |
| [Entfernung zum Zentrum des Zielpunkts](lifecycle-dimensions.md) | `pointofinterestdistance` |
| [Standortgenauigkeit](lifecycle-dimensions.md) | `mobileplaceaccuracy` |
| [Platzierungskategorie](lifecycle-dimensions.md) | `mobileplacecategory` |
| [Orts-ID](lifecycle-dimensions.md) | `mobileplaceid` |
| [Eintritt Beacon Major](lifecycle-dimensions.md) | `entrymobilebeaconmajor` |
| [Beacon-Major-](lifecycle-dimensions.md) | `exitmobilebeaconmajor` |
| [Eintritt Beacon Minor](lifecycle-dimensions.md) | `entrymobilebeaconminor` |
| [Beacon-Minor-](lifecycle-dimensions.md) | `exitmobilebeaconminor` |
| [Eingabe Beacon UUID](lifecycle-dimensions.md) | `entrymobilebeaconuuid` |
| [Beacon-UUID beenden](lifecycle-dimensions.md) | `exitmobilebeaconuuid` |
| [Nähe des Beacons](lifecycle-dimensions.md) | `entrymobilebeaconproximity` |
| [Beacon-Nähe beenden](lifecycle-dimensions.md) | `exitmobilebeaconproximity` |

### Adobe Advertising

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|--- |--- |
| AMO EF ID | `amo_ef_id` |
| AMO-ID | `amo_cid` |

### Activity Map

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|--- |--- |
| [Activity Map-Link nach Region](activity-map-link-by-region.md) | `clickmaplinkbyregion` |
| [Activity Map-Region](activity-map-region.md) | `clickmapregion` |
| [Activity Map-Link](activity-map-link.md) | `clickmaplink` |
| [Activity Map-Seite](activity-map-page.md) | `clickmappage` |

### Nielsen-Integration

Weitere Informationen zur Implementierung dieser Integration finden Sie unter [Nielsen-Erweiterung](https://exchange.adobe.com/apps/ec/101361) auf der Adobe Exchange.

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|--- |--- |
| Nielsen-Anzeigemodell | `nielsenadmodel` |
| Nielsen-Segment C | `nielsensegmentc` |
| Nielsen-Segment B | `nielsensegmentb` |
| Nielsen-Segment A | `nielsensegmenta` |
| Nielsen-Inhalts-ID | `nielsencontentid` |
| Nielsen Asset / Programm | `nielsenasset` |
| Nielsen-VCID | `nielsenvcid` |
| Nielsen Opt-out | `nielsenoptout` |
| Nielsen-Client-ID und -VCID | `nielsenclientidvcid` |
| Nielsen-Client-ID | `nielsenclientid` |
| Einstieg-Nielsen-Ausschluss | `entrynielsenoptout` |
| Ausstieg-Nielsen-Ausschluss | `exitnielsenoptout` |
| Einstieg-Nielsen-Client-ID und -VCID | `entrynielsenclientidvcid` |
| Ausstieg-Nielsen-Client-ID und -VCID | `exitnielsenclientidvcid` |
| Einstieg-Nielsen-Client-ID | `entrynielsenclientid` |
| Ausstieg-Nielsen-Client-ID | `exitnielsenclientid` |

### Adobe Experience Manager (AEM)

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|--- |--- |
| Element-ID | `aemassetid` |
| Asset-Quelle | `aemassetsource` |
| Angeklickte Asset-ID | `aemclickedassetid` |
| Einstieg-Asset-ID | `entryaemassetid` |
| Ausstieg-Asset-ID | `exitaemassetid` |

### Adobe Campaign

| Dimensionsname (in Analytics-UI sichtbar) | Dimension-ID (in API-Anfragen verwendet) |
|--- |--- |
| ID des von Adobe Campaign ausgeführten Versands | `ac_delivery_internal_name` |
