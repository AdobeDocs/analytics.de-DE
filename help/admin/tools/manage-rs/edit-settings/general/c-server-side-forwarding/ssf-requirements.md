---
description: Sie müssen diese Experience Cloud-Lösungs-, Service- und Code-Anforderungen erfüllen, um die Server-seitige Weiterleitung zu implementieren. Diese Anforderungen enthalten auch Anweisungen dazu, wie Sie nach Codeversionen suchen und wo Sie die neuesten Code-Bibliotheken erhalten.
solution: Analytics
title: Anforderungen an die serverseitige Weiterleitung
feature: Report Suite Settings
exl-id: af0cf85a-381e-46d2-a4fd-9a5b073c8a8d
role: Admin
TQID: https://experienceleague.adobe.com/1GCflxlY4IpT-pPTr93FuOmxkJLC4baJe3Z2SGjj1So
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 326
ht-degree: 63%

---

# Anforderungen an die serverseitige Weiterleitung

Sie müssen diese Experience Cloud-Lösungs-, Service- und Code-Anforderungen erfüllen, um die Server-seitige Weiterleitung zu implementieren. Diese Anforderungen enthalten auch Anweisungen dazu, wie Sie nach Codeversionen suchen und wo Sie die neuesten Code-Bibliotheken erhalten.

## Lösungsanforderungen

Die serverseitige Weiterleitung funktioniert mit [Analytics](https://www.adobe.com/de/data-analytics-cloud/analytics.html) und [Audience Manager](https://www.adobe.com/de/analytics/audience-manager.html) und/oder [Zielgruppen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de).

## Dienstanforderungen

Die serverseitige Weiterleitung erfordert den [Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de). Identity Service bietet eine universelle ID zum Identifizieren der Site-Besucher über alle Experience Cloud-Lösungen hinweg. Sie müssen den ID-Dienst implementieren, bevor die serverseitige Weiterleitung funktioniert.

## Codeversionen

Für die Server-seitige Weiterleitung ist Version 1.5 (oder höher) der unten aufgeführten Code-Bibliotheken erforderlich. Als Best Practice wird empfohlen, anstelle der erforderlichen Mindestanforderungen die neuesten Versionen zu verwenden.

* `AppMeasurement.js`
* `AppMeasurement_Module_AudienceManagement.js`
* `VistorAPI.js`

### Bestimmen der Version der Codebibliothek

Jedes Tool, das die von einem Browser ausgelösten HTTP-Anfragen überwacht. kann die Versionsnummer für den AppMeasurement und Visitor API-Code anzeigen. `AppMeasurement_Module_AudienceManagement.js` enthält keine Versions-ID und gibt keine Versions-ID zurück. In den folgenden Beispielen wird veranschaulicht, wie die Versions-IDs für `AppMeasurement.js`- und `VisitorAPI.js`-Code aussehen.

* `AppMeasurement.js`: Der [Adobe Debugger](/help/implement/validate/debugger.md) gibt die AppMeasurement-Version wie folgt zurück: `Version of Code | JS-1.5.1`. In anderen Tools wird möglicherweise eine andere Kennzeichnung verwendet, der Wert folgt jedoch immer dem Muster `JS-X.X.X`, wobei `X` einer Versionsnummer entspricht.
* `VisitorAPI.js`: Suchen Sie nach dem Parameter `d_visid_ver`. Er gibt den Besucher-ID-Dienst wie folgt an: `d_visid_ver: 1.5.5`. Besucher-API-Code, der älter als Version 1.5.2 ist, enthielt keine Versionsnummer. Sie verwenden wahrscheinlich eine ältere Code-Bibliothek (und müssen ein Upgrade durchführen), wenn Ihre Überwachungsergebnisse keine Versionsnummer zurückgeben.
