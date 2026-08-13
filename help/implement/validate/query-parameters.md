---
title: Datenerfassungs-Abfrageparameter
description: Listet alle in Bildanforderungen verwendeten Abfragezeichenfolgenparameter auf.
feature: Implementation Basics
exl-id: 2eb2ade7-a3db-4b00-8a70-2632d1c0aaaf
role: Admin, Developer, Leader, User
TQID: https://experienceleague.adobe.com/aB92GXPxYSkjcDD9wi0vj47jijqndMbOGaECvXs38-Y
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c069c44e-5426-4c1a-accc-8028662f2fde
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a947d2d7f45d4155a61cbfe0f8110851cca32e60
workflow-type: tm+mt
source-wordcount: 1111
ht-degree: 46%

---

# Datenerfassungs-Abfrageparameter

In der folgenden Tabelle sind alle Abfragezeichenfolgenparameter aufgeführt, die Adobe in Bildanforderungen verwendet. Diese Informationen sind beim Debugging mit [Paketanalysatoren](packet-monitor.md) bei der [Hartkodierung von Bildanforderungen](../other/hardcoded.md) oder bei der Verwendung [dynamischer Variablen](../vars/page-vars/dynamic-variables.md) hilfreich.

| Parameter | Analytics-Implementierungsvariable | Beschreibung |
| --- | --- | --- |
| `aamlh` | Keine | Audience Manager-Standorthinweis. Identifiziert das regionale Rechenzentrum, das für die Audience Manager ID-Synchronisierung über den Besucher-ID-Service verwendet wird. |
| `aamb` | Keine | Audience Manager Blob. Kodierte Audience Manager-Profildaten, die während der ID-Synchronisierung durch den Besucher-ID-Service übergeben werden. |
| `aid` | Keine | Die ältere Analytics-Besucher-ID, die im `s_vi`-Cookie gespeichert ist. Wird in modernen Implementierungen durch den `mid`-Parameter ersetzt. |
| `AQB` | Keine | Zeigt den Anfang einer Abfragezeichenfolge für Bildanforderungen an. |
| `AQE` | Keine | Zeigt das Ende einer Bildanforderung an (d. h., dass die Anforderung nicht abgeschnitten wurde). |
| `bh` | Keine | Browser-Höhe (in Pixel). Wird in der Dimension [[!UICONTROL Browser-Höhe]](/help/components/dimensions/browser-height.md) verwendet. |
| `bw` | Keine | Browser-Breite (in Pixel). Wird in der Dimension [[!UICONTROL Browser-Breite]](/help/components/dimensions/browser-width.md) verwendet. |
| `c` | Keine | Farbqualität (in Bit). Wird in der Dimension [[!UICONTROL Farbtiefe]](/help/components/dimensions/color-depth.md) verwendet. |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | Zeigt den Start von Kontextdatenvariablen an. Enthält nie einen Wert. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | Zeigt das Ende der Kontextdatenvariablen an. Enthält nie einen Wert. |
| `c1` – `c75` | [`prop1` – `prop75`](../vars/page-vars/prop.md) | [Props](/help/components/dimensions/prop.md) oder benutzerspezifische Traffic-Variablen. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | Die im Treffer verwendete Währung. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/configuration-variables.md#retired-configuration-variables) | **Wird nicht mehr verwendet.** Die Anzahl der Punkte in einer Domain. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | Die Zeichencodierung der Bildanforderung. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) | Die Lebensdauer des Besucher-Cookies. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | Wird in der Dimension [[!UICONTROL Website-Bereiche]](/help/components/dimensions/site-section.md) verwendet. |
| `cp` | [`customerPerspective`](../vars/page-vars/customerperspective.md) | Gibt an, ob ein Mobile-App-Treffer aufgetreten ist, während sich die App im Vordergrund oder Hintergrund befand. Wird in der Dimension [[!UICONTROL Treffertyp]](/help/components/dimensions/hit-type.md) verwendet. |
| `ct` | Keine | Wird in der Dimension [[!UICONTROL Verbindungstyp]](/help/components/dimensions/connection-type.md) verwendet. |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | Gibt an, was für dynamische Variablen verwendet werden soll. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | Kurzschreibweise für den `events`. |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | Durch Komma getrennte Liste der Ereignisse auf der Seite. Wird von den meisten [Metriken](/help/components/metrics/overview.md) verwendet. |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | Die aktuelle URL der Seite mit bis zu 255 Byte. Wird in der Dimension [[!UICONTROL Seiten-URL]](/help/components/dimensions/page-url.md) verwendet. |
| `-g` | [`pageURL`](../vars/page-vars/pageurl.md) | URLs, die länger als 255 Byte sind, werden geteilt. Die ersten 255 Byte werden im `g`-Parameter und alle verbleibenden Byte im `-g`-Parameter angezeigt. |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | Kurzschreibweise für den `pageName`. |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | Kurzschreibweise für den `pageType`. |
| `h.` | [`collectHighEntropyUserAgentHints`](../vars/config-vars/collecthighentropyuseragenthints.md) | Präfix für mehrere Variablen, die [Client-Hinweise](/help/technotes/client-hints.md) repräsentieren. |
| `h1` – `h5` | [`hier1` – `hier5`](../vars/page-vars/page-variables.md#retired-page-variables) | **Wird nicht mehr verwendet.** Hierarchiedimensionen. |
| `hp` | Keine | **Wird nicht mehr verwendet.** Legte in früheren Versionen von Adobe Analytics fest, ob die aktuelle URL die Homepage des Browsers war. |
| `j` | Keine | **Wird nicht mehr verwendet.** Die im Browser installierte JavaScript-Version. |
| `k` | Keine | Wird in der Dimension [[!UICONTROL Cookie-Unterstützung]](/help/components/dimensions/cookie-support.md) verwendet. |
| `l1` – `l3` | [`list1` – `list3`](../vars/page-vars/list.md) | Listenvariablen. |
| `lat` | Keine | **Wird nicht mehr verwendet.** Breitengrad Wird durch veraltete mobile SDK-Implementierungen festgelegt. Aktuelle mobile Implementierungen senden die Geolokalisierung über Datenströme. |
| `lon` | Keine | **Wird nicht mehr verwendet.** Längengrad Wird durch veraltete mobile SDK-Implementierungen festgelegt. Aktuelle mobile Implementierungen senden die Geolokalisierung über Datenströme. |
| `lrt` | Keine | Die „Dauer der letzten Anfrage“, d. h. die Roundtrip-Zeit für die letzte Anfrage in Millisekunden. Sie wird nur gesendet, wenn mehr als eine Anfrage von einer einzelnen Seite gesendet wird, z. B. in einer Single Page Application (SPA). |
| `mcorgid` | Keine | Die IMS-Organisations-ID, die die Organisation für den Besucher-ID-Service identifiziert. |
| `mid` | Keine | Wird in der Dimension [[!UICONTROL Experience Cloud-Besucher-ID]](/help/components/dimensions/experience-cloud-visitor-id.md) verwendet. |
| `ms_a` | Keine | Wird von Media SDK auf `1` festgelegt, wenn es sich bei den verfolgten Streaming-Medien um Audio- und nicht um Videomedien handelt. |
| `ndh` | Keine | Wird von AppMeasurement zu jeder von ihm generierten Bildanforderung hinzugefügt. Da bei hartcodierten Anforderungen in der Regel keine Daten vorhanden sind, deutet das Vorhandensein darauf hin, dass der Treffer von AppMeasurement stammt. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/configuration-variables.md#retired-configuration-variables) | **Wird nicht mehr verwendet.** Hilft festzustellen, wo Cookies gesetzt werden. |
| `oi` | Keine | **Wird nicht mehr verwendet.** Objektinstanz für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | Objekt-Kennung für die letzte Seite. Wird in der aktuellen Version von Activity Map verwendet. |
| `oidt` | Keine | **Wird nicht mehr verwendet.** Objektkennungstyp für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `ot` | Keine | **Wird nicht mehr verwendet.** Objektname für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `p` | Keine | **Wird nicht mehr verwendet.** Liste der im Browser verwendeten Plug-ins. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | Wird in der Dimension [[!UICONTROL Seite]](/help/components/dimensions/page.md) verwendet. |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | Wird in der Dimension [[!UICONTROL Seiten nicht gefunden]](/help/components/dimensions/pages-not-found.md) verwendet. |
| `pccr` | Keine | Umleitungs-Flag für Prüfung persistenter Cookies. Wird von den Datenerfassungs-Servern von Adobe für neue Besucher festgelegt und immer auf `true` festgelegt. Wenn die Cookie-Unterstützung eines neuen Besuchers unbekannt ist, leitet der Datenerfassungs-Server die Bildanforderung mit diesem Flag an sich selbst weiter, um zu bestätigen, dass die Prüfung auf dauerhafte Cookies bereits stattgefunden hat. Dieser Parameter verhindert unendliche Weiterleitungen, wenn der Besucher Cookies ablehnt. |
| `pe` | [`tl()`](../vars/functions/tl-method.md) | Bestimmt den Typ des Treffers. Gültige Werte sind `lnk_o` ([[!UICONTROL benutzerspezifischer Link]](/help/components/dimensions/custom-link.md)), `lnk_d` ([[!UICONTROL Downloadlink]](/help/components/dimensions/download-link.md)), `lnk_e` ([[!UICONTROL Exitlink]](/help/components/dimensions/exit-link.md)) und `tnt` (ein Analytics for Target-Treffer). |
| `pev1` | [`linkURL`](../vars/config-vars/linkurl.md) | Die URL, auf der der benutzerdefinierte Link aufgetreten ist. |
| `pev2` | [`tl()`](../vars/functions/tl-method.md) | Der Anzeigename des [benutzerspezifischer Link](/help/components/dimensions/custom-link.md). |
| `pev3` | Keine | **Wird nicht mehr verwendet.** Verfolgte Meilensteine in früheren Versionen der Videoberichte. |
| `pf` | Keine | Plattformmarkierung; nur zur Verwendung durch Adobe. Nicht ändern. |
| `pid` | Keine | **Wird nicht mehr verwendet.** Seiten-Kennung für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pidt` | Keine | **Wird nicht mehr verwendet.** Seiten-Kennungstyp für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pl` | [`products`](../vars/page-vars/products.md) | Kurzschreibweise für den `products`. |
| `products` | [`products`](../vars/page-vars/products.md) | Variable „products“ (Produktvariable). Wird in den Dimensionen [[!UICONTROL Produkt]](/help/components/dimensions/product.md) und [[!UICONTROL Kategorie]](/help/components/dimensions/category.md) verwendet. |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | Wird in der Dimension [[!UICONTROL Kauf-ID]](/help/components/dimensions/purchase-id.md) verwendet. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | Referrer-URL des Treffers. Wird in Traffic-Quellendimensionen wie &quot;[[!UICONTROL &quot; &#x200B;]](/help/components/dimensions/referrer.md) &quot;[[!UICONTROL &quot; &#x200B;]](/help/components/dimensions/referring-domain.md). |
| `s` | Keine | Bildschirmauflösung in `width x height`. Wird in der Dimension [[!UICONTROL Bildschirmauflösungen]](/help/components/dimensions/monitor-resolution.md) verwendet. |
| `sdid` | Keine | Zusätzliche Daten-ID. Verknüpft mehrere Treffer, die dasselbe Ereignis beschreiben, z. B. Analytics- und Target-Treffer in einer [Analytics for Target](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t.html)-Integration. |
| `server` | [`server`](../vars/page-vars/server.md) | Verwendet in der Dimension [[!UICONTROL Server]](/help/components/dimensions/server.md). |
| `sv` | [`server`](../vars/page-vars/server.md) | Kurzschreibweise für den `server`. |
| `state` | [`state`](../vars/page-vars/page-variables.md#retired-page-variables) | **Wird nicht mehr verwendet.** Erfasst den US-Bundesstaat, in den ein Besucher eingetreten ist, normalerweise über ein Versand- oder Rechnungsformular. |
| `t` | Keine | Generiertes Datum/Uhrzeit des Treffers. Verwendet das Format `dd/mm/yyyy hh:mm:ss w o`.<br>- `dd/mm/yyyy hh:mm:ss` ist Datum/Uhrzeit in JavaScript. Monat `0` ist Januar, während Monat `11` Dezember ist<br>- `w` der Wochentag ist. `0` ist Sonntag, `6` ist Samstag.<br>- `o` ist der negative GMT-Offset in Minuten. Zum Beispiel ist `420` GMT-7. |
| `tnt` | Keine | Target-Daten-Payload, die in Integrationen [Analytics for Target](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t.html) verwendet wird. Wird gesendet, wenn `pe=tnt`. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | Der benutzerdefinierte Zeitstempel, der mit dem Treffer festgelegt wird. Wird normalerweise für das Offline-Tracking verwendet. |
| `u` | Keine | **Wird nicht mehr verwendet.** Kontomarkierung, die in früheren Versionen von Activity Map verwendet wurde. |
| `v` | Keine | Wird in der Dimension [[!UICONTROL Java aktiviert]](/help/components/dimensions/java-enabled.md) verwendet. |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | Wird in der Dimension [[!UICONTROL Trackingcode]](/help/components/dimensions/tracking-code.md) verwendet. |
| `v1` – `v250` | [`evar1` – `eVar250`](../vars/page-vars/evar.md) | [eVars](/help/components/dimensions/evar.md) oder benutzerspezifische Konversionsdimensionen. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | Variable zur Überschreibung der Besucher-ID. |
| `vidn` | Keine | Wird von Adobe-Datenerfassungs-Servern für neue Besucher festgelegt und fügt den `pccr` in der umgeleiteten Bildanforderung hinzu. Enthält den im Besucher-Cookie gespeicherten Besucher-ID-Wert. |
| `vmf` | [`visitorMigrationServer`](../vars/config-vars/configuration-variables.md#retired-configuration-variables) | **Wird nicht mehr verwendet.** Besuchermigrations-Server, der während der Migration von Drittanbieter- zu Erstanbieter-Cookies verwendet wird. |
| `vmt` | [`visitorMigrationKey`](../vars/config-vars/configuration-variables.md#retired-configuration-variables) | **Wird nicht mehr verwendet.** Migrationsschlüssel für Besuchende, mit dem Implementierungen von Drittanbieter-Cookies zu Erstanbieter-Cookies migriert wurden. |
| `vvp` | Keine | **Wird nicht mehr verwendet.** Variablenanbieter, der in Data Connectors verwendet wird |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | Wird mit Data Sources verwendet, um Online- und Offline-Daten miteinander zu verbinden. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | Wird in der Dimension [Postleitzahl](/help/components/dimensions/zip-code.md) verwendet. |
