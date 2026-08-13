---
title: Util.cookieWrite
description: Schreibt einen Wert für ein Cookie.
feature: Appmeasurement Implementation
exl-id: 079dbe50-5568-467b-a67c-f44481a4a20b
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/VxNoO8-K6rE8NdIgQSA0ubuBwaHXu2OPLCexzNCXdHQ'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 70%

---

# Util.cookieWrite

Cookies können Informationen über Seiten in derselben Domain hinweg speichern und abrufen. Verwenden Sie die `Util.cookieWrite()`-Methode, um einen Wert für ein Cookie festzulegen. Sie können die [`Util.cookieRead()`](util-cookieread.md)-Methode verwenden, um mit `Util.cookieWrite()` eingestellte Werte abzurufen.

## Setzen von Cookies mithilfe der Adobe Analytics-Erweiterung und der Web SDK-Erweiterung

Die Datenerfassung von Adobe Experience Platform bietet keine Möglichkeit, Cookies in der Benutzeroberfläche festzulegen.

## s.Util.cookieWrite() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Rufen Sie die `s.Util.cookieWrite()`-Methode auf, um ein Cookie auf einen gewünschten Wert festzulegen.

```js
s.Util.cookieWrite("example_cookie","Example cookie value")
```

Es ist ein optionales drittes Argument verfügbar, das bestimmt, wann das Cookie abläuft. Cookies, die mit `s.Util.cookieWrite()` gesetzt werden, laufen standardmäßig am Ende der Browser-Sitzung ab.

```js
// Set a cookie with an expiration 6 months from now
var cookieDate = new Date();
cookieDate.setMonth(cookieDate.getMonth() + 6);
s.Util.cookieWrite("example_cookie","Example 6-month cookie",cookieDate);
```

## Beispiele

Sie können eine Variable instanziieren, wenn ein Cookie erfolgreich geschrieben wurde. Diese Variable ist ein boolescher Wert.

```js
var success = s.Util.cookieWrite("example_cookie","Example cookie value");
if (success) {
  console.log("Cookie written successfully");
} else {
  console.log("Cookie write failed");
}
```
