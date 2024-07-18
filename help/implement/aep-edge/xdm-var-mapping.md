---
title: Zuordnung von XDM-Objektvariablen zu Adobe Analytics
description: Erfahren Sie, welche XDM-Felder in Edge automatisch Analytics-Variablen zugeordnet werden.
exl-id: fbff5c38-0f04-4780-b976-023e207023c6
feature: Implementation Basics
role: Admin, Developer
source-git-commit: 4633225cc35658a7de39a40cd77df00137a54461
workflow-type: tm+mt
source-wordcount: '1414'
ht-degree: 56%

---

# Zuordnung von XDM-Objektvariablen zu Adobe Analytics

Die folgende Tabelle zeigt die XDM-Variablen, die das Adobe Experience Platform-Edge Network automatisch Adobe Analytics zuordnet. Wenn Sie diese XDM-Feldpfade verwenden, ist keine zusätzliche Konfiguration erforderlich, um Daten an Adobe Analytics zu senden. Diese Felder sind in der Feldergruppe **[!UICONTROL Adobe Analytics ExperienceEvent Template]** enthalten. Die Verwendung dieser Felder wird empfohlen, wenn Sie Daten an Adobe Analytics und Adobe Experience Platform senden möchten.

Wenn Ihr Unternehmen plant, zu Customer Journey Analytics zu wechseln, empfiehlt Adobe stattdessen die Verwendung des `data` -Objekts, um Daten direkt an Adobe Analytics zu senden, ohne einem Schema zu entsprechen. Diese Strategie ermöglicht es Ihrem Unternehmen, Ihr eigenes Schema zu verwenden, anstatt die [!UICONTROL Adobe Analytics ExperienceEvent-Vorlage] zu verwenden (was weniger auf Customer Journey Analytics anwendbar ist). Eine ähnliche Zuordnungstabelle finden Sie unter [Zuordnung von Datenobjektvariablen zu Adobe Analytics](data-var-mapping.md) .

## Wertprioritäten

Die meisten XDM-Objektfelder in dieser Tabelle entsprechen einem [Datenobjektfeld](data-var-mapping.md). Wenn Sie sowohl ein bestimmtes XDM-Objektfeld als auch das entsprechende Datenobjektfeld festlegen, hat das Datenobjektfeld Priorität. Wenn Sie sowohl das XDM-Objektfeld als auch das Datenobjektfeld verwenden, empfiehlt Adobe, benutzerdefinierte Ereignisse mithilfe des Datenobjektfelds festzulegen. Wenn das Feld `data.__adobe.analytics.events` vorhanden ist, werden alle XDM-Objektfelder, die mit Commerce- und benutzerspezifischen Ereignissen verknüpft sind, überschrieben.

## XDM-Objektfeldzuordnung

