---
title: Zuordnung von XDM-Objektvariablen zu Adobe Analytics
description: Erfahren Sie, welche XDM-Felder in Edge automatisch Analytics-Variablen zugeordnet werden.
exl-id: fbff5c38-0f04-4780-b976-023e207023c6
feature: Implementation Basics
role: Admin, Developer
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '1458'
ht-degree: 49%

---

# Zuordnung von XDM-Objektvariablen zu Adobe Analytics

Die folgende Tabelle zeigt die XDM-Variablen, die Adobe Experience Platform Edge Network automatisch Adobe Analytics zuordnet. Wenn Sie diese XDM-Feldpfade verwenden, ist keine zusätzliche Konfiguration erforderlich, um Daten an Adobe Analytics zu senden. Diese Felder sind in der Feldergruppe **[!UICONTROL Adobe Analytics ExperienceEvent Template]** enthalten. Die Verwendung dieser Felder wird empfohlen, wenn Sie Daten sowohl an Adobe Analytics als auch an Adobe Experience Platform senden möchten.

Wenn Ihr Unternehmen plant, zu Customer Journey Analytics zu wechseln, empfiehlt Adobe, stattdessen das `data`-Objekt zu verwenden, um Daten direkt an Adobe Analytics zu senden, ohne einem Schema zu entsprechen. Mit dieser Strategie kann Ihr Unternehmen Ihr eigenes Schema verwenden, anstatt die [!UICONTROL Adobe Analytics ExperienceEvent-Vorlage] zu verwenden (was auf Customer Journey Analytics weniger anwendbar ist). Siehe [Zuordnung von Datenobjektvariablen zu Adobe Analytics](data-var-mapping.md) für eine ähnliche Zuordnungstabelle.

## Wertprioritäten

Die meisten XDM-Objektfelder in dieser Tabelle entsprechen einem [Datenobjektfeld](data-var-mapping.md). Wenn Sie sowohl ein bestimmtes XDM-Objektfeld als auch das entsprechende Datenobjektfeld festlegen, hat das Datenobjektfeld Priorität. Wenn Sie sowohl das XDM-Objektfeld als auch das Datenobjektfeld verwenden, empfiehlt Adobe, benutzerdefinierte Ereignisse mithilfe des Datenobjektfelds festzulegen. Wenn das Feld `data.__adobe.analytics.events` vorhanden ist, werden alle XDM-Objektfelder im Zusammenhang mit Commerce- und benutzerdefinierten Ereignissen überschrieben.

## XDM-Objektfeldzuordnung

