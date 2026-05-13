---
title: forceOnline
description: Legen Sie den Online-Status von AppMeasurement manuell fest.
feature: Appmeasurement Implementation
exl-id: 318408bf-bec6-49aa-a762-9d2eebab233e
role: Admin, Developer
TQID: https://experienceleague.adobe.com/lGbja9kO5jF-rONRF8mV0wsvZ-MG-xd725Uiuk65nzk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 80%

---

# forceOnline

Mit der `forceOnline()`-Methode können Sie den automatisch erkannten Status von AppMeasurement überschreiben.

>[!WARNING]
>
>Verwenden Sie diese Methode nur, wenn [`trackOffline`](../config-vars/trackoffline.md) aktiviert ist. Die Verwendung dieser Funktion außerhalb von Offline-Tracking kann zu Datenverlusten führen.

AppMeasurement erkennt automatisch den Online-Status des Geräts. Mit der `forceOnline()`-Methode können Sie AppMeasurement zwingen, Treffer so zu behandeln, als ob das Gerät online wäre. Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Ihr einziger Zweck besteht darin, den Online-Status in AppMeasurement zu überschreiben.

## Online erzwingen mit der Web-SDK

Web SDK unterstützt kein Offline-Tracking.

## Erzwingen von Online mithilfe der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.forceOnline() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Sie können die `s.forceOnline()`-Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie das Analytics-Objekt instanziiert haben.

```js
s.forceOnline();
```
