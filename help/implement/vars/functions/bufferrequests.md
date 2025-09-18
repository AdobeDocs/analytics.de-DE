---
title: bufferRequests
description: Erhöhen Sie die Zuverlässigkeit der Erfassung von Linktracking-Anfragen für Browser, die die Seite sofort entladen.
feature: Appmeasurement Implementation
exl-id: f103deb4-f449-4325-b1a0-23e58a3c9ba0
role: Admin, Developer
source-git-commit: 325c035c0b5a9cc828be22ef7781d3b67f104476
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---

# bufferRequests

Mit der `bufferRequests()`-Methode können Sie Bildanforderungen auf der aktuellen Seite zwischenspeichern, anstatt sie an Adobe zu senden. Das Auslösen dieser Methode ist in Szenarien nützlich, in denen ein Browser [`navigator.sendBeacon()`](https://developer.mozilla.org/de-DE/docs/Web/API/Navigator/sendBeacon) nicht unterstützt oder Bildanfragen anderweitig abbricht, wenn eine Seite entladen wird. Viele Versionen von WebKit-Browsern, wie Safari, zeigen häufig das Verhalten, eine Bildanforderung beim Klicken auf einen Link anzuhalten. Die `bufferRequests()` ist in allen Versionen von AppMeasurement v2.25.0 oder höher verfügbar.

Wenn Sie [`t()`](t-method.md) oder [`tl()`](tl-method.md) auf einer nachfolgenden Seite in derselben Browser-Sitzung aufrufen und `bufferRequests()` noch nicht auf dieser Seite aufgerufen wurde, werden alle gepufferten Anfragen zusätzlich zur Bildanforderung dieser Seite gesendet. Gepufferte Anforderungen werden in der richtigen Reihenfolge gesendet, wobei die Bildanforderung der aktuellen Seite zuletzt gesendet wird.

>[!TIP]
>
>Der Zeitstempel gepufferter Anfragen wird für die Seite freigegeben, an die Daten gesendet werden. Wenn Sie mehr Präzision in der exakten Sekunde wünschen, in der eine gepufferte Anfrage aufgezeichnet wird, können Sie die [`timestamp`](../page-vars/timestamp.md) Seitenvariable festlegen, bevor Sie die Anfrage puffern. Wenn Sie diese Variable verwenden, stellen Sie sicher, dass [Zeitstempel optional](/help/admin/tools/manage-rs/edit-settings/general/timestamp-configuration.md) aktiviert ist - andernfalls gehen alle Treffer mit Zeitstempel dauerhaft verloren!

## Einschränkungen

Beachten Sie beim Aufrufen der `bufferRequests()`-Methode die folgenden Einschränkungen. Da diese Methode [`Window.sessionStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) verwendet, gelten viele der gleichen Einschränkungen:

* Der Ziel-Link muss sich in derselben Domain und Subdomain befinden. Gepufferte Anfragen funktionieren nicht domänenübergreifend und auch nicht domänenübergreifend, wenn beide dieselbe Adobe Analytics-Implementierung aufweisen. Diese Einschränkung bedeutet auch, dass Sie gepufferte Anfragen nicht zur Verfolgung von Exitlinks verwenden können.
* Der Ziel-Link muss dasselbe Protokoll wie die aktuelle Seite verwenden. Es können keine gepufferten Anfragen zwischen HTTP und HTTPS gesendet werden.
* Gepufferte Anfragen werden gespeichert, bis Sie `t()` oder `tl()` aufrufen, ohne `bufferRequests()` zuerst aufzurufen, oder bis der Browser oder die Registerkarte geschlossen wird. Wenn eine Browser-Sitzung beendet wird, bevor Sie diese Daten an Adobe senden können, gehen nicht gesendete gepufferte Anfragen dauerhaft verloren.
* Wenn ein Browser die [Web-Speicher-API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) oder die [JSON-API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON) nicht unterstützt, wird eine Warnung an die Browser-Konsole ausgegeben und AppMeasurement versucht, die Bildanforderung mithilfe der `t()`-Methode sofort zu senden.

## Gepufferte Anforderungen in der Web-SDK

Web SDK bietet derzeit nicht die Möglichkeit, Anfragen zu puffern.

## Gepufferte Anfragen, die die Adobe Analytics-Erweiterung verwenden

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.bufferRequests() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `bufferRequests()`-Methode vor dem Aufruf von `t()` oder `tl()` auf. Wenn `bufferRequests()` aufgerufen wird, werden nachfolgende Tracking-Aufrufe in den Sitzungsspeicher geschrieben und nicht an die Datenerfassungs-Server von Adobe gesendet.

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
