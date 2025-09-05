---
title: Erste Schritte mit Activity Map
description: Erste Schritte mit der Activity Map-Überlagerung und -Dimensionen.
feature: Activity Map
role: User, Admin
exl-id: 0b2b9f3d-0c75-4eb8-9235-c9c98eb035d3
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 1%

---

# Erste Schritte mit Activity Map

Activity Map in Adobe Analytics umfasst vier Hauptelemente:

* **Report Suite-**: Sie müssen Activity Map in den Report Suite-Einstellungen aktivieren. Nach der Aktivierung erstellt die Report Suite mehrere reservierte Variablen für Activity Map-Dimensionen und -Metriken.
* **Implementierung**: Erfassen Sie Activity Map-Daten auf Ihrer Website oder Eigenschaft. Durch die Anpassung der Art der Datenerfassung können die Qualität und das Erlebnis von Berichten verbessert werden.
* **Workspace-Dimensionen und -**: Wenn Ihre Implementierung korrekt konfiguriert ist, können Sie Activity Map-Dimensionen und -Metriken in Analysis Workspace verwenden.
* **Überlagerung**: Adobe bietet eine Browser-Erweiterung, um Activity Map-Daten im Kontext Ihrer Website anzuzeigen.

## Report Suite-Einstellungen aktivieren

Für eine Report Suite muss die Activity Map-Berichterstellung aktiviert sein, bevor Sie mit der Datenerfassung beginnen können. Wenn Ihre Implementierung Activity Map-Daten an eine Report Suite sendet, ohne dass Activity Map-Berichte aktiviert sind, sind Activity Map-Daten nicht im Treffer enthalten.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map-Berichte]** > **[!UICONTROL Activity Map-Berichte aktivieren]**

Durch die Aktivierung von Activity Map-Berichten werden mehrere reservierte Backend-Variablen erstellt. Weitere Informationen finden Sie unter {[}Activity Map-Reporting im Adobe Analytics-Administratorhandbuch.](/help/admin/tools/manage-rs/edit-settings/activity-map.md)

## Code-Installation

Ihre Implementierung muss ordnungsgemäß konfiguriert sein, um Activity Map-Daten an Adobe zu senden.

+++Web SDK-Tag-Erweiterung

Für die Datenerfassung in Activity Map ist die **[!UICONTROL Adobe Experience Platform Web SDK]**-Erweiterung v2.23 oder höher erforderlich. Erweiterungsversionen bis Version 2.16 werden nur eingeschränkt unterstützt. Diese vorherigen Erweiterungsversionen senden Activity Map-Daten in einem separaten Ereignis vom Rest Ihrer Daten. Dieses zusätzliche Ereignis erhöht die Anzahl der Treffer, die Sie an Adobe Analytics oder Adobe Experience Platform senden.

Die Konfigurationseinstellung **[!UICONTROL Klicken auf]** Datenerfassung“ verarbeitet die Activity Map-Datenerfassung und ist in der Regel standardmäßig aktiviert. Sie können überprüfen, ob es in den Konfigurationseinstellungen der Erweiterung aktiviert ist:

