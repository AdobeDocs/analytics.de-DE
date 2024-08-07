---
title: Datenquellen - Übersicht
description: Importieren Sie Daten mithilfe externer Dateien in Adobe Analytics.
exl-id: 5ec8bc51-dfd2-497c-aebc-a32d87efc97e
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Datenquellen - Übersicht

Mit Adobe Analytics-Datenquellen können Sie zusätzliche Online- oder Offline-Daten für die Berichterstellung importieren. Sie sind nützlich, um Facetten Ihres Unternehmens außerhalb Ihrer Website zu verstehen und zu verstehen, wie sie mit Ihrer Site interagieren. Der allgemeine Workflow zur Verwendung von Datenquellen umfasst die folgenden Schritte:

1. Ihr Unternehmen erfasst Daten aus anderen Quellen. Beispiele sind Daten vor dem Klick, Callcenter-Daten oder Informationen zu Transaktionen, die außerhalb Ihrer Site aufgetreten sind.
1. Die Formatierung der Daten erfolgt so, dass Adobe Analytics die Verwendung einer tabulatorgetrennten Textdatei versteht.
1. Sie laden die Textdatei zusammen mit der zugehörigen `.fin` -Datei auf eine FTP-Site-Adobe hoch.
1. Adobe erfasst die Textdatei und zeigt diese Daten neben Dimensionen und Metriken an, die auf Ihrer Site erfasst wurden.

Es gibt zwei allgemeine Arten von Datenquellen, die Adobe anbietet. Alle Datenquellenvorlagen basieren auf einem dieser beiden Typen:

* **Zusammenfassungsdatenquelle**: Bietet eine einfache Möglichkeit, allgemeine Daten in Adobe Analytics zu importieren. Sie geben den Zeitstempel, den Variablenwert und die zugehörigen Metriken an. Diese Metriken für jedes Dimensionselement werden dann entsprechend erhöht. Dies ist nützlich, wenn Sie Offline- und Online-Daten nebeneinander anzeigen möchten. Es werden jedoch keine Online- und Offline-Daten miteinander verknüpft.
* **Transaktions-ID-Datenquelle**: Wenn ein von AppMeasurement gesendeter Treffer und eine Datenquellenzeile übereinstimmende Transaktions-IDs enthalten, werden die Dimensions- und Metrikwerte in der Datenquelle an diesen Treffer angehängt.

**Datenquellen mit vollständiger Verarbeitung** werden ab dem 25. März 2021 nicht mehr als Datenquellentyp angeboten. Weitere Informationen finden Sie in der [Mitteilung über das Ende der Lebensdauer](full-processing-eol.md) .

Adobe bietet außerdem die [Datenquellen-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/), mit der Sie Datenquellen erstellen und Daten hochladen können, ohne die Produkt-Benutzeroberfläche oder einen FTP-Speicherort zu verwenden.

## Nächste Schritte

[Erste Schritte mit Datenquellen](getting-started.md): Laden Sie eine einfache Datenquelle in eine Entwicklungs-Report Suite hoch.
