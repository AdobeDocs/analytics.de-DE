---
title: purchaseID
description: Deduplizieren Sie Treffer basierend auf einer eindeutigen Kaufkennung.
feature: Variables
exl-id: 7a4d7f08-65ae-4541-a94e-cc6c445c01db
role: Admin, Developer
source-git-commit: 4bd46fd5a9b98bcca67a66c87c9bca67fa00061a
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 73%

---

# purchaseID

Die `purchaseID`-Variable verhindert, dass Berichte durch Treffer mit demselben Kauf erhöht werden. Wenn ein Besucher z. B. Ihre Kaufbestätigungsseite erreicht, senden Sie normalerweise Daten zum Umsatz, der durch die Transaktion generiert wurde, an Adobe. Wenn der Benutzer diese Seite mehrmals aktualisiert oder die Seite zu einem späteren Zeitpunkt mit Lesezeichen markiert, können diese Treffer die Berichte überhöhen. Die `purchaseID`-Variable dedupliziert Metriken, wenn mehrere Treffer dieselbe Kauf-ID haben.

Wenn Adobe einen Treffer als doppelten Kauf erkennt, werden alle Konversionsdaten (wie z. B. eVars und Ereignisse) nicht in der Berichterstellung angezeigt. In Daten-Feeds wird die `duplicate_purchase`-Spalte auf `1` gesetzt.

Die Kauf-IDs gelten für alle Besucher und laufen nach 37 Monaten ab. Wenn ein Besucher eine bestimmte Kauf-ID festlegt und ein anderer Besucher dieselbe Kauf-ID ein Jahr später festlegt, wird der zweite Kauf dedupliziert.

## Kauf-ID mit dem Web SDK

Die Kauf-ID ist den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.commerce.order.purchaseID`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.purchaseID`

## Kauf-ID mit der Adobe Analytics-Erweiterung

Sie können die Kauf-ID entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie die [!UICONTROL Erweiterung] einer Dropdown-Liste zu Adobe Analytics und dem [!UICONTROL Aktionstyp] nach [!UICONTROL Variablen festlegen].
6. Suchen Sie die [!UICONTROL Kauf-ID] Abschnitt.

Sie können die Kauf-ID auf einen Wert oder ein Datenelement festlegen. Sie können den Wert auch aus einer anderen Analytics-Variablen kopieren.

## s.purchaseID in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.purchaseID`-Variable ist eine Zeichenfolge, die eine eindeutige Kennung für einen Kauf enthält. Sie wird bei demselben Treffer wie ein Kaufereignis gesetzt. Verwenden Sie nur alphanumerische Zeichen, um diese Variable zu füllen.

Diese Variable kann maximal 20 Byte speichern. Werte, die länger als 20 Byte sind, werden abgeschnitten. Wenn dieser abgeschnittene Wert mit nachfolgenden abgeschnittenen Werten übereinstimmt, werden diese nachfolgenden Treffer dedupliziert.

```js
s.purchaseID = "ABC123";
```

Bei Verwendung der `digitalData` [Datenschicht](../../prepare/data-layer.md):

```js
s.purchaseID = digitalData.transaction.transactionID;
```

>[!CAUTION]
>
>Verwenden Sie keine Randomisierungsfunktion, um eine Kauf-ID zu generieren.
