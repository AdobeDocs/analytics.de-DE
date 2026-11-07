---
title: Best Practices für die Attribution
description: Machen Sie sich mit den Best Practices vertraut, um zu entscheiden, welches Attributionsmodell verwendet werden soll.
feature: Attribution
exl-id: 92c6039c-f950-4746-8b34-ba18be258c08
TQID: 'https://experienceleague.adobe.com/3h12v3wRMC0SY63jsXBbG6kkTM8ArVOz6ctJVikdKb4'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
subfeature_v2:
  - id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4
    internal-label: Attribution
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 12464bdfe5e8bf2b7b0d253a27b5ad248716731f
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 58%
---
# Best Practices für die Attribution

Welches Attributionsmodell für Ihr Unternehmen am besten geeignet ist, hängt von einer Reihe von Überlegungen ab. In diesem Artikel werden eine Methodik und einige allgemeine Best Practices untersucht:

* [Explorative Analyse](#exploratory-analysis)
* [Regelbasierte Attribution](#rule-based-attribution)
* [Algorithmische Attribution verwenden](#use-algorithmic-attribution)

## Explorative Analyse

>[!NOTE]
>Diese Analyse muss der Entscheidung für ein bestimmtes Attributionsmodell vorangehen.

In dieser vorbereitenden Phase geht es darum, ein Verständnis des Kundenverhaltens zu gewinnen und Konversionsmetriken zu bestimmen. Basierend auf der Konversionsmetrik erleichtern Tools wie [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) (für Rohdaten) oder Analysis Workspace Ihr Verständnis von

* Anzahl der Kundinnen und Kunden, die vor der Konvertierung verschiedene Marketing-Kanäle nutzten
* Der Anteil/die Verteilung dieser Verhaltensweisen

Wenn beispielsweise 50 % der Kunden vor ihrer Konversion über drei Kanäle mit Ihnen in Kontakt kommen, besteht dann eine Interaktion zwischen diesen drei Kanälen?
Um Ihr Verständnis zu erweitern, führen Sie Analysen der oberen und unteren funnel durch.

### Analyse des oberen Ende des Trichters

Bei der Analyse des oberen Endes des Trichters werden diejenigen Kanäle untersucht, die zur Steigerung der Marken- oder Produktbekanntheit dienen. So zielen etwa TV-Werbespots in der Regel auf die Markenbekanntheit ab. Verwenden Sie [&#x200B; Attributionsmodell des Zeitverfalls](/help/analyze/analysis-workspace/attribution/models.md) da Ihre TV-Anzeige im Zeitverlauf aus dem Gedächtnis Ihrer Zielgruppe verschwinden wird.

### Analyse des unteren Ende des Trichters

Bei der Analyse des unteren Trichters geht man davon aus, dass die Menschen bereits von Ihrer Marke wissen und Sie möchten, dass sie konvertieren. Verwenden Sie E-Mail- oder Push-Benachrichtigungen oder Facebook-Anzeigen.

## Regelbasierte Attribution

Dieser Schritt dient der Validierung Ihrer Hypothesen.

**Beispiel 1**

Angenommen, Ihre Hypothese lautet: &quot;*Mein Erstkontaktkanal hat eine größere Auswirkung auf die Konversion als mein Letztkontaktkanal.*&quot;

Verwenden Sie in diesem Fall das [Umgekehrte J-förmige Attributionsmodell](/help/analyze/analysis-workspace/attribution/models.md) um diese Hypothese zu testen. Dieses Modell schreibt dem ersten Kontaktpunkt (bzw. „Touchpoint“) eine Gewichtung von 60 % zu.

**Beispiel 2**

Angenommen, Ihre Hypothese lautet: *„In der Reisebranche beträgt das Attributionsfenster 60 oder 90 Tage, nicht 30, da Kunden vor dem Kauf viel recherchieren.“*

Ändern Sie in diesem Fall Ihr [Lookback-Fenster](/help/analyze/analysis-workspace/attribution/models.md) auf 90 Tage.

## Algorithmische Attribution verwenden

>[!NOTE]
>
>Sie müssen über das Paket **Ultimate** verfügen, um die algorithmische Attribution verwenden zu können. Wenden Sie sich an Ihren Administrator, wenn Sie sich nicht sicher sind, welches Adobe Analytics-Paket Sie haben.

Wenn Sie noch kein Attributionsmodell haben, das alle Ihre Fragen zufriedenstellend beantwortet, können Sie die [algorithmische Attribution](/help/analyze/analysis-workspace/attribution/algorithmic.md) verwenden. Da es sehr schwierig ist, eine große Anzahl möglicher Hypothesen und Kombinationen zu validieren, verwendet die algorithmische Attribution native Algorithmen, um die Punkte auf die einzelnen Dimensionselemente zu verteilen.

## Weiter Überlegungen

* Möglicherweise sollten Sie ergänzend zu Analysis Workspace einen Datenwissenschaftler hinzuziehen.
* Sie können sich auf Rohdaten verlassen, wie in Daten-Feeds von Adobe.
* Erwägen Sie beispielsweise die Verwendung von [&#128279;](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-overview/cja-b2c-overview/cja-overview)Customer Journey Analytics), wenn Sie Ihre Impressionsdaten berücksichtigen möchten.
