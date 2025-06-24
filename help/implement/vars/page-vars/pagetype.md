---
title: pageType
description: Stellen Sie fest, ob es sich bei der aktuellen Seite um einen 404-Fehler handelt.
feature: Appmeasurement Implementation
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '201'
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
