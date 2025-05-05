---
title: Übersicht über Variablen, Funktionen, Methoden und Plug-ins
description: Erfahren Sie, welche Variablen Sie in die an Adobe gesendeten Daten aufnehmen können, um die Berichterstellung zu verbessern.
keywords: Appmeasurement;Variablen;Vars;Konfiguration;Seite;Implementierung
feature: Variables
exl-id: 7ffcd943-f9ac-4daf-bbdf-248d75925b04
role: Admin, Developer
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 67%

---

# Übersicht über Variablen, Funktionen, Methoden und Plug-ins

Analytics bietet eine Reihe von Variablen zur Erfassung von Analytics-Daten. Die Variablen in diesem Abschnitt sind in mehrere Abschnitte unterteilt:

* **Seitenvariablen** sind Werte, die normalerweise direkt in Berichten verwendet werden. Zu den gebräuchlichen Seitenvariablen zählen `props`, `eVars` und `events`.
* **Konfigurationsvariablen** sind Einstellungswerte, die sicherstellen, dass die richtigen Daten Adobe erreichen. Zu den gebräuchlichen Konfigurationsvariablen zählen `trackingServerSecure`, `charSet` und `linkTrackVars`. Konfigurationsvariablen füllen normalerweise keine Dimensionselemente.
* **Funktionen und Methoden** sind Code-Abschnitte, die eine bestimmte Aufgabe ausführen, wenn darauf verwiesen wird. Zu den gebräuchlichen Funktionen gehören `t()`, `tl()` und `clearVars()`.

## Variablen und Implementierungsmethoden

Adobe bietet mehrere Möglichkeiten, Adobe Analytics zu implementieren. Jede Seite enthält einen Abschnitt über die Implementierung der Variablen mithilfe der Web-SDK, der Adobe Analytics-Erweiterung und der Verwendung von AppMeasurement für JavaScript.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Konfigurieren von Variablen](https://video.tv.adobe.com/v/31812?quality=12&learn=on&captions=ger){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


## Reihenfolge der Vorgänge

AppMeasurement-Bibliotheken, die von Adobe Analytics veröffentlicht werden, befolgen beim Senden von Daten an Adobe eine bestimmte Reihenfolge. Wenn Sie diese Aufgaben nicht in der richtigen Reihenfolge ausführen, können die Daten unvollständig sein.

1. Wenn Ihre Website eine Datenschicht verwendet, stellen Sie sicher, dass alle entsprechenden Variablen zuerst gefüllt werden. Sie füllen `adobeDataLayer.page.title` beispielsweise mit dem Seitentitel. Weitere Informationen finden Sie unter [Datenschicht](../prepare/data-layer.md).
2. Verwenden Sie die Datenschicht, um Analytics-Variablen zu füllen. <br/>Wenn Sie Tags in Adobe Experience Platform verwenden, wird diese Aufgabe durch die Verwendung von Datenelementen dazwischen erreicht. Datenelemente werden mit Werten aus der Datenschicht gefüllt. Beispielsweise ruft Datenelement `Page Title` den Wert aus der Datenschichtvariablen-`adobeDataLayer.page.title` ab. <br/>Anschließend können Sie das Datenelement verwenden, um Analytics-Variablen aufzufüllen. Beispielsweise ruft `eVar4` den Wert aus dem Datenelement `Page Title` ab. <br/>Weitere Informationen finden Sie [Datenelemente](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=de), [Zuordnen von Datenschichtobjekten zu Datenelementen](../launch/layer-to-elements.md) und [Zuordnen von Tag-Datenelementen zu Analytics-Variablen](../launch/elements-to-variable.md)
3. Rufen Sie abschließend die Tracking-Funktion auf. Die meisten AppMeasurement-Bibliotheken verwenden die `t()`-Methode, doch einige mobile SDKs verwenden `track()`. Wenn die Tracking-Funktion aufgerufen wird, werden alle im Analytics-Objekt definierten unterstützten Variablen in Form einer Bildanforderung an Adobe gesendet.

## Unzulässige Zeichen

Die folgenden Zeichen und Zeichenfolgen sind in JavaScript-Variablen nicht zulässig.

* Tab (`0x09`)
* Zeilenumschalter (`0x0D`)
* Umbruch (`0x0A`)
* HTML-Tags (z. B. `<b></b>` oder `&#153`)

Einige Variablen haben zusätzliche Einschränkungen oder Syntaxanforderungen. Die [`products`](page-vars/products.md)-Variable behält beispielsweise Semikolons und Kommas vor, um separate Produkte und Kategorien zu trennen.
