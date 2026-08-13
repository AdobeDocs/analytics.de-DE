---
title: timestamp
description: Setzen Sie den Zeitstempel des Treffers manuell fest.
feature: Appmeasurement Implementation
exl-id: 9d5ce5ef-2d84-4f65-b2e3-7aa3e219bc34
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/f2r9jWtF5HgCP6jUKg3YnLFxNwx1DiUBI-2Nquy5-K0'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 1ed4ab984231b7c72580c5ae505b1a16c0330c2f
workflow-type: tm+mt
source-wordcount: 304
ht-degree: 72%

---

# timestamp

Die `timestamp`-Variable legt den Zeitstempel des Treffers für Report Suites mit aktiviertem Zeitstempel manuell fest.

>[!WARNING]
>
>Verwenden Sie diese Variable nicht, wenn Ihre Report Suite nicht explizit für die Annahme von Treffern mit Zeitstempel konfiguriert ist. AppMeasurement legt die Zeit eines Treffers für Report Suites automatisch fest, die keine Treffer mit Zeitstempel unterstützen. Wenn Sie einen Treffer mit dieser Variablen an eine Report Suite senden, die keine Zeitstempel unterstützt, gehen diese Daten dauerhaft verloren.

## Zeitstempel bei Verwendung der Web-SDK

Der Zeitstempel ist [für Adobe Analytics) unter ](/help/implement/aep-edge/xdm-var-mapping.md) XDM-`xdm.timestamp` zugeordnet. Dieses Feld unterstützt nur Unix-Zeit.

## Zeitstempel bei Verwendung der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.timestamp in AppMeasurement und der benutzerdefinierte Code-Editor der Analytics-Erweiterung

Die `s.timestamp`-Variable ist eine Zeichenfolge, die das Datum und die Uhrzeit des Treffers enthält. Gültige Zeitstempelformate sind [ISO 8601](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6) und [Unix-Zeit](https://de.wikipedia.org/wiki/Unixzeit) in Sekunden.

```js
// Timestamp using ISO 8601
s.timestamp = "2026-01-01T00:00:00Z";

// Timestamp using Unix timestamp
s.timestamp = "1577836800";

// Automatically get the current Unix timestamp
s.timestamp = Math.round(new Date().getTime()/1000);

// Automatically get the current ISO 8601 timestamp
s.timestamp = new Date().toISOString();
```

## Werte nach ISO 8601

Die nach [ISO 8601](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6) angegebenen Daten und Zeiten können in verschiedenen Formen verwendet werden. Adobe unterstützt nicht alle Funktionen von ISO 8601.

* Sowohl das Datum als auch die Uhrzeit müssen durch `T` getrennt angegeben werden.
* Stunden und Minuten sind erforderlich; Sekunden sind optional, werden aber empfohlen.
* Wochentage und Datumsangaben mit Ordnungszahlen werden nicht unterstützt.
* Das Datum kann im standardmäßigen oder im erweiterten Format angegeben werden. Zum Beispiel sind `2026-01-01T00:00:00Z` und `20260101T000000Z` beide gültig.
* Fraktionsminuten und -sekunden sind technisch gültig, aber die Brüche werden ignoriert. Adobe Analytics unterstützt Zeitstempel nur auf zweiter Präzision. Wenn die Genauigkeit auf Millisekunden-Ebene für Ihr Unternehmen eine Priorität darstellt, sollten Sie Customer Journey Analytics verwenden.
* Zeitzonen werden in Standard- und erweiterten Formaten unterstützt.

Die folgenden Beispiele sind gültige Werte nach ISO 8601 in der `timestamp`-Variablen:

```text
2026-01-01T00:00:00+00:00
2026-01-01T00:00:00Z
2026-01-01T00:00:00
2026-01-01T00:00
20260101T000000+0000
20260101T000000Z
20260101T000000
20260101T0000
```
