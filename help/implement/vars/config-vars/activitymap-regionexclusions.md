---
title: ActivityMap.regionExclusions
description: Filtern von Activity Map-Daten nach Region.
role: Admin, Developer
feature: Variables
source-git-commit: 05010d58ba2a3376473097e9d4543ee4415e83e1
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 12%

---

# ActivityMap.regionExclusions

Mit der Variable `ActivityMap.regionExclusions` können Sie Activity Map-Daten anhand der in der Dimension [Activity Map-Region](/help/components/dimensions/activity-map-region.md) erfassten Dimensionselemente selektiv filtern oder ausschließen.

## Regionsausschlüsse in der Web SDK-Erweiterung

Wenn **[!UICONTROL Klickdatenerfassung aktivieren]** aktiviert ist, verwenden Sie den Callback-Codeblock **[!UICONTROL Klickeigenschaften filtern]** . In diesem Codeblock können Sie den Wert von `content.linkRegion` überprüfen und entweder den Wert ändern oder die Erfassung von Linktracking-Daten abbrechen.

## Regionsausschlüsse in der Web SDK JavaScript-Bibliothek

Wenn [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) aktiviert ist, verwenden Sie den Rückruf `filterClickDetails` im Objekt `clickCollection` . Innerhalb dieses Rückrufs können Sie den Wert von `linkRegion` überprüfen und entweder den Wert ändern oder die Erfassung von Linktracking-Daten abbrechen.

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

## Regionsausschlüsse mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.ActivityMap.regionExclusions mithilfe von AppMeasurement

Die Variable `s.ActivityMap.regionExclusions` ist eine Zeichenfolge mit kommagetrennten Ausdrücken, die vom Activity Map-Tracking ausgeschlossen werden sollen. Entspricht einer der Sätze dem Wert, der in der Dimension [Activity Map Region](/help/components/dimensions/activity-map-region.md) erfasst wurde, werden alle Activity Map-Daten aus dem Treffer entfernt.

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
