---
title: offlineThrottleDelay
description: Legt die Häufigkeit von Treffern fest, wenn ein Gerät wieder online geht.
feature: Appmeasurement Implementation
exl-id: fa484638-bb1f-4df9-9ba1-e9763fa6ad27
role: Admin, Developer
TQID: https://experienceleague.adobe.com/COxmVvMrt0ucZhReX3nYg1Ghacb-LBGcOsX50yzVQrY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 195
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
