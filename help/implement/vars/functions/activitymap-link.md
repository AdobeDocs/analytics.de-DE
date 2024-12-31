---
title: ActivityMap.link
description: Anpassen, wie Activity Map den angeklickten Link erfasst.
feature: Variables
role: Admin, Developer
exl-id: 3a31f80b-dbee-4a45-ac3c-0b8ca198c95a
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 9%

---

# ActivityMap.link

Mit der Variablen `ActivityMap.link` können Sie die Logik überschreiben, die Activity Map zum Festlegen von Linkwerten verwendet. Diese Variable ist in Bereichen nützlich, in denen Sie mehr Kontrolle haben möchten als [`ActivityMap.linkExclusions`](../config-vars/activitymap-linkexclusions.md) bietet.

>[!CAUTION]
>Diese Variable überschreibt die Activity Map-Logik vollständig. Wenn Sie hier eine Überschreibungsfunktion festlegen, die falsche Werte zurückgibt, kann dies zu Problemen bei der Datenerfassung mit Activity Map-Dimensionen und der Activity Map-Überlagerung führen.

## Überschreiben von Linkwerten mit der Web-SDK

Sie können [`OnBeforeLinkClickSend`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/onbeforelinkclicksend) Callback verwenden, um die Web-SDK-Payload zu ändern oder den Versand von Daten abzubrechen.

## Link-Überschreibung mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## ActivityMap.link im AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Weisen Sie dieser Variablen eine Funktion zu, die:

* das angeklickte HTML-Element erhält und
* Gibt einen Zeichenfolgenwert zurück. Dieser Zeichenfolgenwert ist der endgültige Wert, der für die Dimension [Activity Map Link](/help/components/dimensions/activity-map-link.md) verwendet wird.

Wenn der Rückgabewert &quot;[&quot; ](https://developer.mozilla.org/de-DE/docs/Glossary/Falsy), werden alle Activity Map-Kontextdatenvariablen gelöscht und es werden keine Linkdaten verfolgt.

## Beispiele

Verwenden Sie nur das Titelattribut aus `<a>` Tags. Wenn das Attribut title nicht vorhanden ist, wird kein Link verfolgt.

```js
s.ActivityMap.link = function(clickedElement) {
  var linkId;
  if (clickedElement && clickedElement.tagName.toUpperCase() === 'A') {
    linkId = clickedElement.getAttribute('title');
  }
  return linkId;
}
```

Gibt den manuell festgelegten Link-Namen in `s.tl` zurück, falls vorhanden. Andernfalls wird die Link-URL zurückgegeben.

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

Anstatt die Standardverknüpfungslogik vollständig zu ersetzen, können Sie sie bedingt ändern.

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

1. Wenn `linkName` übergeben wird, wurde die Methode von `tl()` aufgerufen. Gibt zurück, was als `linkName` übergeben `tl()`.
2. Beim Aufruf von Activity Map wird ein `linkName` nie übergeben. Rufen Sie daher `customFunction()` mit dem Link-Element auf. Sie können jede benutzerdefinierte Funktion verwenden, die Sie als Wert zurückgeben möchten.
3. Wenn keiner der oben genannten Werte zurückgibt, verwenden Sie den Link-Namen, der normalerweise als Fallback erfasst wird.
