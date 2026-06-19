---
title: Dimensionen – Überblick
description: Erfahren Sie, was Dimensionen sind und wie sie in Adobe Analytics verwendet werden.
feature: Dimensions
exl-id: dc00e06a-fdb5-40e3-82e2-269bad3b3677
TQID: https://experienceleague.adobe.com/WypIneraYlrSyIpXv3UQWIFn42A-Dxi0SxeJ2VbeubQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 37%

---

# Dimensionen – Übersicht

Dimensionen sind Variablen in Adobe Analytics, die normalerweise Zeichenfolgenwerte enthalten. Zu den gebräuchlichen Dimensionen gehören [Seite](page.md), [Referrer-Domäne](referring-domain.md) oder eine [eVar](evar.md). Im Gegensatz dazu enthalten [Metriken](../metrics/overview.md) numerische Werte, die mit einer Dimension verknüpft sind. Ein Basisbericht zeigt Zeilen mit Zeichenfolgenwerten (Dimension) gegen eine Spalte mit numerischen Werten (Metrik) an.

Wenn Sie beispielsweise die Dimension **[!UICONTROL Seite]** mit der Metrik **[!UICONTROL Besuche]** kombinieren, erhalten Sie einen Rangbericht, der Ihre am häufigsten besuchten Seiten anzeigt:

| Seite | Besuche |
| --- | ---: |
| Startseite | 800 |
| Produktseite | 500 |
| Kaufseite | 100 |

{style="table-layout:fixed"}

Jede Dimension stellt einen anderen Teil oder eine andere Facette Ihrer Site dar. Sie können eine oder mehrere dieser Dimensionen mit einer oder mehreren Metriken kombinieren, um einen gewünschten Bericht zu erstellen.

## Hinzufügen von Dimensionsbeschreibungen

Analytics-Admins können Beschreibungen für Dimensionen und andere Komponenten entweder innerhalb der Report Suite oder direkt in Analysis Workspace hinzufügen. Informationen zum Hinzufügen von Beschreibungen zu Dimensionen finden Sie unter [Hinzufügen von Komponentenbeschreibungen](/help/analyze/analysis-workspace/components/add-component-descriptions.md).

## Eingestellte Dimensionen

Die folgenden Dimensionen wurden eingestellt. Bei den meisten handelte es sich um Reports &amp; Analytics-Berichte, die nicht in Analysis Workspace verfügbar sind. Sie werden hier als Referenz dokumentiert, wenn Sie sie in veralteten Berichten oder historischen Daten sehen.

* **Hierarchie**: Eine benutzerdefinierte Dimension (`hier1`-`hier5`), mit der die hierarchische Struktur einer Site für das Reporting erfasst wird. Es ist nicht mehr verfügbar und in Analysis Workspace nicht mehr verfügbar. Verwenden Sie stattdessen [eVars](evar.md) und Klassifizierungen.
* **Startseite**: Eine Markierung, die angibt, ob die aktuelle Seite die Browser-Startseite des Besuchers war. Es handelt sich um eine veraltete Dimension ohne modernes Äquivalent aufgrund moderner Datenschutzpraktiken für Browser.
* **JavaScript-Unterstützung**: Gibt an, ob der Browser des Besuchers JavaScript unterstützt. Eine Legacy-Dimension, die für moderne Messungen nicht mehr sinnvoll ist.
* **JavaScript-Version**: Gibt die JavaScript-Version an, die vom Browser des Besuchers unterstützt wird. Eine alte Dimension, die nicht mehr erfasst wird.
* **Nächste Seite**: Eine Pfaddimension, die die nächste Seite anzeigt, die eine Besucherin oder ein Besucher angesehen hat. Verwenden Sie die [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) in Analysis Workspace für aktuelle Pfaddimensionen.
* **Vorherige Seite**: Eine Pfaddimension, die die vorherige Seite anzeigt, die eine Besucherin oder ein Besucher angesehen hat. Verwenden Sie die [Flussvisualisierung](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md) in Analysis Workspace für aktuelle Pfaddimensionen.
* **Zeitzone**: Die Zeitzone des Besuchers, abgeleitet vom Zeitstempelversatz in AppMeasurement-Bildanforderungen. Web SDK erfasst die Zeitzone mithilfe von [`placeContext`](https://experienceleague.adobe.com/de/docs/experience-platform/collection/js/commands/configure/context).
* **Domain auf oberster Ebene**: Die Domain auf oberster Ebene des Zugriffspunkts des Besuchers. Ein veralteter Reports &amp; Analytics-Bericht; verwenden Sie stattdessen die Dimension [Domain](domain.md) .
* **Besuchsnummer**: Die Seitennummer innerhalb eines Besuchs. Ein alter Reports &amp; Analytics-Bericht; verwenden Sie stattdessen die Dimension [Treffertiefe](hit-depth.md) .
* **Besucherstatus**: Gibt den US-Bundesstaat aus der `s.state`-Variablen an. Sie wird zugunsten der Dimension [US-Bundesstaaten“ &#x200B;](us-states.md), die Geosegmentierung verwendet.
