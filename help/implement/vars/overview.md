---
title: Überblick über Variablen, Funktionen, Methoden und Plug-ins
description: Erfahren Sie, welche Variablen Sie in die an Adobe gesendeten Daten aufnehmen können, um die Berichterstellung zu verbessern.
keywords: Appmeasurement;Variablen;Vars;Konfiguration;Seite;Implementierung
feature: Appmeasurement Implementation
exl-id: 7ffcd943-f9ac-4daf-bbdf-248d75925b04
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/Jyw64eX30vu3tLyimiM5A-t9aTqkAZE0wrsd4i0BCmc'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 417
ht-degree: 100%

---

# Überblick über Variablen, Funktionen, Methoden und Plug-ins

Analytics bietet eine Reihe von Variablen zur Erfassung von Analytics-Daten. Die Variablen in diesem Abschnitt sind in mehrere Abschnitte unterteilt:

* **Seitenvariablen** sind Werte, die normalerweise direkt in Berichten verwendet werden. Zu den gebräuchlichen Seitenvariablen zählen `props`, `eVars` und `events`.
* **Konfigurationsvariablen** sind Einstellungswerte, die sicherstellen, dass die richtigen Daten Adobe erreichen. Zu den gebräuchlichen Konfigurationsvariablen zählen `trackingServerSecure`, `charSet` und `linkTrackVars`. Konfigurationsvariablen füllen normalerweise keine Dimensionselemente.
* **Funktionen und Methoden** sind Code-Abschnitte, die eine bestimmte Aufgabe ausführen, wenn darauf verwiesen wird. Zu den gebräuchlichen Funktionen gehören `t()`, `tl()` und `clearVars()`.

## Variablen und Implementierungsmethoden

Adobe bietet mehrere Möglichkeiten, Adobe Analytics zu implementieren. Jede Seite enthält einen Abschnitt zur Implementierung der Variable über Web SDK, die Adobe Analytics-Erweiterung sowie über AppMeasurement für JavaScript.


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Konfigurieren von Variablen](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/administration/manage-report-suites/configuring-variables-in-the-admin-console){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


## Reihenfolge der Vorgänge

AppMeasurement-Bibliotheken, die von Adobe Analytics veröffentlicht werden, befolgen beim Senden von Daten an Adobe eine bestimmte Reihenfolge. Wenn Sie diese Aufgaben nicht in der richtigen Reihenfolge ausführen, können die Daten unvollständig sein.

1. Wenn Ihre Website eine Datenschicht verwendet, stellen Sie sicher, dass alle entsprechenden Variablen zuerst gefüllt werden. Sie füllen `adobeDataLayer.page.title` beispielsweise mit dem Seitentitel. Weitere Informationen finden Sie unter [Datenschicht](../prepare/data-layer.md).
2. Verwenden Sie die Datenschicht, um Analytics-Variablen zu füllen. <br/>Wenn Sie Tags in Adobe Experience Platform verwenden, wird diese Aufgabe durch die Verwendung von Datenelementen dazwischen ausgeführt. Datenelemente werden mit Werten aus der Datenschicht gefüllt. Das Datenelement `Page Title` ruft den Wert beispielsweise aus der Datenschichtvariable `adobeDataLayer.page.title` ab. <br/>Anschließend können Sie das Datenelement verwenden, um Analytics-Variablen auszufüllen. `eVar4` ruft den Wert beispielsweise aus dem Datenelement `Page Title` ab. <br/>Weitere Informationen finden Sie unter [Datenelemente](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=de), [Zuordnen von Datenschichtobjekten zu Datenelementen](../launch/layer-to-elements.md) und [Zuordnen von Tag-Datenelementen zu Analytics-Variablen](../launch/elements-to-variable.md)
3. Rufen Sie abschließend die Tracking-Funktion auf. Die meisten AppMeasurement-Bibliotheken verwenden die `t()`-Methode, doch einige mobile SDKs verwenden `track()`. Wenn die Tracking-Funktion aufgerufen wird, werden alle im Analytics-Objekt definierten unterstützten Variablen in Form einer Bildanforderung an Adobe gesendet.

## Unzulässige Zeichen

Die folgenden Zeichen und Zeichenfolgen sind in JavaScript-Variablen nicht zulässig.

* Tab (`0x09`)
* Zeilenumschalter (`0x0D`)
* Umbruch (`0x0A`)
* HTML-Tags (z. B. `<b></b>` oder `&#153`)

Einige Variablen haben zusätzliche Einschränkungen oder Syntaxanforderungen. Die [`products`](page-vars/products.md)-Variable behält beispielsweise Semikolons und Kommas vor, um separate Produkte und Kategorien zu trennen.
