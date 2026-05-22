---
title: campaign
description: Füllen Sie die Dimension „Trackingcode“.
feature: Appmeasurement Implementation
exl-id: 2278d2b8-8d60-4634-a176-f027a237bc12
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/4OF7xoZs8bLS4UW8wfJYHqSyc-gNVLAfPs5j3NwZCcM'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 244
ht-degree: 74%

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
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und legen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
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
