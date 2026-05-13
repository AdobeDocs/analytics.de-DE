---
description: Aktivieren von Dimensionen und Metriken zur Verwendung beim Tracking von Mobile Apps.
title: App-Berichterstellung
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
TQID: https://experienceleague.adobe.com/oF-tETs2-MWjSLoo5bVUmrr2nS4N1o2shD4DkMDAVLU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
  - id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4
  - id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2
  - id: c77ba355-6681-41fe-b719-563d3f507fdb
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 543
ht-degree: 11%

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

Die folgenden Metriken sind verfügbar:

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
* Verfolgen Sie Bluetooth-Beacons (UUID, Major, Minor und Proximity).

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

Die folgenden Metriken sind verfügbar:

* [!UICONTROL Voice-Endsitzung]
* [!UICONTROL Sprachfehler]
* [!UICONTROL Äußerungen]

## Ältere Berichterstellung und Zuordnung für Hintergrundtreffer

Legacy-Berichte bedeuten, dass Treffer, die generiert werden, wenn eine App im Hintergrund läuft, als reguläre Vordergrundtreffer behandelt werden. Sie werden in Berichten angezeigt und beeinflussen die Attribution. Diese ältere Konfiguration ist in der Regel wünschenswert, um die Konsistenz mit älteren Implementierungen zu gewährleisten.

Adobe empfiehlt, die veraltete Berichterstellung zu deaktivieren, damit Hintergrundtreffer nicht sichtbar sind. Wenn Sie Hintergrundtreffer in Ihre Analyse einbeziehen möchten, können Sie die Einstellung [Virtual Report Suite](/help/components/vrs/vrs-about.md) (Hintergrundtreffer **[!UICONTROL )]**.
