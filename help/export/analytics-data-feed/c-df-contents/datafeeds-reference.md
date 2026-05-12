---
description: Tabellendaten, die die Spalten im Daten-Feed beschreiben.
keywords: Daten-Feed;Spalten
subtopic: data feeds
title: Datenspaltenreferenz
feature: Data Feeds
exl-id: e1492147-6e7f-4921-b509-898e7efda596
TQID: https://experienceleague.adobe.com/EcbkWUUxHG0e3O8f9f8G5yBAqYHb-tocQygeWY2Zqfc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: b7156124-d291-4de4-ac0c-ed17d8078449id: c153fd90-23e1-4614-81d3-3cc7571227f7id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: eb9732ab-8232-4b21-bc4c-89de86dbe4d7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: c069c44e-5426-4c1a-accc-8028662f2fdeid: c4cb071e-4667-4fb1-b1f1-d8994549cfb2id: c9bb7ea6-c04f-4262-b69c-fbb8d91e3559id: ce57bdb9-8bbb-4c80-b9ab-e52598027bb9id: e7d92df1-c5ba-4e93-85df-f83171b889beid: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f1f1a2d4-0976-4881-b091-c2bb8de7ffacid: fe0a7292-80bc-407a-b456-64170267d1cc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 2c048f2c59b19ab8e19f53c3f2acea613e50a64a
workflow-type: tm+mt
source-wordcount: 4148
ht-degree: 78%

---

# Datenspaltenreferenz

Auf dieser Seite erfahren Sie, welche Daten in den einzelnen Spalten enthalten sind. Bei den meisten Implementierungen wird nicht alle Spalten verwendet. Daher können Sie diese Seite konsultieren, wenn Sie entscheiden müssen, welche Spalten in einen Daten-Feed-Export einbezogen werden sollen.

>[!IMPORTANT]
>
>Für bestimmte Spalten (beispielsweise bei Definition als 255 Zeichen) kann ein Daten-Feed zusätzliche Zeichen senden, da Maskierungszeichenwerte in Zeichenfolgen hinzugefügt werden. Berücksichtigen Sie diese möglichen zusätzlichen Zeichen, wenn Ihre Implementierung regelmäßig Werte sendet, die die Zeichenbeschränkungen überschreiten.

## Spalten, Beschreibungen und Datentypen

>[!NOTE]
>
>Die meisten Spalten enthalten eine ähnliche Spalte mit dem Präfix `post_`. Post-Spalten enthalten Werte nach der serverseitigen Logik, den Verarbeitungsregeln und den VISTA-Regeln. Adobe empfiehlt in den meisten Fällen die Verwendung von Post-Spalten. Weitere Informationen finden Sie in den [häufig gestellten Fragen zu Daten-Feeds](../df-faq.md).

