---
title: campaign
description: Füllen Sie die Dimension „Trackingcode“.
feature: Appmeasurement Implementation
exl-id: 2278d2b8-8d60-4634-a176-f027a237bc12
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 67%

---

# campaign

Die `campaign`-Variable dient der Erfassung von Trackingcodes auf Ihrer Website. In früheren Versionen von Adobe Analytics gab es eine Sonderbehandlung, bei der sie als Aufschlüsselung in die meisten Dimensionen verwendet werden konnte. In der aktuellen Version von Adobe Analytics ist sie mit einer eVar identisch.

Diese Variable befüllt die Dimension [Trackingcode](/help/components/dimensions/tracking-code.md) . Normalerweise ruft sie den Wert aus einer Abfragezeichenfolge mithilfe der [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md)-Hilfsmethode ab. Ihre Organisation bestimmt jedoch genau, wie diese Variable festgelegt wird.

## Campaign mit der Web-SDK

Campaign ist den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `marketing.trackingCode`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.campaign` oder `data.__adobe.analytics.v0`

## Campaign mit der Adobe Analytics-Erweiterung

Sie können „campaign“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie [!UICONTROL &#x200B; Dropdown]Liste „Erweiterung“ auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
6. Suchen Sie den Abschnitt [!UICONTROL Kampagne].

Sie können „campaign“ auf einen Wert oder einen Abfragezeichenfolgenparameter setzen.

## s.campaign in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.campaign`-Variable ist eine Zeichenfolge, die normalerweise einen Trackingcode enthält, der in Marketing-Maßnahmen verwendet wird. Die maximale Länge beträgt 255 Byte. Werte, die länger als 255 Byte sind, werden beim Senden an Adobe automatisch abgeschnitten.

```js
// Set the campaign variable to a static value
s.campaign = "abc123";

// Collect the cid query string parameter value from the URL
// https://example.com?cid=abc123
s.campaign = s.Util.getQueryParam("cid");
```
