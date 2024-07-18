---
description: Link zur Adobe Analytics-Admin-API auf GitHub.
title: Häufig gestellte Fragen zum Adobe Analytics 1.4 API EOL
feature: Admin Tools
role: Admin
source-git-commit: da96c049f7cfb73496416c2d8a7f4dcbc8f2303e
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 2%

---

# Häufig gestellte Fragen zum Adobe Analytics 1.4 API EOL

## Hinweis zum Ende der Lebensdauer (End of Life, EOL)

**Was wird eingestellt?**

* Adobe Analytics 1.4-APIs

* Adobe Analytics WSSE-Authentifizierung

**Wann wird es heruntergefahren?**

Diese Dienstleistungen werden am 12. August 2026 eingestellt. Nach diesem Datum ist der Zugriff auf sie nicht mehr möglich.

## 1.4 APIs

**Was sind diese Dienste?**

Bei den [Adobe Analytics 1.4-APIs](https://developer.adobe.com/analytics-apis/docs/1.4/) handelt es sich um eine Sammlung von APIs, die eine breite Palette von Aktionen ermöglichen, z. B. Berichte, Klassifizierungen, Daten-Feeds und Report Suite-Konfigurationen.

**Was muss ich tun, um zu migrieren?**

Die [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/) bieten 1.4-API-Benutzern einen Migrationspfad. Kunden, die derzeit die 1.4-APIs verwenden, können ihre Integrationen zu den 2.0-APIs migrieren (von denselben APIs, von denen die Adobe Analytics-Anwendung abhängig ist) und die neuesten Funktionen nutzen.

Mit den 2.0-APIs können Sie fast jede Aktion ausführen, die Sie in der Analytics-Benutzeroberfläche ausführen können, z. B. Berichte oder Verwalten von Komponenten wie Segmenten und berechneten Metriken.

**Bieten die 2.0-APIs dieselben Funktionen wie die 1.4-APIs?**
Alle Funktionen, die in den 1.4-APIs verfügbar sind, können mit den [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/) ausgeführt werden. Einige Funktionen bieten dieselben Funktionen wie die 1.4-APIs. Sie haben die gleichen Möglichkeiten wie Sie fast jede Aktion ausführen können, die Sie in der Analytics-Benutzeroberfläche ausführen können, z. B. Berichte oder Verwaltung von Komponenten wie Segmenten und berechneten Metriken.

## WSSE-Authentifizierung

**Was sind diese Dienste?**

WSSE-Authentifizierung ist ein Legacy-Authentifizierungsprotokoll, das von den Analytics 1.4-APIs unterstützt wird. Sie wurde durch die OAuth-basierten Authentifizierungsoptionen ersetzt, die in der [Adobe Developer Console](https://developer.adobe.com/console/home) bereitgestellt werden.

**Was muss ich tun, um zu migrieren?**

WSSE-Kunden müssen ihre Authentifizierungen aktualisieren, um in der Adobe Developer Console bereitgestellte Anmeldeinformationen zu verwenden. Melden Sie sich dazu bei [Adobe Developer Console](https://developer.adobe.com/console/home) an, um ein Projekt für Ihre Analytics 2.0-API-Integration zu erstellen. Wählen Sie zwischen den Authentifizierungsmethoden OAuth User und OAuth Server-zu-Server .

## Fragen

F: **Hat dies Auswirkungen auf meine bestehenden Adobe IO-Projekte für die Analytics-APIs?**

A: Alle vorhandenen Projekte, die Analytics 1.4-APIs verwenden, sind betroffen. Diese Integrationen müssen vor Ablauf der EOL-Frist in die [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/) migriert werden.

F: **Ich habe meine Adobe-Anmeldeinformationen für ein anderes Produkt oder eine andere Anwendung freigegeben, das bzw. die die Analytics-APIs verwendet. Sind sie betroffen?**

A: Wenn dieses Produkt oder diese Anwendung Ihre WSSE-Berechtigung verwendet und/oder die Analytics 1.4-APIs aufruft, ist dies betroffen und muss vor Ablauf der Frist für die Einstellung der Einstellung für die Einstellung der Unterstützung migriert werden. Weitere Informationen zu Migrationsplänen und -zeitplan erhalten Sie beim Produkt- oder Anwendungsanbieter.

F: **Ich weiß nicht, welche Adobe Analytics-API wir verwenden.**

A: Sie können anhand der in Ihrer Integration aufgerufenen Adresse ermitteln, welche API Sie verwenden.

Der Zugriff auf die Adobe Analytics 1.4-APIs erfolgt über eine der folgenden URLs:
* https://api.omniture.com
* https://api3.omniture.com
* https://api4.omniture.com
* https://api5.omniture.com

Der Zugriff auf die [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/) erfolgt über folgende URL:
* https://analytics.adobe.io

Wenn Sie api*.omniture.com verwenden, müssen Sie zu den [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/) migrieren.

F: **Sind die Adobe Analytics 2.0-APIs mit den 1.4-APIs identisch? Wenn nicht, welche sind die größten Unterschiede?**

A: Die Adobe Analytics 2.0-APIs sind nicht mit den 1.4-APIs identisch, bieten aber vergleichbare Funktionen, darunter die folgenden Vorteile:

* Schnellere Reaktionszeiten mit einfacheren und effizienteren Abfragemethoden, sodass keine Abfrage mehr erforderlich ist

* Programmierbare Funktionen für Abfragen und dynamische Berichtaktualisierungen

* Gängigere Fehlerbehebung

* Flexible Funktionsweise für alles, was Sie mit Analysis Workspace erreichen können

* Konsistenz und Abgleich von API-Aufrufen mit Benutzeroberflächenaktionen

* Zugriff auf alle in Analysis Workspace verwendeten Attribution IQ-Modelle

* Zugriff auf alle in Analysis Workspace verwendeten Anomalieerkennungsalgorithmen

* Die Möglichkeit der Integration mit anderen Experience Cloud-Produkten

* Verbesserte Kapazität für Berichte mit mehreren Aufschlüsselungen

* Zugriff auf die neuesten Analytics-Funktionen

Im Handbuch [Migration zu Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration/) werden die wichtigsten Unterschiede zwischen den 1.4- und 2.0-APIs erläutert. Weitere Informationen finden Sie auch in den [Häufig gestellten Fragen zur Analytics 2.0-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/faq/) .

F: **Hat dies Auswirkungen auf die Datenerfassung?**

A: Das Adobe Analytics 1.4-EOL hat keine Auswirkungen auf Ihre Tagging-Lösungen, wie Tags (früher Adobe Launch), WebSDK oder AppMeasurement.js. Wenn Sie Ihre Daten jedoch mit den Data Sources- oder Classifications-APIs 1.4 erfassen oder erweitern, müssen Sie diese Workflows zu den Adobe Analytics 2.0-APIs migrieren. Weitere Informationen finden Sie im [2.0 API-Endpunkte-Handbuch](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/) .

F: **Ist die Dateneinfüge-API betroffen?**

A: Nein, die Dateneinfüge-API wird von der Adobe Analytics 1.4 EOL nicht beeinflusst.

F: **Was mache ich, wenn meine Frage in diesen häufig gestellten Fragen nicht beantwortet wurde?**

A: Wenn Sie noch Fragen haben, wenden Sie sich an Ihren Adobe-Kundenbetreuer.

