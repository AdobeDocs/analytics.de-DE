---
title: linkURL
description: Überschreibt die automatisch generierte Link-URL, die AppMeasurement bei Linktracking-Aufrufen verwendet.
feature: Appmeasurement Implementation
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
role: Admin, Developer
TQID: https://experienceleague.adobe.com/O8Bd28njZQDnffeUwCiNGNSNRHk4FU-z48r4pt7Eths
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 34%

---

# linkURL

Wenn ein Linktracking-Aufruf an Adobe gesendet wird, erkennt AppMeasurement die angeklickte URL. Diese URL hilft bei der Bestimmung des Link-Typs, z. B. Download-Links und Exitlinks. Verwenden Sie die `linkURL`-Variable, um die erkannte URL zu überschreiben.

Es gibt keine Dimensionen in Analysis Workspace, die Berichte zu dieser Variablen erstellen. Dadurch wird die Spalte `page_event_var1` in [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) ausgefüllt. Wenn Sie die URL eines angeklickten Links verfolgen möchten, empfiehlt Adobe die Verwendung einer benutzerdefinierten Variablen, z. B. [Prop](../page-vars/prop.md). Die Verwendung von [Activity Map](/help/analyze/activity-map/overview.md) kann dazu beitragen, die Datenerfassung für angeklickte Links zu optimieren.

## Link-URL unter Verwendung der Web-SDK

Die Link-URL ist den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `web.webInteraction.URL`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.linkURL` oder `data.__adobe.analytics.pev1`

## Link-URL mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.linkURL in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.linkURL`-Variable ist eine Zeichenfolge, die die vollständige URL des angeklickten Links enthält. Diese Variable füllt keine in Berichten verfügbaren Dimensionen.

```js
s.linkURL = "https://example.com";
```

Wenn das dritte Argument der Methode [tl()](../functions/tl-method.md) nicht angegeben wird, wird stattdessen die Variable `linkURL` verwendet.
