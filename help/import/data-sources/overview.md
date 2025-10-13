---
title: Übersicht über Datenquellen
description: Importieren von Daten in Adobe Analytics mithilfe externer Dateien.
exl-id: 5ec8bc51-dfd2-497c-aebc-a32d87efc97e
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Übersicht über Datenquellen

Mit Adobe Analytics-Datenquellen können Sie zusätzliche Online- oder Offline-Daten für die Berichterstellung importieren. Sie sind nützlich, um Facetten Ihres Unternehmens außerhalb Ihrer Website zu verstehen und zu verstehen, wie sie mit Ihrer Site interagieren. Der allgemeine Workflow zur Verwendung von Datenquellen besteht aus den folgenden Schritten:

1. Ihr Unternehmen erfasst Daten aus anderen Quellen. Beispiele sind Daten vor einem Klick, Callcenter-Daten oder Informationen über Transaktionen, die außerhalb Ihrer Site stattgefunden haben.
1. Die Daten werden so formatiert, dass Adobe Analytics sie mithilfe einer durch Tabulatoren getrennten Textdatei versteht.
1. Sie laden die Textdatei zusammen mit einer zugehörigen `.fin` auf eine von Adobe bereitgestellte FTP-Site hoch.
1. Adobe nimmt die Textdatei auf und zeigt diese Daten zusammen mit den auf Ihrer Site erfassten Dimensionen und Metriken an.

Es gibt zwei allgemeine Arten von Datenquellen, die Adobe bietet. Alle Datenquellenvorlagen basieren auf einem der beiden folgenden Typen:

* **Zusammenfassungsdatenquelle**: Bietet eine einfache Möglichkeit zum Importieren von allgemeinen Daten in Adobe Analytics. Sie geben den Zeitstempel, den Variablenwert und die zugehörigen Metriken an. Diese Metriken für jedes Dimensionselement werden dann entsprechend erhöht. Dies ist nützlich, wenn Sie Offline- und Online-Daten nebeneinander sehen möchten. Es werden jedoch keine Online- und Offline-Daten miteinander verknüpft.
* **Transaktions-ID-Datenquelle**: Wenn ein von AppMeasurement gesendeter Treffer und eine Datenquellenzeile übereinstimmende Transaktions-IDs enthalten, hängen die Dimensions- und Metrikwerte in der Datenquelle an diesen Treffer an.

**Datenquellen mit vollständiger Verarbeitung** werden seit dem 25. März 2021 nicht mehr als Datenquellentyp angeboten. Weitere Informationen finden Sie [ Ankündigung ](full-processing-eol.md) Ende der Nutzungsdauer .

Adobe bietet außerdem die [Datenquellen-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/), mit der Sie Datenquellen erstellen und Daten hochladen können, ohne die Produkt-Benutzeroberfläche oder einen FTP-Speicherort zu verwenden.

## Nächste Schritte

[Erste Schritte mit Datenquellen](getting-started.md): Laden Sie eine einfache Datenquelle in eine Entwicklungs-Report Suite hoch.
