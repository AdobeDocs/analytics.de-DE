---
title: offlineHitLimit
description: Legen Sie die maximale Anzahl von Treffern fest, die zum Offline-Tracking in die Warteschlange gestellt werden sollen.
feature: Variables
exl-id: de6478b3-b95f-4edc-8427-7b915a46b3ba
role: Admin, Developer
source-git-commit: 8bc5e649c5b5852232f4baddcddad0766bc1569a
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 39%

---

# offlineHitLimit

Offline-Tracking ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin Ihre Site durchsucht, werden Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät erneut eine Verbindung zum Internet herstellt. Offline-Tracking wird hauptsächlich für mobile Anwendungen verwendet.

Die `offlineHitLimit` Variable legt eine Obergrenze für die Anzahl der Treffer fest, die das Gerät lokal speichert. Diese Variable funktioniert nur, wenn [`trackOffline`](trackoffline.md) aktiviert ist.

## Offline-Treffergrenze bei Verwendung der Web-SDK

Web SDK unterstützt kein Offline-Tracking.

## Offline-Treffergrenze bei Verwendung der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.offlineHitLimit auf AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.offlineHitLimit` ist eine Ganzzahl, die die maximale Anzahl von Treffern angibt, die ein Gerät speichert, während es offline ist. Wenn diese Variable nicht definiert ist, wird standardmäßig `10` verwendet. Sie können ihn auf einen beliebigen ganzzahligen Wert festlegen. Achten Sie beim Festlegen hoher Werte auf lokale Speicherobergrenzen im Browser eines Besuchers. Dieser Grenzwert beträgt in der Regel 5 bis 10 MB.

```js
s.offlineHitLimit = 100;
```
