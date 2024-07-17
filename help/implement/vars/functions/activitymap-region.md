---
title: ActivityMap.region
description: Passen Sie an, wie Activity Map die angeklickte Region erfasst.
feature: Variables
role: Admin, Developer
source-git-commit: 1fb57590714ad2412323416289dee967eef07fad
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 12%

---

# ActivityMap.region

Mit der Variable `ActivityMap.region` können Sie die Logik überschreiben, die Activity Map zum Festlegen von Regionswerten verwendet. Diese Variable ist nützlich in Bereichen, in denen Sie mehr Kontrolle haben möchten als von [`ActivityMap.regionExclusions`](../config-vars/activitymap-regionexclusions.md) bereitgestellt wird.

>[!CAUTION]
>Diese Variable überschreibt die Activity Map-Logik vollständig. Wenn Sie hier eine Überschreibungsfunktion einrichten, die falsche Werte zurückgibt, kann dies zu Problemen bei der Datenerfassung mit Activity Map-Dimensionen und der Activity Map-Überlagerung führen.

## Überschreiben von Regionswerten mithilfe des Web SDK

Sie können den Rückruf [`OnBeforeLinkClickSend`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/onbeforelinkclicksend) verwenden, um die Web SDK-Payload zu ändern oder das Senden von Daten abzubrechen.

## Regionsüberschreibungen mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## ActivityMap.region in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Weisen Sie dieser Variablen eine Funktion zu, die:

* empfängt das angeklickte HTML-Element und
* Gibt einen Zeichenfolgenwert zurück. Dieser Zeichenfolgenwert ist der Endwert, der für die Dimension [Activity Map Region](/help/components/dimensions/activity-map-region.md) verwendet wird.

Wenn der Rückgabewert [falsy](https://developer.mozilla.org/de-DE/docs/Glossary/Falsy) ist, werden alle Activity Map-Kontextdatenvariablen gelöscht und es werden keine Linkdaten verfolgt.

## Beispiele

Verwenden Sie einen Tag-Namen in Kleinbuchstaben als region:

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

Verwenden Sie bestimmte gewünschte Klassennamen als region:

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
