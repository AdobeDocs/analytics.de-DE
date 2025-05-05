---
description: Aktivieren von Dimensionen und Metriken zur Verwendung beim Tracking von Mobile Apps.
title: App-Berichterstellung
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 13%

---

# App-Berichterstellung

Über die App-Reporting-Benutzeroberfläche können Sie Lebenszyklusdimensionen und Metriken aktivieren, die für die Verwendung beim Tracking mobiler Anwendungen vorgesehen sind.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL App-Management]** > **[!UICONTROL App-Reporting]**

>[!IMPORTANT]
>
>Sobald eine dieser Funktionen aktiviert ist, können sie nicht mehr deaktiviert werden. Durch die Aktivierung einer bestimmten Funktion werden ihre jeweiligen Dimensionen und Metriken in Analysis Workspace dauerhaft verfügbar.

## [!UICONTROL App-Berichte]

[!UICONTROL App-Berichte] Dimensionen und Metriken werden für die folgenden Zwecke verwendet:

* **Akquise**: Verweisende URLs für App-Download-Kampagnen verfolgen.
* **Lebenszyklus**: Grundlegende Berichtsebene, die von der Messung bereitgestellt wird, die bei jedem Anwendungsstart gesendet wird.
* **App-**: Berichte und Pfade, die auf In-App-Aktionen basieren.
* **Lebenszeitwert**: Verstehen Sie, wie Benutzer mithilfe von App-KPIs (z. B. Käufe, Anzeigenansichten, Videoabschlüsse, Social Shares, Foto-Uploads) im Laufe der Zeit Wert ansammeln.
* **Zeitgesteuerte Ereignisse**: Messen Sie die Zeit (In-App- und Gesamtzeit), die zwischen wichtigen App-Aktionen vergeht (z. B. Zeit vor dem ersten Kauf).

Wenn Sie [!UICONTROL App-Berichte] aktivieren, sind die folgenden Dimensionen verfügbar:

* [!UICONTROL Aktionsname] (mit den Dimensionen [Einstieg](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md))
* [!UICONTROL App-ID]
* [!UICONTROL Akquise-Inhalte]
* [!UICONTROL Akquise-Medium]
* [!UICONTROL Akquise-Name]
* [!UICONTROL Akquise-Source]
* [!UICONTROL Akquisitionsbedingung]
* [!UICONTROL Wochentag (SDK)]
* [!UICONTROL Tage seit der ersten Verwendung]
* [!UICONTROL Tage seit der letzten Verwendung]
* [!UICONTROL Gerätename (SDK)]
* [!UICONTROL Stunde des Tages (SDK)]
* [!UICONTROL Erstes Startdatum]
* [!UICONTROL Startanzahl]
* [!UICONTROL Lebenszeitwert (eVar)]
* [!UICONTROL Betriebssystemversion (SDK)]
* [!UICONTROL Resolution (SDK)]

Die folgenden Metriken stehen zur Auswahl:

* [!UICONTROL Aktionsdauer in Anwendung]
* [!UICONTROL Aktionsdauer insgesamt]
* [!UICONTROL Abstürze]
* [!UICONTROL Erste Starts]
* [!UICONTROL Launches]
* [!UICONTROL Lebenszeitwert (event)]
* [!UICONTROL Gesamtsitzungslänge]
* [!UICONTROL Upgrades]

## [!UICONTROL Standortverfolgung]

[!UICONTROL Standortverfolgung]-Dimensionen werden für die folgenden Zwecke verwendet:

* Breiten- und Längengraddaten verfolgen
* Identifizieren, Erstellen und Visualisieren bestimmter Points of Interest. POIs müssen in der Mobile-SDK-Konfigurationsdatei definiert werden.
* Bluetooth-Beacons (UUID, Major-Wert, Minor-Wert und Nähe) verfolgen.

Wenn Sie [!UICONTROL Standortverfolgung] aktivieren, sind die folgenden Dimensionen verfügbar:

* [!UICONTROL Beacon Major] (mit [Einstieg](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md) Dimensionen)
* [!UICONTROL Beacon Minor] (mit [Eintritt](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md) Dimensionen)
* [!UICONTROL Beacon-Nähe] (mit [Eintritts](/help/components/dimensions/entry-dimensions.md) und [Austritts](/help/components/dimensions/exit-dimensions.md) Dimensionen)
* [!UICONTROL Beacon UUID] (mit [Eintritt](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md) Dimensionen)
* [!UICONTROL Standort (bis 10 km)]
* [!UICONTROL Standort (bis 100 m)]
* [!UICONTROL Standort (bis 1 m)]
* [!UICONTROL Zielpunkt-Bezeichnung]
* [!UICONTROL Entfernung zum Zentrum des Zielpunkts]
* [!UICONTROL Point of Interest-ID]

## [!UICONTROL Stimme und Chatbots]

[!UICONTROL Sprach- und Chatbots] Dimensionen und Metriken ermöglichen es Ihnen, Sprachassistenten wie Alexa oder Google Home zu messen. Außerdem können Sie selbst erstellte Chat-Bots messen. Zu den Messeigenschaften gehören:

* **Lebenszyklus**: Grundlegende Reporting-Ebene für jede App, z. B. Anzahl der Launches und Plattformtyp.
* **Konversationen** Misst Absichten, Antworten und andere Metriken und Dimensionen im Zusammenhang mit der Konversation.

Wenn Sie &quot;[!UICONTROL &#x200B; und Chatbots] aktivieren, sind die folgenden Dimensionen verfügbar:

* [!UICONTROL Sprachgerätefunktionen] (mit den Dimensionen [Einstieg](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md))
* [!UICONTROL Sprachauthentifizierung]
* [!UICONTROL Voice-Fehlertyp]
* [!UICONTROL Sprachabsicht]
* [!UICONTROL Voice-App-Antwort]
* [!UICONTROL Sprache]

Die folgenden Metriken stehen zur Auswahl:

* [!UICONTROL Voice-Endsitzung]
* [!UICONTROL Sprachfehler]
* [!UICONTROL Äußerungen]

## Altes Reporting und Attribution für Hintergrundtreffer

Legacy-Berichte bedeuten, dass Treffer, die generiert werden, wenn eine App im Hintergrund läuft, als reguläre Vordergrundtreffer behandelt werden. Sie werden in Berichten angezeigt und beeinflussen die Attribution. Diese ältere Konfiguration ist in der Regel wünschenswert, um die Konsistenz mit älteren Implementierungen zu gewährleisten.

Adobe empfiehlt, die veraltete Berichterstellung zu deaktivieren, damit Hintergrundtreffer nicht sichtbar sind. Wenn Sie Hintergrundtreffer in Ihre Analyse einbeziehen möchten, können Sie die Einstellung [Virtual Report Suite](/help/components/vrs/vrs-about.md) (Hintergrundtreffer **[!UICONTROL )]**.
