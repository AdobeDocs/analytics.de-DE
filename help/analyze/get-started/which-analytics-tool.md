---
description: Auf dieser Hilfeseite finden Sie empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Tools sollten in der Reihenfolge berücksichtigt werden, in der sie aufgeführt sind. Wenn ein bestimmtes Tool nicht den Anforderungen entspricht, wechseln Sie zum nächsten Tool, um weitere Informationen zu erhalten.
title: Welches Adobe Analytics-Tool sollte ich verwenden?
feature: Analytics Basics
exl-id: d65575df-19c6-4129-89c8-d36de7bb6b2f
TQID: https://experienceleague.adobe.com/xk485fKU7Q2DeZIYaTtN-a4JKnyVamAygW03z7ffAOk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: a421fb65-2c82-457a-921c-28c46b697a39id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7id: f73667dc-d296-4875-8975-ac3fdc3adc42id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: ef60b66e-5984-4336-ba72-6d978b1b6f87
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: c2ae876122715b4fa6367326dc23479dd9648021
workflow-type: tm+mt
source-wordcount: 1175
ht-degree: 67%

---

# Welches Adobe Analytics-Tool sollte ich verwenden?

Auf dieser Hilfeseite finden Sie empfohlene Anwendungsfälle für jedes Adobe Analytics-Tool. Tools sollten in der Reihenfolge berücksichtigt werden, in der sie aufgeführt sind. Wenn ein bestimmtes Tool nicht den Anforderungen entspricht, wechseln Sie zum nächsten Tool, um weitere Informationen zu erhalten.

Weitere Informationen zu Adobe Analytics-Produktvergleichen finden Sie unter [Analytics-Produktvergleich](/help/analyze/get-started/analytics-product-comparison.md).


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Vergleich von Tools](https://video.tv.adobe.com/v/27220?quality=12&learn=on){target="_blank"} finden Sie ein Demovideo.

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

* Wenn Sie Enterprise-Kundendaten in einer CRM-Datenbank (Customer Relationship Management) erfassen und diese Daten in CX Enterprise hochladen möchten.
* Wenn Sie CRM-Daten für eine tiefer gehende Analyse in Analytics oder als Targeting-Kriterien in Adobe Target verwenden möchten.

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)** sollte verwendet werden:

* Wenn Sie Zielgruppendaten von Adobe Audience Manager – wie beispielsweise demografische Daten (z. B. Geschlecht oder Einkommensniveau), psychografische Informationen (z. B. Interessen und Hobbys), CRM-Daten oder Ad-Impression-Daten – in einen beliebigen Analytics-Workflow einbetten möchten.
* Wenn hochgeladene CRM-Daten zeitbasiert sein sollen, da diese Integration neue Informationen per Treffer an Analytics sendet.

## Exportieren von Daten aus Adobe Analytics {#export}

**[Report Builder](/help/analyze/report-builder/rb-overview.md)** sollte verwendet werden:

* Wenn die angepassten Layout-Optionen von Workspace begrenzt sind (alles ist in Report Builder möglich, innerhalb der Grenzen von Excel).
* So binden Sie Benutzereingaben oder Offline-Datenquellen (Impressions, Kosten) lose an Adobe-Daten an. Eine dauerhaftere Lösung für das Einbinden von Daten sind Datenquellen (siehe „Importieren von Daten in Analytics“).
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

* Um den detailliertesten Daten-Feed zu nutzen, den wir bereitstellen können (Besucher-ID, Treffer).
* Wenn der Client Adobe-Daten in einer Client-seitigen Datenbank speichern möchte, können wir sie auf der detailliertesten Ebene senden.
* Wenn der Client ein Business Intelligence-Tool (BI) entwickeln oder Adobe-Daten auf Trefferebene in ein Tool eines Drittanbieters eingeben möchte.

**[Reporting-APIs](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/reporting-guide.md)** sollten verwendet werden, wenn die anderen Visualisierungsoptionen Ihren Anforderungen nicht gerecht werden. Zu den drei API-Optionen gehören:

* **Vollständig verarbeitet**: wenn Sie funktionsreiche Daten benötigen (einschließlich Besuche, Besucher und Segmente). Dies sind in der Regel zusammengefasste Daten der Analytics-Benutzeroberfläche, die in ~30-90 Minuten verfügbar sind. Kann über Report Builder verwendet werden.
* **Echtzeit**: wenn Sie einige Metriken und Dimensionen mit einer Latenz von Sekunden anzeigen möchten. Dies sind begrenzte, teilweise verarbeitete, zusammengefasste Daten, die innerhalb von ~30 Sekunden verfügbar sind. Enthält eindeutige Algorithmen der beliebtesten, Gewinner und Verlierer. Kann über Report Builder verwendet werden.
* **[!UICONTROL Livestream]**: Wenn Sie einen Stream mit teilweise verarbeiteten Analytics-Daten auf Trefferebene innerhalb von Sekunden nach deren Erfassung benötigen. Dies sind teilweise verarbeitete Daten, die innerhalb von ~30 Sekunden verfügbar sind. Nur für Analytics Premium verfügbar. Erfordert eine Möglichkeit zur Visualisierung der Daten, normalerweise durch eine Engineering Services-Interaktion.

## Individuelle Lösungen {#custom-solutions}

Engineering Services sollten in folgenden Fällen verwendet werden:

* Die anderen Adobe-Tools entsprechen nicht Ihren Anforderungen.
* Sie möchten ein benutzerdefiniertes Erlebnis.
* Sie wollen eine vollautomatisierte Lösung.
* Man will viele Geräte erreichen.
* Es gibt mehrere Datenquellen.
* Sie haben komplexe ETL-Anforderungen (Extract-Transform-Load) für Daten.
* Sie möchten benutzerdefiniertes Branding.
* Sie möchten &quot;[!UICONTROL  Live Stream“ ].
