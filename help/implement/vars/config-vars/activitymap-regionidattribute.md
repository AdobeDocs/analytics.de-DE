---
title: ActivityMap.regionIDAttribute
description: Ändern Sie das Attribut, nach dem Activity Map sucht, um die Region zu bestimmen.
feature: Variables
role: Admin, Developer
source-git-commit: 05010d58ba2a3376473097e9d4543ee4415e83e1
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 10%

---

# ActivityMap.regionIDAttribute

Mit der Variable `ActivityMap.regionIDAttribute` können Sie das Attribut ändern, nach dem Activity Map bei der Bestimmung der Dimension [Activity Map Region](/help/components/dimensions/activity-map-region.md) sucht. Wenn Ihre Site so strukturiert ist, dass das Attribut `id` für die Activity Map-Region weniger nützlich ist, können Sie diese Variable so einstellen, dass sie sich ein anderes Attribut ansieht.

## Regions-ID-Attribut in der Web SDK-Erweiterung

Wenn **[!UICONTROL Klickdatenerfassung aktivieren]** aktiviert ist, verwenden Sie den Callback-Codeblock **[!UICONTROL Klickeigenschaften filtern]** . In diesem Codeblock können Sie den Wert von `content.clickedElement` überprüfen und entweder den Wert ändern oder die Erfassung von Linktracking-Daten abbrechen.

## Regions-ID-Attribut in der Web SDK JavaScript-Bibliothek

Wenn [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) aktiviert ist, verwenden Sie den Rückruf `filterClickDetails` im Objekt `clickCollection` . In diesem Rückruf können Sie den Wert von `clickedElement` überprüfen und die Logik der erfassten Region anpassen.

```js
alloy("configure", {
  clickCollectionEnabled: true,
  clickCollection: {
    filterClickDetails: function(content) {
      // If the clicked element was in a table, set the region to the contents of the data-custom attribute
      // If the clicked element was not in a table, or if the data-custom attribute doesn't exist, leave region as-is
      content.region = content.clickedElement.closest('table')?.getAttribute('data-custom') || content.region;
    }
  }
});
```

## Regions-ID-Attribut mithilfe der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.ActivityMap.regionIDAttribute mithilfe von AppMeasurement

Die Variable `s.ActivityMap.regionIDAttribute` ist eine Zeichenfolge, die das Attribut darstellt, mit dem die Dimension [Activity Map Region](/help/components/dimensions/activity-map-region.md) bestimmt wird. Diese Variable ist standardmäßig auf `id` gesetzt. Wenn Sie diese Variable ändern, sucht Activity Map nicht mehr nach dem Attribut `id` , sondern sucht weiterhin nach anderen Kriterien, um die Region zu bestimmen (z. B. semantische Elemente).

```html
<script>
  var s = s_gi("examplersid");
  s.ActivityMap.regionIDAttribute = "data-custom";
</script>

<!-- Clicking any of these links populates the region dimension with 'left-nav' -->
<div id="676967617A656C6C65" data-custom="left-nav">
  <a href="index.html">Home</a>
  <a href="products.html">View our products</a>
  <a href="contact.html">Contact us</a>
</div>
```
