---
title: Übersicht über dynamische Konten
description: Erfahren Sie, wie Sie mit einem Workflow eine Report Suite mit H-Code dynamisch auswählen.
feature: Implementation Basics
exl-id: 6f35dd71-29ad-4923-b1f7-9c7d6ca45bd8
role: Developer
TQID: https://experienceleague.adobe.com/PCeDSQpYH3wym7oG5CYbQblnXkiOQRF4YlcHU6zYfKA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: df312454-73c4-43f6-a90e-18f5043f074cid: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 243
ht-degree: 100%

---

# Übersicht über dynamische Konten

>[!IMPORTANT]
>
>Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder Tags in Adobe Experience Platform nicht unterstützt.

Dynamische Konten sind eine Implementierungsfunktion, mit der Sie anhand der von Ihnen definierten Kriterien festlegen können, welche Report Suite verwendet werden soll. Wenn Ihr Unternehmen mehr als eine Report Suite benötigt, aber dieselbe Implementierung zwischen Ihren Websites verwenden möchte, sind dynamische Konten eine gute Lösung.

>[!TIP]
>
>Adobe empfiehlt, Daten an eine einzelne Report Suite zu senden und dann bei Bedarf Virtual Report Suites zu verwenden, um Daten zu trennen. Weitere Informationen finden Sie unter [Überlegungen zur globalen Report Suite](../../../prepare/global-rs.md).

3 Variablen werden zur dynamischen Auswahl einer Report Suite verwendet.

* [`dynamicAccountSelection`](dynamicaccountselection.md): Aktiviert oder deaktiviert die dynamische Kontoauswahl.
* [`dynamicAccountMatch`](dynamicaccountmatch.md): Bestimmt, welcher Wert zu beachten ist. Beispielsweise die URL oder eine Abfragezeichenfolge.
* [`dynamicAccountList`](dynamicaccountlist.md): Vergleicht die Werte mit `dynamicAccountMatch` und füllt bei Übereinstimmung die `account`-Variable aus.

Wenn `dynamicAccountSelection = true`, wird der Wert innerhalb `dynamicAccountMatch` mit `dynamicAccountList` verglichen. Wenn die Werte in `dynamicAccountList` übereinstimmen, wird die Report Suite-ID in die `account`-Variable einbezogen.

## Standardmäßige Report Suite

Die Variable `account` kann zuvor festgelegt werden und dient dann als Standardwert für den Fall, dass keine der angegebenen Zeichenfolgen gefunden wird. Beispiel:

```javascript
s_account = "examplersiddefault";
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersiddev=dev.example.com;examplersidprod=example.com";
```

Wenn `location.hostname` weder `dev.example.com` noch `example.com` war, würde der Treffer an `examplersiddefault` gesendet.

## Multi-Suite-Tagging

Multi-Suite-Tagging kann mit der dynamischen Kontoauswahl verwendet werden. Beispiel:

```js
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersid1,examplersid2=example.com";
```

Wenn `location.hostname` `example.com` enthält, wird der Treffer sowohl an `examplersid1` als auch an `examplersid2` gesendet.
