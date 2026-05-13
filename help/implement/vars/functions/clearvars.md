---
title: clearVars
description: Löscht Werte aus dem Instanzobjekt.
feature: Appmeasurement Implementation
exl-id: 8ecb2b2d-7b66-4232-b0ea-b8c6cdcc1515
role: Admin, Developer
TQID: https://experienceleague.adobe.com/oZOgS1REUIwiLCwM1URlDy7rkpmeM59hrkOX7DBVVcE
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 68%

---

# clearVars

Einige Implementierungen, z. B. bei Einzelseitenanwendungen, erfordern mehrere Treffer, die mit demselben Seitenladevorgang gesendet werden. Verwenden Sie die `clearVars()`-Methode, um Variablenwerte zu löschen, damit sie nicht auf nachfolgenden Treffern bestehen bleiben.

Diese Methode akzeptiert keine Argumente und gibt keinen Wert zurück. Der einzige Zweck besteht darin, Variablenwerte aus dem Instanzobjekt zu löschen. Diese Methode setzt die folgenden Elemente auf `undefined`:

* `prop1` – `prop75`
* `eVar` – `eVar250`
* `hier1` – `hier5`
* `list1` – `list3`
* `events`
* `products`
* `channel`
* `purchaseID`
* `transactionID`
* `state`
* `zip`
* `campaign`

## Löschen von Variablen mithilfe der Web-SDK

Wenn Sie Daten mithilfe der Web-SDK an Adobe senden, werden alle XDM-Daten automatisch gelöscht.

## Löschen von Variablen mithilfe der Adobe Analytics-Erweiterung

Legen Sie beim Konfigurieren einer Regel die Aktion „Variablen löschen“ fest.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf das Symbol „+“.
5. Legen Sie [!UICONTROL &#x200B; Dropdown]Liste „Erweiterung“ auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen löschen] fest.

## s.clearVars() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Sie können die `s.clearVars()`-Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie die Analytics-Objektinstanz instanziiert haben.

```js
s.clearVars();
```
