---
title: pageType
description: Stellen Sie fest, ob es sich bei der aktuellen Seite um einen 404-Fehler handelt.
feature: Appmeasurement Implementation
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
role: Admin, Developer
TQID: https://experienceleague.adobe.com/SD-hwWJmZby-y99FIZHrnevSBsVqD6T5gwovn5tJfxo
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 75%

---

# pageType

Die `pageType`-Variable ist eine Markierung, mit der Sie Fehlerseiten (wie z. B. 404-Fehler) auf Ihrer Website angeben können. Wenn diese Variable die Zeichenfolge `errorPage` enthält, befüllt sie die [Dimension](/help/components/dimensions/pages-not-found.md) und [Metrik](/help/components/metrics/pages-not-found.md) „Seiten nicht gefunden“.

>[!IMPORTANT]
>
>Richten Sie diese Variable für Nicht-Fehler-Seiten ein.

## Seitentyp unter Verwendung des Web SDK

Der Kanal ist den folgenden Variablen zugeordnet:

* [XDM-](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.web.webPageDetails.isErrorPage` - Dieses XDM-Feld ist ein boolescher Wert. Setzen Sie ihn auf `true`, um die Seite als Fehlerseite zu kennzeichnen, oder auf `false`, wenn es sich nicht um eine Fehlerseite handelt.
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.pageType` - Dieses Datenobjektfeld ist eine Zeichenfolge. Setzen Sie es auf `"errorPage"`, um es als solches zu kennzeichnen.

## Seitentyp unter Verwendung der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.pageType in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.pageType`-Variable ist eine Zeichenfolge, bei der der `errorPage`-Wert der einzige gültige Wert ist. Setzen Sie diese Variable auf diesen Wert auf jeder Fehlerseite Ihrer Website, z. B. auf 404-Seiten.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>Verwenden Sie eine eVar, um den Fehler-Code zu erfassen, damit Sie weitere Informationen zu spezifischen Fehlern erhalten, auf die Besucher Ihrer Website stoßen.
