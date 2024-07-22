---
title: Erste Schritte mit Activity Map
description: Beginnen Sie mit der Verwendung der Activity Map-Überlagerung und -Dimensionen.
feature: Activity Map
role: User, Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
source-git-commit: bfafc1f8eddf82b34fb45e3d6197213f0cee0d97
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Erste Schritte mit Activity Map

Activity Map in Adobe Analytics umfasst vier Hauptkomponenten:

* **Report Suite-Einstellung**: Sie müssen Activity Map in den Report Suite-Einstellungen aktivieren. Wenn diese Option aktiviert ist, erstellt die Report Suite verschiedene reservierte Variablen für Activity Map-Dimensionen und -Metriken.
* **Implementierung**: Erfassen Sie Activity Map-Daten auf Ihrer Website oder Eigenschaft. Durch das Anpassen der Datenerfassung können die Qualität und das Erlebnis von Berichten verbessert werden.
* **Workspace-Dimensionen und -Metriken**: Wenn Ihre Implementierung korrekt konfiguriert ist, können Sie Activity Map-Dimensionen und -Metriken in Analysis Workspace verwenden.
* **Overlay**: Adobe bietet eine Browsererweiterung zum Anzeigen von Activity Map-Daten im Kontext Ihrer Website.

## Report Suite-Einstellung aktivieren

Für eine Report Suite muss die Activity Map-Berichterstellung aktiviert sein, bevor Sie mit der Datenerfassung beginnen können. Wenn Ihre Implementierung Activity Map-Daten an eine Report Suite sendet, ohne dass die Activity Map-Berichterstellung aktiviert ist, werden Activity Map-Daten nicht in den Treffer einbezogen.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map-Reporting]** > **[!UICONTROL Activity Map-Berichte aktivieren]**

Durch die Aktivierung von Activity Map-Berichten werden mehrere vom Backend reservierte Variablen erstellt. Weitere Informationen finden Sie unter [Activity Map Reporting](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/activity-map.md) im Administratorhandbuch zu Adobe Analytics.

## Code-Installation

Ihre Implementierung muss korrekt konfiguriert sein, um Activity Map-Daten an Adobe zu senden.

+++Web SDK-Tag-Erweiterung

Für die Activity Map-Datenerfassung ist die Erweiterung &quot;**[!UICONTROL Adobe Experience Platform Web SDK]**&quot;v2.23 oder höher erforderlich. Erweiterungsversionen bis zur Version 2.16 werden nur eingeschränkt unterstützt. Diese vorherigen Erweiterungsversionen senden Activity Map-Daten in einem separaten Ereignis als das übrige Ihrer Daten. Dieses zusätzliche Ereignis erhöht die Anzahl der Treffer, die Sie an Adobe Analytics oder Adobe Experience Platform senden.

Die Konfigurationseinstellung **[!UICONTROL Klick auf Datenerfassung]** verarbeitet die Activity Map-Datenerfassung und ist in der Regel standardmäßig aktiviert. Sie können überprüfen, ob sie in den Konfigurationseinstellungen der Erweiterung aktiviert ist:

