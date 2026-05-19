---
title: Erste Schritte mit Activity Map
description: Legen Sie jetzt mit der Verwendung von Activity Map-Überlagerungen und -Dimensionen los.
feature: Activity Map
role: User, Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
TQID: https://experienceleague.adobe.com/Wt30b3LTZWyzAQFOKqkqBdWH2Ifatq5FLp-Z0z7nktA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: df312454-73c4-43f6-a90e-18f5043f074cid: e7d92df1-c5ba-4e93-85df-f83171b889beid: ef60b66e-5984-4336-ba72-6d978b1b6f87id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: af860ea2bf90f0f25bfb95b943d9ae11bf808028
workflow-type: tm+mt
source-wordcount: 933
ht-degree: 97%

---

# Erste Schritte mit Activity Map

Activity Map in Adobe Analytics umfasst vier Hauptelemente:

* **Report Suite-Einstellung**: Sie müssen Activity Map in den Report Suite-Einstellungen aktivieren. Nach der Aktivierung erstellt die Report Suite mehrere reservierte Variablen für die Dimensionen und Metriken der Activity Map.
* **Implementierung**: Erfassen Sie Activity Map-Daten auf Ihrer Website oder Eigenschaft. Die Anpassung der Datenerfassung kann die Qualität Ihrer Berichte und die Benutzerfreundlichkeit verbessern.
* **Workspace-Dimensionen und -Metriken**: Wenn Ihre Implementierung korrekt konfiguriert ist, können Sie die Dimensionen und Metriken der Activity Map in Analysis Workspace verwenden.
* **Überlagerung**: Adobe bietet eine Browser-Erweiterung an, um Activity Map-Daten im Kontext Ihrer Website anzuzeigen. Diese Funktion ist nicht für Web SDK-Implementierungen verfügbar.

## Aktivieren von Report Suite-Einstellungen

Eine Report Suite muss für das Activity Map-Reporting aktiviert sein, bevor Sie mit der Datenerfassung beginnen können. Wenn Ihre Implementierung Activity Map-Daten an eine Report Suite sendet, ohne dass Activity Map-Reporting aktiviert ist, sind Activity Map-Daten nicht im Treffer enthalten.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map-Reporting]** > **[!UICONTROL Activity Map-Berichte aktivieren]**

Durch die Aktivierung von Activity Map-Berichten werden mehrere reservierte Backend-Variablen erstellt. Weitere Informationen finden Sie unter [Activity Map-Reporting](/help/admin/tools/manage-rs/edit-settings/activity-map.md) im Administrationshandbuch von Adobe Analytics.

## Code-Installation

Ihre Implementierung muss ordnungsgemäß konfiguriert sein, um Activity Map-Daten an Adobe zu senden. Die Browser-Erweiterung „Überlagerung“ ist nicht verfügbar, wenn Adobe Analytics mit Web SDK implementiert ist.

+++Web SDK-Tag-Erweiterung

Für die Datenerfassung in Activity Map ist die **[!UICONTROL Adobe Experience Platform Web SDK]**-Erweiterung ab Version 2.23 oder höher erforderlich. Erweiterungsversionen bis Version 2.16 werden nur eingeschränkt unterstützt. Diese früheren Erweiterungsversionen senden Activity Map-Daten in einem separaten Ereignis getrennt vom Rest Ihrer Daten. Dieses zusätzliche Ereignis erhöht die Anzahl der Treffer, die Sie an Adobe Analytics oder Adobe Experience Platform senden.