Vorherige Aktualisierungen dieser Tabelle finden Sie auf der Seite [Commit-Verlauf auf GitHub](https://github.com/AdobeDocs/analytics.en/commits/main/help/implement/aep-edge/xdm-var-mapping.md).

| XDM-Feldpfad | Analytics-Variable und -Beschreibung |
| --- | --- |
| `xdm.application.isClose` | Ermöglicht die Definition der Mobile-Lebenszyklusmetrik [Crashes](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.isInstall` | Hilft bei der Bestimmung, wann die Mobile-Lebenszyklusmetrik [Erste Starts](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/) erhöht werden soll. |
| `xdm.application.closeType` | Bestimmt, ob ein Schließen-Ereignis ein Absturz ist oder nicht. Gültige Werte sind `close` (eine Lebenszyklussitzung endet und ein Pausenereignis wurde für die vorherige Sitzung empfangen) und `unknown` (eine Lebenszyklussitzung endet ohne Pausenereignis). Ermöglicht die Definition der Mobile-Lebenszyklusmetrik [Crashes](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.isInstall` | Die Mobile-Lebenszyklusmetrik [Installationen](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.isLaunch` | Die Mobile-Lebenszyklusmetrik [Starts](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.name` | Ermöglicht die Definition der Mobile-Lebenszyklusdimension [App-ID](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.isUpgrade` | Die Mobile-Lebenszyklusmetrik [Upgrades](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.version` | Ermöglicht die Definition der Mobile-Lebenszyklusdimension [App-ID](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.application.sessionLength` | Die Mobile-Lebenszyklusmetrik [Länge der vorherigen Sitzung](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.commerce.checkouts.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Checkouts](/help/components/metrics/checkouts.md) an. |
| `xdm.commerce.checkouts.value` | Inkrementiert die Metrik [Checkouts](/help/components/metrics/checkouts.md) um den gewünschten Wert. |
| `xdm.commerce.order.currencyCode` | Definiert die Konfigurationsvariable [currencyCode](../vars/config-vars/currencycode.md). |
| `xdm.commerce.order.purchaseID` | Definiert die Seitenvariable [purchaseID](../vars/page-vars/purchaseid.md). |
| `xdm.commerce.order.payments[0].transactionID` | Legt die Seitenvariable [transactionID](../vars/page-vars/transactionid.md) fest. |
| `xdm.commerce.productListAdds.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkorbhinzufügungen](/help/components/metrics/cart-additions.md) an. |
| `xdm.commerce.productListAdds.value` | Erhöht die Metrik [Warenkorbhinzufügungen](/help/components/metrics/cart-additions.md). |
| `xdm.commerce.productListOpens.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkörbe](/help/components/metrics/carts.md) an. |
| `xdm.commerce.productListOpens.value` | Erhöht die Metrik [Warenkörbe](/help/components/metrics/carts.md). |
| `xdm.commerce.productListRemovals.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkorbentnahmen](/help/components/metrics/cart-removals.md) an. |
| `xdm.commerce.productListRemovals.value` | Erhöht die Metrik [Warenkorbentnahmen](/help/components/metrics/cart-removals.md). |
| `xdm.commerce.productListViews.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkorbansichten](/help/components/metrics/cart-views.md) an. |
| `xdm.commerce.productListViews.value` | Erhöht die Metrik [Warenkorbansichten](/help/components/metrics/cart-views.md). |
| `xdm.commerce.productViews.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Produktansichten](/help/components/metrics/product-views.md) an. |
| `xdm.commerce.productViews.value` | Erhöht die Metrik [Produktansichten](/help/components/metrics/product-views.md). |
| `xdm.commerce.purchases.value` | Erhöht die Metrik [Bestellungen](/help/components/metrics/orders.md). |
| `xdm.device.model` | Die Mobile-Lebenszyklusdimension [Gerätename](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.device.colorDepth` | Ermöglicht die Definition der Dimension [Farbtiefe](/help/components/dimensions/color-depth.md). |
| `xdm.device.screenHeight` | Ermöglicht die Definition der Dimension [Bildschirmauflösung.](/help/components/dimensions/monitor-resolution.md) |
| `xdm.device.screenWidth` | Ermöglicht die Definition der Dimension [Bildschirmauflösung.](/help/components/dimensions/monitor-resolution.md) |
| `xdm.device.type` | Der Mobilgerätetyp. |
| `xdm.environment.browserDetails.acceptLanguage` | Ermöglicht die Definition der Dimension [Sprache](/help/components/dimensions/language.md). |
| `xdm.environment.browserDetails.cookiesEnabled` | Definiert die Dimension [Cookie-Unterstützung](/help/components/dimensions/cookie-support.md). Gültige Werte sind `Y` (der Browser akzeptiert Cookies) und `N` (der Browser lehnt Cookies ab). |
| `xdm.environment.browserDetails.javaEnabled` | Definiert die Dimension [Java aktiviert](/help/components/dimensions/java-enabled.md). Gültige Werte sind `Y` (Java ist aktiviert) und `N` (Java ist deaktiviert). |
| `xdm.environment.browserDetails.userAgent` | Wird als Fallback-Identifizierungsmethode für [Unique Visitor](/help/components/metrics/unique-visitors.md) verwendet. Wird normalerweise unter Verwendung der HTTP-Anfrage-Kopfzeile `User-Agent` befüllt. Sie können dieses Feld einer eVar zuordnen, wenn Sie es in Berichten verwenden möchten. |
| `xdm.environment.browserDetails.viewportHeight` | Definiert die Dimension [Browser-Höhe](/help/components/dimensions/browser-height.md). |
| `xdm.environment.browserDetails.viewportWidth` | Definiert die Dimension [Browser-Breite](/help/components/dimensions/browser-width.md). |
| `xdm.environment.carrier` | Die Mobile-Lebenszyklusdimension [Anbietername](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.environment.connectionType` | Ermöglicht die Definition der Dimension [Verbindungstyp](/help/components/dimensions/connection-type.md). |
| `xdm.environment.ipV4` | Wird als Fallback-Identifizierungsmethode für [Unique Visitor](/help/components/metrics/unique-visitors.md) verwendet. Wird normalerweise unter Verwendung der HTTP-Kopfzeile `X-Forwarded-For` befüllt. |
| `xdm.environment._dc.language` | Die Mobile-Dimension „Locale“. Wird nur verwendet, wenn xdm.environment.language nicht festgelegt ist. |
| `xdm.environment.language` | Die Mobile-Dimension „Locale“. |
| `xdm.environment.operatingSystem` | Die Mobile-Lebenszyklusdimension [Betriebssystem](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm.environment.operatingSystemVersion` | Ermöglicht die Definition der Mobile-Lebenszyklusdimension [Betriebssystemversion](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/metrics/). |
| `xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar250` | Legt die entsprechende Dimension [eVar](/help/components/dimensions/evar.md) fest. |
| `xdm._experience.analytics.customDimensions.`<br/>`hierarchies.hier1`<br/>`[...]`<br/>`xdm._experience.analytics.customDImensions.`<br/>`hierarchies.hier5` | Legt die entsprechende Dimension [Hierarchie](/help/components/dimensions/hierarchy.md) fest. |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.delimiter`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.delimiter` | Außerkraftsetzen des Trennzeichens für Listen-Props. Die Verwendung dieses Felds wird nicht empfohlen, da das Trennzeichen automatisch von der [Traffic-Variablen-Verwaltung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen abgerufen wird. Die Verwendung dieses Felds kann zu einer Diskrepanz zwischen dem verwendeten Trennzeichen und dem von Analytics erwarteten Trennzeichen führen. |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.values`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.values` | Ein Zeichenfolgen-Array, das die entsprechenden [Listen-Prop](../vars/page-vars/prop.md#list-props)-Werte enthält. |
| `xdm._experience.analytics.customDimensions.`<br/>`lists.list1.list[].value`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`lists.list3.list[].value` | Verknüpft alle `value`-Zeichenfolgen im jeweiligen `list[]`-Array mit der jeweiligen [Listenvariablen](../vars/page-vars/list.md). Das Trennzeichen wird automatisch auf der Grundlage des in den [Report Suite-Einstellungen“ festgelegten Werts ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md). |
| `xdm._experience.analytics.customDimensions.`<br/>`props.prop1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`props.prop75` | Legt die entsprechende [Prop](/help/components/dimensions/prop.md)-Dimension fest. |
| `xdm._experience.analytics.event1to100.`<br/>`event1.id`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die jeweilige Metrik [Benutzerspezifische Ereignisse](/help/components/metrics/custom-events.md) an. Jede Ereignis-ID befindet sich ihrem übergeordneten 100-Gruppen-Element. Verwenden Sie beispielsweise `xdm._experience.analytics.event601to700.event678.id`, um die Serialisierung auf `event678` anzuwenden. |
| `xdm._experience.analytics.event1to100.`<br/>`event1.value`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.value` | Erhöht die jeweilige Metrik [Benutzerspezifische Ereignisse](/help/components/metrics/custom-events.md) um den gewünschten Betrag. Jedes Ereignis befindet sich in seinem übergeordneten 100-Gruppen-Element. Das Feld für `event567` ist zum Beispiel `xdm._experience.analytics.event501to600.event567.value`. |
| `xdm.identityMap.ECID[0].id` | Die [Adobe Experience Cloud Identity Service-ID](https://experienceleague.adobe.com/en/docs/id-service/using/home). |
| `xdm.marketing.trackingCode` | Definiert die Dimension [Trackingcode](/help/components/dimensions/tracking-code.md). |
| `xdm.media.mediaTimed.completes.value` | Die Metrik „Streaming-Mediendienste[ (Inhaltsbeendigung](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-complete). |
| `xdm.media.mediaTimed.dropBeforeStart.value` | `c.a.media.view`, `c.a.media.timePlayed`, `c.a.media.play` |
| `xdm.media.mediaTimed.federated.value` | Die Metrik „Streaming Media Services[ „Federated Data](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#federated-data). |
| `xdm.media.mediaTimed.firstQuartiles.value` | Die Metrik für Streaming-[ (25 % Fortschrittsmarkierung](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#twenty-five--progress-marker). |
| `xdm.media.mediaTimed.mediaSegmentView.value` | Die Metrik „Streaming Media Services[ „Inhaltssegmentansichten](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-segment-views). |
| `xdm.media.mediaTimed.midpoints.value` | Die Metrik Streaming-Mediendienste [50 % Fortschrittsmarkierung](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#progress-marker). |
| `xdm.media.mediaTimed.pauseTime.value` | Die Metrik Streaming-Mediendienste [Pausierung - ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#total-pause-duration). |
| `xdm.media.mediaTimed.pauses.value` | Die Metrik Streaming-Mediendienste [Pause-Ereignisse](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#pause-events). |
| `xdm.mediaCollection.sessionDetails.assetID` | Die Dimension Streaming-Mediendienste [Asset-ID](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#asset-id). |
| `xdm.mediaCollection.sessionDetails.friendlyName` | Die Dimension Streaming-Mediendienste [Videoname](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#video-name). |
| `xdm.mediaCollection.sessionDetails.originator` | Die Dimension Streaming-Mediendienste [Urheber](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#originator). |
| `xdm.mediaCollection.sessionDetails.episode` | Die Dimension Streaming-Mediendienste [Folge](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#episode). |
| `xdm.mediaCollection.sessionDetails.genre` | Die Dimension Streaming-Mediendienste [Genre](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#genre). |
| `xdm.mediaCollection.sessionDetails.rating` | Die Dimension Streaming-Mediendienste [Inhaltsbewertung](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-rating). |
| `xdm.mediaCollection.sessionDetails.season` | Die Dimension Streaming-Mediendienste [Staffel](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#season). |
| `xdm.mediaCollection.sessionDetails.name` | Die Dimension Streaming-Mediendienste [Inhalts-ID](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-id). |
| `xdm.mediaCollection.sessionDetails.show` | Die Dimension Streaming-Mediendienste [Anzeigen](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#show). |
| `xdm.mediaCollection.sessionDetails.showType` | Die Dimension Streaming-Mediendienste [Sendungstyp](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#show-type). |
| `xdm.mediaCollection.sessionDetails.length` | Die Dimension Streaming-Mediendienste [Videolänge](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#video-length). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.@id` | Die Dimension Streaming-Mediendienste [Mediensitzungs-ID](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#media-session-id). |
| `xdm.mediaCollection.sessionDetails.channel` | Die Dimension Streaming-Mediendienste [Inhaltskanal](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-channel). |
| `xdm.mediaCollection.sessionDetails.contentType` | Die Dimension Streaming-Mediendienste [Content-Typ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-type). |
| `xdm.mediaCollection.sessionDetails.network` | Die Dimension Streaming-Mediendienste [Netzwerk](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#network). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`mediaSegmentView.value` | Die Dimension Streaming-Medien[Services (](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-segment)). |
| `xdm.mediaCollection.sessionDetails.playerName` | Die Dimension Streaming-Mediendienste [Content-Player-Name](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-player-name). |
| `xdm.mediaCollection.sessionDetails.appVersion` | Die Dimension Streaming-Mediendienste [SDK-Version](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#sdk-version). |
| `xdm.mediaCollection.sessionDetails.feed` | Die Dimension Streaming-Mediendienste [Medien-Feed-Typ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#media-feed-type). |
| `xdm.mediaCollection.sessionDetails.streamFormat` | Die Dimension Streaming-Mediendienste [Stream-Format](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#stream-format). |
| `xdm.media.mediaTimed.progress10.value` | Die Metrik für Streaming-Mediendienste [10 % Fortschrittsmarkierung](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#ten--progress-marker). |
| `xdm.media.mediaTimed.progress95.value` | Die Metrik für Streaming-[-95 % Fortschrittsmarkierung](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#ninety-five--progress-marker). |
| `xdm.mediaCollection.sessionDetails.hasResume` | Die Metrik Streaming-Mediendienste [Inhaltswiederaufnahmen](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-resumes). |
| `xdm.media.mediaTimed.starts.value` | Die Metrik Streaming-Mediendienste [Medienstarts](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#media-starts). |
| `xdm.media.mediaTimed.thirdQuartiles.value` | Die Metrik für Streaming-[ (75 % Fortschrittsmarkierung](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#seventy-five--progress-marker). |
| `xdm.media.mediaTimed.timePlayed.value` | Die Metrik „Streaming Media Services[Besuchszeit für Inhalte](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#content-time-spent). |
| `xdm.media.mediaTimed.totalTimePlayed.value` | Die Metrik „Streaming-Medien[Services“ ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters#media-time-spent). |
| `xdm.placeContext.geo._schema.latitude` | Der Breitengrad-Standort des Besuchers. Ermöglicht die Definition [ Dimensionen für den mobilen ](/help/components/dimensions/lifecycle-dimensions.md). |
| `xdm.placeContext.geo._schema.longitude` | Die Längengrad-Position des Besuchers. Ermöglicht die Definition [ Dimensionen für den mobilen ](/help/components/dimensions/lifecycle-dimensions.md). |
| `xdm.placeContext.geo.postalCode` | Die Dimension [Postleitzahl](/help/components/dimensions/zip-code.md). |
| `xdm.placeContext.geo.stateProvince` | Die Dimension [US-Bundesstaaten](/help/components/dimensions/us-states.md). |
| `xdm.placeContext.localTime` | Erscheint in [Daten-Feeds](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) als `t_time_info`. |
| `xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar1`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar250` | Wendet die [Produktsyntax](../vars/page-vars/products.md) für das Merchandising auf eVars an. |
| `xdm.productListItems[]._experience.analytics.`<br/>`event1to100.event1.value`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`event901-1000.event1000.value` | Wendet die [Produktsyntax](../vars/page-vars/products.md) für das Merchandising auf Ereignisse an. |
| `xdm.productListItems[].productCategories[].categoryID` | Die Dimension [Kategorie](/help/components/dimensions/category.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). |
| `xdm.productListItems[].name` | Die Dimension [Produkt](/help/components/dimensions/product.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). Wenn `xdm.productListItems[].SKU` und `xdm.productListItems[].name` beide Daten enthalten, wird der Wert in `xdm.productListItems[].SKU` verwendet. |
| `xdm.productListItems[].priceTotal` | Hilft bei der Bestimmung der Metrik [Umsatz](/help/components/metrics/revenue.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). |
| `xdm.productListItems[].quantity` | Hilft bei der Bestimmung der Metrik [Einheiten](/help/components/metrics/units.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). |
| `xdm.productListItems[].SKU` | Die Dimension [Produkt](/help/components/dimensions/product.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). Wenn `xdm.productListItems[].SKU` und `xdm.productListItems[].name` beide Daten enthalten, wird der Wert in `xdm.productListItems[].SKU` verwendet. |
| `xdm.web.webInteraction.URL` | Die Implementierungsvariable [linkURL](../vars/config-vars/linkurl.md). |
| `xdm.web.webInteraction.name` | Die Dimension [Benutzerspezifischer Link](/help/components/dimensions/custom-link.md), [Downloadlink](/help/components/dimensions/download-link.md) oder [Exitlink](/help/components/dimensions/exit-link.md), je nach dem Wert in `xdm.web.webInteraction.type` |
| `xdm.web.webInteraction.type` | Bestimmt den Typ des angeklickten Links. Gültige Werte sind `other` (benutzerspezifische Links), `download` (Downloadlinks) und `exit` (Exitlinks). |
| `xdm.web.webPageDetails.URL` | Die Dimension [Seiten-URL](/help/components/dimensions/page-url.md). |
| `xdm.web.webPageDetails.isErrorPage` | Flag, das bei der Bestimmung der [Dimension](/help/components/dimensions/pages-not-found.md) und [Metrik](/help/components/metrics/pages-not-found.md) „Pages Not Found“ hilft. |
| `xdm.web.webPageDetails.name` | Die Dimension [Seite](/help/components/dimensions/page.md). |
| `xdm.web.webPageDetails.server` | Die Dimension [Server](/help/components/dimensions/server.md). |
| `xdm.web.webPageDetails.siteSection` | Die Dimension [Site-Bereich](/help/components/dimensions/site-section.md). |
| `xdm.web.webReferrer.URL` | Die Dimension [Referrer](/help/components/dimensions/referrer.md). |

{style="table-layout:auto"}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## Zuordnen anderer XDM-Felder zu Analytics-Variablen

Wenn Sie Dimensionen oder Metriken zu Adobe Analytics hinzufügen möchten, können Sie dies über &quot;[&quot; ](../vars/page-vars/contextdata.md).

### Implizite Zuordnung

Alle XDM-Feldelemente, die nicht automatisch zugeordnet werden, werden als Kontextdaten mit dem Präfix `a.x.` an Adobe Analytics gesendet. Sie können dann diese Kontextdatenvariable unter Verwendung von [Verarbeitungsregeln“ der gewünschten Analytics-](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) zuordnen. Angenommen, Sie senden das folgende Ereignis:

```js
alloy("event",{
    "xdm":{
        "_atag":{
            "search":{
                "term":"Example search term"
            }
        }
    }
})
```

Das Web SDK sendet diese Daten als die Kontextdatenvariable `a.x._atag.search.term` an Adobe Analytics. Anschließend können Sie eine Verarbeitungsregel verwenden, um den Wert dieser Kontextdatenvariablen der gewünschten Analytics-Variablen zuzuweisen, z. B. eine `eVar`:

![Suchbegriff-Verarbeitungsregel](assets/examplerule.png)

## Explizites Mapping

Sie können XDM-Feldelemente auch explizit als Kontextdaten zuordnen. Jedes XDM-Feldelement, das mithilfe des `contextData` explizit zugeordnet wird, wird als Kontextdaten ohne Präfix an Adobe Analytics gesendet. Sie können dann diese Kontextdatenvariable unter Verwendung von [Verarbeitungsregeln“ der gewünschten Analytics-](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) zuordnen. Angenommen, Sie senden das folgende Ereignis:

```js
alloy("event",{
    "xdm":{
        "_atag":{
            "analytics": {
                "contextData" : {
                    "someValue" : "1"
                }
            }
        }
    }
})
```

Web SDK sendet diese Daten an Adobe Analytics als die Kontextdatenvariable `somevalue` mit dem Wert `1`.  Anschließend können Sie eine Verarbeitungsregel verwenden, um den Wert dieser Kontextdatenvariablen der gewünschten Analytics-Variablen zuzuweisen, z. B. eine `eVar`:

![Suchbegriff-Verarbeitungsregel](assets/examplerule-explicit.png)
