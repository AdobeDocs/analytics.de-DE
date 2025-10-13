---
title: ActivityMap.regionIDAttribute
description: Ändern Sie das Attribut, nach dem Activity Map sucht, um die Region zu bestimmen.
feature: Appmeasurement Implementation
role: Admin, Developer
exl-id: 4aec045e-1a86-412f-bd37-777ac49ccc7d
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 11%

---

# ActivityMap.regionIDAttribute

Mit der Variablen `ActivityMap.regionIDAttribute` können Sie das Attribut ändern, nach dem Activity Map beim Bestimmen der Dimension [Activity Map Region](/help/components/dimensions/activity-map-region.md) sucht. Wenn Ihre Site so strukturiert ist, dass das Attribut `id` für die Activity Map-Region weniger nützlich ist, können Sie diese Variable so einstellen, dass sie ein anderes Attribut anzeigt.

## Regionskennungsattribut in der Web SDK-Erweiterung

Wenn **[!UICONTROL Click-Datenerfassung aktivieren]** aktiviert ist, verwenden Sie den **[!UICONTROL Filter click properties]** Callback-Code-Block. Innerhalb dieses Code-Blocks können Sie den Wert von `content.clickedElement` überprüfen und entweder den Wert ändern oder die Sammlung von Linktracking-Daten aufgeben.

## Regionskennungsattribut in der Web SDK JavaScript-Bibliothek

Wenn [`clickCollectionEnabled`](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) aktiviert ist, verwenden Sie den `filterClickDetails` Callback im `clickCollection`. Innerhalb dieses Callbacks können Sie den Wert von `clickedElement` überprüfen und die Logik der erfassten Region anpassen.

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

## Regionskennungsattribut, das die Adobe Analytics-Erweiterung verwendet

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.ActivityMap.regionIDAttribute mit AppMeasurement

Die `s.ActivityMap.regionIDAttribute` ist eine Zeichenfolge, die das -Attribut darstellt, um die Dimension [Activity Map Region](/help/components/dimensions/activity-map-region.md) zu bestimmen. Diese Variable ist standardmäßig auf `id` festgelegt. Wenn Sie diese Variable ändern, sucht Activity Map nicht mehr nach dem `id`, sondern nach anderen Kriterien zur Bestimmung der Region (z. B. nach semantischen Elementen).

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
