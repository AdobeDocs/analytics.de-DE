---
title: Übersicht über Datenquellen
description: Importieren von Daten in Adobe Analytics mithilfe externer Dateien.
exl-id: 5ec8bc51-dfd2-497c-aebc-a32d87efc97e
feature: Data Sources
role: Admin
TQID: 'https://experienceleague.adobe.com/AOl1PUYf4TL0FrYB8eHL-JLiWvz6ixJYKUPpIZEFqj8'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: f46a60da-b0b2-4ca3-bd91-271173f4123d
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 4%

---

# Übersicht über Datenquellen

Sie können Adobe Analytics-Datenquellen nutzen, um zusätzliche Online- oder Offline-Daten für die Berichterstellung zu importieren. Sie sind nützlich, um Facetten Ihres Unternehmens außerhalb Ihrer Website zu verstehen und zu verstehen, wie sie mit Ihrer Site interagieren. Der allgemeine Workflow zur Verwendung von Datenquellen besteht aus den folgenden Schritten:

1. Ihr Unternehmen erfasst Daten aus anderen Quellen. Beispiele sind Daten vor einem Klick, Callcenter-Daten oder Informationen über Transaktionen, die außerhalb Ihrer Site stattgefunden haben.
1. Die Daten werden so formatiert, dass Adobe Analytics sie mithilfe einer durch Tabulatoren getrennten Textdatei versteht.
1. Sie laden die Textdatei zusammen mit einer zugehörigen `.fin` auf eine von Adobe bereitgestellte FTP-Site hoch.
1. Adobe nimmt die Textdatei auf und zeigt diese Daten zusammen mit den auf Ihrer Site erfassten Dimensionen und Metriken an.

Es gibt zwei allgemeine Arten von Datenquellen, die Adobe bietet. Alle Datenquellenvorlagen basieren auf einem der beiden folgenden Typen:

* **Zusammenfassungsdatenquelle**: Bietet eine einfache Möglichkeit zum Importieren von allgemeinen Daten in Adobe Analytics. Sie geben den Zeitstempel, den Variablenwert und die zugehörigen Metriken an. Diese Metriken für jedes Dimensionselement werden dann entsprechend erhöht. Dies ist nützlich, wenn Sie Offline- und Online-Daten nebeneinander sehen möchten. Es werden jedoch keine Online- und Offline-Daten miteinander verknüpft.
* **Transaktions-ID-Datenquelle**: Wenn ein von AppMeasurement gesendeter Treffer und eine Datenquellenzeile übereinstimmende Transaktions-IDs enthalten, hängen die Dimensions- und Metrikwerte in der Datenquelle an diesen Treffer an.

**Datenquellen mit vollständiger Verarbeitung** werden seit dem 25. März 2021 nicht mehr als Datenquellentyp angeboten. Weitere Informationen finden Sie [&#x200B; Ankündigung &#x200B;](full-processing-eol.md) Ende der Nutzungsdauer .

Adobe bietet außerdem die [Datenquellen-API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/), mit der Sie Datenquellen erstellen und Daten hochladen können, ohne die Produkt-Benutzeroberfläche oder einen FTP-Speicherort zu verwenden.

## Nächste Schritte

[Erste Schritte mit Datenquellen](getting-started.md): Laden Sie eine einfache Datenquelle in eine Entwicklungs-Report Suite hoch.
