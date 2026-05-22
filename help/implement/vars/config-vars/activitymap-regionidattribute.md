---
title: ActivityMap.regionIDAttribute
description: Ändern Sie das Attribut, nach dem Activity Map sucht, um die Region zu bestimmen.
feature: Appmeasurement Implementation
role: Admin, Developer
exl-id: 4aec045e-1a86-412f-bd37-777ac49ccc7d
TQID: 'https://experienceleague.adobe.com/DJj1qmoYB0iMxDszdGKYTeczkjv0OvxXAYlg2irpKb0'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 15%

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
