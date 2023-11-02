---
description: Diese Hilfeseite enthält empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Die Tools sollten in der Reihenfolge der Liste verwendet werden. Wenn ein bestimmtes Tool Ihren Anforderungen nicht gerecht wird, wählen Sie stattdessen das nächste in der Liste aus.
title: Welches Adobe Analytics-Tool sollte ich verwenden?
feature: Analytics Basics
exl-id: d65575df-19c6-4129-89c8-d36de7bb6b2f
source-git-commit: 266cf18050d60f08f7e170c56453d1e1d805cb7b
workflow-type: ht
source-wordcount: '1227'
ht-degree: 100%

---

# Welches Adobe Analytics-Tool sollte ich verwenden?

Diese Hilfeseite enthält empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Die Tools sollten in der Reihenfolge der Liste verwendet werden. Wenn ein bestimmtes Tool Ihren Anforderungen nicht gerecht wird, wählen Sie stattdessen das nächste in der Liste aus.

Weitere Informationen zu Adobe Analytics-Produktvergleichen finden Sie unter [Analytics-Produktvergleich](/help/analyze/get-started/analytics-product-comparison.md).

In diesem Video werden verschiedene Adobe Analytics-Tools verglichen:

>[!VIDEO](https://video.tv.adobe.com/v/27220/?quality=12)

## Adobe Analytics-Berichtsoberflächen {#user-interfaces}

**[Analysis Workspace](/help/analyze/analysis-workspace/home.md)** sollte die bevorzugte Benutzeroberfläche für alle Berichts- und Analyseaufgaben sein. Adobe investiert weiterhin in dieses Produkt und gibt monatlich Updates dafür heraus. Können Sie eine Aufgabe nicht mit Analysis Workspace durchführen, versuchen Sie eine der unten stehenden Oberflächen.**

**[Reports &amp; Analytics](/help/analyze/reports-analytics/overview/report-overview.md)** sollte verwendet werden:

* Von Einsteigern, die auf eine vorkonfigurierte Berichterstellung zugreifen müssen, in der einfacher navigiert werden kann.
* Für den Zugriff auf Echtzeitdaten in der Benutzeroberfläche
* Zum Einrichten von Kalenderereignissen
* Zum Einrichten von Zielen
* Für den Zugriff auf eindeutige Videovisualisierungen von Videotagesabschnitten und Zuschauerrückgängen.

>[!IMPORTANT]
>
>Adobe beabsichtigt, Reports &amp; Analytics und die zugehörigen Berichte und Funktionen zum **31. Dezember 2023** einzustellen. Ab diesem Zeitpunkt werden Reports &amp; Analytics und alle zugehörigen Berichte und Zeitpläne nicht mehr funktionieren. Die Berichte, Visualisierungen und zugrunde liegenden Technologien von Reports &amp; Analytics entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Reports &amp; Analytics-Funktionen sind in Analysis Workspace verfügbar. Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen und Leistungsmerkmale von Reports &amp; Analytics in Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In dieser Mitteilung wird der End-of-Life-Prozess erläutert.

Es sollte **[Data Workbench](https://experienceleague.adobe.com/docs/data-workbench/using/home.html?lang=de)** verwendet werden:

* Für prädiktive statistische Modellierung (Tendenzauswertung, Clustering, Korrelationen usw.).
* Für die Latenzanalyse (Zeit vor/seit einem Ereignis).
* Für die Identifikation und den Export komplexer Segmente in Adobe Experience Cloud.

>[!IMPORTANT]
>
>Erfahren Sie mehr über die [Mitteilung zum Ende der Nutzungsdauer](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=de) von Data Workbench.


## Importieren von Daten in Adobe Analytics {#import}

**[Classifications](/help/components/classifications/c-classifications.md)** sollte verwendet werden:

* Wenn Metadaten vorliegen, die Sie einem Erfassungswert (eVar, prop, Marketingkanal) zuweisen möchten.
* Optionen:

   * Rule Builder: verwenden, wenn für eine Variable Werte in einem vorhersagbaren Format erfasst werden, z. B. durch Trennzeichen getrennte Werte. Mit diesem Ansatz können Sie Regeln einmal erstellen, ohne sich später weiter damit beschäftigen zu müssen.
   * Browser-Importtool: verwenden, wenn Sie nicht über vorhersagbare Werte oder über eine begrenzte Liste von Werten verfügen, die eine einmalige Aktualisierung erfordern. Bei diesem Ansatz ist eine fortlaufende Überwachung der Klassifizierungen auf neue Werte nötig.

**[Data Sources](/help/import/data-sources/overview.md)** sollte verwendet werden:

* Wenn Offline-Daten vorliegen, die dauerhaft in Adobe Analytics geschrieben werden sollen.
* Optionen:

   * Zusammenfassung: einfache Datenuploads nach Tag oder anhand von begrenzten Dimensionen.
   * Transaktions-ID: Datenuploads, die einen Online-Endpunkt mit Offlinedaten verknüpfen und importierte Daten vollständig einem online erstellten Besucher-Schnappschuss zuordnen (z. B. online abgeschlossene Bestellungen, die offline zurückgegeben werden).
   * Volle Verarbeitung: Datenquellen mit Zeitstempel, verarbeitet, als ob es sich dabei um einen von Adobe-Servern abgerufenen Treffer handeln würde. D. h. die Daten werden direkt in die Visitor Journey eingefügt.

**[Adobe Exchange-Integrationen](https://www.adobeexchange.com/experiencecloud.html)** sollten verwendet werden:

* Wenn Sie mit einem Drittanbieter interagieren, der eine unterstützte Schnittstelle für Adobe Analytics erstellt hat. Integrations-Mobile-Apps übernehmen meist zusammengefasste Daten automatisch, dauerhaft und wiederholt in Adobe Analytics.

Die **[Data Insertion API](/help/import/c-data-insertion-api/c-data-insertion-api.md)** sollte verwendet werden:

* Wenn Sie Daten in Adobe Analytics laden und den Adobe AppMeasurement- oder mobilen SDK-Code nicht nutzen können.

**[Bulk-Dateneinfüge-API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)**

* Die Data Insertion-API und Bulk Data Insertion-API sind beides Methoden, um Server-seitige Sammlungsdaten an Adobe Analytics zu senden. Aufrufe der Data Insertion-API erfolgen jeweils für ein Ereignis. Die Bulk Data Insertion-API akzeptiert Dateien mit Ereignisdaten im CSV-Format, wobei ein Ereignis pro Zeile angegeben wird. Wenn Sie an einer neuen Implementierung der Server-seitigen Sammlung arbeiten, empfehlen wir die Verwendung der Bulk Data Insertion-API.

**[Kundenattribute](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=de)** sollten verwendet werden:

* Wenn Sie Unternehmenskundendaten in einer Datenbank für Customer Relationship Management (CRM) speichern und die Daten in die Experience Cloud hochladen möchten.
* Wenn Sie CRM-Daten für tiefgreifende Analysen in Analytics oder als Targeting-Kriterien in Adobe Target verwenden möchten.

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)** sollte verwendet werden:

* Wenn Sie Zielgruppendaten von Adobe Audience Manager – wie beispielsweise demografische Daten (z. B. Geschlecht oder Einkommensniveau), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten oder Ad-Impression-Daten – in einen beliebigen Analytics-Workflow einbetten möchten.
* Wenn Sie möchten, dass hochgeladene CRM-Daten zeitbasiert sind, da diese Integration für jeden Treffer Daten an Analytics übermittelt.

## Exportieren von Daten aus Adobe Analytics {#export}

**[Report Builder](/help/analyze/report-builder/home.md)** sollte verwendet werden:

* Wenn die individuellen Layoutoptionen von Workspace zu sehr einschränken (in Report Builder sind sämtliche Optionen möglich, die Excel bietet).
* Zur lockeren Verknüpfung von Benutzereingaben oder Offline-Datenquellen (Impressionen, Kosten) mit Adobe-Daten. Eine dauerhaftere Lösung für das Einbinden von Daten ist Data Sources (siehe „Importieren von Daten in Analytics“).
* Zum Zusammenführen von Daten aus verschiedenen dimensionalen Berichten (z. B. Kombination eines Berichts über Promo-Impressionen mit einem Bericht über den Klick-zu-Konversion-Verlauf bei einer Promo).
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
