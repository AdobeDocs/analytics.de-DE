---
title: ActivityMap.regionExclusions
description: Filtern von Activity Map-Daten nach Region.
role: Admin, Developer
feature: Variables
exl-id: 353282aa-860c-45dc-a6b0-8d9f1fa09f13
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 13%

---

# ActivityMap.regionExclusions

Mit der Variablen `ActivityMap.regionExclusions` können Sie Activity Map-Daten selektiv filtern oder ausschließen, basierend auf den Dimensionselementen, die in der Dimension [Activity Map-Region](/help/components/dimensions/activity-map-region.md) erfasst wurden.

## Regionsausschlüsse in der Web SDK-Erweiterung

Wenn **[!UICONTROL Click-Datenerfassung aktivieren]** aktiviert ist, verwenden Sie den **[!UICONTROL Filter click properties]** Callback-Code-Block. Innerhalb dieses Code-Blocks können Sie den Wert von `content.linkRegion` überprüfen und entweder den Wert ändern oder die Sammlung von Linktracking-Daten aufgeben.

## Regionsausschlüsse in der Web SDK JavaScript-Bibliothek

Wenn [`clickCollectionEnabled`](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) aktiviert ist, verwenden Sie den `filterClickDetails` Callback im `clickCollection`. Innerhalb dieses Callbacks können Sie den Wert von `linkRegion` überprüfen und entweder den Wert ändern oder die Sammlung von Linktracking-Daten aufgeben.

```js
alloy("configure", {
  clickCollectionEnabled: true,
  clickCollection: {
    filterClickDetails: function(content) {
      // If the clicked region has personal links in it, don't send click data
      if(content.linkRegion.includes("personal")) {
        return false;
      }
    }
  }
});
```

## Regionale Ausschlüsse, die die Adobe Analytics-Erweiterung verwenden

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.ActivityMap.regionExclusions mit AppMeasurement

Die `s.ActivityMap.regionExclusions` ist eine Zeichenfolge, die durch Kommas getrennte Phrasen enthält, die vom Activity Map-Tracking ausgeschlossen werden sollen. Wenn eine der Phrasen mit dem Wert übereinstimmt, der in der Dimension [Activity Map Region](/help/components/dimensions/activity-map-region.md) erfasst wurde, werden alle Activity Map-Daten aus dem Treffer entfernt.

```html
<script>
  var s = s_gi("examplersid");
  s.ActivityMap.regionExclusions = "contact";
</script>

<!-- Clicking any of these links tracks normally. -->
<!-- While "contact" is present, it is not tracked in region. The region is "nav" -->
<nav>
  <a href="index.html">Home</a>
  <a href="products.html">View our products</a>
  <a href="contact.html">Contact us</a>
</nav>

<!-- Activity Map data is not tracked for any of these links. -->
<!-- All these links belong to the region "Personal contact information" -->
<div id="personal-contact-information">
 <a href="mailto:user@example.com">Example user</a>
 <a href="mailto:user2@example.com">Example user 2</a>
 <a href="mailto:user3@example.com">Example user 3</a>
</div>
```
