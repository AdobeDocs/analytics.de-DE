---
title: Kaufereignis
description: Verwenden Sie das Kaufereignis, um Daten zu den Metriken „Bestellungen“, „Einheiten“ und „Umsatz“ zu erfassen.
feature: Appmeasurement Implementation
exl-id: 5ad148d6-cf45-4dea-846a-255004300bc2
role: Admin, Developer
TQID: https://experienceleague.adobe.com/r-L330P6HA5qWBmEW-2LwECo-d3dhVK1ovWsfraErXE
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 66%

---

# Kaufereignis

Das Kaufereignis ist ein Wert in der `events`-Variablen. Dieser Wert ist nützlich für Organisationen, die Daten über den Umsatz erfassen möchten, den ihre Website generiert. Er ist stark von den Variablen [`products`](../products.md) und [`purchaseID`](../purchaseid.md) abhängig.

Wenn Sie ein Kaufereignis festlegen, wirkt sich dies auf die folgenden Metriken aus:

* Die Metrik „Bestellungen“ erhöht sich um 1
* Die Metrik „Einheiten“ erhöht sich um die Anzahl der Produkte in der `products`-Variablen
* Die Metrik „Umsatz“ erhöht sich um die Summe der Preisparameter in der `products`-Variablen

>[!NOTE]
>
>Umsatz wird nicht mit dem Mengenfeld multipliziert. Beispielsweise fließen `s.products="Womens;Socks;5;4.50"` 22,50 USD nicht in den Umsatz ein, sondern 4,50 USD. Stellen Sie sicher, dass Ihre Implementierung den Gesamtumsatz für die aufgelistete Menge weitergibt. Zum Beispiel `s.products="Womens;Socks;5;22.50"`.

## Festlegen des Kaufereignisses mit der Web-SDK

Bei Verwendung des [**XDM-**](/help/implement/aep-edge/xdm-var-mapping.md)) verwendet das Kaufereignis die folgenden XDM-Felder:

* Bestellungen werden `xdm.commerce.purchases.value` zugeordnet.
* Einheiten werden der Summe aller `xdm.productListItems[].quantity`-Felder zugeordnet. Weitere Informationen finden Sie unter [`products`](../products.md) .
* Der Umsatz wird der Summe aller `xdm.productListItems[].priceTotal`-Felder zugeordnet.

```json
{
  "xdm": {
    "commerce": {
      "purchases": {
        "value": 1
      }
    }
  }
}
```

Bei Verwendung des [**Datenobjekts**](/help/implement/aep-edge/data-var-mapping.md) verwendet das Kaufereignis `data.__adobe.analytics.events`, wobei die AppMeasurement-Zeichenfolgensyntax befolgt wird.

```json
{
  "data": {
    "__adobe": {
      "analytics": {
        "events": "purchase"
      }
    }
  }
}
```

## Festlegen des Kaufereignisses mit der Adobe Analytics-Erweiterung

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und legen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen] fest.
6. Suchen Sie den Abschnitt [!UICONTROL Ereignisse] und legen Sie für die [!UICONTROL -Liste &#x200B;]Ereignisse“ [!UICONTROL Kauf] fest.

Andere abhängige Variablen wie `products` und `purchaseID` verfügen über keine eigenen Felder in der Analytics-Erweiterung in der Datenerfassung von Adobe Experience Platform. Verwenden Sie für diese Variablen den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## Kaufereignis in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung festlegen

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
* Stimmt die temporäre Kauf-ID mit einer der letzten fünf gespeicherten temporären Kauf-IDs überein? Wenn dies der Fall ist, wird die Bildanforderung als doppelter Kauf betrachtet. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht in Berichten angezeigt.
* Wenn die `purchaseID`-Variable definiert ist, stimmt sie mit einem Wert überein, der bereits in der Report Suite für alle Besucher erfasst wurde? Wenn dies der Fall ist, wird die Bildanforderung als doppelter Kauf betrachtet. Alle Konversionsvariablen, einschließlich des Kaufereignisses, werden nicht in Berichten angezeigt.