Die Konfigurationseinstellung **[!UICONTROL Klickdatenerfassung]** verarbeitet die Activity Map-Datenerfassung und ist in der Regel standardmäßig aktiviert. Sie können überprüfen, ob sie in den Konfigurationseinstellungen der Erweiterung aktiviert ist:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei ](https://experience.adobe.com)[Adobe CX Enterprise an.
1. Wählen Sie **[!UICONTROL Datenerfassung]** im Schnellzugriffsmenü oder über die Produktauswahl oben rechts aus.
1. Wählen Sie im linken Navigationsmenü **[!UICONTROL Tags]** aus.
1. Wählen Sie das gewünschte Tag aus, das Sie bearbeiten möchten.
1. Wählen Sie im linken Navigationsmenü **[!UICONTROL Erweiterungen]** aus.
1. Wählen Sie **[!UICONTROL Adobe Experience Platform Web SDK]** in der Liste der installierten Erweiterungen aus und wählen Sie dann auf der rechten Seite **[!UICONTROL Konfigurieren]** aus.
1. Suchen Sie den Abschnitt [!UICONTROL Datenerfassung] und stellen Sie sicher, dass das Kontrollkästchen zum **[!UICONTROL Aktivieren der Klickdatenerfassung]** aktiviert ist.
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Erstellen Sie bei Bedarf eine Bibliothek mit Ihren Änderungen und veröffentlichen Sie Ihre Änderungen in der Produktionsumgebung.

Weitere Informationen finden Sie unter [Konfigurieren der Web SDK-Tag-Erweiterung](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#data-collection).

+++

+++Web SDK-JavaScript-Bibliothek (`alloy.js`)

Für die Datenerfassung in Activity Map ist die Web-SDK-JavaScript-Bibliothek Version 2.20 oder höher erforderlich. Bibliotheksversionen bis Version 2.15 werden nur eingeschränkt unterstützt. Diese früheren Bibliotheksversionen senden Activity Map-Daten in einem separaten Ereignis getrennt vom Rest Ihrer Daten. Dieses zusätzliche Ereignis erhöht die Anzahl der Treffer, die Sie an Adobe Analytics oder Adobe Experience Platform senden.

Die Web SDK-Konfigurationsvariable [`clickCollectionEnabled`](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) verarbeitet die automatische Erfassung von Activity Map-Daten. Sie ist standardmäßig aktiviert, es sei denn, sie wurde explizit deaktiviert.

```js
alloy("configure", {
  datastreamId: "ebebf826-a01f-4458-8cec-ef61de241c93",
  orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg",
  clickCollectionEnabled: true
});
```

+++

+++Tag-Erweiterung für Adobe Analytics

Die Konfigurationseinstellung **[!UICONTROL Activity Map verwenden]** verarbeitet die Activity Map-Datenerfassung und ist in der Regel standardmäßig aktiviert. Sie ist für alle Tag-Erweiterungen der Version 1.9.0 oder höher verfügbar. Sie können überprüfen, ob sie in den Konfigurationseinstellungen der Erweiterung aktiviert ist:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei ](https://experience.adobe.com)[Adobe CX Enterprise an.
1. Wählen Sie **[!UICONTROL Datenerfassung]** im Schnellzugriffsmenü oder über die Produktauswahl oben rechts aus.
1. Wählen Sie im linken Navigationsmenü **[!UICONTROL Tags]** aus.
1. Wählen Sie das gewünschte Tag aus, das Sie bearbeiten möchten.
1. Wählen Sie im linken Navigationsmenü **[!UICONTROL Erweiterungen]** aus.
1. Wählen Sie **[!UICONTROL Adobe Analytics]** in der Liste der installierten Erweiterungen aus und wählen Sie dann auf der rechten Seite **[!UICONTROL Konfigurieren]** aus.
1. Stellen Sie sicher, dass das Kontrollkästchen **[!UICONTROL Activity Map verwenden]** aktiviert ist.
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Erstellen Sie bei Bedarf eine Bibliothek mit Ihren Änderungen und veröffentlichen Sie Ihre Änderungen in der Produktionsumgebung.

Weitere Informationen finden Sie in der [Produktbeschreibung für Adobe Analytics-Erweiterungen](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/analytics/overview).

+++

+++Adobe Analytics-JavaScript-Bibliothek (`AppMeasurement.js`)

Das Activity Map-Modul verarbeitet die Activity Map-Datenerfassung und ist in allen AppMeasurement-Bibliotheken der Version 1.6 oder höher enthalten. Sie können die Datei `AppMeasurement.js` überprüfen, um sicherzustellen, dass es enthalten ist.

1. Navigieren Sie zur [neuesten Version von Adobe Analytics AppMeasurement](https://github.com/adobe/appmeasurement/releases/latest) auf GitHub.
1. Laden Sie die komprimierte AppMeasurement-Bibliotheksdatei herunter und öffnen Sie dann die darin enthaltene Datei `AppMeasurement.js`.
1. Das Activity Map-Modul befindet sich im oberen Bereich dieser Datei. Stellen Sie sicher, dass dieses Modul in der AppMeasurement-Bibliothek enthalten ist, die Ihre Site verwendet.

+++

## Verfügbare Dimensionen

Wenn Activity Map sowohl für Ihre Report Suite als auch für die Implementierung aktiviert ist, können Sie die folgenden Dimensionen in Analysis Workspace verwenden:

* [[!UICONTROL Activity Map-Link]](/help/components/dimensions/activity-map-link.md)
* [[!UICONTROL Activity Map-Region]](/help/components/dimensions/activity-map-region.md)
* [[!UICONTROL Activity Map-Seite]](/help/components/dimensions/activity-map-page.md)
* [[!UICONTROL Activity Map-Link nach Region]](/help/components/dimensions/activity-map-link-by-region.md)

## Herunterladen und Installieren der Browser-Erweiterung oder des Add-ons

Zusätzlich zu den in Analysis Workspace verfügbaren Dimensionen können Sie Activity Map-Daten auch als Überlagerung auf Ihrer Website anzeigen. Um diese Überlagerung anzuzeigen, laden Sie die Browser-Erweiterung oder das Add-on für Activity Map herunter und installieren Sie diese.

**[!UICONTROL Tools]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map herunterladen]**

Dieser Link führt Sie zum unterstützten Erweiterungs- oder Add-on-Marketplace Ihres Browsers für die Installation. Nach der Installation wird die Erweiterung oder das Add-on oben rechts in Ihrem Browser angezeigt, wo Sie sich anmelden und die Überlagerung aktivieren können.
