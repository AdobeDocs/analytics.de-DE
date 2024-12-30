---
description: Link zur Adobe Analytics-Admin-API auf GitHub.
title: Häufig gestellte Fragen zur Einstellung der Adobe Analytics 1.4-API
feature: Admin Tools
role: Admin
exl-id: 88769032-a7cd-4ca8-958f-3300a4bfe71f
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 4%

---

# Häufig gestellte Fragen zur Einstellung der Adobe Analytics 1.4-API

## Hinweis auf das Ende der Nutzungsdauer (EOL)

**Was ist im Ruhestand?**

* Adobe Analytics 1.4-APIs

* WSSE-Authentifizierung von Adobe Analytics 

**Wann wird es heruntergefahren?**

Diese Services werden am 12. August 2026 eingestellt. Sie werden nach diesem Datum nicht mehr zugänglich sein.

## 1.4 APIs

**Was sind diese Services?**

Die [Adobe Analytics 1.4-APIs](https://developer.adobe.com/analytics-apis/docs/1.4/) sind eine Sammlung von APIs, die eine Vielzahl von Aktionen ermöglichen, z. B. Berichte, Klassifizierungen, Daten-Feeds und Report Suite-Konfigurationen.

**Was muss ich tun, um zu migrieren?**

Die [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/) bieten einen Migrationspfad für 1.4-API-Benutzer. Kunden, die derzeit die 1.4-APIs verwenden, können ihre Integrationen zu den 2.0-APIs migrieren (die gleichen APIs, von denen die Adobe Analytics-Anwendung abhängig ist) und die neuesten Funktionen nutzen.

Mit den 2.0-APIs können Sie fast alle Aktionen ausführen, die Sie in der Analytics-Benutzeroberfläche ausführen können, z. B. das Reporting oder die Verwaltung von Komponenten wie Segmenten und berechneten Metriken.

**Bieten die 2.0-APIs dieselben Funktionen wie die 1.4-APIs?**
Alle Funktionen, die in den 1.4-APIs verfügbar sind, können mithilfe der [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/) erreicht werden. Einige Funktionen bieten dieselben Funktionen wie die 1.4-APIs. Sie bieten dieselbe Möglichkeit zur Durchführung fast jeder Aktion, die Sie in der Analytics-Benutzeroberfläche ausführen können, z. B. Reporting oder Verwaltung von Komponenten wie Segmenten und berechneten Metriken.

## WSSE-Authentifizierung

**Was sind diese Services?**

Die WSSE-Authentifizierung ist ein veraltetes Authentifizierungsprotokoll, das von den Analytics 1.4-APIs unterstützt wird. Sie wurde durch die OAuth-basierten Authentifizierungsoptionen ersetzt, die in der [Adobe Developer Console bereitgestellt ](https://developer.adobe.com/console/home).

**Was muss ich tun, um zu migrieren?**

WSSE-Kundinnen und -Kunden müssen ihre Authentifizierungen aktualisieren, um die in der Adobe Developer Console bereitgestellten Anmeldeinformationen zu verwenden. Melden Sie sich dazu bei der [Adobe Developer Console](https://developer.adobe.com/console/home) an, um ein Projekt für Ihre Analytics 2.0-API-Integration zu erstellen. Wählen Sie zwischen den Authentifizierungsmethoden OAuth-Benutzer und OAuth-Server-zu-Server aus.

## Fragen

F: **Hat dies Auswirkungen auf meine bestehenden Adobe-IO-Projekte für die Analytics-APIs?**

A.: Alle vorhandenen Projekte, die die Analytics 1.4-APIs verwenden, sind betroffen. Diese Integrationen müssen vor Ablauf der Frist für das Ende der Nutzungsdauer ](https://developer.adobe.com/analytics-apis/docs/2.0/) die [Adobe Analytics 2.0-APIs migriert werden.

F: **Ich habe meine Adobe-Anmeldedaten für ein anderes Produkt oder eine andere Anwendung freigegeben, das bzw. die die Analytics-APIs verwendet. Sind sie betroffen?**

A.: Wenn dieses Produkt oder diese Anwendung Ihre WSSE-Anmeldedaten verwendet und/oder die Analytics 1.4-APIs aufruft, ist es betroffen und muss vor Ablauf der Frist migriert werden. Wenden Sie sich an den Produkt- oder Anwendungsanbieter, um weitere Informationen zu seinen Migrationsplänen und zum Zeitplan zu erhalten.

F: **Ich bin mir nicht sicher, welche Adobe Analytics-API wir verwenden.**

A.: Sie können anhand der Adresse, die in Ihrer Integration aufgerufen wird, identifizieren, welche API Sie verwenden.

Sie können auf die Adobe Analytics 1.4-APIs zugreifen, indem Sie eine der folgenden URLs aufrufen:
* https://api.omniture.com
* https://api3.omniture.com
* https://api4.omniture.com
* https://api5.omniture.com

Der Zugriff auf die [Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0/)APIs erfolgt über die folgende URL:
* https://analytics.adobe.io

Wenn Sie api*.omniture.com verwenden, müssen Sie zu den [Adobe Analytics 2.0-APIs} ](https://developer.adobe.com/analytics-apis/docs/2.0/).

F: **Sind die Adobe Analytics 2.0-APIs mit den 1.4-APIs identisch? Wenn nicht, was sind die größten Unterschiede?**

A: Die Adobe Analytics 2.0-APIs sind nicht identisch mit den 1.4-APIs, bieten jedoch vergleichbare Funktionen, einschließlich der folgenden Vorteile:

* Schnellere Antwortzeiten durch einfachere und effizientere Abfragemethoden, wodurch das Abrufen überflüssig wird

* Programmgesteuerte Funktionen für Abfragen und dynamische Berichtsaktualisierungen

* Kontrolliertere Fehlerbehandlung

* Flexible Funktionsweise für alle Aufgaben, die Sie mit Analysis Workspace erledigen können

* Konsistenz und Zuordnung von API-Aufrufen an Benutzeroberflächenaktionen

* Zugriff auf alle in Analysis Workspace verwendeten Attribution IQ-Modelle

* Zugriff auf alle in Analysis Workspace verwendeten Anomalieerkennungsalgorithmen

* Integration mit anderen Experience Cloud-Produkten

* Erhöhte Kapazität für Berichte mit mehreren Aufschlüsselungen

* Zugriff auf die neuesten Analytics-Funktionen

Das [Migrieren zu Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration/) erläutert die wichtigsten Unterschiede zwischen den 1.4- und 2.0-APIs. Weitere Informationen finden Sie auch in den häufig gestellten Fragen zur [ 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/faq/).

F: **Wirkt sich dies auf die Datenerfassung aus?**

A.: Das Ende der Nutzungsdauer von Adobe Analytics 1.4 wirkt sich nicht auf Ihre Tagging-Lösungen wie Tags (ehemals Adobe Launch), WebSDK oder AppMeasurement.js aus. Wenn Sie jedoch die 1.4-Datenquellen- oder Klassifizierungs-APIs zum Erfassen oder Erweitern Ihrer Daten verwenden, müssen Sie diese Workflows zu den Adobe Analytics 2.0-APIs migrieren. Weitere Informationen finden Sie im [2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/)Endpunkthandbuch.

F: **Ist die Dateneinfüge-API betroffen?**

A: Nein, die Dateneinfüge-API ist vom Ende der Nutzungsdauer von Adobe Analytics 1.4 nicht betroffen.

F: **Was kann ich tun, wenn meine Frage in dieser FAQ nicht beantwortet wurde?**

A: Wenn Sie noch Fragen haben, wenden Sie sich bitte an Ihren Adobe-Kundenbetreuer.
