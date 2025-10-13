---
title: trackingServerSecure
description: Die Domain, die zum Senden von Daten über HTTPS an Adobe verwendet wird.
feature: Appmeasurement Implementation
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
role: Admin, Developer
source-git-commit: 7918b18e73618368543a996ca121b64b7afb33ab
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 13%

---

# trackingServerSecure

Die `trackingServerSecure` bestimmt die Domain, die AppMeasurement verwendet, um Daten über HTTPS an Adobe zu senden. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

Vor dem [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/de/docs/id-service/using/home) bestimmte diese Variable auch, wo Drittanbieter-Cookies gesetzt wurden. Adobe empfiehlt dringend, nach Möglichkeit den ID-Service in allen Implementierungen zu verwenden.

## Edge-Domain unter Verwendung der Web-SDK-Erweiterung

Die Web-SDK verwendet die [!UICONTROL Edge]Domain, um sowohl den Tracking-Server als auch den sicheren Tracking-Server zu verarbeiten. Sie können den gewünschten Wert für die [!UICONTROL Edge-Domain] beim Konfigurieren der Web-SDK-Erweiterung festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Wählen Sie die gewünschte Tag-Eigenschaft aus.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und wählen Sie dann die Schaltfläche **[!UICONTROL Konfigurieren]** unter [!UICONTROL Adobe Experience Platform Web SDK] aus.
1. Legen Sie das gewünschte Textfeld **[!UICONTROL Edge Domain]** fest.

Weitere Informationen [&#x200B; Sie in der Web](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=de)SDK-Dokumentation unter „Konfigurieren der Adobe Experience Platform WebSDKErweiterung“.

>[!TIP]
>
>Wenn Ihr Unternehmen von einer AppMeasurement- oder Analytics-Erweiterungsimplementierung zum Web SDK wechselt, kann dieses Feld denselben in `trackingServerSecure` (oder `trackingServer`) enthaltenen Wert verwenden.

## Edge-Domain - Manuelle Implementierung der Web-SDK

Konfigurieren Sie die SDK mithilfe von [`edgeDomain`](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/edgedomain). Das Feld ist eine Zeichenfolge, die die Domain bestimmt, an die Daten gesendet werden sollen.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## SSL-Tracking-Server mit der Adobe Analytics-Erweiterung

[!UICONTROL SSL-Tracking-Server] ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Wählen Sie die gewünschte Tag-Eigenschaft aus.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter &quot;Adobe Analytics **[!UICONTROL auf]** Konfigurieren“.
1. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL SSL-Tracking-Server] angezeigt wird.

Wenn dieses Feld leer gelassen wird, wird standardmäßig der Wert in [!UICONTROL Tracking Server] verwendet. Wenn sowohl [!UICONTROL SSL-Tracking] als auch [!UICONTROL Tracking-Server] leer sind, wird standardmäßig `[rsid].data.adobedc.net` verwendet.

## s.trackingServerSecure in AppMeasurement und der benutzerdefinierte Code-Editor der Analytics-Erweiterung

Die `s.trackingServerSecure` ist eine Zeichenfolge, die die Domain enthält, an die Daten an Adobe gesendet werden sollen. Nur Domain; Protokoll, Pfad, Port und Schrägstriche auslassen. Wenn diese Variable leer ist, verwendet sie den Wert in der `s.trackingServer`. Wenn sowohl `s.trackingServerSecure` als auch `s.trackingServer` leer sind, wird standardmäßig `[rsid].2o7.net` verwendet.

```js
// Example value when participating in the Adobe-managed certificate program
s.trackingServerSecure = "data.example.com";

// Example value sending data directly to Adobe
s.trackingServerSecure = "example.data.adobedc.net";
```

## Überlegungen zur Bestimmung des Werts für `trackingServerSecure`

Der Wert, den Sie für die `trackingServerSecure` (oder `edgeDomain`) verwenden, hängt von mehreren Faktoren ab:

