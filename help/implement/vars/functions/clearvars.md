---
title: clearVars
description: Löschen Sie Werte aus dem Instanzobjekt.
feature: Variables
exl-id: 8ecb2b2d-7b66-4232-b0ea-b8c6cdcc1515
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 67%

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

## Variablen mithilfe des Web SDK löschen

Wenn Sie Daten mit dem Web SDK an Adobe senden, werden alle XDM-Daten automatisch gelöscht.

## Variablen mithilfe der Adobe Analytics-Erweiterung löschen

Legen Sie beim Konfigurieren einer Regel die Aktion „Variablen löschen“ fest.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf das Symbol „+“.
5. Setzen Sie die Dropdownliste [!UICONTROL Erweiterung] auf Adobe Analytics und den Aktionstyp [!UICONTROL 3} auf [!UICONTROL Variablen löschen].]

## s.clearVars() in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Sie können die `s.clearVars()`-Methode an einer beliebigen Stelle in Ihrer Implementierung aufrufen, nachdem Sie die Analytics-Objektinstanz instanziiert haben.

```js
s.clearVars();
```
