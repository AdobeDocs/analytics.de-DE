---
title: Häufig gestellte Fragen zur Implementierung
description: Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.
feature: Implementation Basics
exl-id: 4bab6d51-0077-42ce-8091-f75207d4c4db
role: Admin, Developer, Leader, User
TQID: https://experienceleague.adobe.com/Hm9pIJE9P3jEljJAgB69k2M9-fTa9G0wsCjfvN4xH3E
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c77ba355-6681-41fe-b719-563d3f507fdb
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
  - id: df312454-73c4-43f6-a90e-18f5043f074c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 1be0f3577403db7cf9bd40ef9e7c4bfcfa6c0b17
workflow-type: tm+mt
source-wordcount: 512
ht-degree: 100%

---

# Häufig gestellte Fragen zur Implementierung von Analytics

Häufig gestellte Fragen zur Implementierung sowie Links zu weiteren Informationen.

## Was ist der Unterschied zwischen der Experience Cloud-Besucher-ID und der Analytics-Besucher-ID?

Der Identitätsdienst weist eine eindeutige, beständige ID zu, die von den anderen Lösungen in Experience Cloud gemeinsam genutzt werden kann. Die Analytics-Besucher-ID wird nur von Analytics verwendet. Adobe empfiehlt, den Experience Cloud-Besucher-ID-Dienst in Ihrer Implementierung zu verwenden.

## Wie wird Heartbeat-Video-Tracking implementiert?

Weitere Informationen finden Sie unter [Messen von Audio und Video in Adobe Analytics](https://experienceleague.adobe.com/de/docs/media-analytics/using/media-overview).

## Kann eine Dienstunterbrechung bei Adobe die Performance beeinträchtigen?

Nein. Die JavaScript-Datei wird nicht auf Adobe-Servern gehostet, sodass sich ein Systemausfall bei Adobe nicht auf Ihre AppMeasurement-Bibliothek auswirkt. Wenn Sie Tags in Adobe Experience Platform verwenden, wird die JavaScript-Datei von Akamai oder an einem von Ihrem Unternehmen bestimmten Server-Speicherort gehostet.

## Kann das Senden von Daten vom Browser an die Adobe-Dienste die Performance beeinträchtigen?

AppMeasurement erstellt innerhalb der HTML-Seite ein Bildobjekt, das der Browser dann von den Adobe-Datenerfassungs-Servern anfordert. Falls der Datenerfassungs-Server sehr langsam ist oder nicht reagiert, wird der Thread, der diese Anforderung verarbeitet, bis zur Rückgabe des Bildes verzögert, oder es kommt zu einer Zeitüberschreitung. Da in Browsern die Verarbeitung von Bildern durch mehrere Threads erfolgt, hätte ein Systemausfall bei Adobe nur geringe Auswirkungen auf die Seitenladezeit. Es wäre dabei nur ein Thread gebunden, während die anderen nach wie vor funktionierten.

## Wie kann ich eine Analytics-Implementierung ungültig machen oder entfernen?

Manchmal möchte ein Unternehmen eine Implementierung aufgrund des Vertragsablaufs entfernen oder die Anzahl der Serveraufrufe verringern.

* **Implementierungen mit der Adobe Experience Platform-Datenerfassung**: Deaktivieren oder deinstallieren Sie die entsprechende Adobe Analytics-, Web SDK- oder Mobile SDK-Erweiterung im [!UICONTROL Erweiterungen] und veröffentlichen Sie dann.
* **Ältere AppMeasurement-Implementierungen**: Ersetzen Sie den gesamten Inhalt Ihrer `s_code.js`-Datei durch die folgende Codezeile:

```js
var s = new Object();
```

>[!WARNING]
>
>Beachten Sie Folgendes:
>
>* Ändern Sie die Report Suite nicht in einen ungültigen Wert, da dies die Server von Adobe unnötig belastet.
>* Entfernen Sie die `s_code.js`-Datei nicht vollständig, es sei denn, Sie entfernen alle Verweise auf die Datei auf jeder Seite.
>* Ändern Sie die `trackingServer`-Variable nicht von Adobe weg. AppMeasurement sendet weiterhin Bildanforderungen, die 404-Fehler zurückgeben.

## Ich habe AppMeasurement über einen Code Analyzer ausgeführt und die Verwendung von `Math.random()` wurde als potenzielles Sicherheitsrisiko gekennzeichnet. Wird `Math.random()` mit vertraulichen Daten verwendet?

Nein. Die Zahlen, die `Math.random()` verwenden, werden nicht zum Maskieren, Senden oder Empfangen sensibler Daten verwendet. Daten, die an Datenerfassungs-Server von Adobe gesendet werden, sind auf die Sicherheit der zugrunde liegenden HTTPS-Verbindung angewiesen. <!-- AN-173590 -->

AppMeasurement verwendet `Math.random()` in drei zentralen Bereichen:

* **Sampling**: Je nach Implementierung können einige Informationen für nur einen kleinen Prozentsatz der Besucher Ihrer Site gesammelt werden. `Math.random()` bestimmt, ob ein Besucher Daten senden soll. Bei den meisten Implementierungen wird kein Sampling verwendet.
* **Fallback-Besucher-ID**: Wenn die Besucher-ID nicht aus Cookies abgerufen werden kann, wird eine zufällige Besucher-ID generiert. Dieser Teil von AppMeasurement verwendet zwei Aufrufe von `Math.random()`.
* **Zwischenspeichern von Daten**: Am Ende der Bildanforderungs-URLs wird eine zufällig ausgewählte Zahl hinzugefügt, um die Zwischenspeicherung im Browser zu verhindern.
