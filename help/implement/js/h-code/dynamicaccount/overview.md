---
title: Übersicht über dynamische Konten
description: Erfahren Sie, wie Sie eine Report Suite mit H-Code dynamisch auswählen.
feature: Implementation Basics
exl-id: 6f35dd71-29ad-4923-b1f7-9c7d6ca45bd8
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '241'
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
