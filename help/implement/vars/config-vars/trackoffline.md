---
title: trackOffline
description: Aktivieren oder deaktivieren Sie Offline-Tracking, wodurch sich die Datenerfassung in AppMeasurement ändert.
feature: Appmeasurement Implementation
exl-id: 23a17ddc-01e6-42b6-81b0-c60f15a07231
role: Admin, Developer
TQID: https://experienceleague.adobe.com/xAeUI6N625MJfnAWWO53NkBe4IKxI-i703vHHoxpuzg
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
source-wordcount: 283
ht-degree: 89%

---

# trackOffline

Offline-Tracking ist eine optionale Methode zur Datenerfassung in Adobe Analytics. Wenn ein Besucher die Verbindung zum Internet trennt, aber weiterhin auf Ihrer Website surft, werden die Treffer in einer Offline-Warteschlange gespeichert, bis das Gerät wieder eine Verbindung zum Internet herstellt. Offline-Tracking wird hauptsächlich für mobile Anwendungen verwendet.

Die `trackOffline`-Variable bestimmt, ob Sie Offline-Tracking in Ihrer Implementierung verwenden möchten.

>[!WARNING]
>
>Sie müssen Ihre Report Suite so konfigurieren, dass sie Treffer mit Zeitstempel akzeptiert, bevor Sie diese Variable aktivieren. Wenn eine Report Suite keine Treffer mit Zeitstempel akzeptiert und diese Variable aktiviert ist, gehen diese Daten verloren und können nicht wiederhergestellt werden.

Wenn diese Option aktiviert ist, verwendet AppMeasurement den folgenden Prozess zum Senden von Daten an Adobe:

* Beim Kompilieren einer Bildanforderung wird ein Abfragezeichenfolgenparameter für Zeitstempel eingefügt.
* Wenn das Gerät nicht auf Adobe-Datenerfassungs-Server zugreifen kann, wird der Treffer lokal auf dem Gerät gespeichert.
* Bei jedem nachfolgenden Treffer versucht AppMeasurement, eine Bildanforderung an Adobe zu senden.
   * Wenn nicht auf Adobe-Datenerfassungs-Server zugegriffen werden kann, wird der Treffer Warteschlange auf dem Gerät hinzugefügt.
   * Wenn auf Adobe-Datenerfassungs-Server zugegriffen werden kann, werden der Treffer und die Warteschlange der Treffer gesendet, während das Gerät offline war.

## Offline-Tracking mit der Web-SDK

Web SDK unterstützt kein Offline-Tracking.

## Offline-Tracking mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.trackOffline in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.trackOffline`-Variable ist ein boolescher Wert, der Offline-Tracking aktiviert oder deaktiviert. Der Standardwert lautet `false`. Setzen Sie diesen Wert auf `true`, wenn Sie Offline-Tracking aktivieren möchten.

```js
s.trackOffline = true;
```
