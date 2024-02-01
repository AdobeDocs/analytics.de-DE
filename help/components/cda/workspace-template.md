---
title: CDA Workspace-Vorlage
description: Beschreibt die einzelnen Felder in der CDA-Vorlage in Analysis Workspace.
exl-id: 293001ff-bf7b-4de8-b175-7c2c17d1794d
feature: CDA
role: Admin
source-git-commit: be5a73347d417c8dc6667d4059e7d46ef5f0f5cd
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 93%

---

# CDA Workspace-Vorlage

Adobe bietet eine Vorlage zum Anzeigen wichtiger geräteübergreifender Leistungsdaten.

1. Navigieren Sie zu [experiencecloud.adobe.com](https://experiencecloud.adobe.com) und melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie oben auf das 9-Raster-Symbol und dann auf Analytics.
1. Klicken Sie oben auf [!UICONTROL Workspace] und anschließend auf [!UICONTROL Neues Projekt erstellen].
1. Suchen Sie nach der Vorlage „Geräteübergreifende Analyse“ und klicken Sie dann auf [!UICONTROL Erstellen].
1. Ändern Sie bei Aufforderung die Report Suite in eine Report Suite, die CDA unterstützt.

Es wird ein Analysis Workspace-Projekt erstellt, das mehrere Bedienfelder enthält. Oben werden ein Inhaltsverzeichnis und eine Einführung angezeigt, die den Kontext zum Bericht geben und die Navigation zu einzelnen Berichten ermöglichen. Klicken Sie auf einen Link im Inhaltsverzeichnis oder erweitern Sie das Akkordeon eines Bedienfelds, um diese Berichte anzuzeigen.

<!--The content below is mirrored in /help/analyze/analysis-workspace/build-workspace-project/starter-projects.md-->

* **Identifizierung der Benutzer**: Zeigt an, wie oft Besucher Ihrer Site mit Methoden identifiziert werden, die auf geräteübergreifenden Analysen basieren.
* **Messen der Zielgruppengröße**: Zeigt einen Vergleich von „Eindeutige Geräte“ mit „Personen“ an. Der Anteil dieser beiden Zahlen wird als „geräteübergreifende Komprimierung“ bezeichnet, eine berechnete Metrik, die in diesem Bedienfeld angezeigt wird. Diese Komprimierungsmetrik hängt von einer Vielzahl von Faktoren ab:
   * Anmelderate: Je mehr Benutzer sich auf Ihrer Site anmelden, desto besser kann Adobe Besucher geräteübergreifend identifizieren und zuordnen. Sites mit einer niedrigen Anmelderate haben auch niedrige Komprimierungsraten.
   * Experience Cloud ID-Abdeckung: Es können nur Besucher mit einer ECID zugeordnet werden. Ein geringerer Prozentsatz der Site-Besucher, die eine ECID verwenden, steht im Zusammenhang mit niedrigeren Komprimierungsraten.
   * Verwendung mehrerer Geräte: Wenn Besucher Ihrer Site nicht mehrere Geräte verwenden, erhalten Sie niedrigere Komprimierungsraten.
   * Berichtsgranularität: Die Komprimierung nach Tag ist in der Regel kleiner als die Komprimierung nach Monat oder Jahr. Die Wahrscheinlichkeit, dass eine Person mehrere Geräte verwendet, ist innerhalb eines Tages geringer als innerhalb eines ganzen Monats. Bei der Segmentierung, Filterung oder Verwendung von Aufschlüsselungsdimensionen kann es auch zu einer niedrigeren Komprimierungsrate kommen.
* **Benutzerbasierte Segmente**: Enthält eine Segment-Dropdownliste, mit der Sie gerätespezifische Daten anzeigen können. In diesem Bedienfeld können Sie mit Segmenten experimentieren, um festzustellen, wie sich das Einschließen oder Ausschließen von Gerätetypen auf Berichte auswirkt.
* **Analyse der geräteübergreifenden Journey**: Bietet Fluss- und Fallout-Berichte je nach Gerätetyp.
* **Geräteübergreifende Attribution**: Kombinieren Sie die Funktionen von Journey IQ und Attribution miteinander.
* **Weitere Tipps und Tricks**: Hilfreiche Themen rund um CDA, mit denen Sie die Nutzung optimieren können.