* Ihre Teilnahme am [Adobe-Managed Certificate Program](https://experienceleague.adobe.com/de/docs/core-services/interface/data-collection/adobe-managed-cert)
* Wenn Sie den [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/de/docs/id-service/using/home) implementiert und ordnungsgemäß eingerichtet haben

**Wenn Ihr Unternehmen am Adobe-Managed Certificate Program teilnimmt** setzen Sie den Wert auf die Erstanbieter-Domain, die beim Einrichten des Zertifikats ausgewählt wurde. Normalerweise ist dieser Wert eine Subdomain, die Ihrem Unternehmen gehört. Beispiel: `data.example.com`. CNAME-Datensätze in Ihrem Unternehmen leiten diese Daten an Adobe weiter.

**Wenn Sie nicht am Zertifikatprogramm teilnehmen** setzen Sie den Wert auf eine Subdomain von `data.adobedc.net`. Adobe empfiehlt, aus Konsistenzgründen die Unternehmens-ID Ihres Unternehmens zu verwenden. Beispiel: `example.data.adobedc.net`. Gehen Sie wie folgt vor, um Ihre Unternehmens-ID zu ermitteln:

1. Melden Sie sich mit Ihren Adobe ID[Anmeldeinformationen bei &#x200B;](https://experience.adobe.com)experience.adobe.com) an.
1. Drücken Sie an einer beliebigen Stelle in der Experience Cloud-Benutzeroberfläche `[Cmd]` + `[I]` (iOS) oder `[Ctrl]` + `[I]` (Windows).
1. Ein **[!UICONTROL User Data Debugger]** wird angezeigt. Wählen Sie die **[!UICONTROL Zugewiesene Organisationen]** aus.
1. Erweitern Sie die gewünschte IMS-Organisation.
1. Suchen Sie das Feld **[!UICONTROL Mandant]** . Dieser Wert ist die empfohlene Subdomain von `data.adobedc.net`.

>[!NOTE]
>
>Verwenden Sie keine Subdomänen, die tiefer als `example.data.adobedc.net` gehen. Zum Beispiel ist `custom.example.data.adobedc.net` kein gültiger Trackingserver.

Ältere Implementierungen haben möglicherweise Werte wie `sc.omtrdc.net` oder `2o7.net`. Diese wurden hauptsächlich in früheren Versionen von Adobe Analytics verwendet, sind aber noch gültig.

Adobe empfiehlt dringend, diese Informationen in einem [Lösungs-Design-Dokument](../../prepare/solution-design.md) zu speichern, um die Konsistenz in Ihrem gesamten Unternehmen zu gewährleisten.

## Auswirkungen der Nichtverwendung des Besucher-ID-Service

Adobe empfiehlt dringend, in allen Implementierungen den [Adobe Experience Cloud Identity &#x200B;](https://experienceleague.adobe.com/de/docs/id-service/using/home)Service) zu verwenden. Der ID-Service kann auf verschiedene Weise implementiert werden:

* Manuelle AppMeasurement-Implementierungen verwenden `VisitorAPI.js` und rufen die `getInstance`-Methode auf. Weitere [&#x200B; finden Sie unter „Implementieren des Experience Cloud Identity &#x200B;](https://experienceleague.adobe.com/de/docs/id-service/using/implementation/setup-analytics) für Analytics“.
* Implementierungen, die die Adobe Analytics-Tag-Erweiterung verwenden, verwenden die [Tag-Erweiterung des Adobe Experience Cloud ID-](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/id-service/overview). Nach dem Hinzufügen ist keine zusätzliche Konfiguration erforderlich.
* Bei Implementierungen, bei denen eine beliebige Form der Web-SDK (`alloy.js` oder die Web-SDK-Tag-Erweiterung) verwendet wird, ist der ID-Service bereits nativ integriert. Außer dem Festlegen des `edgeDomain` ist keine Konfiguration erforderlich.

**Wenn Ihre Implementierung den Identity Service nicht verwendet** sollten Sie die folgenden Auswirkungen auf Ihre Implementierung berücksichtigen:

* Wenn der Identity Service nicht verwendet wird, bestimmt `trackingServerSecure` den Cookie-Speicherort. Wenn Sie diese Variable auf eine Domain eines Drittanbieters setzen, muss AppMeasurement ein Ausweich-Cookie verwenden, da die meisten modernen Browser Cookies von Drittanbietern ablehnen.
* Internes Linktracking und Activity Map sind möglicherweise weniger zuverlässig.
