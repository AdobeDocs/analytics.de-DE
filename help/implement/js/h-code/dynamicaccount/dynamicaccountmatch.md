---
title: dynamicAccountMatch
description: Die Variable „dynamicAccountMatch“ legt fest, welcher Wert in dynamischen Konten betrachtet werden soll.
feature: Implementation Basics
exl-id: 3b68f2e6-1bd9-4b16-9d03-a87c9217e1b7
role: Developer
TQID: https://experienceleague.adobe.com/Ag4YQOjHPMRsktGSbzpErM55lVCydDHXfNiS4HJofIU
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: df312454-73c4-43f6-a90e-18f5043f074cid: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 93%

---

# dynamicAccountMatch

>[!IMPORTANT]
>
>Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder Tags in Adobe Experience Platform nicht unterstützt.

Die Variable `dynamicAccountMatch` ist der Wert, den `dynamicAccountList` betrachtet und vergleicht. Wenn `dynamicAccountSelection` nicht auf `true` gesetzt ist, wird diese Variable ignoriert.

Wenn diese Variable nicht definiert ist, lautet ihr Standardwert `window.location.host`.

## Syntax

```js
s.dynamicAccountMatch=[DOM object]
```

## Beispiele

```js
// Look at the URL path to determine report suite
s.dynamicAccountMatch = location.pathname;

// Use a query string
s.dynamicAccountMatch = location.search;

// Use the full URL
s.dynamicAccountMatch = location.href;

// Use concatenated variables
s.dynamicAccountMatch =  location.hostname + location.pathname + location.search;
```

## Weitere Hinweise

* Auf Seiten, die auf einer Festplatte gespeichert werden, sind nicht mehrere `location`-Variablen definiert (z. B. ist `location.host` leer). Stellen Sie sicher, dass in `s_account` eine standardmäßige Report Suite enthalten ist.
* Bei über ein Web-basiertes Tool (wie z. B. Google) übersetzten Seiten funktioniert die dynamisches Kontoauswahl nicht richtig. Für eine präzisere Nachverfolgung müssen Sie die `s_account` Server-seitig auffüllen.
