---
title: bufferRequests
description: Erhöhen Sie die Zuverlässigkeit bei der Erfassung von Linktracking-Anforderungen für Browser, die die Seite sofort entladen.
feature: Variables
exl-id: f103deb4-f449-4325-b1a0-23e58a3c9ba0
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---

# bufferRequests

Mit der `bufferRequests()` -Methode können Sie Bildanforderungen auf der aktuellen Seite zwischenspeichern, anstatt sie an Adobe zu senden. Das Auslösen dieser Methode ist in Szenarien nützlich, in denen ein Browser [`navigator.sendBeacon()`](https://developer.mozilla.org/de-DE/docs/Web/API/Navigator/sendBeacon) nicht unterstützt oder Bildanforderungen anderweitig abbricht, wenn eine Seite entladen wird. Viele Versionen von WebKit-Browsern wie Safari zeigen normalerweise das Verhalten, eine Bildanforderung beim Klicken auf einen Link zu stoppen. Die `bufferRequests()` -Methode ist für alle Versionen von AppMeasurement v2.25.0 oder höher verfügbar.

Wenn Sie [`t()`](t-method.md) oder [`tl()`](tl-method.md) auf einer nachfolgenden Seite in derselben Browsersitzung aufrufen und `bufferRequests()` noch nicht auf dieser Seite aufgerufen wurde, werden alle gepufferten Anforderungen zusätzlich zur Bildanforderung dieser Seite gesendet. Pufferte Anforderungen werden in der richtigen Reihenfolge gesendet, wobei die Bildanforderung der aktuellen Seite zuletzt gesendet wird.

>[!TIP]
>
>Der Zeitstempel der gepufferten Anforderungen wird für die Seite freigegeben, an die Daten gesendet werden. Wenn Sie in der exakten Sekunde, in der eine gepufferte Anforderung aufgezeichnet wird, mehr Präzision wünschen, können Sie die Variable &quot;[`timestamp`](../page-vars/timestamp.md)&quot;für die Seite festlegen, bevor Sie die Anforderung puffern. Wenn Sie diese Variable verwenden, stellen Sie sicher, dass [Zeitstempel optional](/help/technotes/timestamps-optional.md) aktiviert ist - wenn dies nicht der Fall ist, gehen alle Treffer mit Zeitstempel dauerhaft verloren!

## Einschränkungen

Beachten Sie beim Aufrufen der `bufferRequests()` -Methode die folgenden Einschränkungen. Da diese Methode [`Window.sessionStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) verwendet, gelten viele der gleichen Einschränkungen:

* Der Ziel-Link muss sich in derselben Domäne und Subdomäne befinden. Gebuchte Anforderungen funktionieren nicht domänenübergreifend oder unterdomänenübergreifend, auch wenn beide über dieselbe Adobe Analytics-Implementierung verfügen. Diese Einschränkung bedeutet auch, dass Sie gepufferte Anfragen nicht zur Verfolgung von Exitlinks verwenden können.
* Der Ziel-Link muss dasselbe Protokoll wie die aktuelle Seite verwenden. Sie können keine gepufferten Anfragen zwischen HTTP und HTTPS senden.
* Pufferte Anforderungen werden gespeichert, bis Sie `t()` oder `tl()` aufrufen, ohne zuerst `bufferRequests()` aufzurufen, oder bis der Browser oder die Registerkarte geschlossen ist. Wenn eine Browsersitzung beendet wird, bevor Sie diese Daten an Adobe senden können, gehen nicht gesendete gepufferte Anfragen dauerhaft verloren.
* Wenn ein Browser die [Web-Speicher-API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) oder die [JSON-API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON) nicht unterstützt, wird eine Warnung an die Browser-Konsole ausgegeben und AppMeasurement versucht, die Bildanforderung unverzüglich mit der `t()` -Methode zu senden.

## Pufferte Anforderungen im Web SDK

Das Web SDK bietet derzeit keine Möglichkeit zum Puffern von Anforderungen.

## Pufferte Anforderungen mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.bufferRequests() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die Methode `bufferRequests()` auf, bevor Sie `t()` oder `tl()` aufrufen. Wenn `bufferRequests()` aufgerufen wird, werden nachfolgende Tracking-Aufrufe in die Sitzungsspeicherung geschrieben und nicht an Adobe-Datenerfassungsserver gesendet.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// Flag the request to be buffered
s.bufferRequests();

// The t() or tl() method then writes the data to session storage instead of sending it to Adobe
s.tl(true,"o","Example link click");

// On a subsequent page, the tracking call sends both the above link tracking call and the page view call
s.t();
```
