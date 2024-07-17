---
title: ActivityMap.link
description: Passen Sie an, wie Activity Map den angeklickten Link erfasst.
feature: Variables
role: Admin, Developer
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 8%

---

# ActivityMap.link

Mit der Variable `ActivityMap.link` können Sie die Logik überschreiben, die Activity Map zum Festlegen von Link-Werten verwendet. Diese Variable ist nützlich in Bereichen, in denen Sie mehr Kontrolle haben möchten als von [`ActivityMap.linkExclusions`](../config-vars/activitymap-linkexclusions.md) bereitgestellt wird.

>[!CAUTION]
>Diese Variable überschreibt die Activity Map-Logik vollständig. Wenn Sie hier eine Überschreibungsfunktion einrichten, die falsche Werte zurückgibt, kann dies zu Problemen bei der Datenerfassung mit Activity Map-Dimensionen und der Activity Map-Überlagerung führen.

## Linkwerte mithilfe des Web SDK überschreiben

Sie können den Rückruf [`OnBeforeLinkClickSend`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/onbeforelinkclicksend) verwenden, um die Web SDK-Payload zu ändern oder das Senden von Daten abzubrechen.

## Linküberschreibungen mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## ActivityMap.link in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Weisen Sie dieser Variablen eine Funktion zu, die:

* empfängt das angeklickte HTML-Element und
* Gibt einen Zeichenfolgenwert zurück. Dieser Zeichenfolgenwert ist der endgültige Wert, der für die Dimension [Activity Map-Link](/help/components/dimensions/activity-map-link.md) verwendet wird.

Wenn der Rückgabewert [falsy](https://developer.mozilla.org/de-DE/docs/Glossary/Falsy) ist, werden alle Activity Map-Kontextdatenvariablen gelöscht und es werden keine Linkdaten verfolgt.

## Beispiele

Verwenden Sie nur das Titelattribut von `<a>` -Tags. Wenn das Titelattribut nicht vorhanden ist, wird kein Link verfolgt.

```js
s.ActivityMap.link = function(clickedElement) {
  var linkId;
  if (clickedElement && clickedElement.tagName.toUpperCase() === 'A') {
    linkId = clickedElement.getAttribute('title');
  }
  return linkId;
}
```

Geben Sie den manuell festgelegten Link-Namen in `s.tl` zurück, falls er vorhanden ist. Andernfalls wird die Link-URL zurückgegeben.

```js
s.ActivityMap.link = function(ele, linkName) {
  if (linkName) {
    return linkName;
  }
  if (ele && ele.tagName == 'A' && ele.href) {
    return ele.href;
  }
}
```

Anstatt die standardmäßige Link-Logik vollständig zu ersetzen, können Sie sie bedingt ändern.

```html
<script>
  // Copy the original link function
  var originalLinkFunction = s.ActivityMap.link;
  // Return the link name from s.tl, a modified activity map value, or the original activity map value
  s.ActivityMap.link = function(element,linkName)
  {
    return linkName || customFunction(element) || originalLinkFunction(element,linkName);
  };
</script>

<button type="button" onclick="s.tl(this,'o',customFunction(this)">Add To Cart</button>
```

1. Wenn `linkName` übergeben wird, wurde die Methode von `tl()` aufgerufen. Gibt zurück, was `tl()` als `linkName` übergeben hat.
2. Wenn von Activity Map aufgerufen wird, wird nie ein `linkName` übergeben. Rufen Sie daher `customFunction()` mit dem Link-Element auf. Sie können jede benutzerdefinierte Funktion verwenden, die Sie als Wert zurückgeben möchten.
3. Wenn keiner der oben genannten Rückgabewerte auftritt, verwenden Sie den Link-Namen, der normalerweise als Fallback erfasst wird.
