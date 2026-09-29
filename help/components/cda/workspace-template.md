---
title: CDA Workspace-Vorlage
description: Beschreibt die einzelnen Felder in der CDA-Vorlage in Analysis Workspace.
exl-id: 293001ff-bf7b-4de8-b175-7c2c17d1794d
feature: CDA
role: Admin
TQID: 'https://experienceleague.adobe.com/Zui1m27pi3eQnm-dac2akfGRF01IbPaQ0SwLD01iDAE'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4
    internal-label: Attribution
  - id: e38cbddc-1633-4cd5-bed5-9f289f2a6029
    internal-label: Panels
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
    internal-label: Report suites
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
  - id: f99536a1-75c7-4151-a2c8-073630632526
    internal-label: CDA
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
    internal-label: Experimentation
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 92%
---
# CDA Workspace-Vorlage

{{available-existing-customers}}

Adobe bietet eine Vorlage zum Anzeigen wichtiger geräteübergreifender Leistungsdaten.

1. Navigieren Sie zu [experiencecloud.adobe.com](https://experiencecloud.adobe.com) und melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie oben auf das 9-Raster-Symbol und dann auf Analytics.
1. Klicken Sie oben auf [!UICONTROL Workspace] und anschließend auf [!UICONTROL Neues Projekt erstellen].
1. Suchen Sie nach der Vorlage „Geräteübergreifende Analyse“ und klicken Sie dann auf [!UICONTROL Erstellen].
1. Ändern Sie bei Aufforderung die Report Suite in eine, die CDA unterstützt.

Es wird ein Analysis Workspace-Projekt erstellt, das mehrere Panels enthält. Oben werden ein Inhaltsverzeichnis und eine Einführung angezeigt, die den Kontext zum Bericht geben und die Navigation zu einzelnen Berichten ermöglichen. Klicken Sie auf einen Link im Inhaltsverzeichnis oder erweitern Sie das Akkordeon eines Panels, um diese Berichte anzuzeigen.

<!--The content below is mirrored in /help/analyze/analysis-workspace/build-workspace-project/starter-projects.md-->

* **Identifizierung der Benutzer**: Zeigt an, wie oft Besucher Ihrer Site mit Methoden identifiziert werden, die auf geräteübergreifenden Analysen basieren.
* **Messen der Zielgruppengröße**: Zeigt einen Vergleich von „Eindeutige Geräte“ mit „Personen“ an. Der Anteil dieser beiden Zahlen wird als „Gerätekomprimierung“ bezeichnet, eine berechnete Metrik, die in diesem Panel angezeigt wird. Diese Komprimierungsmetrik hängt von einer Vielzahl von Faktoren ab:
  * Anmelderate: Je mehr Benutzer sich auf Ihrer Site anmelden, desto besser kann Adobe Besucher geräteübergreifend identifizieren und zuordnen. Sites mit einer niedrigen Anmelderate haben auch niedrige Komprimierungsraten.
  * Experience Cloud ID-Abdeckung: Es können nur Besucher mit einer ECID zugeordnet werden. Ein geringerer Prozentsatz der Site-Besucher, die eine ECID verwenden, steht im Zusammenhang mit niedrigeren Komprimierungsraten.
  * Verwendung mehrerer Geräte: Wenn Besucher Ihrer Site nicht mehrere Geräte verwenden, erhalten Sie niedrigere Komprimierungsraten.
  * Berichtsgranularität: Die Komprimierung nach Tag ist in der Regel kleiner als die Komprimierung nach Monat oder Jahr. Die Wahrscheinlichkeit, dass eine Person mehrere Geräte verwendet, ist innerhalb eines Tages geringer als innerhalb eines ganzen Monats. Bei der Segmentierung, Filterung oder Verwendung von Aufschlüsselungsdimensionen kann es auch zu einer niedrigeren Komprimierungsrate kommen.
* **Personenbasierte Segmente**: Enthält eine Dropdown-Liste für Segmente , in der Sie gerätespezifische Daten anzeigen können. In diesem Panel können Sie mit Segmenten experimentieren, um festzustellen, wie sich das Einschließen oder Ausschließen von Gerätetypen auf Berichte auswirkt.
* **Analyse der geräteübergreifenden Journey**: Bietet Fluss- und Fallout-Berichte je nach Gerätetyp.
* **Geräteübergreifende Attribution**: Kombinieren Sie die Funktionen der geräteübergreifenden Analyse und der Attribution miteinander.
* **Weitere Tipps und Tricks**: Hilfreiche Themen rund um CDA, mit denen Sie die Nutzung optimieren können.
