---
title: ActivityMap.linkExclusions
description: Filtern von Activity Map-Daten nach Link-Name.
role: Admin, Developer
feature: Appmeasurement Implementation
exl-id: 9fc95016-362d-4c21-806e-e23adce9b6f7
TQID: https://experienceleague.adobe.com/y8RH2nGcIHYvrTwotHAbtFxu7hIXoh48FuU2OBsAuuM
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 206
ht-degree: 17%

---

# ActivityMap.linkExclusions

Mit der `ActivityMap.linkExclusions` Variable können Sie Activity Map-Daten basierend auf dem Text in der Dimension [Activity Map Link](/help/components/dimensions/activity-map-link.md) selektiv filtern oder ausschließen.

## Verknüpfen von Ausschlüssen in der Web SDK-Erweiterung

Wenn **[!UICONTROL Click-Datenerfassung aktivieren]** aktiviert ist, verwenden Sie den **[!UICONTROL Filter click properties]** Callback-Code-Block. Innerhalb dieses Code-Blocks können Sie den Wert von `content.linkName` überprüfen und entweder den Wert ändern oder die Sammlung von Linktracking-Daten aufgeben.

## Verknüpfen von Ausschlüssen in der Web SDK JavaScript-Bibliothek

Wenn [`clickCollectionEnabled`](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) aktiviert ist, verwenden Sie den `filterClickDetails` Callback im `clickCollection`. Innerhalb dieses Callbacks können Sie den Wert von `linkName` überprüfen und entweder den Wert ändern oder die Sammlung von Linktracking-Daten aufgeben.

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

Die `s.ActivityMap.linkExclusions`-Variable ist eine Zeichenfolge, die kommagetrennte Werte von Phrasen enthält, die vom Activity Map-Tracking ausgeschlossen werden sollen. Wenn eine der Phrasen mit dem in der Dimension [Activity Map Link](/help/components/dimensions/activity-map-link.md) erfassten Wert übereinstimmt, werden alle Activity Map-Daten aus dem Treffer entfernt. Beachten Sie, dass diese Variable `linkName` betrachtet, nicht `linkUrl`.

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
