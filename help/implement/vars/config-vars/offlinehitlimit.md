---
title: offlineHitLimit
description: Legen Sie die maximale Anzahl von Treffern fest, die zum Offline-Tracking in die Warteschlange gestellt werden sollen.
feature: Appmeasurement Implementation
exl-id: de6478b3-b95f-4edc-8427-7b915a46b3ba
role: Admin, Developer
TQID: https://experienceleague.adobe.com/-uvCAqUO0A-7XjlemN4XwHXVG9DFK-UoVTW77up9-AY
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 39%

---

# offlineHitLimit

Offline-Tracking ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin Ihre Site durchsucht, werden Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät erneut eine Verbindung zum Internet herstellt. Offline-Tracking wird hauptsächlich für mobile Anwendungen verwendet.

Die `offlineHitLimit` Variable legt eine Begrenzung für die Anzahl der Treffer fest, die das Gerät lokal speichert. Diese Variable funktioniert nur, wenn [`trackOffline`](trackoffline.md) aktiviert ist.

## Offline-Treffergrenze bei Verwendung der Web-SDK

Web SDK unterstützt kein Offline-Tracking.

## Offline-Treffergrenze bei Verwendung der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.offlineHitLimit in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.offlineHitLimit` ist eine Ganzzahl, die die maximale Anzahl von Treffern angibt, die ein Gerät speichert, während es offline ist. Wenn diese Variable nicht definiert ist, wird standardmäßig `10` verwendet. Sie können ihn auf einen beliebigen ganzzahligen Wert festlegen. Achten Sie beim Festlegen hoher Werte auf lokale Speicherobergrenzen im Browser eines Besuchers. Dieser Grenzwert beträgt in der Regel 5 bis 10 MB.

```js
s.offlineHitLimit = 100;
```
