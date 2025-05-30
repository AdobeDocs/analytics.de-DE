---
description: Diese Hilfeseite enthält empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Die Tools sollten in der Reihenfolge der Liste verwendet werden. Wenn ein bestimmtes Tool Ihren Anforderungen nicht gerecht wird, wählen Sie stattdessen das nächste in der Liste aus.
title: Welches Adobe Analytics-Tool sollte ich verwenden?
feature: Analytics Basics
exl-id: d65575df-19c6-4129-89c8-d36de7bb6b2f
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: ht
source-wordcount: '1122'
ht-degree: 100%

---

# Welches Adobe Analytics-Tool sollte ich verwenden?

Diese Hilfeseite enthält empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Die Tools sollten in der Reihenfolge der Liste verwendet werden. Wenn ein bestimmtes Tool Ihren Anforderungen nicht gerecht wird, wählen Sie stattdessen das nächste in der Liste aus.

Weitere Informationen zu Adobe Analytics-Produktvergleichen finden Sie unter [Analytics-Produktvergleich](/help/analyze/get-started/analytics-product-comparison.md).


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Vergleich von Tools](https://video.tv.adobe.com/v/30167?quality=12&learn=on&captions=ger){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


## Adobe Analytics-Berichtsoberflächen {#user-interfaces}

**[Analysis Workspace](/help/analyze/analysis-workspace/home.md)** sollte die bevorzugte Benutzeroberfläche für alle Berichts- und Analyseaufgaben sein. Adobe investiert weiterhin in dieses Produkt und gibt monatlich Updates dafür heraus. Können Sie eine Aufgabe nicht mit Analysis Workspace durchführen, versuchen Sie eine der unten stehenden Oberflächen.**

**[Adobe Analytics-Dashboards](/help/analyze/mobile-app/home.md)** ermöglichen Benutzenden mobilen Zugriff auf intuitive Scorecards. Scorecards sind eine Sammlung von Schlüsselmetriken und anderen Komponenten, die in einem gekachelten Layout dargestellt werden. Sie können auf eine Scorecard tippen, um detailliertere Aufschlüsselungen und Trendberichte zu erhalten. Die mobile App wird sowohl auf iOS- als auch auf Android-Geräten unterstützt.

**[Report Builder](/help/analyze/report-builder/rb-overview.md)** ist ein Add-in für Microsoft Excel, das unter Mac, Windows und in Webbrowsern ausgeführt werden kann. Mit Report Builder können Sie benutzerdefinierte Anfragen aus Adobe Analytics-Daten erstellen, die Sie in Excel-Arbeitsblätter einfügen können. Anforderungen können dynamisch auf Zellen innerhalb Ihres Arbeitsblatts verweisen, und die Darstellung der Daten in Report Builder lässt sich aktualisieren und anpassen.

**[Die Vorgängerversion von Report Builder](/help/analyze/legacy-report-builder/home.md)** ist ein Add-in für Microsoft Excel, das nur unter Windows ausgeführt werden kann. Mit Report Builder können Sie benutzerdefinierte Anfragen aus Adobe Analytics-Daten erstellen, die Sie in Excel-Arbeitsblätter einfügen können. Anforderungen können dynamisch auf Zellen innerhalb Ihres Arbeitsblatts verweisen, und die Darstellung der Daten in Report Builder lässt sich aktualisieren und anpassen.

Die **[Activity Map](/help/analyze/activity-map/overview.md)** ist eine Funktion in Adobe Analytics, die eine visuelle Darstellung der Benutzerinteraktion auf Web-Seiten und mobilen Apps bietet. Sie ermöglicht es Marketing-Fachleuten sowie Analystinnen und Analysten, Benutzerinteraktionen wie Klicks, Mausberührungen und das Scroll-Verhalten zu verfolgen und zu analysieren.

## Importieren von Daten in Adobe Analytics {#import}

**[Klassifizierungen](/help/components/classifications/classifications-overview.md)** sollten verwendet werden:

* Wenn Metadaten vorliegen, die Sie einem Erfassungswert (eVar, prop, Marketing-Kanal) zuweisen möchten. Adobe empfiehlt stattdessen die Verwendung von [Klassifizierungssätzen](/help/components/classifications/sets/overview.md). Der Classification Rule Builder und Classification Importer sind veraltete Methoden zum Übertragen von Klassifizierungsdaten in Adobe Analytics.

**[Data Sources](/help/import/data-sources/overview.md)** sollte verwendet werden:

* Wenn Offline-Daten vorliegen, die dauerhaft in Adobe Analytics geschrieben werden sollen.
* Optionen:
   * Zusammenfassung: einfache Datenuploads nach Tag oder anhand von begrenzten Dimensionen.
   * Transaktions-ID: Datenuploads, die einen Online-Endpunkt mit Offlinedaten verknüpfen und importierte Daten vollständig einem online erstellten Besucher-Schnappschuss zuordnen (z. B. online abgeschlossene Bestellungen, die offline zurückgegeben werden).

**[Adobe Exchange-Integrationen](https://www.adobeexchange.com/experiencecloud.html)** sollten verwendet werden:

* Wenn Sie mit einem Drittanbieter interagieren, der eine unterstützte Schnittstelle für Adobe Analytics erstellt hat. Integrations-Mobile-Apps übernehmen meist zusammengefasste Daten automatisch, dauerhaft und wiederholt in Adobe Analytics.

**[Bulk Data Insertion API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)**

* Das Bulk Data Insertion API akzeptiert Dateien mit Ereignisdaten im CSV-Format, wobei ein Ereignis pro Zeile angegeben wird. Adobe empfiehlt die Verwendung des Bulk Insertion API für jede Implementierung, für die Server-seitiger Code erforderlich ist, ohne den AppMeasurement oder das Web-SDK nicht für die Datenerfassung verwendet werden kann.

Das **[Data Insertion API (veraltet)](/help/import/c-data-insertion-api/c-data-insertion-api.md)** sollte in folgenden Fällen verwendet werden:

* Wenn Sie Daten in Adobe Analytics importieren müssen und AppMeasurement, Web-SDK oder das Bulk Data Insertion API nicht verwenden können.

**[Kundenattribute](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=de)** sollten verwendet werden:

* Wenn Sie Unternehmenskundendaten in einer Datenbank für Customer Relationship Management (CRM) speichern und die Daten in die Experience Cloud hochladen möchten.
* Wenn Sie CRM-Daten für tiefgreifende Analysen in Analytics oder als Targeting-Kriterien in Adobe Target verwenden möchten.

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)** sollte verwendet werden:

* Wenn Sie Zielgruppendaten von Adobe Audience Manager – wie beispielsweise demografische Daten (z. B. Geschlecht oder Einkommensniveau), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten oder Ad-Impression-Daten – in einen beliebigen Analytics-Workflow einbetten möchten.
* Wenn Sie möchten, dass hochgeladene CRM-Daten zeitbasiert sind, da diese Integration für jeden Treffer Daten an Analytics übermittelt.

## Exportieren von Daten aus Adobe Analytics {#export}

**[Report Builder](/help/analyze/report-builder/rb-overview.md)** sollte verwendet werden:

* Wenn die individuellen Layoutoptionen von Workspace zu sehr einschränken (in Report Builder sind sämtliche Optionen möglich, die Excel bietet).
* Zur lockeren Verknüpfung von Benutzereingaben oder Offline-Datenquellen (Impressionen, Kosten) mit Adobe-Daten. Eine dauerhaftere Lösung für das Einbinden von Daten sind Datenquellen (siehe „Importieren von Daten in Analytics“).
* Zum Zusammenführen von Daten aus verschiedenen dimensionalen Berichten (z. B. Kombination eines Berichts über Promo-Impressionen mit einem Bericht über den Klick-zu-Konversion-Verlauf bei einer Promo).
* Zum Zusammenführen von Daten aus verschiedenen Report Suites, entweder durch Zusammenfassen oder durch paralleles Anzeigen in derselben Tabelle.
* Wenn bei der Planung Automatisierung gewünscht wird (XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Data Warehouse](/help/export/data-warehouse/data-warehouse.md)** sollte verwendet werden:

* Für den Zugriff auf Variablen, die ansonsten in der Benutzeroberfläche verborgen sind: IP-Adresse, Experience Cloud ID, Analytics-Besucher-ID, Seiten-URL.
* Für den Zugriff auf granularere Daten als jene in der Benutzeroberfläche (denormalisierte Tabellenansicht).
* Für den Download von Daten in einem für die Pivot-Tabellen-Eingabe geeigneten Format.
* Wenn der Kunde Adobe-Daten in ein Drittanbieter-Tool für die Datenvisualisierung eingeben möchte (leicht zusammengefasst und nicht auf Trefferebene).
* Für den Zugriff auf alle eindeutigen Dimensionselemente, wenn in Adobe Analytics ein geringer Datenverkehr für Sie vorliegt.

**[Analytics-Daten-Feed](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)** sollte verwendet werden:

* Zur Nutzung des granularsten Daten-Feeds, der möglich ist (Besucher-ID, Treffer).
* Wenn der Kunde Adobe-Dateien in einer clientseitigen Datenbank und so granular wie möglich speichern möchte.
* Wenn der Kunde ein Business Intelligence-Tool entwickeln oder Adobe-Daten auf Trefferebene in ein Drittanbieter-Tool importieren möchte.

**[Reporting-APIs](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/reporting-guide.md)** sollten verwendet werden, wenn die anderen Visualisierungsoptionen Ihren Anforderungen nicht gerecht werden. Die 3 API-Optionen sind:

* **Vollständig verarbeitet:** Wenn Sie umfangreiche Daten präsentieren möchten (einschließlich Besuchen, Besuchern und Segmenten). Dabei handelt es sich üblicherweise um in der Analytics-Benutzeroberfläche zusammengefasste Daten, die innerhalb von etwa 30–90 Minuten verfügbar sind. Die Verwendung ist überall im Report Builder möglich.
* **Echtzeit:** Wenn Sie einige Metriken und Dimensionen mit nur wenigen Sekunden Latenz anzeigen möchten. Hierbei handelt es sich um begrenzte, teilweise verarbeitete, zusammengefasste Daten, die innerhalb von etwa 30 Sekunden verfügbar sind. Umfasst eindeutige Algorithmen für die beliebtesten Elemente, Gewinner und Verlierer. Die Verwendung ist überall im Report Builder möglich.
* **[!UICONTROL Livestream]**: Wenn Sie einen Stream mit teilweise verarbeiteten Analytics-Daten auf Trefferebene innerhalb von Sekunden nach deren Erfassung benötigen. Hierbei handelt es sich um teilweise verarbeitete Daten, die innerhalb von etwa 30 Sekunden verfügbar sind. Nur für Analytics Premium verfügbar. Benötigt eine Option zur Visualisierung der Daten, üblicherweise mithilfe von Engineering Services.

## Individuelle Lösungen {#custom-solutions}

Engineering Services sollten in folgenden Fällen verwendet werden:

* Die anderen Adobe-Tools entsprechen nicht Ihren Anforderungen.
* Sie benötigen ein individuelles Erlebnis.
* Sie benötigen eine vollständig automatisierte Lösung.
* Sie möchten viele Geräte erreichen.
* Sie verfügen über mehrere Datenquellen.
* Sie haben komplizierte Daten-ETL-Anforderungen (Anforderungen für Extraktion, Transformation und Laden).
* Sie benötigen individuelles Branding.
* Sie möchten [!UICONTROL Analytics-Live-Stream] visualisieren.