Vorherige Aktualisierungen dieser Tabelle finden Sie auf der Seite [Commit-Verlauf auf GitHub](https://github.com/AdobeDocs/analytics.en/commits/main/help/implement/aep-edge/xdm-var-mapping.md).

| XDM-Feldpfad | Analytics-Variable und -Beschreibung |
| --- | --- |
| `xdm.application.isClose` | Ermöglicht die Definition der Mobile-Lebenszyklusmetrik [Crashes](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.isInstall` | Hilft bei der Bestimmung, wann die Mobile-Lebenszyklusmetrik [Erste Starts](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/) erhöht werden soll. |
| `xdm.application.closeType` | Bestimmt, ob ein Schließen-Ereignis ein Absturz ist oder nicht. Gültige Werte sind `close` (eine Lebenszyklussitzung endet und ein Pausenereignis wurde für die vorherige Sitzung empfangen) und `unknown` (eine Lebenszyklussitzung endet ohne Pausenereignis). Ermöglicht die Definition der Mobile-Lebenszyklusmetrik [Crashes](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.isInstall` | Die Mobile-Lebenszyklusmetrik [Installationen](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.isLaunch` | Die Mobile-Lebenszyklusmetrik [Starts](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.name` | Ermöglicht die Definition der Mobile-Lebenszyklusdimension [App-ID](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.isUpgrade` | Die Mobile-Lebenszyklusmetrik [Upgrades](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.version` | Ermöglicht die Definition der Mobile-Lebenszyklusdimension [App-ID](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.application.sessionLength` | Die Mobile-Lebenszyklusmetrik [Länge der vorherigen Sitzung](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.commerce.checkouts.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Checkouts](../../components/metrics/checkouts.md) an. |
| `xdm.commerce.checkouts.value` | Inkrementiert die Metrik [Checkouts](../../components/metrics/checkouts.md) um den gewünschten Wert. |
| `xdm.commerce.order.currencyCode` | Definiert die Konfigurationsvariable [currencyCode](../vars/config-vars/currencycode.md). |
| `xdm.commerce.order.purchaseID` | Definiert die Seitenvariable [purchaseID](../vars/page-vars/purchaseid.md). |
| `xdm.commerce.order.payments[0].transactionID` | Legt die Seitenvariable [transactionID](../vars/page-vars/transactionid.md) fest. |
| `xdm.commerce.productListAdds.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkorbhinzufügungen](../../components/metrics/cart-additions.md) an. |
| `xdm.commerce.productListAdds.value` | Erhöht die Metrik [Warenkorbhinzufügungen](../../components/metrics/cart-additions.md). |
| `xdm.commerce.productListOpens.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkörbe](../../components/metrics/carts.md) an. |
| `xdm.commerce.productListOpens.value` | Erhöht die Metrik [Warenkörbe](../../components/metrics/carts.md). |
| `xdm.commerce.productListRemovals.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkorbentnahmen](../../components/metrics/cart-removals.md) an. |
| `xdm.commerce.productListRemovals.value` | Erhöht die Metrik [Warenkorbentnahmen](../../components/metrics/cart-removals.md). |
| `xdm.commerce.productListViews.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkorbansichten](../../components/metrics/cart-views.md) an. |
| `xdm.commerce.productListViews.value` | Erhöht die Metrik [Warenkorbansichten](../../components/metrics/cart-views.md). |
| `xdm.commerce.productViews.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Produktansichten](../../components/metrics/product-views.md) an. |
| `xdm.commerce.productViews.value` | Erhöht die Metrik [Produktansichten](../../components/metrics/product-views.md). |
| `xdm.commerce.purchases.value` | Erhöht die Metrik [Bestellungen](../../components/metrics/orders.md). |
| `xdm.device.model` | Die Mobile-Lebenszyklusdimension [Gerätename](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.device.colorDepth` | Ermöglicht die Definition der Dimension [Farbtiefe](../../components/dimensions/color-depth.md). |
| `xdm.device.screenHeight` | Ermöglicht die Definition der Dimension [Bildschirmauflösung.](../../components/dimensions/monitor-resolution.md) |
| `xdm.device.screenWidth` | Ermöglicht die Definition der Dimension [Bildschirmauflösung.](../../components/dimensions/monitor-resolution.md) |
| `xdm.device.type` | Der Mobilgerätetyp. |
| `xdm.environment.browserDetails.acceptLanguage` | Ermöglicht die Definition der Dimension [Sprache](../../components/dimensions/language.md). |
| `xdm.environment.browserDetails.cookiesEnabled` | Definiert die Dimension [Cookie-Unterstützung](../../components/dimensions/cookie-support.md). Gültige Werte sind `Y` (der Browser akzeptiert Cookies) und `N` (der Browser lehnt Cookies ab). |
| `xdm.environment.browserDetails.javaEnabled` | Definiert die Dimension [Java aktiviert](../../components/dimensions/java-enabled.md). Gültige Werte sind `Y` (Java ist aktiviert) und `N` (Java ist deaktiviert). |
| `xdm.environment.browserDetails.userAgent` | Wird als Fallback-Identifizierungsmethode für [Unique Visitor](../../components/metrics/unique-visitors.md) verwendet. Wird normalerweise unter Verwendung der HTTP-Anfrage-Kopfzeile `User-Agent` befüllt. Sie können dieses Feld einer eVar zuordnen, wenn Sie es in Berichten verwenden möchten. |
| `xdm.environment.browserDetails.viewportHeight` | Definiert die Dimension [Browser-Höhe](../../components/dimensions/browser-height.md). |
| `xdm.environment.browserDetails.viewportWidth` | Definiert die Dimension [Browser-Breite](../../components/dimensions/browser-width.md). |
| `xdm.environment.carrier` | Die Mobile-Lebenszyklusdimension [Anbietername](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.environment.connectionType` | Ermöglicht die Definition der Dimension [Verbindungstyp](../../components/dimensions/connection-type.md). |
| `xdm.environment.ipV4` | Wird als Fallback-Identifizierungsmethode für [Unique Visitor](../../components/metrics/unique-visitors.md) verwendet. Wird normalerweise unter Verwendung der HTTP-Kopfzeile `X-Forwarded-For` befüllt. |
| `xdm.environment.language` | Die Mobile-Dimension „Locale“. |
| `xdm.environment.operatingSystem` | Die Mobile-Lebenszyklusdimension [Betriebssystem](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm.environment.operatingSystemVersion` | Ermöglicht die Definition der Mobile-Lebenszyklusdimension [Betriebssystemversion](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/metrics/). |
| `xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`eVars.eVar250` | Legt die entsprechende Dimension [eVar](../../components/dimensions/evar.md) fest. |
| `xdm._experience.analytics.customDimensions.`<br/>`hierarchies.hier1`<br/>`[...]`<br/>`xdm._experience.analytics.customDImensions.`<br/>`hierarchies.hier5` | Legt die entsprechende Dimension [Hierarchie](/help/components/dimensions/hierarchy.md) fest. |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.delimiter`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.delimiter` | Außerkraftsetzen des Trennzeichens für Listen-Props. Die Verwendung dieses Felds wird nicht empfohlen, da das Trennzeichen automatisch von der [Traffic-Variablen-Verwaltung](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) in den Report Suite-Einstellungen abgerufen wird. Die Verwendung dieses Felds kann zu einer Diskrepanz zwischen dem verwendeten Trennzeichen und dem von Analytics erwarteten Trennzeichen führen. |
| `xdm._experience.analytics.customDimensions.`<br/>`listProps.prop1.values`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`listProps.prop75.values` | Ein Zeichenfolgen-Array, das die entsprechenden [Listen-Prop](../vars/page-vars/prop.md#list-props)-Werte enthält. |
| `xdm._experience.analytics.customDimensions.`<br/>`lists.list1.list[].value`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`lists.list3.list[].value` | Verknüpft alle `value`-Zeichenfolgen im jeweiligen `list[]`-Array mit der jeweiligen [Listenvariablen](../vars/page-vars/list.md). Das Trennzeichen wird automatisch auf der Grundlage des in den [Report Suite-Einstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md) definierten Werts ausgewählt. |
| `xdm._experience.analytics.customDimensions.`<br/>`props.prop1`<br/>`[...]`<br/>`xdm._experience.analytics.customDimensions.`<br/>`props.prop75` | Legt die entsprechende [Prop](../../components/dimensions/prop.md)-Dimension fest. |
| `xdm._experience.analytics.event1to100.`<br/>`event1.id`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die jeweilige Metrik [Benutzerspezifische Ereignisse](../../components/metrics/custom-events.md) an. Jede Ereignis-ID befindet sich ihrem übergeordneten 100-Gruppen-Element. Verwenden Sie beispielsweise `xdm._experience.analytics.event601to700.event678.id`, um die Serialisierung auf `event678` anzuwenden. |
| `xdm._experience.analytics.event1to100.`<br/>`event1.value`<br/>`[...]`<br/>`xdm._experience.analytics.event901to1000.`<br/>`event1000.value` | Erhöht die jeweilige Metrik [Benutzerspezifische Ereignisse](../../components/metrics/custom-events.md) um den gewünschten Betrag. Jedes Ereignis befindet sich in seinem übergeordneten 100-Gruppen-Element. Das Feld für `event567` ist zum Beispiel `xdm._experience.analytics.event501to600.event567.value`. |
| `xdm.identityMap.ECID[0].id` | Die [Adobe Experience Cloud Identity Service-ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de). |
| `xdm.marketing.trackingCode` | Definiert die Dimension [Trackingcode](../../components/dimensions/tracking-code.md). |
| `xdm.media.mediaTimed.completes.value` | Die Metrik für Streaming-Medien [Inhaltsbeendigung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-complete). |
| `xdm.media.mediaTimed.dropBeforeStart.value` | `c.a.media.view`, `c.a.media.timePlayed`, `c.a.media.play` |
| `xdm.media.mediaTimed.federated.value` | Die Metrik für Streaming-Medien [Federated Data](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#federated-data). |
| `xdm.media.mediaTimed.firstQuartiles.value` | Die Streaming-Medien-Metrik [5 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#twenty-five-progress-marker). |
| `xdm.media.mediaTimed.mediaSegmentView.value` | Die Metrik für Streaming-Medien [Ansichten des Inhaltssegments](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-segment-views). |
| `xdm.media.mediaTimed.midpoints.value` | Die Streaming-Medien-Metrik [50 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#fifty-progress-marker). |
| `xdm.media.mediaTimed.pauseTime.value` | Die Metrik für Streaming-Medien [Pausierung - Gesamtdauer ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#total-pause-duration). |
| `xdm.media.mediaTimed.pauses.value` | Die Streaming-Medien-Metrik [Pausenereignisse](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#pause-events). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`@id` | Die Dimension für Streaming-Medien [Asset-ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#asset-id). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`dc:title` | Die Dimension für Streaming-Medien [Videoname](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#video-name). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Creator[N].iptc4xmpExt:Name` | Die Dimension für Streaming-Medien [Urheber](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#originator). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Episode.iptc4xmpExt:Number` | Die Dimension für Streaming-Medien [Folge](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#episode). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Genre` | Die Dimension für Streaming-Medien [Genre](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#genre). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Rating[N].iptc4xmpExt:RatingValue` | Die Dimension &quot;Streaming-Medien&quot;[Inhaltsbewertung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-rating). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Season.iptc4xmpExt:Number` | Die Dimension für Streaming-Medien [Staffel](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#season). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Identifier` | Die Dimension für Streaming-Medien [Inhalts-ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-id). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Name` | Die Dimension &quot;Streaming-Medien&quot;[Anzeigen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#show). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`showType` | Die Dimension für Streaming-Medien [Show Type](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#show-type). |
| `xdm.media.mediaTimed.primaryAssetReference.`<br/>`xmpDM:duration` | Die Dimension für Streaming-Medien [Videolänge](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#video-length). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`@id` | Die Dimension für Streaming-Medien [Mediensitzungs-ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#media-session-id). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastChannel` | Die Dimension für Streaming-Medien [Inhaltskanal](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-channel). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastContentType` | Die Dimension für Streaming-Medien [Content-Typ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-type). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastNetwork` | Die Dimension für Streaming-Medien [Netzwerk](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#network). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`mediaSegmentView.value` | Die Dimension für Streaming-Medien [Inhaltssegment](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-segment). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`playerName` | Die Dimension für Streaming-Medien [Inhalts-Player-Name](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-player-name). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`playerSDKVersion.version` | Die Dimension &quot;Streaming-Medien&quot;[SDK-Version](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#sdk-version). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`sourceFeed` | Die Dimension für Streaming-Medien [Medien-Feed-Typ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#media-feed-type). |
| `xdm.media.mediaTimed.primaryAssetViewDetails.`<br/>`streamFormat` | Die Dimension für Streaming-Medien [Stream-Format](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#stream-format). |
| `xdm.media.mediaTimed.progress10.value` | Die Streaming-Medien-Metrik [10 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#ten-progress-marker). |
| `xdm.media.mediaTimed.progress95.value` | Die Streaming-Medien-Metrik [95 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#ninety-five-progress-marker). |
| `xdm.media.mediaTimed.resumes.value` | Die Metrik für Streaming-Medien [Inhaltswiederaufnahmen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-resumes). |
| `xdm.media.mediaTimed.starts.value` | Die Metrik für Streaming-Medien [Medienstarts](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#media-starts). |
| `xdm.media.mediaTimed.thirdQuartiles.value` | Die Streaming-Medien-Metrik [75 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#seventy-five-progress-marker). |
| `xdm.media.mediaTimed.timePlayed.value` | Die Metrik für Streaming-Medien [Besuchszeit für Inhalt](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-time-spent). |
| `xdm.media.mediaTimed.totalTimePlayed.value` | Die Metrik für Streaming-Medien [Besuchszeit für Medien](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#media-time-spent). |
| `xdm.placeContext.geo._schema.latitude` | Die Position des Besuchers im Breitengrad. Hilft bei der Festlegung von [Standort des mobilen Lebenszyklus](/help/components/dimensions/lifecycle-dimensions.md) -Dimensionen. |
| `xdm.placeContext.geo._schema.longitude` | Der Längengrad des Besuchers. Hilft bei der Festlegung von [Standort des mobilen Lebenszyklus](/help/components/dimensions/lifecycle-dimensions.md) -Dimensionen. |
| `xdm.placeContext.geo.postalCode` | Die Dimension [Postleitzahl](../../components/dimensions/zip-code.md). |
| `xdm.placeContext.geo.stateProvince` | Die Dimension [US-Bundesstaaten](../../components/dimensions/us-states.md). |
| `xdm.placeContext.localTime` | Erscheint in [Daten-Feeds](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) als `t_time_info`. |
| `xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar1`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar250` | Wendet die [Produktsyntax](../vars/page-vars/products.md) für das Merchandising auf eVars an. |
| `xdm.productListItems[]._experience.analytics.`<br/>`event1to100.event1.value`<br/>`[...]`<br/>`xdm.productListItems[]._experience.analytics.`<br/>`event901-1000.event1000.value` | Wendet die [Produktsyntax](../vars/page-vars/products.md) für das Merchandising auf Ereignisse an. |
| `xdm.productListItems[].productCategories[].categoryID` | Die Dimension [Kategorie](../../components/dimensions/category.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). |
| `xdm.productListItems[].name` | Die Dimension [Produkt](../../components/dimensions/product.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). Wenn `xdm.productListItems[].SKU` und `xdm.productListItems[].name` beide Daten enthalten, wird der Wert in `xdm.productListItems[].SKU` verwendet. |
| `xdm.productListItems[].priceTotal` | Hilft bei der Bestimmung der Metrik [Umsatz](../../components/metrics/revenue.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). |
| `xdm.productListItems[].quantity` | Hilft bei der Bestimmung der Metrik [Einheiten](../../components/metrics/units.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). |
| `xdm.productListItems[].SKU` | Die Dimension [Produkt](../../components/dimensions/product.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). Wenn `xdm.productListItems[].SKU` und `xdm.productListItems[].name` beide Daten enthalten, wird der Wert in `xdm.productListItems[].SKU` verwendet. |
| `xdm.web.webInteraction.URL` | Die Implementierungsvariable [linkURL](../vars/config-vars/linkurl.md). |
| `xdm.web.webInteraction.name` | Die Dimension [Benutzerspezifischer Link](../../components/dimensions/custom-link.md), [Downloadlink](../../components/dimensions/download-link.md) oder [Exitlink](../../components/dimensions/exit-link.md), je nach dem Wert in `xdm.web.webInteraction.type` |
| `xdm.web.webInteraction.type` | Bestimmt den Typ des angeklickten Links. Gültige Werte sind `other` (benutzerspezifische Links), `download` (Downloadlinks) und `exit` (Exitlinks). |
| `xdm.web.webPageDetails.URL` | Die Dimension [Seiten-URL](../../components/dimensions/page-url.md). |
| `xdm.web.webPageDetails.isErrorPage` | Flag, das bei der Bestimmung der [Dimension](../../components/dimensions/pages-not-found.md) und [Metrik](../../components/metrics/pages-not-found.md) „Pages Not Found“ hilft. |
| `xdm.web.webPageDetails.name` | Die Dimension [Seite](../../components/dimensions/page.md). |
| `xdm.web.webPageDetails.server` | Die Dimension [Server](../../components/dimensions/server.md). |
| `xdm.web.webPageDetails.siteSection` | Die Dimension [Site-Bereich](../../components/dimensions/site-section.md). |
| `xdm.web.webReferrer.URL` | Die Dimension [Referrer](../../components/dimensions/referrer.md). |

{style="table-layout:auto"}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## Zuordnen anderer XDM-Felder zu Analytics-Variablen

Wenn es Dimensionen oder Metriken gibt, die Sie zu Adobe Analytics hinzufügen möchten, können Sie dies über [Kontextdatenvariablen](../vars/page-vars/contextdata.md) tun.

### Implizite Zuordnung

Alle XDM-Feldelemente, die nicht automatisch zugeordnet werden, werden als Kontextdaten mit dem Präfix `a.x.` an Adobe Analytics gesendet. Sie können diese Kontextdatenvariable dann mithilfe von [Verarbeitungsregeln](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html?lang=de) der gewünschten Analytics-Variablen zuordnen. Angenommen, Sie senden das folgende Ereignis:

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

Das Web SDK sendet diese Daten als die Kontextdatenvariable `a.x._atag.search.term` an Adobe Analytics. Anschließend können Sie eine Verarbeitungsregel verwenden, um diesen Wert der Kontextdatenvariablen der gewünschten Analytics-Variablen zuzuweisen, z. B. &quot;`eVar`&quot;:

![Suchbegriff-Verarbeitungsregel](assets/examplerule.png)

## Explizites Mapping

Sie können XDM-Feldelemente auch explizit als Kontextdaten zuordnen. Jedes XDM-Feldelement, das explizit mithilfe des Elements `contextData` zugeordnet ist, wird als Kontextdaten ohne Präfix an Adobe Analytics gesendet. Sie können dann diese Kontextdatenvariable unter Verwendung von [Verarbeitungsregeln](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html?lang=de) der gewünschten Analytics-Variablen zuordnen. Angenommen, Sie senden das folgende Ereignis:

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

Das Web SDK sendet diese Daten als Kontextdatenvariable `somevalue` mit dem Wert `1` an Adobe Analytics.  Anschließend können Sie eine Verarbeitungsregel verwenden, um diesen Wert der Kontextdatenvariablen der gewünschten Analytics-Variablen zuzuweisen, z. B. &quot;`eVar`&quot;:

![Suchbegriff-Verarbeitungsregel](assets/examplerule-explicit.png)
