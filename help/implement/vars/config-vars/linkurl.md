---
title: linkURL
description: Überschreibt die automatisch generierte Link-URL, die AppMeasurement bei Linktracking-Aufrufen verwendet.
feature: Appmeasurement Implementation
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
role: Admin, Developer
source-git-commit: 7176e068dd05c5589d741f3194d2ad5d795e017d
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 37%

---

# linkURL

Wenn ein Linktracking-Aufruf an Adobe gesendet wird, erkennt AppMeasurement die angeklickte URL. Diese URL hilft bei der Bestimmung des Link-Typs, z. B. Download-Links und Exitlinks. Verwenden Sie die `linkURL`-Variable, um die erkannte URL zu überschreiben.

Es gibt keine Dimensionen in Analysis Workspace, die Berichte zu dieser Variablen erstellen. Dadurch wird die Spalte `page_event_var1` in [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md) ausgefüllt. Wenn Sie die URL eines angeklickten Links verfolgen möchten, empfiehlt Adobe die Verwendung einer benutzerdefinierten Variablen, z. B. [Prop](../page-vars/prop.md).

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