Vorherige Aktualisierungen dieser Tabelle finden Sie auf der Seite [Commit-Verlauf auf GitHub](https://github.com/AdobeDocs/analytics.en/commits/main/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md).

| POST | Spaltenname | Spaltenbeschreibung | Datentyp |
| ---: | :--- | --- | --- |
| | **`accept_language`** | Führt alle unterstützten Sprachen, wie im HTTP-Header Accept-Language angegeben, in einer Bildanforderung auf. | char(20) |
| **`post_`** | **`adload`** | Medien-Anzeigenladevorgänge | varchar(255) |
| **`post_`** | **`aemassetid`** | Mehrwert-Variable, die den Asset-IDs (GUIDs) eines Satzes von Adobe Experience Manager-Assets entspricht. Erhöht Impressionsereignisse. | Text |
| **`post_`** | **`aemassetsource`** | Identifiziert die Quelle des Asset-Ereignisses. Wird in Adobe Experience Manager verwendet. | varchar(255) |
| **`post_`** | **`aemclickedassetid`** | Asset-ID eines Adobe Experience Manager-Assets. Erhöht Klickereignisse. | varchar(255) |
| **`post_`** | **`amo_cid`** | Die Dimension [AMO ID](/help/components/dimensions/amo-id.md), die in Adobe Advertising-Integrationen verwendet wird. | varchar(255) |
| **`post_`** | **`amo_ef_id`** | Die Dimension [AMO EF ID](/help/components/dimensions/amo-ef-id.md), die in Adobe Advertising-Integrationen verwendet wird. | varchar(255) |
| | **`browser`** | Numerische ID, die den Browser darstellt. Verweist auf die `browser.tsv` Suchtabelle. | int unsigned |
| **`post_`** | **`browser_height`** | Die Dimension [Browser-Höhe](/help/components/dimensions/browser-height.md). | smallint unsigned |
| **`post_`** | **`browser_width`** | Die [Browser-Breite](/help/components/dimensions/browser-width.md) | smallint unsigned |
| **`post_`** | **`campaign`** | Die Dimension [Trackingcode](/help/components/dimensions/tracking-code.md). | varchar(255) |
| | **`carrier`** | Variable der Adobe Advertising-Integration. Gibt den Mobilnetzbetreiber an. Der Schlüsselwert für die [dynamische Suche](dynamic-lookups.md) von `carrier.tsv`. | varchar(100) |
| **`post_`** | **`channel`** | Die Dimension [Site-Bereiche](/help/components/dimensions/site-section.md). | varchar(100) |
| | **`ch_hdr`** | Client-Hinweise, die über die Kopfzeile der HTTP-Anfrage erfasst werden. | Text |
| | **`ch_js`** | Client-Hinweise, die über die JavaScript-API für Client-Hinweise von Benutzeragenten erfasst werden. | Text |
| **`post_`** | **`clickmaplink`** | Die Dimension [Activity Map](/help/components/dimensions/activity-map-link.md)Link. | varchar(255) |
| **`post_`** | **`clickmaplinkbyregion`** | Die Dimension [Activity Map-Link nach ](/help/components/dimensions/activity-map-link-by-region.md). | varchar(255) |
| **`post_`** | **`clickmappage`** | Die Dimension [Activity Map](/help/components/dimensions/activity-map-page.md)Seite | varchar(255) |
| **`post_`** | **`clickmapregion`** | Die Dimension [Activity Map Region](/help/components/dimensions/activity-map-region.md). | varchar(255) |
| | **`code_ver`** | API- oder Client SDK-Version, die für das Kompilieren und Senden der Bildanforderung verwendet wird. | char(16) |
| | **`color`** | Farbtiefen-ID, basierend auf dem Wert der Spalte `c_color`. Verweist auf die Suchtabelle `color_depth.tsv`. | smallint unsigned |
| | **`connection_type`** | Numerische ID, die die Dimension [Verbindungstyp](/help/components/dimensions/connection-type.md) darstellt. Verweist auf die Suchtabelle `connection_type.tsv` | tinyint unsigned |
| **`post_`** | **`cookies`** | Die [Cookie-Unterstützung](/help/components/dimensions/cookie-support.md) dimension.<br>Y: Aktiviert<br>N: Deaktiviert<br>U: Unbekannt | char(1) |
| | **`country`** | Numerische ID, die das Land der Besucherin bzw. des Besuchers darstellt. Verweist auf die Suchtabelle `country.tsv`. | smallint unsigned |
| **`post_`** | **`currency`** | Der während der Transaktion verwendete Währungscode. Festgelegt über [`currencyCode`](/help/implement/vars/config-vars/currencycode.md). | char(8) |
| | **`ct_connect_type`** | Verknüpft mit der Spalte `connection_type`. Die häufigsten Werte sind LAN/WLAN, Mobilnetzbetreiber und Modem. | char(20) |
| | **`curr_factor`** | Bestimmt die Dezimalstelle für die Währung. Wird für die Währungsumrechnung verwendet. Beispielsweise verwendet USD zwei Dezimalstellen, daher wäre dieser Spaltenwert `2`. | tinyint |
| | **`curr_rate`** | Der Wechselkurs zum Zeitpunkt der Transaktion. Adobe arbeitet mit XE zusammen, um den Wechselkurs des aktuellen Tages zu ermitteln. | decimal(24,12) |
| **`post_`** | **`customer_perspective`** | Bestimmt, ob es sich bei dem Treffer um einen mobilen Hintergrundtreffer handelt. Weitere Informationen finden Sie unter [Kontextbezogene Sitzungen](/help/components/vrs/vrs-mobile-visit-processing.md). | tinyint unsigned |
| **`post_`** | **`cust_hit_time_gmt`** | Nur für Report Suites mit aktiviertem Zeitstempel. Der mit dem Treffer gesendete Zeitstempel in UNIX®-Zeit. | int |
| **`post_`** | **`cust_visid`** | Die benutzerdefinierte Besucher-ID, sofern sie über [`visitorID`](/help/implement/vars/config-vars/visitorid.md) festgelegt wurde. | varchar(255) |
| | **`c_color`** | Bit-Tiefe der Farbpalette. Wird bei der Berechnung der Dimension [Farbtiefe](/help/components/dimensions/color-depth.md) verwendet. AppMeasurement verwendet die JavaScript-Funktion `screen.colorDepth()`. | char(20) |
| | **`daily_visitor`** | Markierung, die bestimmt, ob es sich bei dem Treffer um eine neue tägliche Besucherin oder einen neuen täglichen Besucher handelt. | tinyint unsigned |
| | **`dataprivacyconsentoptin`** | Die Dimension [Opt-in für Einwilligungsverwaltung](/help/components/dimensions/cm-opt-in.md). Pro Treffer können mehrere Werte vorhanden sein, getrennt durch einen senkrechten Strich (`\|`). Gültige Werte sind `DMP` und `SELL`. | varchar(100) |
| | **`dataprivacyconsentoptout`** | Die Dimension [Opt-out für Einwilligungsverwaltung](/help/components/dimensions/cm-opt-out.md). Pro Treffer können mehrere Werte vorhanden sein, getrennt durch einen senkrechten Strich (`\|`). Gültige Werte sind `SSF`, `DMP` und `SELL`. | varchar(100) |
| | **`date_time`** | Die Uhrzeit des Treffers in lesbarem Format, basierend auf der Zeitzone der Report Suite. | datetime |
| | **`domain`** | Die Dimension [Domain](/help/components/dimensions/domain.md). Basierend auf dem Internetzugangspunkt der Besuchenden. | varchar(100) |
| | **`duplicated_from`** | Wird nur in Report Suites mit VISTA-Regeln zur Trefferkopie verwendet. Gibt an, von welcher Report Suite der Treffer kopiert wurde. | varchar(40) |
| | **`duplicate_events`** | Listet jedes Ereignis auf, das als Duplikat gezählt wurde. | varchar(255) |
| | **`duplicate_purchase`** | Markierung, die bestimmt, ob das Kaufereignis für diesen Treffer ignoriert wird, weil es ein Duplikat ist. | tinyint unsigned |
| **`post_`** | **`ef_id`** | Die EF-ID, die in Adobe Advertising-Integrationen verwendet wird. | varchar(255) |
| **`post_`** | **`evar1 - evar250`** | Benutzerdefinierte Variablen 1–250. Wird in [eVar](/help/components/dimensions/evar.md)-Dimensionen verwendet. Jede Organisation verwendet eVars anders. Die beste Anlaufstelle für weitere Informationen darüber, wie Ihre Organisation die jeweiligen eVars ausfüllt, ist ein für Ihre Organisation spezifisches [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md). | varchar(255) |
| **`post_`** | **`event_list`** | Kommagetrennte Liste numerischer IDs, die die durch den Treffer ausgelösten Ereignisse darstellen. Umfasst sowohl Commerce-Ereignisse als [benutzerspezifische Ereignisse 1-1000](/help/components/metrics/custom-events.md). Verwendet die `event.tsv`-Suche. | Text |
| | **`exclude_hit`** | Markierung, die bestimmt, ob der Treffer aus dem Reporting ausgeschlossen wird. Die `visit_num` Spalte wird für ausgeschlossene Treffer nicht inkrementiert<br>1: Nicht verwendet. Teil eines verschrotteten Features.<br>2: Nicht verwendet. Teil einer verschrotteten Funktion.<br>3: Nicht mehr verwendet. Ausschluss des Benutzeragenten<br>4: Ausschluss basierend auf IP-Adresse<br>5: Wichtige Hit-Informationen fehlen, z. B. `page_url`, `pagename`, `page_event` oder `event_list`<br>6: JavaScript hat Hit nicht korrekt verarbeitet<br>7: Kontospezifischer Ausschluss, z. B. in VISTA-Regeln<br>8: Nicht verwendet. Alternative kontospezifische Ausnahme.<br>9: Nicht verwendet. Teil einer ausgemusterten Funktion.<br>10: Ungültiger Währungs-Code<br>11: Bei einem Treffer fehlt ein Zeitstempel in einer Report Suite, die nur einen Zeitstempel enthält, oder ein Treffer enthält einen Zeitstempel in einer Report Suite, die keinen Zeitstempel enthält<br>12: Nicht verwendet. Teil einer verschrotteten Funktion.<br>13: Nicht verwendet. Teil einer ausrangierten Funktion.<br>14: Target-Treffer, der keinem Analytics-Treffer entsprach<br>15: Derzeit nicht verwendet.<br>16: Adobe Advertising-Treffer, der keinem Analytics-Treffer entsprach | tinyint unsigned |
| | **`first_hit_pagename`** | Die Dimension [Ursprüngliche Einstiegsseite](/help/components/dimensions/entry-dimensions.md). Der Name der ursprünglichen Entrypage des Besuchers. | varchar(100) |
| | **`first_hit_page_url`** | Die allererste URL des Besuchers. | varchar(255) |
| | **`first_hit_referrer`** | Die allererste verweisende URL des Besuchers. | varchar(255) |
| | **`first_hit_ref_domain`** | Die Dimension [Ursprünglich verweisende Domain](/help/components/dimensions/original-referring-domain.md). Basierend auf `first_hit_referrer`. Die allererste verweisende Domain des Besuchers. | varchar(100) |
| | **`first_hit_ref_type`** | Numerische ID, die den Referrer-Typ des ursprünglichen Referrers der oder des Besuchenden darstellt. Verweist auf die Suchtabelle `referrer_type.tsv` | tinyint unsigned |
| | **`first_hit_time_gmt`** | Zeitstempel des allerersten Treffers der Besucherin oder des Besuchers in UNIX®-Zeit. | int |
| | **`geo_city`** | Name der Stadt, aus der der Treffer stammt, basierend auf der IP-Adresse. Wird in der Dimension [Städte](/help/components/dimensions/cities.md) verwendet. | char(32) |
| | **`geo_country`** | Abkürzung für das Land, aus dem der Treffer stammt, basierend auf der IP-Adresse. Wird in der Dimension [Länder](/help/components/dimensions/countries.md) verwendet. | char(4) |
| | **`geo_dma`** | Numerische ID des demografischen Bereichs, aus dem der Treffer stammt, basierend auf der IP-Adresse. Wird in der Dimension [US DMA](/help/components/dimensions/us-dma.md) verwendet. | int unsigned |
| | **`geo_region`** | Name des Bundeslands oder der Region des Treffers, basierend auf der IP-Adresse. Wird in der Dimension [Regionen](/help/components/dimensions/regions.md) verwendet. | char(32) |
| | **`geo_zip`** | Die Postleitzahl, von der der Treffer stammt, basierend auf der IP. Hilft beim Ausfüllen der Dimension [Postleitzahl](/help/components/dimensions/zip-code.md). Siehe auch `zip`. | varchar(16) |
| | **`hitid_high`** | Wird mit `hitid_low` zur Identifizierung eines Treffers verwendet. | bigint unsigned |
| | **`hitid_low`** | Wird mit `hitid_high` zur Identifizierung eines Treffers verwendet. | bigint unsigned |
| | **`hit_source`** | Quelle, aus der der Treffer stammt. Die Trefferquellen 1 und 2 werden in Rechnung gestellt. <br>1: Standardbildanforderung ohne Zeitstempel <br>2: Standardbildanforderung mit Zeitstempel <br>3: Live-Datenquellen-Upload mit Zeitstempeln <br>4: Nicht verwendet <br>5: Generischer Datenquellen-Upload <br>6: Nicht mehr verwendet; Full Processing Data Source Upload <br>7: TransactionID Data Source Upload <br>8: Nicht mehr verwendet; Frühere Versionen von Adobe Advertising Data Sources <br>9: Nicht mehr verwendet; Adobe Social-Zusammenfassungsmetriken <br>10: Server-seitige Weiterleitung von Audience Manager verwendet | tinyint unsigned |
| | **`hit_time_gmt`** | Der Zeitstempel des Zeitpunkts, wo der Adobe-Datenerfassungs-Server den Treffer erhielt, basierend auf der UNIX®-Zeit. | int |
| | **`hourly_visitor`** | Markierung, die bestimmt, ob es sich bei dem Treffer um eine neue stündliche Besucherin oder einen neuen stündlichen Besucher handelt. | tinyint unsigned |
| | **`ip`** | IPv4-Adresse basierend auf der HTTP-Kopfzeile der Bildanforderung. Sich gegenseitig ausschließend für `ipv6`; wenn diese Spalte eine nicht verschleierte IP-Adresse enthält, ist `ipv6` leer. | char(20) |
| | **`ipv6`** | Die komprimierte IPv6-Adresse, falls verfügbar. Sich gegenseitig ausschließend für `ip`; wenn diese Spalte eine nicht verschleierte IP-Adresse enthält, ist `ip` leer. | varchar(40) |
| | **`javascript`** | Lookup-ID der JavaScript-Version basierend auf `j_jscript`. Verweist auf die Suchtabelle `javascript_version` | tinyint unsigned |
| **`post_`** | **`java_enabled`** | Die Dimension [[!UICONTROL Java aktiviert]](/help/components/dimensions/java-enabled.md). <br>Y: Aktiviert <br>N: Deaktiviert <br>U: Unbekannt | char(1) |
| | **`j_jscript`** | Vom Browser unterstützte JavaScript-Version. | char(5) |
| | **`language`** | Numerische ID, die die Sprache der oder des Besuchenden darstellt. Verweist auf die Suchtabelle `languages.tsv`. | smallint unsigned |
| | **`last_hit_time_gmt`** | Zeitstempel (in UNIX®-Zeit) des vorherigen Treffers. Wird zur Berechnung der Dimension [[!UICONTROL Tage seit dem letzten Besuch]](/help/components/dimensions/days-since-last-visit.md) verwendet. | int |
| | **`last_purchase_num`** | Die Dimension [Kundentreue](/help/components/dimensions/customer-loyalty.md). Die Anzahl der vorherigen Käufe des Besuchers. <br>0: Keine vorherigen Käufe (kein Kunde) <br>1: 1 vorheriger Kauf (neuer Kunde) <br>2: 2 vorherige Käufe (Bestandskunde) <br>3: 3 oder mehr vorherige Käufe (treuer Kunde) | int unsigned |
| | **`last_purchase_time_gmt`** | Wird in der Dimension [[!UICONTROL Tage seit dem letzten Kauf]](/help/components/dimensions/days-since-last-purchase.md) verwendet. Zeitstempel (in UNIX®-Zeit) des letzten Kaufs. Bei Erstkäufen und Besuchern, die zuvor noch nichts gekauft haben, ist dieser Wert `0`. | int |
| | **`latlon1`** | Standort (bis 10 km) | varchar(255) |
| | **`latlon23`** | Standort (bis 100 m) | varchar(255) |
| | **`latlon45`** | Standort (bis 1 m) | varchar(255) |
| | **`mcvisid`** | Experience Cloud-Besucher-ID. 128-Bit-Zahl bestehend aus zwei verketteten 64-Bit-Zahlen verteilt auf 19 Ziffern. | varchar(255) |
| **`post_`** | **`mc_audiences`** | Liste der Segment-IDs von Audience Manager, zu denen der Besucher gehört. Die Spalte `post_mc_audiences` ändert das Trennzeichen in `--**--`. | Text |
| **`post_`** | **`mobileaction`** | Mobile Aktion. Wird automatisch erfasst, wenn in mobilen Implementierungen `trackAction` aufgerufen wird. Ermöglicht automatisches Action Pathing in der App. | varchar(100) |
| **`post_`** | **`mobileappid`** | ID der Mobile App. Speichert den Namen und die Version der App im folgenden Format: `[AppName] [BundleVersion]`. | varchar(255) |
| | **`mobileappperformanceappid`** | Wird im Apteligent-Daten-Connector verwendet. Die in Apteligent verwendete App-ID. | varchar(255) |
| | **`mobileappperformancecrashid`** | Wird im Apteligent-Daten-Connector verwendet. Die in Apteligent verwendete Absturz-ID. | varchar(255) |
| | **`mobileappstoreobjectid`** | Wird im [!DNL Appfigures]-Daten-Connector verwendet. App Store-Objekt-ID. | varchar(255) |
| | **`mobilebeaconmajor`** | Mobile Services – Haupt-Beacon | varchar(100) |
| | **`mobilebeaconminor`** | Mobile Services – Neben-Beacon | varchar(100) |
| | **`mobilebeaconproximity`** | Mobile Services – Beacon-Nähe | varchar(255) |
| | **`mobilebeaconuuid`** | Mobile Services-Beacon UUID | varchar(100) |
| **`post_`** | **`mobilecampaigncontent`** | Der Name oder die ID des Inhalts, der den Link angezeigt hat. Erfasst durch App-Akquise. | varchar(255) |
| **`post_`** | **`mobilecampaignmedium`** | Marketing-Medium, z. B. ein Banner oder eine E-Mail. Erfasst durch App-Akquise. | varchar(255) |
| **`post_`** | **`mobilecampaignname`** | Name der Kampagne, der zusätzlich in der Kampagnenvariable gespeichert wird. Erfasst durch App-Akquise. | varchar(255) |
| **`post_`** | **`mobilecampaignsource`** | Ursprünglicher Referrer, z. B. ein Newsletter oder ein Social Media-Netzwerk. Erfasst durch App-Akquise. | varchar(255) |
| **`post_`** | **`mobilecampaignterm`** | Bezahlte Suchbegriffe oder andere Begriffe, die Sie mit dieser Akquise verfolgen möchten. Erfasst durch App-Akquise. | varchar(255) |
| **`post_`** | **`mobiledayofweek`** | Nummer des Wochentags, an dem die App gestartet wurde. | varchar(255) |
| **`post_`** | **`mobiledayssincefirstuse`** | Anzahl der Tage, die seit dem ersten Ausführen der App vergangen sind. | varchar(255) |
| **`post_`** | **`mobiledayssincelastuse`** | Anzahl der Tage, die vergangen sind, seitdem die App das letzte Mal ausgeführt wurde. | varchar(255) |
| | **`mobiledeeplinkid`** | Erfasst mit der Kontextdatenvariablen `a.deeplink.id`. Wird in Akquise-Berichten als Identifikator für mobilen Akquise-Link verwendet. | varchar(255) |
| **`post_`** | **`mobiledevice`** | Mobilgerätname. Unter iOS als kommagetrennte 2-Ziffern-Zeichenfolge gespeichert. Die erste Ziffer steht für die Gerätegeneration, die zweite für die Gerätefamilie. | varchar(255) |
| **`post_`** | **`mobilehourofday`** | Gibt die Stunde des Tages an, zu der die App gestartet wurde. Angaben im 24-Stunden-Format. | varchar(255) |
| **`post_`** | **`mobileinstalldate`** | Installationsdatum der Mobile App. Stellt das Datum zur Verfügung, an dem eine Person die Mobile App erstmalig geöffnet hat. | varchar(255) |
| **`post_`** | **`mobilelaunchnumber`** | Wird immer dann erhöht, wenn die Mobile App gestartet wird. | varchar(255) |
| **`post_`** | **`mobilemessagebuttonname`** | Erfasst mit der Kontextdatenvariablen `a.message.button.id`. Wird für In-App-Nachrichten verwendet, um die Schaltfläche zu identifizieren, mit der die Nachricht geschlossen wurde. | varchar(100) |
| **`post_`** | **`mobilemessageid`** | In-App-Nachrichten-ID | varchar(255) |
| **`post_`** | **`mobilemessageonline`** | In-App-Online-Nachricht | varchar(255) |
| **`post_`** | **`mobilemessagepushoptin`** | Erfasst mit der Kontextdatenvariablen `a.push.optin`. Setzen Sie sie auf „true“, wenn sich der Benutzer für Push-Nachrichten anmeldet; andernfalls ist der Wert „false“. | varchar(255) |
| **`post_`** | **`mobilemessagepushpayloadid`** | Erfasst mit der Kontextdatenvariablen `a.push.payloadid`. Wird in Push-Nachrichten als Payload-ID verwendet. | varchar(255) |
| **`post_`** | **`mobileosversion`** | Betriebssystemversion der Mobile Services | varchar(255) |
| | **`mobileplaceaccuracy`** | Erfasst mit der Kontextdatenvariablen `a.loc.acc`. Gibt die Genauigkeit des GPS in Metern zum Erfassungszeitpunkt an. | varchar(255) |
| | **`mobileplacecategory`** | Erfasst mit der Kontextdatenvariablen `a.loc.category`. Beschreibt die Kategorie eines bestimmten Orts. | varchar(255) |
| | **`mobileplaceid`** | Erfasst mit der Kontextdatenvariablen `a.loc.id`. Kennung für einen bestimmten Zielpunkt. | varchar(255) |
| **`post_`** | **`mobilepushoptin`** | Mobile Services-Push-Opt-in | varchar(255) |
| **`post_`** | **`mobilepushpayloadid`** | Mobile Services-Push-Payload-ID | varchar(255) |
| | **`mobilerelaunchcampaigncontent`** | Startinhalte für Mobile Services | varchar(255) |
| | **`mobilerelaunchcampaignmedium`** | Startmedium für Mobile Services | varchar(255) |
| | **`mobilerelaunchcampaignsource`** | Startquelle für Mobile Services | varchar(255) |
| | **`mobilerelaunchcampaignterm`** | Startbedingung für Mobile Services | varchar(255) |
| | **`mobilerelaunchcampaigntrackingcode`** | Erfasst mit der Kontextdatenvariablen `a.launch.campaign.trackingcode`. Wird bei der Akquise als Trackingcode für die Startkampagne verwendet. | varchar(255) |
| **`post_`** | **`mobileresolution`** | Auflösung des Mobilgeräts. `[Width] x [Height]` in Pixel. | varchar(255) |
| | **`mobile_id`** | Die numerische Geräte-ID, wenn die Person ein Mobilgerät verwendet. Der Schlüsselwert für die `mobile_attributes.tsv` [dynamische Suche](dynamic-lookups.md). | int |
| | **`monthly_visitor`** | Markierung, die bestimmt, ob die Besucherin oder der Besucher im aktuellen Monat eindeutig ist. | tinyint unsigned |
| **`post_`** | **`mvvar1`** – **`mvvar3`** | Werte für [Listenvariablen](/help/implement/vars/page-vars/list.md). Enthält eine durch Trennzeichen getrennte Liste benutzerdefinierter Werte in Abhängigkeit von der Implementierung. Die Spalten `post_mvvar1` - `post_mvvar3` ersetzen das ursprüngliche Trennzeichen durch `--**--`. | Text |
| **`post_`** | **`mvvar1_instances`** – **`mvvar3_instances`** | Die Werte der Listenvariablen, die beim aktuellen Treffer festgelegt wurden. Ersetzt das ursprüngliche Trennzeichen durch `--**--`. Die Spalten `post` enthalten normalerweise keine Daten. | Text |
| | **`new_visit`** | Markierung, die bestimmt, ob es sich bei dem aktuellen Treffer um einen neuen Besuch handelt. Wird von Adobe nach 30-minütiger Inaktivität während eines Besuchs festgelegt. | tinyint unsigned |
| | **`os`** | Numerische ID, die das Betriebssystem der oder des Besuchenden darstellt. Basiert auf der Spalte `user_agent`. Der Schlüsselwert für `operating_system.tsv` Standardsuche und `operating_system_type.tsv` [Dynamische Suche](dynamic-lookups.md). | int unsigned |
| **`post_`** | **`pagename`** | Die Dimension [Seite](/help/components/dimensions/page.md). Wenn die Variable [`pagename`](/help/implement/vars/page-vars/pagename.md) leer ist, verwendet Analytics stattdessen `page_url`. | varchar(100) |
| **`post_`** | **`pagename_no_url`** | Ähnlich wie `pagename`, allerdings ohne Fallback auf `page_url`. Nur die Spalte `post` ist verfügbar. | varchar(100) |
| **`post_`** | **`page_event`** | Die Art des Treffers, die in der Bildanforderung gesendet wird (Standardtreffer, Downloadlink, benutzerspezifischer Link, Exitlink). Siehe [Seitenereignissuche](datafeeds-page-event.md). | tinyint unsigned |
| **`post_`** | **`page_event_var1`** | Wird nur bei Bildanforderungen für Linktracking verwendet. Die URL des angeklickten Downloadlinks, Exitlinks oder benutzerspezifischen Links. | Text |
| **`post_`** | **`page_event_var2`** | Wird nur bei Bildanforderungen für Linktracking verwendet. Benutzerdefinierter Name des Links (falls angegeben). Die Dimension [Benutzerspezifischer Link](/help/components/dimensions/custom-link.md), [Download-Link](/help/components/dimensions/download-link.md) oder [Exit-Link](/help/components/dimensions/exit-link.md), je nach Wert in `page_event`. | varchar(100) |
| **`post_`** | **`page_type`** | Die Dimension [Seiten nicht gefunden](/help/components/dimensions/pages-not-found.md), die normalerweise für 404-Seiten verwendet wird. | char(20) |
| **`post_`** | **`page_url`** | **`page_url`**: Die URL des Treffers. Verwendet einen Datentyp von text.<br>**`post_page_url`**: für Bildanforderungen zum Linktracking ([`tl()`](/help/implement/vars/functions/tl-method.md)) entfernt. Verwendet einen Datentyp von varchar(255). | text<br>varchar(255) |
| | **`paid_search`** | Markierung, die bestimmt, ob der Treffer mit Paid-Search-Erkennung übereinstimmt. | tinyint unsigned |
| **`post_`** | **`persistent_cookie`** | Wird in der Dimension [Unterstützung persistenter Cookies](/help/components/dimensions/persistent-cookie-support.md) verwendet. Gibt an, ob der Benutzer Cookies unterstützt, die nicht nach jedem Treffer gelöscht werden. | char(1) |
| **`post_`** | **`pointofinterest`** | Name des Mobile Services-Zielpunkts | varchar(255) |
| **`post_`** | **`pointofinterestdistance`** | Entfernung der Mobile Services zur Zielpunktmitte | varchar(255) |
| **`post_`** | **`product_list`** | Seitenvariable [`products`](/help/implement/vars/page-vars/products.md). Hilft beim Ausfüllen mehrerer Dimensionen und Metriken, einschließlich [Kategorie](/help/components/dimensions/category.md), [Produkt](/help/components/dimensions/product.md), [Einheiten](/help/components/metrics/units.md) und [Umsatz](/help/components/metrics/revenue.md). | Text |
| **`post_`** | **`prop1`** – **`prop75`** | Benutzerdefinierte Traffic-Variablen 1 bis 75. Wird in den Dimensionen [Prop](/help/components/dimensions/prop.md) verwendet. | varchar(100) |
| **`post_`** | **`purchaseid`** | Eindeutige Kennung für einen Kauf, so wie durch das Festlegen der Variable [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) bestimmt. Von der Spalte `duplicate_purchase` verwendet. | char(20) |
| | **`quarterly_visitor`** | Markierung, die bestimmt, ob es sich bei dem Treffer um eine neue Quartals-Besucherin oder einen neuen Quartals-Besucher handelt. | tinyint unsigned |
| **`post_`** | **`referrer`** | Die Dimension [Referrer](/help/components/dimensions/referrer.md). Beachten Sie, dass während `referrer` einen Datentyp von varchar(255) verwendet, `post_referrer` einen Datentyp von varchar(244) verwendet. | varchar(255)<br>varchar(244) |
| | **`ref_domain`** | Die Dimension [Referrer-Domain](/help/components/dimensions/referring-domain.md). Basierend auf der Spalte `referrer`. | varchar(100) |
| | **`ref_type`** | Numerische ID, die den Referenztyp für den Treffer darstellt. Wird in der Dimension [Referrer-Typ](/help/components/dimensions/referrer-type.md) verwendet.<br>1: Innerhalb Ihrer Site<br>2: Andere Websites<br>3: Suchmaschinen<br>4: Festplatte<br>5: USENET<br>6: Eingegeben/Mit Lesezeichen versehen (kein Referrer)<br>7: E-Mail<br>8: Kein JavaScript<br>9: Soziale Netzwerke<br>10: Konversationelle KI-Tools | tinyint unsigned |
| | **`resolution`** | Numerische ID, die die Auflösung des Bildschirms darstellt. In der Dimension [Bildschirmauflösung](/help/components/dimensions/monitor-resolution.md) verwendet. Verwendet die Suchtabelle `resolution.tsv`. | smallint unsigned |
| **`post_`** | **`search_engine`** | Numerische ID, die die Suchmaschine darstellt, über die die Besucherin oder der Besucher auf Ihre Site gelangt ist. Wird in der Dimension [Suchmaschinen](/help/components/dimensions/search-engine.md) verwendet. Verweist auf die Suchtabelle `search_engines.tsv`. | smallint unsigned |
| | **`search_page_num`** | Verwendet von der Dimension [Alle Suchseiten-Ranglisten](/help/components/dimensions/all-search-page-rank.md). Gibt an, auf welcher Seite der Suchergebnisse Ihre Site angezeigt wurde, ehe die Person sich zu Ihrer Site durchgeklickt hat. | smallint unsigned |
| | **`secondary_hit`** | Markierung, die bestimmt, ob der Treffer ein sekundärer Treffer ist. Diese Markierung stammt normalerweise aus dem Multi-Suite-Tagging und aus VISTA-Regeln, die Treffer kopieren. | tinyint unsigned |
| | **`sourceid`** | Quell-ID | int unsigned |
| | **`stats_server`** | Nicht verwendet. Interner Adobe-Server, der den Treffer verarbeitet hat. | char(30) |
| **`post_`** | **`s_kwcid`** | Die Keyword-ID, die in Adobe Advertising-Integrationen verwendet wird. | varchar(255) |
| | **`s_resolution`** | Rohwert der Bildschirmauflösung. Erfasst mit der JavaScript-Funktion `screen.width x screen.height`. | char(20) |
| **`post_`** | **`tnt`** | Wird in Adobe Target-Integrationen verwendet. Stellt alle Tests dar, für die er derzeit qualifiziert ist. Das Format ist: `TargetCampaignID:TargetRecipeID:TargetType\|Event/Action`. | Text |
| **`post_`** | **`tnt_action`** | Wird in Adobe Target-Integrationen verwendet. Stellt alle Tests dar, für die der Treffer qualifiziert ist. | Text |
| | **`tnt_instances`** | Wird in Adobe Target-Integrationen verwendet. Target-Instanzvariable. | Text |
| **`post_`** | **`transactionid`** | Eine eindeutige Kennung, bei der verschiedene Datenpunkte später über Datenquellen hochgeladen werden können. Erfasst mithilfe der Variablen [`transactionID`](/help/implement/vars/page-vars/transactionid.md). | Text |
| | **`truncated_hit`** | Eine Markierung, die angibt, dass die Bildanforderung abgeschnitten wurde (ein Teiltreffer wurde empfangen). <br>Y: Treffer abgeschnitten; Teiltreffer erhalten <br>N: Treffer nicht abgeschnitten; vollständigen Treffer erhalten | char(1) |
| **`post_`** | **`t_time_info`** | Lokale Zeit des Besuchers. Das Format ist: `M/D/YYYY HH:MM:SS Month (0-11, 0=January) Timezone offset (in minutes)` | varchar(100) |
| | **`userid`** | Nicht verwendet. Die numerische ID für die Report Suite-ID. Verwenden Sie stattdessen `username`. | int unsigned |
| | **`username`** | Die Report Suite-ID für den Treffer. | char(40) |
| | **`user_agent`** | Benutzeragenten-Zeichenfolge, die im HTTP-Header der Bildanforderung gesendet wird. | Text |
| | **`user_hash`** | Nicht verwendet. Hash der Report Suite-ID. Verwenden Sie stattdessen `username`. | int unsigned |
| **`post_`** | **`user_server`** | Verwendet in der Dimension [Server](/help/components/dimensions/server.md). | varchar(100) |
| | **`va_closer_detail`** | Die Dimension [Details des Letztkontakts](/help/components/dimensions/last-touch-detail.md). | varchar(255) |
| | **`va_closer_id`** | Numerische ID, die die Dimension [Letztkontaktkanal](/help/components/dimensions/last-touch-channel.md) identifiziert. Informationen zu dieser ID befinden sich im Marketing-Kanal-Manager. | tinyint unsigned |
| | **`va_finder_detail`** | Die Dimension [Details des Erstkontakts](/help/components/dimensions/first-touch-detail.md). | varchar(255) |
| | **`va_finder_id`** | Numerische ID, die die Dimension [Erstkontaktkanal](/help/components/dimensions/first-touch-channel.md) identifiziert. Informationen zu dieser ID befinden sich im Marketing-Kanal-Manager. | tinyint unsigned |
| | **`va_instance_event`** | Markierung, die den Marketing-Kanal [Instanzen](/help/components/metrics/instances.md) identifiziert. | tinyint unsigned |
| | **`va_new_engagement`** | Markierung, die den Marketing-Kanal [Neue Interaktionen](/help/components/metrics/new-engagements.md) identifiziert. | tinyint unsigned |
| **`post_`** | **`video`** | Die Dimension [Inhalte](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/content) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoad`** | Die Dimension [Anzeige](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/ad) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoadinpod`** | Die Dimension [Anzeigenposition innerhalb der Werbeunterbrechung](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/ad-in-pod-position) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoadlength`** | Die Dimension [Anzeigenlänge (variabel)](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/ad-length) für Streaming-Mediendienste. | Ganzzahl |
| **`post_`** | **`videoadname`** | Die Dimension [Anzeigenname (variabel)](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/ad-name) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoadplayername`** | Die Dimension [Name des Anzeigenplayers](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/ad-player-name) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoadpod`** | Die Dimension [Anzeigen-Pod](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/ad-pod) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoadvertiser`** | Die Dimension [Advertiser](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/advertiser) für Streaming-Mediendienste. | varchar(255) |
| | **`videoaudioalbum`** | Die Dimension [Album](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/album) für Streaming-Mediendienste. | varchar(255) |
| | **`videoaudioartist`** | Die Dimension [Künstler](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/artist) für Streaming-Mediendienste. | varchar(255) |
| | **`videoaudioauthor`** | Die Dimension [Autor](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/author) für Streaming-Mediendienste. | varchar(255) |
| | **`videoaudiolabel`** | Die Dimension [Label](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/label) für Streaming-Mediendienste. | varchar(255) |
| | **`videoaudiopublisher`** | Die Dimension [Publisher](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/publisher) für Streaming-Mediendienste. | varchar(255) |
| | **`videoaudiostation`** | Die Dimension [Station](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/station) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videocampaign`** | Die Dimension [Kampagnen-ID](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/campaign-id) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videochannel`** | Die Dimension [Inhaltskanal](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/content-channel) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videochapter`** | Die Dimension [Kapitel](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/chapter) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videocontenttype`** | Die Dimension [Content-Typ](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/content-type) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videodaypart`** | Die Dimension [Tagesteil](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/day-part) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoepisode`** | Die Dimension [Folge](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/episode) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videofeedtype`** | Die Dimension [Medien-Feedtyp](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/media-feed-type) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videogenre`** | Die Dimension [Genre](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/genre) für Streaming-Mediendienste. Diese Dimension erlaubt mehrere Werte im selben Treffer, getrennt durch ein Komma. | Text |
| **`post_`** | **`videolength`** | Die Dimension [Länge des Inhalts (variabel)](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/content-length) für Streaming-Mediendienste. | Ganzzahl |
| **`post_`** | **`videomvpd`** | Die Dimension [MVPD](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/mvpd) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoname`** | Die Dimension [Name des Inhalts (variabel)](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/content-name) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videonetwork`** | Die Dimension [Sender](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/network) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videopath`** | Die Dimension [Medienpfad](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/media-path) für Streaming-Mediendienste. | varchar(100) |
| **`post_`** | **`videoplayername`** | Die Dimension [Inhalts-Player-Name](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/content-player-name) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoqoebitrateaverageevar`** | Die Dimension [Durchschnittliche Bitrate](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/average-bitrate) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoqoebitratechangecountevar`** | Die Dimension [Bitratenänderungen](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/bitrate-changes) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoqoebuffercountevar`** | Die Dimension [Pufferereignisse](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/buffer-events) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoqoebuffertimeevar`** | Die Dimension [Gesamtpufferdauer](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/total-buffer-duration) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoqoedroppedframecountevar`** | Die Dimension [Dropped Frames](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/dropped-frames) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoqoeerrorcountevar`** | Die Dimension [Fehler](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/errors) für Streaming-Mediendienste. | varchar(255) |
| | **`videoqoeextneralerrors`** | Die Dimension [Externe Fehler-IDs](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/external-error-ids) für Streaming-Mediendienste. Diese Dimension erlaubt mehrere Werte im selben Treffer. | Text |
| **`post_`** | **`videoqoeplayersdkerrors`** | Die Dimension [Fehler-IDs von Player-SDK](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/player-sdk-error-ids) für Streaming-Mediendienste. Diese Dimension erlaubt mehrere Werte im selben Treffer. | Text |
| **`post_`** | **`videoqoetimetostartevar`** | Die Dimension [Zeit bis Start](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/time-to-start) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoseason`** | Die Dimension [Staffel](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/season) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videosegment`** | Die Dimension [Inhaltssegment](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/content-segment) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videosessionid`** | Die Dimension [Mediensitzungs-ID](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/media-session-id) Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoshow`** | Die Dimension [Serie](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/show) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`videoshowtype`** | Die Dimension [Serientyp](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/show-type) für Streaming-Mediendienste. | varchar(255) |
| | **`videostreamtype`** | Die Dimension [Stream-Typ](https://experienceleague.adobe.com/en/docs/media-analytics/using/reporting/dimensions/stream-type) für Streaming-Mediendienste. | varchar(255) |
| **`post_`** | **`visid_high`** | Wird mit `visid_low` zur eindeutigen Identifizierung von Besuchenden verwendet. | bigint unsigned |
| **`post_`** | **`visid_low`** | Wird mit `visid_high` zur eindeutigen Identifizierung von Besuchenden verwendet. | bigint unsigned |
| | **`visid_new`** | Markierung, die bestimmt, ob der Treffer eine neu generierte Besucher-ID enthält. | char(1) |
| | **`visid_timestamp`** | Wurde eine Besucher-ID neu generiert, wird der Zeitstempel (in UNIX®-Zeit) der Generierung der Besucher-ID bereitgestellt. | int |
| **`post_`** | **`visid_type`** | Nicht zur externen Verwendung; intern von Adobe für Verarbeitungsoptimierungen verwendet. Eine numerische ID, die die Methode zur Identifizierung des Besuchers darstellt.<br>`0`: Benutzerspezifische Besucher-ID oder unbekannt/nicht anwendbar<br>`1`: IP- und Benutzeragenten-Fallback-<br>`2`: HTTP-Kopfzeile mobiler Teilnehmer <br>`3`: Legacy-Cookie-Wert (`s_vi`) <br>`4`: Fallback-Cookie-Wert (`s_fid`) <br>`5`: Identity Service | tinyint unsigned |
| **`post_`** | **`visit_keywords`** | Die Dimension [Suchbegriff](/help/components/dimensions/search-keyword.md). Diese Spalte verwendet eine nicht standardmäßige Zeichenbeschränkung von varchar(244), um der von Adobe verwendeten Backend-Logik Rechnung zu tragen. Die nachbearbeitete Spalte ist `**post_keywords**`, nicht `**post_visit_keywords**`. | varchar(244) |
| | **`visit_num`** | Die Dimension [Besuchsnummer](/help/components/dimensions/visit-number.md). Beginnt bei 1 und erhöht sich bei jedem neuen Besuch eines Besuchers. | int unsigned |
| | **`visit_page_num`** | Die Dimension [Treffertiefe](/help/components/dimensions/hit-depth.md). Erhöht sich um 1 für jeden von Besuchenden generierten Treffer. Setzt jeden Besuch zurück. | int unsigned |
| | **`visit_referrer`** | Die erste verweisende Stelle des Besuchs. | varchar(255) |
| | **`visit_ref_domain`** | Basierend auf der Spalte `visit_referrer`. Die allererste verweisende Domain des Besuchs. | varchar(100) |
| | **`visit_ref_type`** | Numerische ID, die den Referrer-Typ des ursprünglichen Referrers des Besuchs darstellt. Verweist auf die Suchtabelle `referrer_type.tsv` | tinyint unsigned |
| | **`visit_search_engine`** | Numerische ID, die die erste Suchmaschine des Besuchs darstellt. Verweist auf die Suchtabelle `search_engines.tsv`. | smallint unsigned |
| | **`visit_start_pagename`** | [Seite](/help/components/dimensions/page.md) des ersten Treffers des Besuchs. | varchar(100) |
| | **`visit_start_page_url`** | URL des ersten Treffers des Besuchs. | varchar(255) |
| | **`visit_start_time_gmt`** | Zeitstempel (in UNIX®-Zeit) des ersten Treffers des Besuchs. | int |
| | **`weekly_visitor`** | Markierung, die bestimmt, ob es sich bei dem Treffer um eine neue wöchentliche Besucherin oder einen neuen wöchentlichen Besucher handelt. | tinyint unsigned |
| | **`yearly_visitor`** | Markierung, die bestimmt, ob es sich bei dem Treffer um eine neue jährliche Besucherin oder einen neuen jährlichen Besucher handelt. | tinyint unsigned |
| **`post_`** | **`zip`** | Hilft beim Ausfüllen der Dimension [Postleitzahl](/help/components/dimensions/zip-code.md). Siehe auch `geo_zip`. | varchar(50) |

## Nicht verwendete oder eingestellte Spalten

Die folgenden Spalten werden nicht verwendet, wurden eingestellt oder sind für das Reporting nicht relevant. Einige dieser Spalten sind an Funktionen gebunden, die nicht mehr verfügbar sind, während andere aufgrund neuer und robusterer Funktionen nicht mehr benötigt werden. Die meisten dieser Spalten enthalten keine Daten. Spalten, die möglicherweise noch Daten enthalten, werden von aktuellen Datenerfassungsbibliotheken nicht unterstützt und stehen in Analysis Workspace nicht als Dimensionen zur Verfügung.

| POST | Spaltenname |
| ---: | :--- |
| `post_` | `adclassificationcreative` |
| | `click_action` |
| | `click_action_type` |
| | `click_context` |
| | `click_context_type` |
| | `click_sourceid` |
| | `click_tag` |
| | `dataprivacydmaconsent` |
| `post_` | `hier1` – `hier5` |
| | `homepage` |
| | `ip2` |
| | `mobileacquisitionclicks` |
| | `mobileactioninapptime` |
| | `mobileactiontotaltime` |
| | `mobileappperformanceaffectedusers` |
| | `mobileappperformanceappid.app-perf-app-name` |
| | `mobileappperformanceappid.app-perf-platform` |
| | `mobileappperformancecrashes` |
| | `mobileappperformancecrashid.app-perf-crash-name` |
| | `mobileappperformanceloads` |
| | `mobileappstoreavgrating` |
| | `mobileappstoredownloads` |
| | `mobileappstoreinapprevenue` |
| | `mobileappstoreinapproyalties` |
| | `mobileappstoreobjectid.app-store-user` |
| | `mobileappstoreobjectid.application-name` |
| | `mobileappstoreobjectid.application-version` |
| | `mobileappstoreobjectid.appstore-name` |
| | `mobileappstoreobjectid.category-name` |
| | `mobileappstoreobjectid.country-name` |
| | `mobileappstoreobjectid.device-manufacturer` |
| | `mobileappstoreobjectid.device-name` |
| | `mobileappstoreobjectid.in-app-name` |
| | `mobileappstoreobjectid.platform-name-version` |
| | `mobileappstoreobjectid.rank-category-type` |
| | `mobileappstoreobjectid.region-name` |
| | `mobileappstoreobjectid.review-comment` |
| | `mobileappstoreobjectid.review-title` |
| | `mobileappstoreoneoffrevenue` |
| | `mobileappstoreoneoffroyalties` |
| | `mobileappstorepurchases` |
| | `mobileappstorerank` |
| | `mobileappstorerankdivisor` |
| | `mobileappstorerating` |
| | `mobileappstoreratingdivisor` |
| | `mobileavgprevsessionlength` |
| | `mobilecrashes` |
| | `mobilecrashrate` |
| | `mobiledailyengagedusers` |
| | `mobiledayssincelastupgrade` |
| | `mobiledeeplinkid.name` |
| | `mobileinstalls` |
| | `mobilelaunches` |
| | `mobilelaunchessincelastupgrade` |
| `post_` | `mobileltv` |
| | `mobileltvtotal` |
| `post_` | `mobilemessageclicks` |
| `post_` | `mobilemessageid.dest` |
| `post_` | `mobilemessageid.name` |
| `post_` | `mobilemessageid.type` |
| `post_` | `mobilemessageimpressions` |
| `post_` | `mobilemessagepushpayloadid.name` |
| `post_` | `mobilemessageviews` |
| | `mobilemonthlyengagedusers` |
| | `mobileosenvironment` |
| | `mobileplacedwelltime` |
| | `mobileplaceentry` |
| | `mobileplaceexit` |
| | `mobileprevsessionlength` |
| | `mobilerelaunchcampaigntrackingcode.name` |
| | `mobileupgrades` |
| | `namespace` |
| | `p_plugins` |
| `post_` | `page_event_var3` |
| `post_` | `partner_plugins` |
| | `plugins` |
| | `prev_page` |
| | `product_merchandising` |
| | `sampled_hit` |
| | `service` |
| `post_` | `socialaccountandappids` |
| `post_` | `socialassettrackingcode` |
| `post_` | `socialauthor` |
| `post_` | `socialaveragesentiment` |
| `post_` | `socialaveragesentiment (deprecated)` |
| `post_` | `socialcontentprovider` |
| `post_` | `socialfbstories` |
| `post_` | `socialfbstorytellers` |
| `post_` | `socialinteractioncount` |
| `post_` | `socialinteractiontype` |
| `post_` | `sociallanguage` |
| `post_` | `sociallatlong` |
| `post_` | `sociallikeadds` |
| `post_` | `sociallink` |
| `post_` | `sociallink (deprecated)` |
| `post_` | `socialmentions` |
| `post_` | `socialowneddefinitioninsighttype` |
| `post_` | `socialowneddefinitioninsightvalue` |
| `post_` | `socialowneddefinitionmetric` |
| `post_` | `socialowneddefinitionpropertyvspost` |
| `post_` | `socialownedpostids` |
| `post_` | `socialownedpropertyid` |
| `post_` | `socialownedpropertyname` |
| `post_` | `socialownedpropertypropertyvsapp` |
| `post_` | `socialpageviews` |
| `post_` | `socialpostviews` |
| `post_` | `socialproperty` |
| `post_` | `socialproperty (deprecated)` |
| `post_` | `socialpubcomments` |
| `post_` | `socialpubposts` |
| `post_` | `socialpubrecommends` |
| `post_` | `socialpubsubscribers` |
| `post_` | `socialterm` |
| `post_` | `socialtermslist` |
| `post_` | `socialtermslist (deprecated)` |
| `post_` | `socialtotalsentiment` |
| `post_` | `state` |
| `post_` | `survey` |
| | `survey_instances` |
| | `tnt_post_vista` |
| | `ua_color` |
| | `ua_os` |
| | `ua_pixels` |
| | `videoadload` |
| `post_` | `videoauthorized` |
| | `videoaverageminuteaudience` |
| | `videochaptercomplete` |
| | `videochapterstart` |
| | `videochaptertime` |
| | `videopause` |
| | `videopausecount` |
| | `videopausetime` |
| | `videoplay` |
| | `videoprogress10` |
| | `videoprogress25` |
| | `videoprogress50` |
| | `videoprogress75` |
| | `videoprogress96` |
| | `videoqoebitrateaverage` |
| | `videoqoebitratechange` |
| | `videoqoebuffer` |
| | `videoqoedropbeforestart` |
| | `videoqoedroppedframes` |
| | `videoqoeerror` |
| | `videoresume` |
| | `videotime` |
| | `videototaltime` |
| | `videouniquetimeplayed` |

>[!MORELIKETHIS]
>
>[XDM-Objektvariablenzuordnung](/help/implement/aep-edge/xdm-var-mapping.md)
>[Zuordnen von Datenobjektvariablen](/help/implement/aep-edge/data-var-mapping.md)
