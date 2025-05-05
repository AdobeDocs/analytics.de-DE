---
title: ActivityMap.region
description: Anpassen, wie Activity Map die angeklickte Region erfasst.
feature: Variables
role: Admin, Developer
exl-id: 9bbdb124-b865-4431-8a98-9814c3f2e65c
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 13%

---

# ActivityMap.region

Mit der Variablen `ActivityMap.region` können Sie die Logik überschreiben, die Activity Map zum Festlegen von Bereichswerten verwendet. Diese Variable ist in Bereichen nützlich, in denen Sie mehr Kontrolle haben möchten als [`ActivityMap.regionExclusions`](../config-vars/activitymap-regionexclusions.md) bietet.

>[!CAUTION]
>Diese Variable überschreibt die Activity Map-Logik vollständig. Wenn Sie hier eine Überschreibungsfunktion festlegen, die falsche Werte zurückgibt, kann dies zu Problemen bei der Datenerfassung mit Activity Map-Dimensionen und der Activity Map-Überlagerung führen.

## Überschreiben von Regionswerten mit der Web-SDK

Sie können [`OnBeforeLinkClickSend`](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/onbeforelinkclicksend) Callback verwenden, um die Web-SDK-Payload zu ändern oder den Versand von Daten abzubrechen.

## Überschreiben von Regionen mithilfe der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## ActivityMap.Region im AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Weisen Sie dieser Variablen eine Funktion zu, die:

* das angeklickte HTML-Element erhält und
* Gibt einen Zeichenfolgenwert zurück. Dieser Zeichenfolgenwert ist der endgültige Wert, der für die Dimension [Activity Map Region](/help/components/dimensions/activity-map-region.md) verwendet wird.

Wenn der Rückgabewert &quot;[&quot; ](https://developer.mozilla.org/de-DE/docs/Glossary/Falsy), werden alle Activity Map-Kontextdatenvariablen gelöscht und es werden keine Linkdaten verfolgt.

## Beispiele

Verwenden Sie einen Tag-Namen in Kleinbuchstaben als Region:

```js
s.ActivityMap.region = function(clickedElement) {
  while (clickedElement && (clickedElement = clickedElement.parentNode)) {
    var regionId = clickedElement.tagName;
    if (regionId) {
      return regionId.toLowerCase();
    }
  }
}
```

Verwenden Sie bestimmte gewünschte Klassennamen als Region:

```js
s.ActivityMap.region = function(ele) {
  var className,
  classNames = {
    'header': 1,
    'navbar': 1,
    'left-content': 1,
    'main-content': 1,
    'footer': 1,
  };
  while ((ele && (ele = ele.parentNode))) {
    if ((className = ele.className)) {
      let classes = className.split(' ');
      for (let i = 0; i < classes.length; i++) {
        if (classNames[classes[i]]) {
          return classes[i];
        }
      }
    }
  }
  return "BODY";
}
```
