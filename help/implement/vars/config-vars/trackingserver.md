---
title: trackingServer
description: Stellen Sie fest, an welcher Position Bildanforderungen gesendet werden.
feature: Variables
exl-id: bcc23286-4dd5-45ac-ac6f-7b60e95cb798
role: Admin, Developer
source-git-commit: 284f121428ce9d682b42309dd85cfd117285a7e5
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 52%

---

# trackingServer

Adobe erfasst Daten auf Ihrer Website, indem es eine vom Besucher generierte Bildanforderung empfängt. Die `trackingServer`-Variable bestimmt die Position, an der eine Bildanforderung gesendet wird. Wenn diese Variable nicht richtig definiert ist, kann es bei Ihrer Implementierung zu Datenverlusten kommen.

>[!WARNING]
>
>Wenn Sie diesen Wert ändern, sucht AppMeasurement an einer anderen Stelle nach Cookies. Die Zahl der Unique Visitors kann bei der Berichterstellung vorübergehend zu Spitzenwerten führen, da Besucher-Cookies an der neuen Position gesetzt werden.

## Edge-Domäne mit der Web SDK-Erweiterung

Das Web SDK verwendet [!UICONTROL Edge-Domäne] zur Verarbeitung von Tracking-Server und Secure Tracking Server. Sie können die gewünschte [!UICONTROL Edge-Domäne] Wert beim Konfigurieren der Web SDK-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Navigieren Sie zu [!UICONTROL Erweiterungen] und klicken Sie auf die **[!UICONTROL Konfigurieren]** Schaltfläche unter [!UICONTROL Adobe Experience Platform Web SDK].
1. Legen Sie die gewünschte **[!UICONTROL Edge-Domäne]** Textfeld.

Siehe [Konfigurieren der Adobe Experience Platform Web SDK-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=de) in der Web SDK-Dokumentation finden Sie weitere Informationen.

>[!TIP]
>
>Wenn Ihr Unternehmen von einer AppMeasurement- oder Analytics-Erweiterungsimplementierung zum Web SDK wechselt, kann dieses Feld denselben Wert verwenden, der in `trackingServerSecure` (oder `trackingServer`).

## Edge-Domäne, die das Web SDK manuell implementiert

SDK mit konfigurieren [`edgeDomain`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de). Das Feld ist eine Zeichenfolge, die die Domäne bestimmt, an die Daten gesendet werden sollen.

```json
alloy("configure", {
  "edgeDomain": "data.example.com"
});
```

## Tracking-Server mit der Adobe Analytics-Erweiterung

„Tracking-Server“ ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL Tracking-Server] angezeigt wird.

Wenn dieses Feld leer gelassen wird, wird standardmäßig `[rsid].data.adobedc.net`ausgewählt.

## s.trackingServer in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.trackingServer`-Variable ist eine Zeichenfolge, die den Ort enthält, an die Daten gesendet werden sollen.

## Überlegungen zur Bestimmung des Werts für `trackingServer`

Sie können die Verwendung von Adobe Tracking-Server-Domains (z. B. `adobedc.net`) oder Sie können einen speziellen Prozess durchlaufen, um einen Trackingserver einzurichten, der Ihrer Sites-Domäne entspricht (z. B. `data.mydomain.com`), auch als CNAME-Implementierung bezeichnet. Ein Trackingserver, der Ihrer Site-Domäne entspricht, kann abhängig von anderen Aspekten Ihrer Implementierung einige Vorteile bieten. Wenn der Tracking-Server nicht mit der Domäne der aktuellen Seite übereinstimmt, müssen von AppMeasurement festgelegte Cookies als Drittanbieter gesetzt werden. Wenn der Browser keine Drittanbieter-Cookies unterstützt, kann diese Diskrepanz bestimmte Analytics-Funktionen beeinträchtigen:

- Festlegen von Identifikatoren: Wenn Sie den Experience Cloud Identity-Dienst verwenden, hat der Tracking-Server keine Auswirkungen auf das Setzen von Cookies. Wenn Sie jedoch ältere Analytics-IDs verwenden (auch `s_vi` -Cookie) und der Erfassungsserver nicht mit der aktuellen Domäne übereinstimmt, müssen Cookies als Drittanbieter gesetzt werden. Wenn Drittanbieter-Cookies vom Browser blockiert werden, setzt Analytics eine Erstanbieter-Ausweich-ID (`s_fid`) anstelle des Standards `s_vi` Cookie.
- Das Linktracking funktioniert bei internen Links nicht.
- Activity Map funktioniert nicht für interne Links.
- Cookie-Prüfung.

### Erstanbieter-Cookies

Wenn Sie eine Erstanbieter-Cookie-Implementierung verwenden, ist es wahrscheinlich, dass jemand in Ihrem Unternehmen den Erstanbieter-Cookie-Prozess bereits abgeschlossen hat. Weitere Informationen zum Erstanbieter-Cookie-Prozess finden Sie unter [Erstanbieter-Cookies in der Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html?lang=de) im Core Services-Benutzerhandbuch.

Die Person, die die Erstanbieter-Cookie-Implementierung anfänglich konfiguriert, definiert auch die verwendete Domain und Unterdomäne. Beispiel:

```js
s.trackingServer = "data.example.com";
```

### Tracking-Server von Drittanbietern

>[!TIP]
>
>Durch die zunehmenden Datenschutzpraktiken in modernen Browsern werden die Cookies von Drittanbietern weniger zuverlässig. Adobe empfiehlt, den Erstanbieter-Cookie-Workflow zu befolgen.

Wenn Sie eine Drittanbieter-Cookie-Implementierung verwenden, ist der Wert für `trackingServer` eine Unterdomäne von `data.adobedc.net`. Beispiel:

```js
s.trackingServer = "example.data.adobedc.net";
```

Wählen Sie eine für Ihre Organisation eindeutige Subdomain aus, die wahrscheinlich nicht von einer anderen Organisation ausgewählt wird, die Adobe Analytics verwendet.  Es wird empfohlen, den Ihrem Unternehmen zugewiesenen Namespace für Besucher zu verwenden.  Stellen Sie sicher, dass alle Implementierungen in Ihrem Unternehmen denselben Tracking-Server verwenden. Es kann hilfreich sein, diese Informationen in einem [Lösungsdesigndokument](../../prepare/solution-design.md) zu verwalten.

Ihr Unternehmen verwendet möglicherweise bereits einen Tracking-Server eines Drittanbieters in den Domains `sc.omtrdc.net` oder `2o7.net`. Diese wurden hauptsächlich in früheren Versionen von Adobe Analytics verwendet, sind aber noch gültig.

>[!NOTE]
>
>Verwenden Sie keine Subdomänen, die tiefer als `example.data.adobedc.net` gehen. Zum Beispiel ist `custom.example.data.adobedc.net` kein gültiger Trackingserver.
