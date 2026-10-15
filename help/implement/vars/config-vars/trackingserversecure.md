---
title: trackingServerSecure
description: Die Domain, die zum Senden von Daten über HTTPS an Adobe verwendet wird.
feature: Appmeasurement Implementation
exl-id: d5b112f9-f3f6-43ac-8ee5-d9ad8062e380
role: Admin, Developer
TQID: https://experienceleague.adobe.com/8-M-5apvXuUfQyxdd4Es8Lr5LkgXPK2UNHrhpTzT8xE
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
  - id: df312454-73c4-43f6-a90e-18f5043f074c
    internal-label: Tags
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 832a3752ab758d573e5b15b2dc38dad120fe8300
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 11%
---
# trackingServerSecure

Die `trackingServerSecure` bestimmt die Domain, die AppMeasurement verwendet, um Daten über HTTPS an Adobe zu senden. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

>[!NOTE]
>
>[`trackingServer`](configuration-variables.md#retired-configuration-variables) ist eine eingestellte Variante dieser Variablen. Sie spezifizierte die Domain für über HTTP gesendete Daten. Da HTTPS weit verbreitet ist, sollte stattdessen `trackingServerSecure` verwendet werden. Wenn `s.trackingServerSecure` leer ist, kehrt AppMeasurement auf den `s.trackingServer` Wert zurück.

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

Konfigurieren Sie die SDK mithilfe von [`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/edgedomain). Das Feld ist eine Zeichenfolge, die die Domain bestimmt, an die Daten gesendet werden sollen.

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
// Example value when using a first-party domain
s.trackingServerSecure = "data.example.com";

// Example value when using a third-party domain
s.trackingServerSecure = "example.data.adobedc.net";
```

## Überlegungen zur Bestimmung des Werts für `trackingServerSecure`

Der Wert, den Sie für die `trackingServerSecure` (oder `edgeDomain`) verwenden, hängt davon ab, wie Ihr Unternehmen Daten an Adobe sendet:

* **Wenn Ihr Unternehmen eine Erstanbieterdomäne verwendet** z. B. über das [Adobe-Managed Certificate Program](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/adobe-managed-cert), ein [Customer-Managed Certificate](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/customer-managed-cert) oder ein [Content Delivery Network (CDN)](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cdn), setzen Sie den Wert auf diese Domain. Beispiel: `data.example.com`.
* **Wenn Ihr Unternehmen eine Domain eines Drittanbieters verwendet** setzen Sie den Wert auf Ihre Mandanten-ID-Subdomain von `data.adobedc.net`. Beispiel: `example.data.adobedc.net`.

Einzelheiten zu [&#x200B; einzelnen Optionen, einschließlich der Suche nach &#x200B;](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/collection-domain) Mandanten-ID, finden Sie unter „Auswählen einer Datenerfassungs-Domain“ im Handbuch für die Benutzeroberfläche und Administration von CX Enterprise.

Adobe empfiehlt dringend, diese Informationen in einem [Lösungs-Design-Dokument](../../prepare/solution-design.md) zu speichern, um die Konsistenz in Ihrem gesamten Unternehmen zu gewährleisten.

## Auswirkungen der Nichtverwendung des Besucher-ID-Service oder Experience Platform Identity Services

Adobe empfiehlt dringend, in allen Implementierungen ECID als primäre Form der Besucheridentität zu verwenden. Die Erfassung von ECIDs kann je nach Implementierungstyp auf verschiedene Arten implementiert werden:

* Manuelle AppMeasurement-Implementierungen verwenden `VisitorAPI.js` und rufen die `getInstance`-Methode auf. Weitere [&#x200B; finden Sie unter „Implementieren des Besucher-ID](https://experienceleague.adobe.com/en/docs/id-service/using/implementation/setup-analytics)Service für Analytics“.
* Implementierungen, die die Adobe Analytics-Tag-Erweiterung verwenden, verwenden die [[!UICONTROL Experience Cloud ID Service]-Tag-Erweiterung](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview), die den Besucher-ID-Service implementiert. Nach dem Hinzufügen ist keine zusätzliche Konfiguration erforderlich.
* Implementierungen, die eine beliebige Form der Web-SDK (`alloy.js` oder die Web-SDK-Tag-Erweiterung) verwenden, schließen automatisch den Experience Platform Identity Service ein. Außer dem Festlegen des `edgeDomain` ist keine Konfiguration erforderlich.

**Wenn Ihre Implementierung keine ECIDs verwendet** sollten Sie die folgenden Auswirkungen auf Ihre Implementierung berücksichtigen:

* Wenn Sie den Besucher-ID-Dienst oder Experience Platform Identity Service nicht verwenden, bestimmt `trackingServerSecure` den Cookie-Speicherort. Wenn Sie diese Variable auf eine Domain eines Drittanbieters setzen, muss AppMeasurement ein Ausweich-Cookie verwenden, da die meisten modernen Browser Cookies von Drittanbietern ablehnen.
* Internes Linktracking und Activity Map sind möglicherweise weniger zuverlässig.
