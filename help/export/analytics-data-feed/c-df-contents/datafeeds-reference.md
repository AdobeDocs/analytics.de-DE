---
description: Tabellendaten, die die Spalten im Daten-Feed beschreiben.
keywords: Daten-Feed;Spalten
subtopic: data feeds
title: Datenspaltenreferenz
feature: Data Feeds
exl-id: e1492147-6e7f-4921-b509-898e7efda596
source-git-commit: 808ab76ee3f7c7451f8b3569c282abebbc9ac32f
workflow-type: tm+mt
source-wordcount: '3617'
ht-degree: 67%

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

| Spaltenname | Spaltenbeschreibung | Datentyp |
| --- | --- | --- |
| **`accept_language`** | Führt alle unterstützten Sprachen, wie im HTTP-Header Accept-Language angegeben, in einer Bildanforderung auf. | char(20) |
| **`adload`** | Medien-Anzeigenladevorgänge | varchar(255) |
| **`aemassetid`** | Eine Variable mit mehreren Werten, die Asset-IDs (GUIDs) eines Satzes von Adobe Experience Manager Assets entspricht. Erhöht Impressionsereignisse. | text |
| **`aemassetsource`** | Identifiziert die Quelle des Asset-Ereignisses. Wird in Adobe Experience Manager verwendet. | varchar(255) |
| **`aemclickedassetid`** | Asset-ID eines Adobe Experience Manager-Assets. Erhöht Klickereignisse. | varchar(255) |
| **`browser`** | Eine numerische ID, die den Browser darstellt. Verweist auf die `browser.tsv` Suchtabelle. | int unsigniert |
| **`browser_height`** | Die Dimension [Browser-Höhe](/help/components/dimensions/browser-height.md) . | smallint unsigned |
| **`browser_width`** | Die [Browser-Breite](/help/components/dimensions/browser-width.md) | smallint unsigned |
| **`c_color`** | Bit-Tiefe der Farbpalette. Wird bei der Berechnung der Dimension [Farbtiefe](/help/components/dimensions/color-depth.md) verwendet. AppMeasurement verwendet die JavaScript-Funktion `screen.colorDepth()`. | char(20) |
| **`campaign`** | Die [Tracking-Symbol](/help/components/dimensions/tracking-code.md) Dimension. | varchar(255) |
| **`carrier`** | Variable der Adobe Advertising-Integration. Gibt den Mobilnetzbetreiber an. Der Schlüsselwert für die [dynamische Suche](dynamic-lookups.md) von `carrier.tsv`. | varchar(100) |
| **`ch_hdr`** | Client-Hinweise, die über die Kopfzeile der HTTP-Anfrage erfasst werden. | Text |
| **`ch_js`** | Client-Hinweise, die über die JavaScript-API für Client-Hinweise von Benutzeragenten erfasst werden. | Text |
| **`channel`** | Die [ „Site-](/help/components/dimensions/site-section.md)&quot;. | varchar(100) |
| **`clickmaplink`** | Activity Map-Link | varchar(255) |
| **`clickmaplinkbyregion`** | Activity Map-Link nach Region | varchar(255) |
| **`clickmappage`** | Activity Map-Seite | varchar(255) |
| **`clickmapregion`** | Activity Map-Region | varchar(255) |
| **`code_ver`** | API- oder Client SDK-Version, die für das Kompilieren und Senden der Bildanforderung verwendet wird. | char(16) |
| **`color`** | Farbtiefen-ID, basierend auf dem Wert der Spalte `c_color`. Verweist auf die Suchtabelle `color_depth.tsv`. | smallint unsigniert |
| **`connection_type`** | Eine numerische ID, die den Verbindungstyp darstellt. Die Dimension [Verbindungstyp](/help/components/dimensions/connection-type.md) . Verweist auf die Suchtabelle `connection_type.tsv` | tinyint unsigniert |
| **`cookies`** | Die Dimension [Cookie-Unterstützung](/help/components/dimensions/cookie-support.md) .<br>Y: aktiviert<br>N: deaktiviert<br>U: unbekannt | char(1) |
| **`country`** | Eine numerische ID, die das Land des Besuchers darstellt. Verweist auf die Suchtabelle `country.tsv`. | smallint unsigniert |
| **`ct_connect_type`** | Verknüpft mit der Spalte `connection_type`. Die gebräuchlichsten Werte sind LAN/WiFi, Mobilnetzbetreiber und Modem. | char(20) |
| **`curr_factor`** | Bestimmt die Dezimalstelle für die Währung und wird zur Währungsumrechnung verwendet. Beispiel: In USD werden zwei Dezimalstellen verwendet, sodass dieser Spaltenwert `2` würde. | tinyint |
| **`curr_rate`** | Der Wechselkurs zum Zeitpunkt der Transaktion. Adobe arbeitet mit XE zusammen, um den aktuellen Wechselkurs zu bestimmen. | Dezimalzahl(24,12) |
| **`currency`** | Der Währungscode, der während der Transaktion verwendet wurde. Festlegen mithilfe von [`currencyCode`](/help/implement/vars/config-vars/currencycode.md). | char(8) |
| **`cust_hit_time_gmt`** | Nur für Report Suites mit aktiviertem Zeitstempel. Der mit dem Treffer gesendete Zeitstempel in UNIX®-Zeit. | int |
| **`cust_visid`** | Die benutzerdefinierte Besucher-ID, wenn sie mithilfe von [`visitorID`](/help/implement/vars/config-vars/visitorid.md) festgelegt wird. | varchar(255) |
| **`daily_visitor`** | Eine Markierung, die bestimmt, ob der Treffer ein neuer täglicher Besucher ist. | tinyint unsigniert |
| **`dataprivacyconsentoptin`** | Die Dimension [Einverständnisverwaltungs-Opt-in](/help/components/dimensions/cm-opt-in.md) . Pro Treffer können mehrere Werte vorhanden sein, getrennt durch einen senkrechten Strich (`\|`). Gültige Werte sind `DMP` und `SELL`. | varchar(100) |
| **`dataprivacyconsentoptout`** | Die Dimension [Einverständnisverwaltungs-Opt-out](/help/components/dimensions/cm-opt-out.md) . Pro Treffer können mehrere Werte vorhanden sein, getrennt durch einen senkrechten Strich (`\|`). Gültige Werte sind `SSF`, `DMP` und `SELL`. | varchar(100) |
| **`dataprivacydmaconsent`** | Ein -Wert, der angibt, ob das Einverständnis für das Senden von Daten von Adobe Analytics über Adobe Advertising an Drittanbieter-Werbeanbieter (wie Google) eingeholt wurde. Weitere Informationen finden Sie unter [Einwilligung in Werbung](/help/components/dimensions/ad-consent.md). | varchar(100) |
| **`date_time`** | Die Uhrzeit des Treffers in lesbarem Format, basierend auf der Zeitzone der Report Suite. | datetime |
| **`domain`** | Die [Domäne](/help/components/dimensions/domain.md) Dimension. Basiert auf dem Internet-Zugangspunkt des Besucher. | varchar(100) |
| **`duplicate_events`** | Listet alle Ereignisse auf, die als Duplikat gezählt wurden. | varchar(255) |
| **`duplicate_purchase`** | Eine Markierung, die bestimmt, ob das Kaufereignis für diesen Treffer ignoriert wird, da es ein Duplikat ist. | tinyint unsigniert |
| **`duplicated_from`** | Wird nur in Report Suites mit VISTA-Regeln zur Trefferkopie verwendet. Gibt an, von welcher Report Suite der Treffer kopiert wurde. | varchar(40) |
| **`ef_id`** | Die in Adobe Advertising-Integrationen verwendete `ef_id`. | varchar(255) |
| **`evar1 - evar250`** | Benutzerdefinierte Variablen 1–250. Wird in [eVar](/help/components/dimensions/evar.md)-Dimensionen verwendet. Jede Organisation verwendet eVars anders. Weitere Informationen darüber, wie Ihr Unternehmen die entsprechenden eVars füllt, finden Sie in einem [ für Ihr Unternehmen spezifischen ](/help/implement/prepare/solution-design.md) (Lösungsentwurfsdokument). | varchar(255) |
| **`event_list`** | Kommagetrennte Liste von numerisch-IDs, die Ereignisse darstellen, die auf der Treffer ausgelöst werden. Enthält sowohl die Standardereignisse als [auch die benutzerdefinierten Ereignisse 1–1000.](/help/components/metrics/custom-events.md) Verwendet die `event.tsv`-Suche. | text |
| **`exclude_hit`** | Eine Hervorhebung, die bestimmt, ob die Treffer von Berichte ausgeschlossen wird. Die Spalte `visit_num` wird bei ausgenommenen Hits nicht erhöht.<br>1: Nicht verwendet. Teil einer veralteten Funktion.<br>2: Nicht verwendet. Teil einer veralteten Funktion.<br>3: Wird nicht mehr verwendet. Ausschluss des Benutzeragenten<br>4: Ausschluss basierend auf IP-Adresse<br>5: Wichtige Hit-Informationen fehlen, z. B. `page_url`, `pagename`, `page_event` oder `event_list`<br>6: JavaScript hat Hit nicht korrekt verarbeitet<br>7: Kontospezifischer Ausschluss, z. B. in VISTA-Regeln<br>8: Nicht verwendet. Alternativer kontospezifischer Ausschluss.<br>9: Nicht verwendet. Teil einer veralteten Funktion.<br>10: Ungültiger Währungscode<br>11: Treffer, bei dem ein Zeitstempel für eine Report Suite mit Zeitstempel fehlt, oder ein Treffer, der einen Zeitstempel in einer Report Suite ohne Zeitstempel aufweist<br>12: Nicht verwendet. Teil einer veralteten Funktion.<br>13: Nicht verwendet. Teil einer veralteten Funktion.<br>14: Target-Treffer, der nicht mit einem Analytics-Treffer übereinstimmte<br>15: Derzeit nicht verwendet.<br>16: Advertising Cloud-Treffer, der nicht mit einem Analytics-Treffer übereinstimmte | tinyint unsigniert |
| **`first_hit_page_url`** | Die allererste URL des Besuchers. | varchar(255) |
| **`first_hit_pagename`** | Die Dimension [Ursprüngliche Einstiegsseite](/help/components/dimensions/entry-dimensions.md) . Der Name der ursprünglichen Entrypage des Besuchers. | varchar(100) |
| **`first_hit_ref_domain`** | Die Dimension [Ursprüngliche Referrer](/help/components/dimensions/original-referring-domain.md)Domain“. Basierend auf `first_hit_referrer`. Die allererste verweisende Domain des Besuchers. | varchar(100) |
| **`first_hit_ref_type`** | Eine numerische ID, die den Referrer-Typ des allerersten Referrers des Besuchers darstellt. Verweist auf die Suchtabelle `referrer_type.tsv` | tinyint unsigniert |
| **`first_hit_referrer`** | Die allererste verweisende URL des Besuchers. | varchar(255) |
| **`first_hit_time_gmt`** | Zeitstempel des allerersten Treffers der Besucherin oder des Besuchers in UNIX®-Zeit. | int |
| **`geo_city`** | Der Name der Stadt, aus der der Treffer stammt, basierend auf der IP. Wird in der Dimension [Städte](/help/components/dimensions/cities.md) verwendet. | char(32) |
| **`geo_country`** | Die Abkürzung für das Land, aus dem der Treffer stammt, basierend auf der IP. Wird in der Dimension [Länder](/help/components/dimensions/countries.md) verwendet. | char(4) |
| **`geo_dma`** | Eine numerische ID des demografischen Bereichs, aus dem der Treffer stammt, basierend auf der IP. Wird in der Dimension [US DMA](/help/components/dimensions/us-dma.md) verwendet. | int unsigniert |
| **`geo_region`** | Der Name des Bundeslandes oder der Region, aus dem/der der Treffer stammt, basierend auf der IP. Wird in der Dimension [Regionen](/help/components/dimensions/regions.md) verwendet. | char(32) |
| **`geo_zip`** | Die Postleitzahl, von der der Treffer stammt, basierend auf der IP. Hilft beim Ausfüllen der Dimension [Postleitzahl](/help/components/dimensions/zip-code.md). Siehe auch `zip`. | varchar(16) |
| **`hit_source`** | Die Quelle, von der der Treffer stammt. Trefferquellen 1, 2 und 6 werden in Rechnung gestellt. <br>1: Standardbildanfrage ohne Zeitstempel <br>2: Standardbildanfrage mit Zeitstempel <br>3: Hochladen der Live-Datenquelle mit Zeitstempel <br>4: Nicht verwendet <br>5: Generischer Datenquellen-Upload <br>6: Datenquellen-Upload mit vollständiger Verarbeitung <br>7: TransactionID-Datenquellen-Upload<br>8: Nicht mehr verwendet; frühere Versionen der Adobe Advertising Cloud-Datenquellen <br>9: Nicht mehr verwendet; zusammengefasste Metriken von Adobe Social <br>10: Server-seitige Weiterleitung in Audience Manager verwendet | tinyint unsigniert |
| **`hit_time_gmt`** | Der Zeitstempel des Zeitpunkts, wo der Adobe-Datenerfassungs-Server den Treffer erhielt, basierend auf der UNIX®-Zeit. | int |
| **`hitid_high`** | Wird mit `hitid_low` zur Identifizierung eines Treffers verwendet. | bigint unsigned |
| **`hitid_low`** | Wird mit `hitid_high` zur Identifizierung eines Treffers verwendet. | bigint unsigned |
| **`hourly_visitor`** | Eine Markierung, die bestimmt, ob der Treffer ein neuer stündlicher Besucher ist. | tinyint unsigniert |
| **`ip`** | IPv4-Adresse basierend auf der HTTP-Kopfzeile der Bildanforderung. Sich gegenseitig ausschließend für `ipv6`; wenn diese Spalte eine nicht verschleierte IP-Adresse enthält, ist `ipv6` leer. | char(20) |
| **`ipv6`** | Die komprimierte IPv6-Adresse, falls verfügbar. Sich gegenseitig ausschließend für `ip`; wenn diese Spalte eine nicht verschleierte IP-Adresse enthält, ist `ip` leer. | varchar(40) |
| **`j_jscript`** | Vom Browser unterstützte JavaScript-Version. | char(5) |
| **`java_enabled`** | Die [[!UICONTROL Java aktiviert]](/help/components/dimensions/java-enabled.md). <br>Y: Aktiviert <br>N: Deaktiviert <br>U: Unbekannt | char(1) |
| **`javascript`** | Eine Such-ID JavaScript Version basierend auf `j_jscript`. Verweist auf die Suchtabelle `javascript_version` | tinyint unsigniert |
| **`language`** | Eine numerisch-ID, die die Sprache des Besucher darstellt. Verweist auf die Suchtabelle `languages.tsv`. | smallint unsigniert |
| **`last_hit_time_gmt`** | Zeitstempel (in UNIX®-Zeit) des vorherigen Treffers. Wird zur Berechnung der Dimension [[!UICONTROL Tage seit dem letzten Besuch]](/help/components/dimensions/days-since-last-visit.md) verwendet. | int |
| **`last_purchase_num`** | Die Dimension [Kundentreue](/help/components/dimensions/customer-loyalty.md) . Die Anzahl der vorherigen Käufe des Besuchers. <br>0: Keine vorherigen Käufe (kein Kunde) <br>1: 1 vorheriger Kauf (neuer Kunde) <br>2: 2 vorherige Käufe (Bestandskunde) <br>3: 3 oder mehr vorherige Käufe (treuer Kunde) | int unsigniert |
| **`last_purchase_time_gmt`** | Wird in der Dimension [[!UICONTROL Tage seit dem letzten Kauf]](/help/components/dimensions/days-since-last-purchase.md) verwendet. Zeitstempel (in UNIX®-Zeit) des letzten Kaufs. Bei Erstkäufen und Besuchern, die zuvor noch nichts gekauft haben, ist dieser Wert `0`. | int |
| **`latlon1`** | Standort (bis 10 km) | varchar(255) |
| **`latlon23`** | Standort (bis 100 m) | varchar(255) |
| **`latlon45`** | Standort (bis 1 m) | varchar(255) |
| **`mc_audiences`** | Liste der Segment-IDs von Audience Manager, zu denen der Besucher gehört. Die Spalte `post_mc_audiences` ändert das Trennzeichen in `--**--`. | text |
| **`mcvisid`** | Experience Cloud-Besucher-ID. 128-Bit-Zahl bestehend aus zwei verketteten 64-Bit-Zahlen verteilt auf 19 Ziffern. | varchar(255) |
| **`mobile_id`** | Die numerische Geräte-ID, wenn die Person ein Mobilgerät verwendet. Der Schlüsselwert für die `mobile_attributes.tsv` [dynamische Suche](dynamic-lookups.md). | int |
| **`mobileaction`** | Mobile Aktion. Wird automatisch erfasst, wenn `trackAction` in mobilen Implementierungen aufgerufen wird. Ermöglicht automatisches Action Pathing in der App. | varchar(100) |
| **`mobileappid`** | ID der Mobile App. Speichert den Namen und die Version der App im folgenden Format: `[AppName] [BundleVersion]`.  | varchar(255) |
| **`mobileappperformanceappid`** | Wird im Apteligent-Daten-Connector verwendet. Die in Apteligent verwendete App-ID. | varchar(255) |
| **`mobileappperformancecrashid`** | Wird im Apteligent-Daten-Connector verwendet. Die in Apteligent verwendete Absturz-ID. | varchar(255) |
| **`mobileappstoreobjectid`** | Wird im [!DNL Appfigures] Data Connector verwendet. App Store-Objekt-ID. | varchar(255) |
| **`mobilebeaconmajor`** | Mobile Services – Haupt-Beacon | varchar(100) |
| **`mobilebeaconminor`** | Mobile Services – Neben-Beacon | varchar(100) |
| **`mobilebeaconproximity`** | Mobile Services – Beacon-Nähe | varchar(255) |
| **`mobilebeaconuuid`** | Mobile Services-Beacon UUID | varchar(100) |
| **`mobilecampaigncontent`** | Der Name oder die ID des Inhalts, der den Link angezeigt hat. Erfasst durch App-Akquise. | varchar(255) |
| **`mobilecampaignmedium`** | Marketing-Medium, z. B. ein Banner oder eine E-Mail. Erfasst durch App-Akquise. | varchar(255) |
| **`mobilecampaignname`** | Der Name der Kampagne, der auch in der Kampagnenvariablen gespeichert ist. Erfasst durch App-Akquise. | varchar(255) |
| **`mobilecampaignsource`** | Ursprünglicher Referrer, z. B. ein Newsletter oder ein Social Media-Netzwerk. Erfasst durch App-Akquise. | varchar(255) |
| **`mobilecampaignterm`** | Bezahlte Suchbegriffe oder andere Begriffe, die Sie mit dieser Akquise verfolgen möchten. Erfasst durch App-Akquise. | varchar(255) |
| **`mobiledayofweek`** | Nummer des Wochentags, an dem die App gestartet wurde. | varchar(255) |
| **`mobiledayssincefirstuse`** | Anzahl der Tage, die seit dem ersten Ausführen der App vergangen sind. | varchar(255) |
| **`mobiledayssincelastuse`** | Anzahl der Tage, die vergangen sind, seitdem die App das letzte Mal ausgeführt wurde. | varchar(255) |
| **`mobiledeeplinkid`** | Erfasst mit der Kontextdatenvariablen `a.deeplink.id`. Wird in Akquise-Berichten als Identifikator für mobilen Akquise-Link verwendet. | varchar(255) |
| **`mobiledevice`** | Mobilgerätname. Unter iOS als kommagetrennte 2-Ziffern-Zeichenfolge gespeichert. Die erste Zahl gibt die Gerätegeneration an und die zweite die Gerätefamilie. | varchar(255) |
| **`mobilehourofday`** | Gibt die Stunde des Tages an, zu der die App gestartet wurde. Angaben im 24-Stunden-Format. | varchar(255) |
| **`mobileinstalldate`** | Installationsdatum der Mobile App. Stellt das Datum zur Verfügung, an dem eine Person die Mobile App erstmalig geöffnet hat. | varchar(255) |
| **`mobilelaunchnumber`** | Wird immer dann erhöht, wenn die Mobile App gestartet wird. | varchar(255) |
| **`mobilemessagebuttonname`** | Erfasst mit der Kontextdatenvariablen `a.message.button.id`. Wird für In-App-Nachrichten verwendet, um die Schaltfläche zu identifizieren, mit der die Nachricht geschlossen wurde. | varchar(100) |
| **`mobilemessageid`** | In-App-Nachrichten-ID | varchar(255) |
| **`mobilemessageonline`** | In-App-Online-Nachricht | varchar(255) |
| **`mobilemessagepushoptin`** | Erfasst mit der Kontextdatenvariablen `a.push.optin`. Setzen Sie sie auf „true“, wenn sich der Benutzer für Push-Nachrichten anmeldet; andernfalls ist der Wert „false“. | varchar(255) |
| **`mobilemessagepushpayloadid`** | Erfasst mit der Kontextdatenvariablen `a.push.payloadid`. Wird in Push-Nachrichten als Payload-ID verwendet. | varchar(255) |
| **`mobileosversion`** | Betriebssystemversion der Mobile Services | varchar(255) |
| **`mobileplaceaccuracy`** | Erfasst mit der Kontextdatenvariablen `a.loc.acc`. Gibt die Genauigkeit des GPS in Metern zum Erfassungszeitpunkt an. | varchar(255) |
| **`mobileplacecategory`** | Erfasst mit der Kontextdatenvariablen `a.loc.category`. Beschreibt die Kategorie eines bestimmten Orts. | varchar(255) |
| **`mobileplaceid`** | Erfasst mit der Kontextdatenvariablen `a.loc.id`. Kennung für einen bestimmten Zielpunkt. | varchar(255) |
| **`mobilepushoptin`** | Mobile Services-Push-Opt-in | varchar(255) |
| **`mobilepushpayloadid`** | Mobile Services-Push-Payload-ID | varchar(255) |
| **`mobilerelaunchcampaigncontent`** | Startinhalte für Mobile Services | varchar(255) |
| **`mobilerelaunchcampaignmedium`** | Startmedium für Mobile Services | varchar(255) |
| **`mobilerelaunchcampaignsource`** | Startquelle für Mobile Services | varchar(255) |
| **`mobilerelaunchcampaignterm`** | Startbedingung für Mobile Services | varchar(255) |
| **`mobilerelaunchcampaigntrackingcode`** | Erfasst mit der Kontextdatenvariablen `a.launch.campaign.trackingcode`. Wird bei der Akquise als Trackingcode für die Startkampagne verwendet. | varchar(255) |
| **`mobileresolution`** | Auflösung des Mobilgeräts. `[Width] x [Height]` in Pixel. | varchar(255) |
| **`monthly_visitor`** | Eine Markierung, die bestimmt, ob der Besucher für den aktuellen Monat eindeutig ist. | tinyint unsigniert |
| **`mvvar1`** - `mvvar3` | [Listenvariable](/help/implement/vars/page-vars/list.md)-Werte. Enthält eine durch Trennzeichen getrennte Liste benutzerdefinierter Werte in Abhängigkeit von der Implementierung. Die Spalten `post_mvvar1` - `post_mvvar3` ersetzen das ursprüngliche Trennzeichen durch `--**--`. | text |
| **`mvvar1_instances`** – `mvvar3_instances` | Die Werte der Listenvariablen, die beim aktuellen Treffer festgelegt wurden. Ersetzt das ursprüngliche Trennzeichen durch `--**--`. Die `post` Spalten enthalten normalerweise keine Daten. | Text |
| **`new_visit`** | Eine Markierung, die bestimmt, ob der aktuelle Treffer ein neuer Besuch ist. Wird durch Adobe nach 30 Minuten Besuchs-Inaktivität festgelegt. | tinyint unsigniert |
| **`os`** | Eine numerische ID, die das Betriebssystem des Besuchers darstellt. Basiert auf der Spalte `user_agent`. Der Schlüsselwert für `operating_system.tsv` Standardsuche und `operating_system_type.tsv` [Dynamische Suche](dynamic-lookups.md). | int unsigniert |
| **`page_event`** | Die Art des Treffers, die in der Bildanforderung gesendet wird (Standardtreffer, Downloadlink, benutzerspezifischer Link, Exitlink). Siehe [Seitenereignissuche](datafeeds-page-event.md). | tinyint unsigniert |
| **`page_event_var1`** | Wird nur in Linktracking-Bildanforderungen verwendet. Die URL des angeklickten Downloadlinks, Exitlinks oder benutzerspezifischen Links. | text |
| **`page_event_var2`** | Wird nur in Linktracking-Bildanforderungen verwendet. Der benutzerdefinierte Name (falls angegeben) des Links. Legt den [benutzerspezifischer Link](/help/components/dimensions/custom-link.md), [Downloadlink](/help/components/dimensions/download-link.md) oder [Exitlink](/help/components/dimensions/exit-link.md) abhängig vom Wert in `page_event` fest. | varchar(100) |
| **`page_type`** | Die [Seiten nicht gefunden](/help/components/dimensions/pages-not-found.md) Dimension, die normalerweise für 404-Seiten verwendet wird. | char(20) |
| **`page_url`** | Die URL des Treffers. Beachten Sie, dass `post_page_url` es für Linktracking Bildanforderungen ([`tl()`](/help/implement/vars/functions/tl-method.md)) entfernt wird und den Datentyp varchar(255) verwendet. | Text |
| **`pagename`** | Die Dimension [Seite](/help/components/dimensions/page.md) . Wenn die Variable [`pagename`](/help/implement/vars/page-vars/pagename.md) leer ist, verwendet Analytics stattdessen `page_url`. | varchar(100) |
| **`pagename_no_url`** | Ähnlich wie `pagename`, allerdings ohne Fallback auf `page_url`. Nur die Spalte `post` ist verfügbar. | varchar(100) |
| **`paid_search`** | Eine Markierung, die bestimmt, ob der Treffer mit der Erkennung der Paid Search übereinstimmt. | tinyint unsigniert |
| **`persistent_cookie`** | Wird in der Dimension [Unterstützung persistenter Cookies](/help/components/dimensions/persistent-cookie-support.md) verwendet. Gibt an, ob der Benutzer Cookies unterstützt, die nicht nach jedem Treffer gelöscht werden. | char(1) |
| **`pointofinterest`** | Name des Mobile Services-Zielpunkts | varchar(255) |
| **`pointofinterestdistance`** | Entfernung der Mobile Services zur Zielpunktmitte | varchar(255) |
| **`post_`**-Spalten | Enthält den in diesen Berichten ultimativ verwendeten Wert. Jede Post-Spalte wird nach der serverseitigen Logik, den Verarbeitungsregeln und den VISTA-Regeln gefüllt. Adobe empfiehlt in den meisten Fällen die Verwendung von Post-Spalten. | Vgl. entsprechende non-post-Spalte |
| **`product_list`** | Die [`products`](/help/implement/vars/page-vars/products.md) Seitenvariable. Hilft beim Ausfüllen mehrerer Dimensionen und Metriken, einschließlich [Kategorie](/help/components/dimensions/category.md), [Produkt](/help/components/dimensions/product.md), [Einheiten](/help/components/metrics/units.md) und [Umsatz](/help/components/metrics/revenue.md). | text |
| **`prop1`** – `prop75` | Benutzerdefinierte Traffic-Variablen 1 bis 75. Wird in den Dimensionen [Prop](/help/components/dimensions/prop.md) verwendet. | varchar(100) |
| **`purchaseid`** | Eindeutige Kennung für einen Kauf, so wie durch das Festlegen der Variable [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) bestimmt. Von der Spalte `duplicate_purchase` verwendet. | char(20) |
| **`quarterly_visitor`** | Eine Markierung, die bestimmt, ob der Treffer ein neuer vierteljährlicher Besucher ist. | tinyint unsigniert |
| **`ref_domain`** | Die Dimension [Verweisende Domain](/help/components/dimensions/referring-domain.md) . Basiert auf der Spalte `referrer` . | varchar(100) |
| **`ref_type`** | Eine numerische ID, die den Typ der Empfehlung für den Treffer darstellt. In der Dimension [Referrer-Typ](/help/components/dimensions/referrer-type.md) verwendet. <br>1: Auf Ihrer Site<br>2: Andere Websites <br>3: Suchmaschinen <br>4: Festplatte <br>5: USENET <br>6: Eingegeben/mit Lesezeichen versehen (kein Referrer) <br>7: E-Mail <br>8: Kein JavaScript <br>9: Soziale Netzwerke | tinyint unsigniert |
| **`referrer`** | Die Dimension [Referrer](/help/components/dimensions/referrer.md). Beachten Sie, dass während `referrer` einen Datentyp von varchar(255) verwendet, `post_referrer` einen Datentyp von varchar(244) verwendet. | varchar(255) |
| **`resolution`** | Eine numerische ID, die für die Auflösung des Monitors steht. In der Dimension [Bildschirmauflösung](/help/components/dimensions/monitor-resolution.md) verwendet. Verwendet die Suchtabelle `resolution.tsv`. | smallint unsigniert |
| **`s_kwcid`** | Die Keyword-ID, die in Adobe Advertising-Integrationen verwendet wird. | varchar(255) |
| **`s_resolution`** | Rohwert der Bildschirmauflösung. Erfasst mit der JavaScript-Funktion `screen.width x screen.height`. | char(20) |
| **`search_engine`** | Eine numerische ID, die die Suchmaschine darstellt, die den Besucher auf Ihre Site verwiesen hat. Wird in [Suchmaschinen](/help/components/dimensions/search-engine.md)-Dimensionen verwendet. Verweist auf die Suchtabelle `search_engines.tsv`. | smallint unsigniert |
| **`search_page_num`** | Verwendet von der Dimension [Alle Suchseiten-Ranglisten](/help/components/dimensions/all-search-page-rank.md). Gibt an, auf welcher Seite der Suchergebnisse Ihre Site angezeigt wurde, ehe die Person sich zu Ihrer Site durchgeklickt hat. | smallint unsigned |
| **`secondary_hit`** | Eine Markierung, die bestimmt, ob der Treffer ein sekundärer Treffer ist. Dieses Flag stammt in der Regel von Multi-Suite-Tagging und VISTA-Regeln, die Treffer kopieren. | tinyint unsigniert |
| **`sourceid`** | Quell-ID | int unsigniert |
| **`state`** | Statusvariable. | varchar(50) |
| **`stats_server`** | Wird nicht verwendet. Interner Adobe-Server, der den Treffer verarbeitet hat. | char(30) |
| **`t_time_info`** | Lokale Zeit des Besuchers. Das Format ist: `M/D/YYYY HH:MM:SS Month (0-11, 0=January) Timezone offset (in minutes)` | varchar(100) |
| **`tnt`** | Wird in Adobe Target-Integrationen verwendet. Stellt alle Tests dar, für die er derzeit qualifiziert ist. Das Format ist: `TargetCampaignID:TargetRecipeID:TargetType\|Event/Action`. | text |
| **`tnt_action`** | Wird in Adobe Target-Integrationen verwendet. Stellt alle Tests dar, für die der Treffer qualifiziert ist. | text |
| **`tnt_instances`** | Wird in Adobe Target-Integrationen verwendet. Target-Instanzvariable. | text |
| **`transactionid`** | Eine eindeutige Kennung, bei der später verschiedene Datenpunkte via Datenquellen hochgeladen werden können. Erfasst mithilfe der Variablen [`transactionID`](/help/implement/vars/page-vars/transactionid.md). | text |
| **`truncated_hit`** | Eine Markierung, die anzeigt, dass die Bildanforderung abgeschnitten wurde. Zeigt den Erhalt eines teilweisen Treffers an. <br>Y: Treffer abgeschnitten; Teiltreffer erhalten <br>N: Treffer nicht abgeschnitten; vollständigen Treffer erhalten | char(1) |
| **`user_agent`** | Die Benutzeragenten-Zeichenfolge, die im HTTP-Header der Bildanforderung gesendet wird. | text |
| **`user_hash`** | Wird nicht verwendet. Doppelkreuz in der Report Suite-ID. Verwenden Sie stattdessen `username`. | int unsigniert |
| **`user_server`** | Verwendet in der Dimension [Server](/help/components/dimensions/server.md). | varchar(100) |
| **`userid`** | Wird nicht verwendet. Die numerische ID für die Report Suite-ID. Verwenden Sie stattdessen `username`. | int unsigniert |
| **`username`** | Die Report Suite-ID für den Treffer. | char(40) |
| **`va_closer_detail`** | Die Dimension [Detail des Letztkontakts](/help/components/dimensions/last-touch-detail.md). | varchar(255) |
| **`va_closer_id`** | Eine numerische ID, die die Dimension [Letztkontaktkanal](/help/components/dimensions/last-touch-channel.md) identifiziert. Die Suche nach dieser ID finden Sie im Marketing-Kanal-Manager. | tinyint unsigniert |
| **`va_finder_detail`** | Die Dimension [Detail des Erstkontakts](/help/components/dimensions/first-touch-detail.md) . | varchar(255) |
| **`va_finder_id`** | Eine numerische ID, die die Dimension [Erstkontaktkanal](/help/components/dimensions/first-touch-channel.md) identifiziert. Die Suche nach dieser ID finden Sie im Marketing-Kanal-Manager. | tinyint unsigniert |
| **`va_instance_event`** | Eine Markierung, die den Marketing-Kanal [Instanzen](/help/components/metrics/instances.md) identifiziert. | tinyint unsigniert |
| **`va_new_engagement`** | Eine Markierung, die den Marketing-Kanal [Neue Interaktionen](/help/components/metrics/new-engagements.md) identifiziert. | tinyint unsigniert |
| **`video`** | Die Dimension [Inhalt](/help/components/dimensions/sm-core.md) Streaming-Medien . | varchar(255) |
| **`videoad`** | Die Dimension [Anzeige](/help/components/dimensions/sm-ads.md) Streaming-Medien . | varchar(255) |
| **`videoadinpod`** | Die Dimension [Anzeige in Pod-Position](/help/components/dimensions/sm-ads.md) Streaming-Medien . | varchar(255) |
| **`videoadlength`** | Die Dimension [Anzeigenlänge (Variable)](/help/components/dimensions/sm-ads.md) Streaming-Medien . | Ganzzahl |
| **`videoadload`** | Die Dimension [Anzeige lädt](/help/components/dimensions/sm-ads.md) Streaming-Medien . | varchar(255) |
| **`videoadname`** | Die Dimension [Anzeigename (Variable)](/help/components/dimensions/sm-ads.md) Streaming-Medien . | varchar(255) |
| **`videoadplayername`** | Die Dimension [Anzeigenplayer-Name](/help/components/dimensions/sm-ads.md) Streaming-Medien . | varchar(255) |
| **`videoadpod`** | Die Dimension [Ad Pod](/help/components/dimensions/sm-ads.md) Streaming Media . | varchar(255) |
| **`videoadvertiser`** | Der Werbetreibende,](/help/components/dimensions/sm-ads.md) der [Dimension für das Streaming von Medien. | varchar(255) |
| **`videoaudioalbum`** | Das [Album](/help/components/dimensions/sm-audio-metadata.md) Streaming Media Dimension. | varchar(255) |
| **`videoaudioartist`** | Die Dimension [Interpret](/help/components/dimensions/sm-audio-metadata.md) Streaming-Medien . | varchar(255) |
| **`videoaudioauthor`** | Die Dimension [Autor](/help/components/dimensions/sm-audio-metadata.md) Streaming-Medien . | varchar(255) |
| **`videoaudiolabel`** | Die Dimension [Label](/help/components/dimensions/sm-audio-metadata.md) Streaming-Medien . | varchar(255) |
| **`videoaudiopublisher`** | Die Dimension [Publisher](/help/components/dimensions/sm-audio-metadata.md) Streaming-Medien . | varchar(255) |
| **`videoaudiostation`** | Die Dimension [Station](/help/components/dimensions/sm-audio-metadata.md) Streaming-Medien . | varchar(255) |
| **`videocampaign`** | Die Dimension [Kampagnen-ID](/help/components/dimensions/sm-ads.md) Streaming-Medien . | varchar(255) |
| **`videochannel`** | Die Dimension [Inhaltskanal](/help/components/dimensions/sm-core.md) Streaming-Medien . | varchar(255) |
| **`videochapter`** | Die Dimension [Kapitel](/help/components/dimensions/sm-chapters.md) Streaming-Medien . | varchar(255) |
| **`videocontenttype`** | Der [Content-Typ](/help/components/dimensions/sm-core.md) &quot;Streaming Media&quot; Dimension. | varchar(255) |
| **`videodaypart`** | Der [Tag Teil](/help/components/dimensions/sm-video-metadata.md) Streaming Media Dimension. | varchar(255) |
| **`videoepisode`** | Die Dimension [Folge](/help/components/dimensions/sm-video-metadata.md) Streaming-Medien . | varchar(255) |
| **`videofeedtype`** | Die Dimension [Medien-Feed](/help/components/dimensions/sm-video-metadata.md)Typ: Streaming-Medien. | varchar(255) |
| **`videogenre`** | Das [Genre](/help/components/dimensions/sm-video-metadata.md) Streaming Media Dimension. Bei dieser Dimension sind mehrere Werte im selben Treffer, durch ein Komma getrennt, zulässig. | Text |
| **`videolength`** | Die Dimension [Inhaltslänge (Variable)](/help/components/dimensions/sm-core.md) Streaming-Medien . | Ganzzahl |
| **`videomvpd`** | Die Dimension [MVPD](/help/components/dimensions/sm-video-metadata.md) Streaming-Medien . | varchar(255) |
| **`videoname`** | Die Dimension [Inhaltsname (Variable)](/help/components/dimensions/sm-core.md) Streaming-Medien . | varchar(255) |
| **`videonetwork`** | Die Dimension [Netzwerk](/help/components/dimensions/sm-video-metadata.md) Streaming-Medien . | varchar(255) |
| **`videopath`** | Die Dimension [Medienpfad](/help/components/dimensions/sm-core.md) Streaming-Medien . | varchar(100) |
| **`videoplayername`** | Die Dimension [Name des Content](/help/components/dimensions/sm-core.md)Players“ für Streaming-Medien. | varchar(255) |
| **`videotime`** | Die Metrik [Besuchszeit für Inhalt](/help/components/metrics/sm-core.md) Streaming-Medien . | Ganzzahl |
| **`videoqoebitrateaverageevar`** | Die Dimension [Durchschnittliche Bitrate](/help/components/dimensions/sm-quality.md) Streaming-Medien . | varchar(255) |
| **`videoqoebitratechangecountevar`** | Die Dimension [Bitratenänderungen](/help/components/dimensions/sm-quality.md) Streaming-Medien . | varchar(255) |
| **`videoqoebuffercountevar`** | Die Dimension [Pufferereignisse](/help/components/dimensions/sm-quality.md) Streaming-Medien. | varchar(255) |
| **`videoqoebuffertimeevar`** | Die Dimension [Gesamtpufferdauer](/help/components/dimensions/sm-quality.md) Streaming-Medien . | varchar(255) |
| **`videoqoedroppedframecountevar`** | Die Dimension [Abgelegte Frames](/help/components/dimensions/sm-quality.md) Streaming-Medien . | varchar(255) |
| **`videoqoeerrorcountevar`** | Die Dimension [Fehler](/help/components/dimensions/sm-quality.md) Streaming-Medien . | varchar(255) |
| **`videoqoeextneralerrors`** | Die Dimension [Externe Fehler-IDs](/help/components/dimensions/sm-quality.md) Streaming-Medien . Diese Dimension ermöglicht mehrere Werte im selben Treffer. | Text |
| **`videoqoeplayersdkerrors`** | Die [Player SDK Fehler-IDs](/help/components/dimensions/sm-quality.md) Streaming Media Dimension. Auf dieser Dimension sind mehrere Werte in derselben Treffer zulässig. | Text |
| **`videoqoetimetostartevar`** | Die [Zeit zu Beginn](/help/components/dimensions/sm-quality.md) Dimension für Streamingmedien. | varchar(255) |
| **`videoseason`** | Die [Saison](/help/components/dimensions/sm-video-metadata.md) Streaming-Media-Dimension. | varchar(255) |
| **`videosegment`** | Die Dimension [Inhaltssegment](/help/components/dimensions/sm-core.md) Streaming-Medien . | varchar(255) |
| **`videoshow`** | Die Dimension [Anzeigen](/help/components/dimensions/sm-video-metadata.md) Streaming-Medien . | varchar(255) |
| **`videoshowtype`** | Die Dimension [Sendungstyp](/help/components/dimensions/sm-video-metadata.md) Streaming-Medien. | varchar(255) |
| **`videostreamtype`** | Die Dimension [Stream-Typ](/help/components/dimensions/sm-core.md) Streaming-Medien . | varchar(255) |
| **`visid_high`** | Wird mit `visid_low` zur eindeutigen Identifizierung von Besuchenden verwendet. | bigint unsigned |
| **`visid_low`** | Wird mit `visid_high` zur eindeutigen Identifizierung von Besuchenden verwendet. | bigint unsigned |
| **`visid_new`** | Eine Markierung, die bestimmt, ob der Treffer eine neu generierte Besucher-ID enthält. | char(1) |
| **`visid_timestamp`** | Wenn eine Besucher-ID neu generiert wird, gibt den Zeitstempel in UNIX® an, zu dem die Besucher-ID generiert wurde. | int |
| **`visid_type`** | Nicht zur externen Verwendung; intern von Adobe für Verarbeitungsoptimierungen verwendet. Eine numerische ID, die die Methode zur Identifizierung des Besuchers darstellt.<br>`0`: Benutzerspezifische Besucher-ID oder unbekannt/nicht anwendbar<br>`1`: IP- und Benutzeragenten-Fallback<br>`2`: HTTP-Kopfzeile mobiler Teilnehmer <br>`3`: Alter Cookie-Wert (`s_vi`) <br>`4`: Fallback-Cookie-Wert (`s_fid`) <br>`5`: Identity Service | tinyint unsigniert |
| **`visit_keywords`** | Die Dimension [Suchbegriff](/help/components/dimensions/search-keyword.md) . Diese Spalte verwendet eine nicht standardmäßige Zeichenbeschränkung von varchar(244), um der von Adobe verwendeten Backend-Logik Rechnung zu tragen. | varchar(244) |
| **`visit_num`** | Die [Besuchsnummer](/help/components/dimensions/visit-number.md) Dimension. Beginnt bei 1 und erhöht sich bei jedem neuen Besuch eines Besuchers. | int unsigniert |
| **`visit_page_num`** | Die [Treffertiefe](/help/components/dimensions/hit-depth.md) Dimension. Wird für jedes Treffer, das der Besucher generiert, um 1 erhöht. Setzt jeden Besuch zurück. | int unsigniert |
| **`visit_ref_domain`** | Basierend auf der Spalte `visit_referrer`. Die allererste verweisende Domain des Besuchs. | varchar(100) |
| **`visit_ref_type`** | Eine numerisch-ID, die den Werber Typ der ersten Werber der Visit darstellt. Verweist auf die Suchtabelle `referrer_type.tsv` | tinyint unsigniert |
| **`visit_referrer`** | Die erste verweisende Stelle des Besuchs. | varchar(255) |
| **`visit_search_engine`** | Eine numerische ID, die die erste Suchmaschine des Besuchs darstellt. Verweist auf die Suchtabelle `search_engines.tsv`. | smallint unsigniert |
| **`visit_start_page_url`** | Die erste URL des Besuchs. | varchar(255) |
| **`visit_start_pagename`** | Der Wert „Seitenname“ im ersten Treffer des Besuchs. | varchar(100) |
| **`visit_start_time_gmt`** | Zeitstempel (in UNIX®-Zeit) des ersten Treffers des Besuchs. | int |
| **`weekly_visitor`** | Eine Markierung, die bestimmt, ob der Treffer ein neuer wöchentlicher Besucher ist. | tinyint unsigniert |
| **`yearly_visitor`** | Eine Markierung, die bestimmt, ob der Treffer ein neuer jährlicher Besucher ist. | tinyint unsigniert |
| **`zip`** | Hilft beim Ausfüllen der Dimension [Postleitzahl](/help/components/dimensions/zip-code.md). Siehe auch `geo_zip`. | varchar(50) |

{style="table-layout:auto"}

## Nicht verwendete oder eingestellte Spalten

Die folgende Liste von Spalten ist nicht verwendet, nicht mehr verwendet oder enthält anderweitig keinen Wert im Reporting. Einige dieser Spalten sind an Funktionen gebunden, die nicht mehr unterstützt werden, während andere aufgrund neuer und robusterer Funktionen nicht mehr benötigt werden. Die meisten dieser Spalten enthalten keine Daten. Spalten, die möglicherweise noch Daten enthalten, werden von aktuellen Datenerfassungsbibliotheken nicht unterstützt und sind in Analysis Workspace nicht für Dimensionen verfügbar.

* `adclassificationcreative`
* `click_action`
* `click_action_type`
* `click_context`
* `click_context_type`
* `click_sourceid`
* `click_tag`
* `hier1` - `hier5`
* `homepage`
* `ip2`
* `mobileacquisitionclicks`
* `mobileactioninapptime`
* `mobileactiontotaltime`
* `mobileappperformanceaffectedusers`
* `mobileappperformanceappid.app-perf-app-name`
* `mobileappperformanceappid.app-perf-platform`
* `mobileappperformancecrashes`
* `mobileappperformancecrashid.app-perf-crash-name`
* `mobileappperformanceloads`
* `mobileappstoreavgrating`
* `mobileappstoredownloads`
* `mobileappstoreinapprevenue`
* `mobileappstoreinapproyalties`
* `mobileappstoreobjectid.app-store-user`
* `mobileappstoreobjectid.application-name`
* `mobileappstoreobjectid.application-version`
* `mobileappstoreobjectid.appstore-name`
* `mobileappstoreobjectid.category-name`
* `mobileappstoreobjectid.country-name`
* `mobileappstoreobjectid.device-manufacturer`
* `mobileappstoreobjectid.device-name`
* `mobileappstoreobjectid.in-app-name`
* `mobileappstoreobjectid.platform-name-version`
* `mobileappstoreobjectid.rank-category-type`
* `mobileappstoreobjectid.region-name`
* `mobileappstoreobjectid.review-comment`
* `mobileappstoreobjectid.review-title`
* `mobileappstoreoneoffrevenue`
* `mobileappstoreoneoffroyalties`
* `mobileappstorepurchases`
* `mobileappstorerank`
* `mobileappstorerankdivisor`
* `mobileappstorerating`
* `mobileappstoreratingdivisor`
* `mobileavgprevsessionlength`
* `mobilecrashes`
* `mobilecrashrate`
* `mobiledailyengagedusers`
* `mobiledayssincelastupgrade`
* `mobiledeeplinkid.name`
* `mobileinstalls`
* `mobilelaunches`
* `mobilelaunchessincelastupgrade`
* `mobileltv`
* `mobileltvtotal`
* `mobilemessageclicks`
* `mobilemessageid.dest`
* `mobilemessageid.name`
* `mobilemessageid.type`
* `mobilemessageimpressions`
* `mobilemessagepushpayloadid.name`
* `mobilemessageviews`
* `mobilemonthlyengagedusers`
* `mobileosenvironment`
* `mobileplacedwelltime`
* `mobileplaceentry`
* `mobileplaceexit`
* `mobileprevsessionlength`
* `mobilerelaunchcampaigntrackingcode.name`
* `mobileupgrades`
* `namespace`
* `p_plugins`
* `page_event_var3`
* `partner_plugins`
* `plugins`
* `prev_page`
* `product_merchandising`
* `sampled_hit`
* `service`
* `socialaccountandappids`
* `socialassettrackingcode`
* `socialauthor`
* `socialaveragesentiment`
* `socialaveragesentiment (deprecated)`
* `socialcontentprovider`
* `socialfbstories`
* `socialfbstorytellers`
* `socialinteractioncount`
* `socialinteractiontype`
* `sociallanguage`
* `sociallatlong`
* `sociallikeadds`
* `sociallink`
* `sociallink (deprecated)`
* `socialmentions`
* `socialowneddefinitioninsighttype`
* `socialowneddefinitioninsightvalue`
* `socialowneddefinitionmetric`
* `socialowneddefinitionpropertyvspost`
* `socialownedpostids`
* `socialownedpropertyid`
* `socialownedpropertyname`
* `socialownedpropertypropertyvsapp`
* `socialpageviews`
* `socialpostviews`
* `socialproperty`
* `socialproperty (deprecated)`
* `socialpubcomments`
* `socialpubposts`
* `socialpubrecommends`
* `socialpubsubscribers`
* `socialterm`
* `socialtermslist`
* `socialtermslist (deprecated)`
* `socialtotalsentiment`
* `survey`
* `survey_instances`
* `tnt_post_vista`
* `ua_color`
* `ua_os`
* `ua_pixels`
* `videoauthorized`
* `videoaverageminuteaudience`
* `videochaptercomplete`
* `videochapterstart`
* `videochaptertime`
* `videopause`
* `videopausecount`
* `videopausetime`
* `videoplay`
* `videoprogress10`
* `videoprogress25`
* `videoprogress50`
* `videoprogress75`
* `videoprogress96`
* `videoqoebitrateaverage`
* `videoqoebitratechange`
* `videoqoebuffer`
* `videoqoedropbeforestart`
* `videoqoedroppedframes`
* `videoqoeerror`
* `videoresume`
* `videototaltime`
* `videouniquetimeplayed`
