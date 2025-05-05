---
title: Ende der Nutzungsdauer für Datenquellen mit vollständiger Verarbeitung
description: Erfahren Sie mehr über die Mitteilung zum Ende der Nutzungsdauer für Datenquellen mit vollständiger Verarbeitung.
exl-id: 7dd6d518-156f-4bf5-86cb-04d0acc8ff0c
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 4%

---

# Ende der Nutzungsdauer für Datenquellen mit vollständiger Verarbeitung

Datenquellen mit vollständiger Verarbeitung haben es Unternehmen bisher ermöglicht, Daten auf Trefferebene an Adobe Analytics zu senden. Diese Daten wurden auf die gleiche Weise verarbeitet wie Daten, die über herkömmliche Datenerfassungsmittel wie AppMeasurement erfasst wurden. Im Jahr 2020 veröffentlichte Adobe die [Bulk Data Insertion API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/), die dieselben Funktionen wie Full Processing Data Sources ausführt, jedoch mit zusätzlichen Funktionen. Auf dieser Seite finden Sie Details zu zusätzlichen Funktionen, die von der Bulk Data Insertion-API bereitgestellt werden, und beschreiben Unterschiede in Dateiformaten.

Am 25. März 2021 verhinderte Adobe die Erstellung neuer Verbindungen mit Full Processing Data Sources. Am 31. Januar 2022 wurden alle Full Processing Data Services deaktiviert.

## Hauptunterschiede zwischen Full Processing Data Sources und der Bulk Data Insertion-API

* Mit Bulk Data Insertion können Sie mehrere Dateien zur parallelen Verarbeitung übermitteln. Besuchergruppen stellen die Besucherkontinuität und die eVar-Attribution sicher.
* Bulk Data Insertion verfügt über Datenvalidierungs- und Fehlerbehandlungsfunktionen, wodurch ein Teil der Verwaltungsarbeit beim Senden von Trefferdaten entfällt.
* Bulk Data Insertion unterstützt mehrere Methoden zur Besucher-ID-Identifizierung.
* Bulk Data Insertion verfügt über einige zusätzliche erforderliche Felder: eine Besucheridentifizierungsspalte, eine `pageName` (oder ein Link-Äquivalent), `reportSuiteID`, `timestamp` und `userAgent`.
* Um die Besucherkontinuität und -zuordnung sicherzustellen, erfordert das Einfügen von Massendaten, dass Zeilen innerhalb von Dateien in chronologischer Reihenfolge sortiert werden. Weitere Informationen zur dateiübergreifenden Sortierung von Besucheraktivitäten finden Sie unter [Besuchergruppen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/visitor-groups/).
* Bulk Data Insertion erfordert, dass die Dateien im .gzip-Format .csv-komprimiert sind.
* BDIA verwendet `timestamp` anstelle von `date`.

## Variablenvergleich zwischen BDIA und Datenquellen mit vollständiger Verarbeitung

Die folgenden Variablen wurden zum Einfügen von Bulk-Daten eingeführt, die zuvor nicht in Datenquellen mit vollständiger Verarbeitung verfügbar waren:

* **`aamlh`**: Adobe Audience Manager-Standorthinweis.
* **`contextData.key`**: [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md).
* **`customerID`**: Experience Cloud-ID-Dienstvariablen. Umfasst `id`, `authState` und `isMCSeed`.
* **`hints`**: [Client-](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/user-agent-client-hints.html?lang=de)). Umfasst `bitness`, `brands`, `mobile`, `model`, `platform`, `platformversion` und `wow64`.
* **`ipaddress`**: Die IP-Adresse des Besuchers.
* **`language`**: Die Dimension [Sprache](/help/components/dimensions/language.md) .
* **`list1`** - **`list3`**: [Listenvariablen](/help/implement/vars/page-vars/list.md).
* **`marketingCloudVisitorID`**: Die Experience Cloud-ID des Besuchers.
* **`tnta`**: Target-Daten-Payload, die in Integrationen [Analytics for Target“ ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=de) wird.
* **`trackingServer`**: Die [`trackingServer`](/help/implement/vars/config-vars/trackingserver.md).
* **`transactionID`**: Die [`transactionID`](/help/implement/vars/page-vars/transactionid.md).
* **`userAgent`**: Die Benutzeragenten-Zeichenfolge des Geräts.

Die folgenden Variablen werden durch das Einfügen von Bulk-Daten nicht unterstützt:

* **`charSet`**: Die [`charSet`](/help/implement/vars/config-vars/charset.md). Bulk Data Insertion unterstützt nur UTF-8.
* **`timezone`**: Zeitzonenversatz des Besuchers gegenüber GMT in Stunden.
* **`clickAction`**, **`clickActionType`**, **`clickContext`**, **`clickContextType`**, **`clickSourceID`**, **`clickTag`**: Variablen, die beim Activity Map von Datenerfassungen verwendet werden.
