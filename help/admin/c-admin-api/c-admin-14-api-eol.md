---
description: Details zur Mitteilung zum Ende der Nutzungsdauer der Adobe Analytics 1.4-API.
title: Häufig gestellte Fragen zur Einstellung der Adobe Analytics 1.4-API
feature: Admin Tools
role: Admin
exl-id: 88769032-a7cd-4ca8-958f-3300a4bfe71f
source-git-commit: 73c0210ac931f3e7f823e033a3bffdc22e159ddb
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 4%

---

# Häufig gestellte Fragen zur Einstellung der Adobe Analytics 1.4-API

Adobe plant, die Adobe Analytics 1.4-API am **. August 2026**. Sie werden nach diesem Datum nicht mehr zugänglich sein. Diese Ankündigung wirkt sich direkt auf Folgendes aus:

* Adobe Analytics 1.4-APIs, mit Ausnahme der Data Insertion-API
* WSSE-Authentifizierung von Adobe Analytics 

## 1.4 APIs

Die [Adobe Analytics 1.4-](https://developer.adobe.com/analytics-apis/docs/1.4/) bieten eine breite Palette von Aktionen, z. B. Berichte, Klassifizierungen, Daten-Feeds und Report Suite-Konfigurationen. Sie werden zugunsten der [Adobe Analytics 2.0-APIs eingestellt](https://developer.adobe.com/analytics-apis/docs/2.0/). Mit den 2.0-APIs können Sie fast alle Aktionen ausführen, die Sie in der Analytics-Benutzeroberfläche ausführen können, z. B. das Reporting oder die Verwaltung von Komponenten wie Segmenten und berechneten Metriken.

Adobe bietet einen [Migrationspfad](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration/) für 1.4-API-Benutzer. Sie können Ihre Integrationen zu den 2.0-APIs (den APIs, von denen die Adobe Analytics-Anwendung abhängig ist) migrieren und die neuesten Funktionen nutzen. Alle Funktionen, die in den 1.4-APIs verfügbar sind, können mit den [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/) erreicht werden.

## WSSE-Authentifizierung

Die WSSE-Authentifizierung ist ein veraltetes Authentifizierungsprotokoll, das von den Analytics 1.4-APIs unterstützt wird. Sie wurde durch die OAuth-basierten Authentifizierungsoptionen ersetzt, die in der [Adobe Developer Console bereitgestellt ](https://developer.adobe.com/console/home). Projekte, die die WSSE-Authentifizierung verwenden, müssen ihre Anmeldeinformationen auf die in der Adobe Developer Console bereitgestellten aktualisieren. Melden Sie sich dazu bei der [Adobe Developer Console](https://developer.adobe.com/console/home) an, um ein Projekt für Ihre Analytics 2.0-API-Integration zu erstellen. Wählen Sie entweder die Authentifizierungsmethode OAuth-Benutzer oder OAuth-Server-zu-Server aus.

## Häufig gestellte Fragen

+++**Hat dies Auswirkungen auf meine bestehenden Adobe IO-Projekte für die Analytics-APIs?**

Alle vorhandenen Projekte, die die Analytics 1.4-APIs verwenden, sind betroffen. Diese Integrationen müssen vor Ablauf der Frist für das Ende der Nutzungsdauer [&#128279;](https://developer.adobe.com/analytics-apis/docs/2.0/) die Adobe Analytics 2.0-APIs migriert werden.

+++

+++**Ich habe meine Adobe-Anmeldedaten für ein anderes Produkt oder eine andere Anwendung freigegeben, das bzw. die die Analytics-APIs verwendet. Sind sie betroffen?**

Wenn dieses Produkt oder diese Anwendung Ihre WSSE-Anmeldeinformationen verwendet und/oder die Analytics 1.4-APIs aufruft, ist es betroffen und muss vor Ablauf der Frist migriert werden. Wenden Sie sich an den Produkt- oder Anwendungsanbieter, um weitere Informationen zu seinen Migrationsplänen und zum Zeitplan zu erhalten.

+++

+++**Wie kann ich feststellen, welche API mein Projekt verwendet?**

Die Basis-URL, die die API aufruft, bestimmt, welche API-Version Ihr Projekt verwendet. Die Adobe Analytics 1.4-APIs verwenden die folgenden URLs:
* `https://api.omniture.com`
* `https://api3.omniture.com`
* `https://api4.omniture.com`
* `https://api5.omniture.com`

Die [Adobe Analytics 2.0-](https://developer.adobe.com/analytics-apis/docs/2.0/) verwenden die folgende URL:

* `https://analytics.adobe.io`

Wenn eines Ihrer API-Projekte `api*.omniture.com` verwendet, verwendet es die Adobe Analytics 1.4-APIs und muss zu den 2.0-APIs migrieren.

+++

+++**Hat dieses Ende der Nutzungsdauer Auswirkungen auf die Datenerfassung?**

Das Ende der Nutzungsdauer von Adobe Analytics 1.4 wirkt sich nicht auf Ihre Tagging-Lösungen aus, z. B. Tags (ehemals Adobe Launch), Web SDK oder AppMeasurement. Wenn Sie jedoch die 1.4-Datenquellen- oder Klassifizierungs-APIs zur Verbesserung Ihrer Daten verwenden, müssen Sie diese Workflows zu den Adobe Analytics 2.0-APIs migrieren.

Die Dateneinfüge-API ist von dieser Mitteilung zum Ende der Nutzungsdauer nicht betroffen. Während Adobe plant, die Dateneinfüge-API weiterhin zu unterstützen, empfiehlt Adobe stattdessen die Verwendung [Bulk Data Insertion-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/).

+++

Wenn Sie weitere Fragen zu dieser Mitteilung zum Ende der Nutzungsdauer haben, die auf dieser Seite nicht beantwortet werden, wenden Sie sich an Ihr Adobe Account Team.
