---
title: Kaufereignis
description: Verwenden Sie das Kaufereignis, um Daten zu den Metriken „Bestellungen“, „Einheiten“ und „Umsatz“ zu erfassen.
feature: Variables
exl-id: 5ad148d6-cf45-4dea-846a-255004300bc2
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 72%

---

# Kaufereignis

Das Kaufereignis ist ein Wert in der `events`-Variablen. Dieser Wert ist nützlich für Organisationen, die Daten über den Umsatz erfassen möchten, den ihre Website generiert. Er ist stark von den Variablen [`products`](../products.md) und [`purchaseID`](../purchaseid.md) abhängig.

Wenn Sie ein Kaufereignis festlegen, wirkt sich dies auf die folgenden Metriken aus:

* Die Metrik „Bestellungen“ erhöht sich um 1
* Die Metrik „Einheiten“ erhöht sich um die Anzahl der Produkte in der `products`-Variablen
* Die Metrik „Umsatz“ erhöht sich um die Summe der Preisparameter in der `products`-Variablen

>[!NOTE]
>
>Umsatz wird nicht mit dem Mengenfeld multipliziert. Beispiel: `s.products="Womens;Socks;5;4.50"` überweist keine 22,50 USD in den Umsatz; Er überspringt 4,50 USD. Stellen Sie sicher, dass Ihre Implementierung den Gesamtumsatz für die aufgeführte Menge ausweist. Zum Beispiel `s.products="Womens;Socks;5;22.50"`.

## Festlegen des Kaufereignisses mit dem Web SDK

Das Kaufereignis ist [für Adobe Analytics zugeordnet](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) unter mehreren XDM-Feldern:

* Bestellungen werden zugeordnet zu `commerce.purchases.value`.
* Einheiten werden der Summe aller `productListItems[].quantity` -Felder.
* Der Umsatz wird der Summe aller `productListItems[].priceTotal` -Felder.

## Festlegen des Kaufereignisses mit der Adobe Analytics-Erweiterung

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Ereignisse] und wählen Sie im Dropdown-Menü „Ereignisse“ [!UICONTROL purchase] aus.

Andere abhängige Variablen wie `products` und `purchaseID` verfügen nicht über dedizierte Felder in der Analytics-Erweiterung in der Adobe Experience Platform-Datenerfassung. Verwenden Sie für diese Variablen den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## Festlegen des Kaufereignisses in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Das Kaufereignis ist eine Zeichenfolge, die als Teil der Ereignisvariablen festgelegt wird.

```js
// Set the purchase event by itself
s.events = "purchase";

// Set the purchase event alongside other events
s.events = "purchase,event1,event2";
```

## Deduplizierung des Kaufereignisses

Wenn Sie ein Kaufereignis auslösen, prüft Adobe Folgendes:

* Enthält der Treffer die `purchaseID`-Variable? Andernfalls verwendet Adobe Informationen aus dem Treffer, um eine „temporäre Kauf-ID“ zu erstellen. Diese temporäre Kauf-ID gilt nur für den Besucher des Treffers. Die vorigen 5 temporären Kauf-IDs werden für jede Besucher-ID pro Report Suite gespeichert.
* Stimmt die temporäre Kauf-ID mit einer der letzten fünf gespeicherten temporären Kauf-IDs überein? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.
* Wenn die `purchaseID`-Variable definiert ist, stimmt sie mit einem Wert überein, der bereits in der Report Suite für alle Besucher erfasst wurde? Wenn ja, wird bei der Bildanforderung von einem doppelten Kauf ausgegangen. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht im Reporting angezeigt.
