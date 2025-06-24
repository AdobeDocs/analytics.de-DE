---
title: offlineThrottleDelay
description: Legt die Häufigkeit von Treffern fest, wenn ein Gerät wieder online geht.
feature: Appmeasurement Implementation
exl-id: fa484638-bb1f-4df9-9ba1-e9763fa6ad27
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 83%

---

# offlineThrottleDelay

Offline-Tracking ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin auf Ihrer Website surft, werden die Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät wieder eine Verbindung zum Internet herstellt. Offline-Tracking wird hauptsächlich für mobile Anwendungen verwendet.

Wenn ein Gerät wieder online geht, werden alle auf dem Gerät gespeicherten Treffer an die Adobe-Datenerfassungs-Server gesendet. Eine große Anzahl von Treffern in der Warteschlange kann sich möglicherweise auf die Leistung älterer Geräte auswirken. Verwenden Sie die `offlineThrottleDelay`-Variable, um festzulegen, wie oft Treffer in der Warteschlange an Adobe gesendet werden.

## Offline-Einschränkungsverzögerung mithilfe der Web-SDK

Web SDK unterstützt kein Offline-Tracking.

## Offline-Einschränkungsverzögerung mithilfe der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.offlineThrottleDelay in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.offlineThrottleDelay`-Variable ist eine Ganzzahl, die die Anzahl der Millisekunden angibt, die AppMeasurement zwischen dem Senden von Treffern in der Warteschlange wartet. Der Standardwert lautet `0`, was bedeutet, dass alle Treffer in der Warteschlange gleichzeitig gesendet werden. Wenn diese Variable auf `trackOffline` `false` gesetzt ist, hat sie keine Auswirkung.

```js
s.offlineThrottleDelay = 500;
```