1. Melden Sie sich bei [experience.adobe.com](https://experience.adobe.com)
1. Wählen **[!UICONTROL Datenerfassung]** im Schnellzugriffsmenü oder über die Produktauswahl oben rechts aus.
1. Wählen **[!UICONTROL Tags]** im linken Navigationsmenü aus.
1. Wählen Sie das gewünschte Tag aus, das Sie bearbeiten möchten.
1. Wählen **[!UICONTROL Erweiterungen]** im linken Navigationsmenü aus.
1. Wählen Sie **[!UICONTROL Adobe Experience Platform Web SDK]** in der Liste der installierten Erweiterungen aus und wählen Sie dann **[!UICONTROL Konfigurieren]** auf der rechten Seite.
1. Suchen Sie den Abschnitt mit [!UICONTROL Datenerfassung] und stellen Sie sicher, dass das Kontrollkästchen **[!UICONTROL Aktivieren und auf Datenerfassung klicken]** aktiviert ist.
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Erstellen Sie bei Bedarf Ihre Änderungen in einer Bibliothek und veröffentlichen Sie Ihre Änderungen in der Produktionsumgebung.

Weitere [ finden Sie unter „Konfigurieren der Tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#data-collection)Erweiterung für Web SDK&quot;.

+++

+++Web SDK JavaScript Library (`alloy.js`)

Für die Datenerfassung in Activity Map ist die Web-SDK-JavaScript-Bibliothek Version 2.20 oder höher erforderlich. Bibliotheksversionen bis Version 2.15 werden nur eingeschränkt unterstützt. Diese früheren Bibliotheksversionen senden Activity Map-Daten in einem separaten Ereignis vom Rest Ihrer Daten. Dieses zusätzliche Ereignis erhöht die Anzahl der Treffer, die Sie an Adobe Analytics oder Adobe Experience Platform senden.

Die Web SDK-Konfigurationsvariable [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) verarbeitet die automatische Erfassung von Activity Map-Daten. Sie ist standardmäßig aktiviert, es sei denn, sie wird explizit deaktiviert.

```js
alloy("configure", {
  datastreamId: "ebebf826-a01f-4458-8cec-ef61de241c93",
  orgId: "ADB3LETTERSANDNUMBERS@AdobeOrg",
  clickCollectionEnabled: true
});
```

+++

+++Adobe Analytics-Tag-Erweiterung

Die **[!UICONTROL Activity Map verwenden]** Konfigurationseinstellung verarbeitet die Activity Map-Datenerfassung und ist in der Regel standardmäßig aktiviert. Sie ist für alle Tag-Erweiterungen der Version 1.9.0 oder höher verfügbar. Sie können überprüfen, ob es in den Konfigurationseinstellungen der Erweiterung aktiviert ist:

1. Melden Sie sich bei [experience.adobe.com](https://experience.adobe.com)
1. Wählen **[!UICONTROL Datenerfassung]** im Schnellzugriffsmenü oder über die Produktauswahl oben rechts aus.
1. Wählen **[!UICONTROL Tags]** im linken Navigationsmenü aus.
1. Wählen Sie das gewünschte Tag aus, das Sie bearbeiten möchten.
1. Wählen **[!UICONTROL Erweiterungen]** im linken Navigationsmenü aus.
1. Wählen Sie **[!UICONTROL Adobe Analytics]** in der Liste der installierten Erweiterungen aus und wählen Sie dann **[!UICONTROL Konfigurieren]** auf der rechten Seite.
1. Stellen Sie sicher, dass das Kontrollkästchen **[!UICONTROL Activity Map verwenden]** aktiviert ist.
1. Wählen Sie **[!UICONTROL Speichern]** aus.
1. Erstellen Sie bei Bedarf Ihre Änderungen in einer Bibliothek und veröffentlichen Sie Ihre Änderungen in der Produktionsumgebung.

Weiterführende Informationen dazu finden Sie in der [ zur Adobe Analytics-Erweiterung ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/analytics/overview).

+++

+++Adobe Analytics JavaScript Library (`AppMeasurement.js`)

Das Activity Map-Modul verarbeitet die Activity Map-Datenerfassung und ist in allen AppMeasurement-Bibliotheken Version 1.6 oder höher enthalten. Sie können die `AppMeasurement.js`-Datei überprüfen, um sicherzustellen, dass sie enthalten ist.

1. Navigieren Sie zur [neuesten Version von Adobe Analytics AppMeasurement](https://github.com/adobe/appmeasurement/releases/latest) auf GitHub.
1. Laden Sie die komprimierte AppMeasurement-Bibliotheksdatei herunter und öffnen Sie dann die darin enthaltenen `AppMeasurement.js`.
1. Das Activity Map-Modul ist am Anfang dieser Datei enthalten. Stellen Sie sicher, dass dieses Modul in der AppMeasurement-Bibliothek enthalten ist, die Ihre Site verwendet.

+++

## Verfügbare Dimensionen

Wenn Activity Map sowohl für Ihre Report Suite als auch für die Implementierung aktiviert ist, können Sie in Analysis Workspace mit der Verwendung der folgenden Dimensionen beginnen:

* [[!UICONTROL Activity Map-Link]](/help/components/dimensions/activity-map-link.md)
* [[!UICONTROL Activity Map-Region]](/help/components/dimensions/activity-map-region.md)
* [[!UICONTROL Activity Map-Seite]](/help/components/dimensions/activity-map-page.md)
* [[!UICONTROL Activity Map-Link nach Region]](/help/components/dimensions/activity-map-link-by-region.md)

## Herunterladen und Installieren der Browser-Erweiterung oder des Add-ons

Zusätzlich zu den in Analysis Workspace verfügbaren Dimensionen können Sie Activity Map-Daten auch als Überlagerung auf Ihrer Website anzeigen. Um diese Überlagerung anzuzeigen, laden Sie die Activity Map-Browser-Erweiterung oder das Add-on herunter und installieren Sie sie.

**[!UICONTROL Tools]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map herunterladen]**

Dieser Link führt Sie zum unterstützten Erweiterungs- oder Add-on-Marketplace Ihres Browsers, auf dem Sie ihn installieren können. Nach der Installation wird die Erweiterung oder das Add-on oben rechts in Ihrem Browser angezeigt, wo Sie sich anmelden und die Überlagerung aktivieren können.
