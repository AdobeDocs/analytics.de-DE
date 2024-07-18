---
description: Aktivieren Sie Dimensionen und Metriken für die Verfolgung mobiler Anwendungen.
title: App-Berichterstellung
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 13%

---

# App-Berichterstellung

Über die Benutzeroberfläche für die App-Berichterstellung können Sie Lebenszyklusdimensionen und Metriken aktivieren, die für die Verfolgung mobiler Anwendungen vorgesehen sind.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL App-Verwaltung]** > **[!UICONTROL App-Berichterstellung]**

>[!IMPORTANT]
>
>Sobald eine dieser Funktionen aktiviert ist, können sie nicht mehr deaktiviert werden. Durch die Aktivierung einer bestimmten Funktion sind die entsprechenden Dimensionen und Metriken dauerhaft in Analysis Workspace verfügbar.

## [!UICONTROL App-Berichte]

Die Dimensionen und Metriken für [!UICONTROL App-Berichte] werden für folgende Zwecke verwendet:

* **Akquise**: Verfolgen Sie Referrer-URLs für App-Download-Kampagnen.
* **Lebenszyklus**: Foundation-Ebene der Berichterstellung, die durch die bei jedem App-Start gesendeten Messungen bereitgestellt wird.
* **App-Aktionen**: Berichte und Pfade basierend auf In-App-Aktionen.
* **Lebenszeitwert**: Erfahren Sie, wie Benutzer mithilfe von App-KPIs im Zeitverlauf Werte ansammeln (z. B. Käufe, Anzeigenansichten, Videobeendigungen, Teilen über soziale Netzwerke, Foto-Uploads).
* **Zeitgesteuerte Ereignisse**: Messen Sie die Zeit (in der App und insgesamt) zwischen wichtigen App-Aktionen (z. B. Zeit vor dem ersten Kauf).

Wenn Sie [!UICONTROL App-Berichte] aktivieren, sind die folgenden Dimensionen verfügbar:

* [!UICONTROL Aktionsname] (mit den Dimensionen [Einstieg](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md))
* [!UICONTROL App-ID]
* [!UICONTROL Akquise-Inhalt]
* [!UICONTROL Akquise-Medium]
* [!UICONTROL Akquise-Name]
* [!UICONTROL Akquise-Source]
* [!UICONTROL Akquise-Begriff]
* [!UICONTROL Wochentag (SDK)]
* [!UICONTROL Tage seit der ersten Verwendung]
* [!UICONTROL Tage seit der letzten Verwendung]
* [!UICONTROL Gerätename (SDK)]
* [!UICONTROL Stunde des Tages (SDK)]
* [!UICONTROL Erstes Startdatum]
* [!UICONTROL Startanzahl]
* [!UICONTROL Lebenszeitwert (evar)]
* [!UICONTROL Betriebssystemversion (SDK)]
* [!UICONTROL Auflösung (SDK)]

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

Die Dimensionen [!UICONTROL Standortverfolgung] werden für folgende Zwecke verwendet:

* Daten zu Breiten- und Längengrad verfolgen
* Identifizieren, Erstellen und Visualisieren spezifischer Zielpunkte. Zielpunkte müssen in der Mobile SDK-Konfigurationsdatei definiert werden.
* Bluetooth-Beacons (UUID, Major-Wert, Minor-Wert und Nähe) verfolgen.

Wenn Sie [!UICONTROL Standortverfolgung] aktivieren, sind die folgenden Dimensionen verfügbar:

* [!UICONTROL Beacon Major] (mit den Dimensionen [Einstieg](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md) )
* [!UICONTROL Beacon Minor] (mit den Dimensionen [Einstieg](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md) )
* [!UICONTROL Beacon-Nähe] (mit den Dimensionen [Einstieg](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md) )
* [!UICONTROL Beacon-UUID] (mit den Dimensionen [Einstieg](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md) )
* [!UICONTROL Standort (bis 10 km)]
* [!UICONTROL Standort (bis 100 m)]
* [!UICONTROL Standort (bis 1 m)]
* [!UICONTROL Zielpunkt-Bezeichnung]
* [!UICONTROL Entfernung zum Zentrum des Zielpunkts]
* [!UICONTROL POI-ID]

## [!UICONTROL Stimme und Chatbots]

Mit den Dimensionen und Metriken von [!UICONTROL Voice and Chatbots] können Sie Sprachassistenten wie Alexa oder Google Home messen. Sie können auch selbst erstellte Chatbots messen. Zu den Messeigenschaften gehören:

* **Lebenszyklus**: Foundation-Ebene der Berichterstellung für jede App, z. B. die Anzahl der Starts und der Plattformtyp.
* **Konversationen**: Misst die Intents, Antworten und andere Metriken und Dimensionen, die mit der Konversation zusammenhängen.

Wenn Sie [!UICONTROL Voice und Chatbots] aktivieren, sind die folgenden Dimensionen verfügbar:

* [!UICONTROL Sprachgerätefunktionen] (mit den Dimensionen [Einstieg](/help/components/dimensions/entry-dimensions.md) und [Ausstieg](/help/components/dimensions/exit-dimensions.md) )
* [!UICONTROL Sprachauthentifizierung]
* [!UICONTROL Sprachfehlertyp]
* [!UICONTROL Sprachabsichten]
* [!UICONTROL Sprachanwendungs-Antwort]
* [!UICONTROL Sprachsprache]

Die folgenden Metriken stehen zur Auswahl:

* [!UICONTROL Sprachende-Sitzung]
* [!UICONTROL Sprachfehler]
* [!UICONTROL Spracheinstellungen]

## Ältere Berichterstellung und Attribution für Hintergrundtreffer

Die veraltete Berichterstellung bedeutet, dass Treffer, die generiert werden, wenn sich eine App im Hintergrund befindet, als reguläre Vordergrundtreffer behandelt werden. Sie werden in Berichten angezeigt und wirken sich auf die Attribution aus. Diese alte Konfiguration ist in der Regel wünschenswert, um die Konsistenz mit älteren Implementierungen sicherzustellen.

Adobe empfiehlt, die alte Berichterstellung zu deaktivieren, damit Hintergrundtreffer nicht sichtbar sind. Wenn Sie Hintergrundtreffer in Ihre Analyse einbeziehen möchten, können Sie die Einstellung [Virtual Report Suite](/help/components/vrs/vrs-about.md) aktivieren, um Hintergrundtreffer einschließen **[!UICONTROL 3} festzulegen.]**
