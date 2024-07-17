---
title: ActivityMap.linkExclusions
description: Filtern von Activity Map-Daten nach Linknamen.
role: Admin, Developer
feature: Variables
source-git-commit: 05010d58ba2a3376473097e9d4543ee4415e83e1
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 11%

---

# ActivityMap.linkExclusions

Mit der Variable `ActivityMap.linkExclusions` können Sie Activity Map-Daten selektiv filtern oder ausschließen, basierend auf dem Text in der Dimension [Activity Map-Link](/help/components/dimensions/activity-map-link.md) .

## Link-Ausschlüsse in der Web SDK-Erweiterung

Wenn **[!UICONTROL Klickdatenerfassung aktivieren]** aktiviert ist, verwenden Sie den Callback-Codeblock **[!UICONTROL Klickeigenschaften filtern]** . In diesem Codeblock können Sie den Wert von `content.linkName` überprüfen und entweder den Wert ändern oder die Erfassung von Linktracking-Daten abbrechen.

## Link-Ausschlüsse in der Web SDK JavaScript-Bibliothek

Wenn [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) aktiviert ist, verwenden Sie den Rückruf `filterClickDetails` im Objekt `clickCollection` . Innerhalb dieses Rückrufs können Sie den Wert von `linkName` überprüfen und entweder den Wert ändern oder die Erfassung von Linktracking-Daten abbrechen.

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

## Verknüpfen von Ausschlüssen mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.ActivityMap.linkExclusions mithilfe von AppMeasurement

Die Variable `s.ActivityMap.linkExclusions` ist eine Zeichenfolge, die kommagetrennte Werte von Ausdrücken enthält, die vom Activity Map-Tracking ausgeschlossen werden sollen. Entspricht einer der Sätze dem Wert, der in der Dimension [Activity Map-Link](/help/components/dimensions/activity-map-link.md) erfasst wurde, werden alle Activity Map-Daten aus dem Treffer entfernt. Beachten Sie, dass diese Variable auf `linkName` und nicht auf `linkUrl` prüft.

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
