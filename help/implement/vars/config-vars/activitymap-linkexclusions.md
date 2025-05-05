---
title: ActivityMap.linkExclusions
description: Filtern von Activity Map-Daten nach Link-Name.
role: Admin, Developer
feature: Variables
exl-id: 9fc95016-362d-4c21-806e-e23adce9b6f7
source-git-commit: bcab98e453247c74b7d96497d34e6aea9ca32bc7
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 12%

---

# ActivityMap.linkExclusions

Mit der `ActivityMap.linkExclusions` können Sie Activity Map-Daten basierend auf dem Text in der Dimension [Activity Map-Link&rbrace; selektiv filtern oder ](/help/components/dimensions/activity-map-link.md).

## Verknüpfen von Ausschlüssen in der Web SDK-Erweiterung

Wenn **[!UICONTROL Click-Datenerfassung aktivieren]** aktiviert ist, verwenden Sie den **[!UICONTROL Filter click properties]** Callback-Code-Block. Innerhalb dieses Code-Blocks können Sie den Wert von `content.linkName` überprüfen und entweder den Wert ändern oder die Sammlung von Linktracking-Daten aufgeben.

## Verknüpfen von Ausschlüssen in der Web SDK JavaScript-Bibliothek

Wenn [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) aktiviert ist, verwenden Sie den `filterClickDetails` Callback im `clickCollection`. Innerhalb dieses Callbacks können Sie den Wert von `linkName` überprüfen und entweder den Wert ändern oder die Sammlung von Linktracking-Daten aufgeben.

```js
alloy("configure", {
  clickCollectionEnabled: true,
  clickCollection: {
    filterClickDetails: function(content) {
      // If the link is a clickable telephone number, anonymize it
      if(content.linkUrl.includes("tel:")) {
        content.linkName = content.linkUrl = "Phone number";
      }
      // If the link is an email address, anonymize it
      if(content.linkUrl.includes("mailto:")) {
        content.linkName = content.linkUrl = "Email address";
      }
    }
  }
});
```

## Verknüpfen von Ausschlüssen mithilfe der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.ActivityMap.linkExclusions mit AppMeasurement

Die `s.ActivityMap.linkExclusions`-Variable ist eine Zeichenfolge, die kommagetrennte Werte von Phrasen enthält, die vom Activity Map-Tracking ausgeschlossen werden sollen. Wenn eine der Phrasen mit dem Wert übereinstimmt, der in der Dimension [Activity Map Link](/help/components/dimensions/activity-map-link.md) erfasst wurde, werden alle Activity Map-Daten aus dem Treffer entfernt. Beachten Sie, dass diese Variable `linkName` betrachtet, nicht `linkUrl`.

```html
<script>
  var s = s_gi("examplersid");
  s.ActivityMap.linkExclusions = "Contact";
</script>

<!-- Clicking this link tracks normally -->
<a href="products.html">View our products</a>

<!-- Activity Map data is not tracked for this link -->
<a href="mailto:user@example.com">Contact this user</a>
```