1. Anmelden bei [experience.adobe.com](https://experience.adobe.com)
1. Wählen Sie im Schnellzugriffsmenü die Option **[!UICONTROL Datenerfassung]** oder oben rechts die Produktselektor.
1. Wählen Sie im linken Navigationsmenü **[!UICONTROL Tags]** aus.
1. Wählen Sie das gewünschte Tag aus, das Sie bearbeiten möchten.
1. Wählen Sie im linken Navigationsmenü **[!UICONTROL Erweiterungen]** aus.
1. Wählen Sie **[!UICONTROL Adobe Experience Platform Web SDK]** in der Liste der installierten Erweiterungen und dann rechts **[!UICONTROL Konfigurieren]** aus.
1. Suchen Sie den Abschnitt mit der Bezeichnung [!UICONTROL Datenerfassung] und stellen Sie sicher, dass das Kontrollkästchen **[!UICONTROL Klickdatenerfassung aktivieren]** aktiviert ist.
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Erstellen Sie bei Bedarf Ihre Änderungen in einer Bibliothek und veröffentlichen Sie Ihre Änderungen in der Produktion.

Weitere Informationen finden Sie unter [Konfigurieren der Web SDK-Tag-Erweiterung](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#data-collection) .

+++

+++Web SDK JavaScript-Bibliothek (`alloy.js`)

Für die Activity Map-Datenerfassung ist die Web SDK JavaScript-Bibliothek v2.20 oder höher erforderlich. Bibliotheksversionen bis zur Version 2.15 werden nur eingeschränkt unterstützt. Diese vorherigen Bibliotheksversionen senden Activity Map-Daten in einem separaten Ereignis als das übrige Ihrer Daten. Dieses zusätzliche Ereignis erhöht die Anzahl der Treffer, die Sie an Adobe Analytics oder Adobe Experience Platform senden.

Die Web SDK-Konfigurationsvariable [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) verarbeitet die automatische Erfassung von Activity Map-Daten. Sie ist standardmäßig aktiviert, es sei denn, sie ist explizit deaktiviert.

```js
alloy("configure", {
  datastreamId: "ebebf826-a01f-4458-8cec-ef61de241c93",
  orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg",
  clickCollectionEnabled: true
});
```

+++

++ + Adobe Analytics-Tag-Erweiterung

Die Konfigurationseinstellung **[!UICONTROL Activity Map verwenden]** verarbeitet die Activity Map-Datenerfassung und ist in der Regel standardmäßig aktiviert. Sie ist für alle Tag-Erweiterungen Version 1.9.0 oder höher verfügbar. Sie können überprüfen, ob sie in den Konfigurationseinstellungen der Erweiterung aktiviert ist:

1. Anmelden bei [experience.adobe.com](https://experience.adobe.com)
1. Wählen Sie im Schnellzugriffsmenü die Option **[!UICONTROL Datenerfassung]** oder oben rechts die Produktselektor.
1. Wählen Sie im linken Navigationsmenü **[!UICONTROL Tags]** aus.
1. Wählen Sie das gewünschte Tag aus, das Sie bearbeiten möchten.
1. Wählen Sie im linken Navigationsmenü **[!UICONTROL Erweiterungen]** aus.
1. Wählen Sie **[!UICONTROL Adobe Analytics]** in der Liste der installierten Erweiterungen und dann rechts **[!UICONTROL Konfigurieren]**.
1. Stellen Sie sicher, dass das Kontrollkästchen **[!UICONTROL Activity Map verwenden]** aktiviert ist.
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Erstellen Sie bei Bedarf Ihre Änderungen in einer Bibliothek und veröffentlichen Sie Ihre Änderungen in der Produktion.

Weitere Informationen finden Sie unter [Übersicht über die Adobe Analytics-Erweiterung](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/analytics/overview) .

+++

+ + + Adobe Analytics JavaScript-Bibliothek (`AppMeasurement.js`)

Das Activity Map-Modul verarbeitet die Activity Map-Datenerfassung und ist in allen AppMeasurement-Bibliotheken ab Version 1.6 enthalten. Sie können die Datei &quot;`AppMeasurement.js`&quot; überprüfen, um sicherzustellen, dass sie enthalten ist.

1. Navigieren Sie zur [neuesten Adobe Analytics AppMeasurement-Version](https://github.com/adobe/appmeasurement/releases/latest) auf GitHub.
1. Laden Sie die komprimierte AppMeasurement-Bibliotheksdatei herunter und öffnen Sie dann die darin enthaltene `AppMeasurement.js`-Datei.
1. Das Activity Map-Modul befindet sich oben in der Datei. Stellen Sie sicher, dass dieses Modul in der von Ihrer Site verwendeten AppMeasurement-Bibliothek enthalten ist.

+++

## Verfügbare Dimensionen

Wenn Activity Map sowohl für Ihre Report Suite als auch für Ihre Implementierung aktiviert ist, können Sie die folgenden Dimensionen in Analysis Workspace verwenden:

* [[!UICONTROL Activity Map-Link]](/help/components/dimensions/activity-map-link.md)
* [[!UICONTROL Activity Map Region]](/help/components/dimensions/activity-map-region.md)
* [[!UICONTROL Activity Map-Seite]](/help/components/dimensions/activity-map-page.md)
* [[!UICONTROL Activity Map-Link nach Region]](/help/components/dimensions/activity-map-link-by-region.md)

## Browsererweiterung oder Add-on herunterladen und installieren

Zusätzlich zu den in Analysis Workspace verfügbaren Dimensionen können Sie auch Activity Map-Daten als Überlagerung auf Ihrer Website anzeigen. Um diese Überlagerung anzuzeigen, laden Sie die Activity Map-Browsererweiterung oder das Add-on herunter und installieren Sie sie.

**[!UICONTROL Tools]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map herunterladen]**

Über diesen Link gelangen Sie zur unterstützten Erweiterung oder zum Add-on-Marketplace Ihres Browsers, wo Sie ihn installieren können. Nach der Installation wird die Erweiterung oder das Add-on oben rechts im Browser angezeigt, wo Sie sich anmelden und die Überlagerung aktivieren können.
