---
title: events
description: Legen Sie die Ereignisvariable fest, die die meisten Metriken auf Ihrer Website steuert.
feature: Variables
exl-id: 6ef99ee5-40c3-4ff2-a75d-c97f2e8ec1f8
role: Admin, Developer
source-git-commit: 3e72235ce1455177efeb21017f61af25d21bd500
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 85%

---

# events

Dimensionen und Metriken sind wichtige Komponenten für Berichte. Die `events`-Variable ist für die Datenerfassung vieler Metriken auf Ihrer Website verantwortlich. Ereignis inkrementieren normalerweise die [Metriken](/help/components/metrics/overview.md) in Berichten.

Bevor Sie Ereignisse implementieren, stellen Sie sicher, dass Sie sie in den Report Suite-Einstellungen unter [Erfolgsereignisse](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) erstellen und konfigurieren. Wenn Sie vorhaben, benutzerspezifische Ereignisse in Linktracking-Treffern zu verwenden, stellen Sie sicher, dass [`linkTrackVars`](../../config-vars/linktrackvars.md) und [`linkTrackEvents`](../../config-vars/linktrackevents.md) korrekt eingestellt sind.

## Ereignisse, die das Web SDK verwenden

Wenn Sie die [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md), verwenden benutzerdefinierte Ereignisse die folgenden XDM-Felder:

* Benutzerdefinierte Ereignisse 1–100 werden zugeordnet zu `xdm._experience.analytics.event1to100.event1` – `xdm._experience.analytics.event1to100.event100`.
* Benutzerdefinierte Ereignisse 101–200 werden zugeordnet zu `xdm._experience.analytics.event101to200.event100` – `xdm._experience.analytics.event101to200.event200`.
* Dieses Muster wiederholt alle 100 Ereignisse bis `xdm._experience.analytics.event901to1000.event901` – `xdm._experience.analytics.event901to1000.event1000`. `eventx.value` wird verwendet, um die zu inkrementierende Menge anzugeben. `eventx.id` wird für [Serialisierung](event-serialization.md) verwendet.
* Bestellungen werden `xdm.commerce.purchases.value` zugeordnet.
* Einheiten werden der Summe aller `productListItems[].quantity`-Felder zugeordnet.
* Der Umsatz wird der Summe aller `productListItems[].priceTotal`-Felder zugeordnet.
* Produktansichten werden `xdm.commerce.productViews.value` zugeordnet.
* Warenkörbe werden `xdm.commerce.productListOpens.value` zugeordnet.
* Hinzufügungen zum Warenkorb werden `xdm.commerce.productListAdds.value` zugeordnet.
* Entnahmen aus dem Warenkorb werden `xdm.commerce.productListRemovals.value` zugeordnet.
* Warenkorbansichten werden `xdm.commerce.productListViews.value` zugeordnet.
* Checkouts werden `xdm.commerce.checkouts.value` zugeordnet.

>[!NOTE]
>
>Wenn ein Ereignis unter `productListItems` festgelegt ist (z. B. `productListItems._experience.analytics.event1.value`) und sich dieses Ereignis noch nicht in diesem Feld befindet, wird dieses Ereignis automatisch diesem Feld hinzugefügt.

Wenn Sie die [**Datenobjekt**](/help/implement/aep-edge/data-var-mapping.md), verwenden alle Ereignisse `data.__adobe.analytics.events`, die der AppMeasurement-String-Syntax folgt. Wenn Sie dieses Feld festlegen, werden alle im XDM-Objekt festgelegten Ereignisse überschrieben und nicht an Adobe Analytics gesendet.

## Ereignisse, die die Adobe Analytics-Erweiterung verwenden

Sie können Ereignisse entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie die [!UICONTROL Erweiterung] einer Dropdown-Liste zu Adobe Analytics und dem [!UICONTROL Aktionstyp] nach [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Ereignisse].

Es stehen verschiedene Funktionen zur Verfügung:

* Eine Dropdown-Liste, in der Sie das einzuschließende Ereignis auswählen können
* Ein optionales Textfeld zur Serialisierung. Weitere Informationen finden Sie unter [Ereignis-Serialisierung](event-serialization.md).
* Ein optionales Textfeld für einen Ereigniswert. Sie können Währung für Währungsereignisse oder eine Ganzzahl für Ereignisse ohne Währungsangaben einschließen, um sie mehrmals zu erhöhen. Wählen Sie beispielsweise `event1` unter der Dropdown-Liste und einschließlich `10` in diesem Feld erhöht `event1` um 10 Uhr in der Berichterstellung.
* Eine Schaltfläche zum Hinzufügen eines weiteren Ereignisses. Sie können zu einer einzelnen Regel beliebig viele Ereignisse hinzufügen.

## s.events in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.events`-Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Ereignissen enthält, die in den Treffer einbezogen werden sollen. Die -Variable lässt bis zu 64.000 Byte zu, sodass so viele Ereignisse wie ein Treffer benötigt werden. Zu gültigen Werten gehören:

* `event1` - `event1000`: Benutzerdefinierte Ereignisse, die Sie nach Belieben einstellen können. Zeichnen Sie im [Lösungsdesigndokument](../../../prepare/solution-design.md) Ihres Unternehmens auf, wie Sie die einzelnen Ereignisse verwenden. Die Anzahl der verfügbaren Ereignisse hängt vom Analytics-Vertrag Ihres Unternehmens ab. In den meisten Unternehmen, die nicht über einen Altvertrag verfügen, stehen 1000 benutzerdefinierte Ereignisse zur Verfügung. Wenden Sie sich an Ihr Adobe Account Team, wenn Sie nicht sicher sind, wie viele benutzerspezifische Ereignisse für Sie verfügbar sind.
* `purchase`: Erhöht die Metrik [Bestellungen](/help/components/metrics/orders.md) um 1 und berechnet anhand der in der `products`-Variable festgelegten Werte [Einheiten](/help/components/metrics/units.md) und [Umsatz](/help/components/metrics/revenue.md). Weitere Informationen finden Sie unter [Kaufereignis](event-purchase.md).
* `prodView`: Erhöht die Metrik [Produktansichten](/help/components/metrics/product-views.md).
* `scOpen`: Erhöht die Metrik [Warenkorb](/help/components/metrics/carts.md).
* `scAdd`: Erhöht die Metrik [Zusatz zum Warenkorb](/help/components/metrics/cart-additions.md).
* `scRemove`: Erhöht die Metrik [Entnahme aus Warenkorb](/help/components/metrics/cart-removals.md).
* `scView`: Erhöht die Metrik [Warenkorbansicht](/help/components/metrics/cart-views.md).
* `scCheckout`: Erhöht die Metrik [Checkouts](/help/components/metrics/checkouts.md).

>[!NOTE]
>
>Bei dieser Variable wird zwischen Groß- und Kleinschreibung unterschieden. Vermeiden Sie die falsche Großschreibung von Ereigniswerten, um eine genaue Datenerfassung sicherzustellen.

```js
// Set the events variable to a single value
s.events = "event1";

// Set the events variable to multiple values
s.events = "event1,event13,purchase";
```

### Zählerereignisse mehrmals erhöhen

Sie können benutzerspezifische Ereignisse bei Bedarf mehrmals zählen. Weisen Sie dem gewünschten Ereignis in der Zeichenfolge eine Ganzzahl zu. In den Report Suite-Einstellungen erstellte Ereignisse sind standardmäßig Zählerereignisse.

```js
// Count event1 ten times
s.events = "event1=10";

// Count event1 twice and event2 once
s.events = "event1=2,event2";
```

>[!NOTE]
>
>Zählerereignisse unterstützen keine Währungs- oder Dezimalwerte. Verwenden Sie Währungsereignisse für Währungswerte oder numerische Ereignisse für Dezimalwerte.

### Währungsereignisse verwenden

Sie können ein benutzerspezifisches Ereignis ändern, um anstelle von Ganzzahlen eine Währung zu verwenden. Währungsereignisse werden automatisch in die Währung der Report Suite konvertiert, wenn die Währung der Report Suite und die `currencyCode`-Variable nicht übereinstimmen. Sie sind hilfreich, um Versandkosten, Rabatte oder Erstattungen zu berechnen. Sie können Währungsereignisse in der `products`-Variablen festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

Bevor Sie Währungsereignisse implementieren, stellen Sie sicher, dass Sie das gewünschte Ereignis in den Report Suite-Einstellungen unter [Erfolgsereignisse](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) auf „Währung“ festlegen.

```js
// Send $9.99 USD in event1 using the events variable. Make sure the event type for event1 is Currency in Report suite settings
s.currencyCode = "USD";
s.events = "event1=9.99";

// Send $9.99 USD in event1 using the products variable. Make sure the event type for event1 is Currency in Report suite settings
s.currencyCode = "USD";
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=9.99";
```

>[!NOTE]
>
>Wenn Sie einen Währungswert sowohl in der `events`-Variable als auch in der `products`-Variable festlegen, wird der Währungswert in `events` verwendet. Vermeiden Sie das Setzen von Währungswerten sowohl in der `events`- als auch in der `products`-Variablen.

### Numerische Ereignisse verwenden

Sie können ein benutzerspezifisches Ereignis ändern, um Dezimalwerte anstelle von Ganzzahlen zu akzeptieren. Numerische Ereignisse verhalten sich ähnlich wie Währungsereignisse, verwenden jedoch keine Währungsumrechnung. Sie können numerische Ereignisse in der `products`-Variablen festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

Bevor Sie numerische Ereignisse implementieren, stellen Sie sicher, dass Sie das gewünschte Ereignis in den Report Suite-Einstellungen unter [Erfolgsereignisse](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) auf „Numerisch“ festlegen.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

>[!NOTE]
>
>Wenn Sie einen numerischen Wert sowohl in der `events`-Variable als auch in der `products`-Variable festlegen, wird der numerische Wert in `events` verwendet. Vermeiden Sie das Setzen von numerischen Werten sowohl in der `events`- als auch in der `products`-Variable.
