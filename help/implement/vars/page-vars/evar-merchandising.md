---
title: eVar (Merchandising-Variable)
description: Benutzerdefinierte Variablen, die mit Einzelprodukten verknüpft sind.
feature: Appmeasurement Implementation
exl-id: 26e0c4cd-3831-4572-afe2-6cda46704ff3
mini-toc-levels: 3
role: Admin, Developer
TQID: 'https://experienceleague.adobe.com/BdChWcR9AJqLZ0KjOxSvFAjB8-58JmmGahrpvTyFeFI'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
    internal-label: Variables
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: ca917b867cd84b09b899ce7b72586f0b15003106
workflow-type: tm+mt
source-wordcount: '787'
ht-degree: 29%
---
# eVar (Merchandising)

>[!BEGINSHADEBOX]

*Auf dieser Hilfeseite wird die Implementierung von Merchandising-eVars beschrieben. Informationen dazu, wie Merchandising-eVars als Dimension funktionieren, finden Sie unter [eVar (Merchandising-Dimension)](/help/components/dimensions/evar-merchandising.md) im Komponenten-Benutzerhandbuch.*

>[!ENDSHADEBOX]

Merchandising-eVars binden einen Wert an einzelne Produkte, sodass Erfolgsereignisse, die jedes Produkt betreffen, dem an dieses Produkt gebundenen Wert gutgeschrieben werden. Sie haben zwei Möglichkeiten, den Wert festzulegen:

* **[!UICONTROL Produktsyntax]**: Legen Sie den Wert für jedes Produkt in der [`products`](products.md) fest.
* **[!UICONTROL Konversionsvariablensyntax]**: Legen Sie den Wert in der eVar selbst fest. Der Wert wird an die Produkte in einem Treffer gebunden, der ein Binding-Ereignis enthält.

Informationen zur Funktionsweise von Bindung, Zuordnung und Gültigkeit finden Sie unter [eVar (Merchandising-Dimension)](/help/components/dimensions/evar-merchandising.md).

## Einrichten von eVars in den Report Suite-Einstellungen

Bevor Sie eVars in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie die eVar in den Report Suite-Einstellungen gemäß der gewünschten Syntax konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md).

>[!WARNING]
>
>Wenn Merchandising-eVars nicht korrekt konfiguriert werden, führt dies zu unerwarteten Werten oder Datenverlusten für die Variable. Vergewissern Sie sich, dass sie für Ihre Implementierung korrekt konfiguriert ist.

## Syntax auswählen

Verwenden Sie [!UICONTROL Produktsyntax] wenn der Merchandising-Wert zum Zeitpunkt der Festlegung der `products` verfügbar ist oder wenn Produkte im selben Treffer unterschiedliche Werte benötigen. Verwenden Sie [!UICONTROL Konversionsvariablensyntax] wenn der Wert vor dem Produkt bekannt ist, z. B. der Suchbegriff oder die interne Kampagne, die den Besucher zum Produkt geführt hat. Siehe [Funktionsweise von Bindung und Zuordnung](/help/components/dimensions/evar-merchandising.md#how-binding-and-allocation-work) für einen vollständigen Vergleich.

## Implementieren mit der Produktsyntax

Wenn [!UICONTROL Produktsyntax] aktiviert ist, wird der Merchandising-Wert direkt innerhalb der `products` festgelegt, sodass keine Binding-Ereignisse verwendet werden. Merchandising-eVars befinden sich im letzten Segment jedes Produkts:

```js
s.products = "[category];[name];[quantity];[revenue];[events];[eVars]";
```

Trennen Sie mehrere Merchandising-eVars für dasselbe Produkt durch einen senkrechten Strich (`|`). Die leeren Platzhalter für Menge, Umsatz und Ereignisse sind erforderlich, auch wenn Sie sie nicht verwenden. Ohne sie wird der eVar-Wert ignoriert.

Der Wert ist an das Produkt in diesem Treffer gebunden. Ob ein späterer Wert eine vorhandene Bindung ersetzt, hängt von der Einstellung [!UICONTROL Zuordnung] ab. Siehe [Funktionsweise von Bindung und Zuordnung](/help/components/dimensions/evar-merchandising.md#how-binding-and-allocation-work).

```js
// The bare minimum to set a merchandising eVar with product syntax
s.products = ";Example product;;;;eVar1=Example merchandising value";

// An example single product with product syntax
s.products = "Example category;Example product;1;5.99;event1=1;eVar1=Turtles";

// Tie a merchandising eVar to different values on two different products
s.products = "Birds;Scarlet Macaw;1;4200;;eVar1=talking bird,Birds;Turtle dove;2;550;;eVar1=love birds";
```

### Produktsyntax, die das Web SDK verwendet

Wenn Sie das [**XDM-Objekt**](/help/implement/aep-edge/xdm-var-mapping.md) verwenden, verwenden Merchandising-Variablen mit Produktsyntax die folgenden XDM-Felder:

* Merchandising-eVars mit Produktsyntax sind unter `xdm.productListItems[]._experience.analytics.customDimensions.eVars.eVar1` bis `xdm.productListItems[]._experience.analytics.customDimensions.eVars.eVar250` zugeordnet.
* Merchandising-Ereignisse mit Produktsyntax sind unter `xdm.productListItems[]._experience.analytics.event1to100.event1.value` bis `xdm.productListItems[]._experience.analytics.event901to1000.event1000.value` zugeordnet. XDM-Felder zur [Ereignis-Serialisierung](events/event-serialization.md) sind unter `xdm.productListItems[]._experience.analytics.event1to100.event1.id` bis `xdm.productListItems[]._experience.analytics.event901to1000.event1000.id` zugeordnet.

>[!NOTE]
>
>Beim Festlegen von Ereignissen unter `productListItems` müssen Sie diese nicht in der Ereigniszeichenfolge festlegen. Falls sie an beiden Stellen festgelegt sind, hat der Wert in der Ereigniszeichenfolge Vorrang.

Das folgende Beispiel zeigt ein [Produkt](products.md) unter Verwendung mehrerer Merchandising-eVars und -Ereignisse:

```json
"productListItems": [
  {
    "name": "Bahama Shirt",
    "priceTotal": "12.99",
    "quantity": 3,
    "_experience": {
      "analytics": {
        "customDimensions" : {
          "eVars" : {
            "eVar10" : "green",
            "eVar33" : "large"
          }
        },
        "event1to100" : {
          "event4" : {
            "value" : 1
          },
          "event10" : {
            "value" : 2,
            "id" : "abcd"
          }
        }
      }
    }
  }
]
```

Das obige Beispielobjekt würde wie folgt an Adobe Analytics gesendet werden: `";Bahama Shirt;3;12.99;event4|event10=2:abcd;eVar10=green|eVar33=large"`.

Bei Verwendung des [**Datenobjekts**](/help/implement/aep-edge/data-var-mapping.md) werden Merchandising-eVars mit Produktsyntax in `data.__adobe.analytics.products` festgelegt, wobei dieselbe Syntax wie bei der AppMeasurement-`products` verwendet wird. Das Datenobjekt-Äquivalent des obigen XDM-Beispiels:

```json
"data": {
  "__adobe": {
    "analytics": {
      "products": ";Bahama Shirt;3;12.99;event4|event10=2:abcd;eVar10=green|eVar33=large"
    }
  }
}
```

## Implementieren mit Syntax der Konversionsvariablen

Verwenden Sie [!UICONTROL Konversionsvariablensyntax] wenn der eVar-Wert nicht verfügbar ist, um ihn in der `products`-Variablen festzulegen. Dieses Szenario bedeutet in der Regel, dass Ihre Produktseite keinen Kontext des Merchandising-Kanals oder der Suchmethode hat. Legen Sie in diesen Fällen die Merchandising-eVar auf oder vor der Seite fest, auf der das Binding-Ereignis auftritt. Der Wert bleibt erhalten, bis er abläuft, oder wird mit einem neuen Wert überschrieben.

Wenn ein Treffer sowohl die Variable `products` als auch ein ausgewähltes [!UICONTROL Merchandising-Binding-Ereignis] enthält, wird der aktuelle Wert der eVar an jedes Produkt in diesem Treffer gebunden. Wenn Sie die eVar neben einem Produkt ohne Binding-Ereignis festlegen, wird der Wert nicht gebunden. Ob eine spätere Bindung eine vorhandene ersetzt, hängt von der Einstellung [!UICONTROL Zuordnung] ab. Siehe [Funktionsweise von Bindung und Zuordnung](/help/components/dimensions/evar-merchandising.md#how-binding-and-allocation-work).

Ein Beispiel, das mehrere eVars für Produktsuchmethoden gleichzeitig festlegt, finden Sie [Best Practice: Produktsuchmethoden](/help/components/dimensions/evar-merchandising.md#best-practice-product-finding-methods).

Im folgenden Beispiel wird eine Merchandising-eVar vor dem Binding-Ereignis festgelegt:

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = ";Canary";
```

Wenn [!UICONTROL Produktansichtsereignis] ein Binding-Ereignis ist, ist der für `eVar1` `"Aviary"` Wert an die `"Canary"` gebunden. Nachfolgende Erfolgsereignisse, die dieses Produkt betreffen, werden `"Aviary"` gutgeschrieben. Der Wert `"Aviary"` auch an Produkte bei späteren Treffern gebunden, die ein Binding-Ereignis enthalten, bis eine der folgenden Bedingungen erfüllt ist:

* Die eVar läuft ab (basierend auf der Einstellung [!UICONTROL Läuft ab nach]).
* Die Merchandising-eVar wird mit einem neuen Wert überschrieben.

### Konversionsvariablensyntax, die das Web SDK verwendet

Bei Verwendung des [**XDM-**](/help/implement/aep-edge/xdm-var-mapping.md)) funktioniert die Syntax ähnlich wie die Implementierung anderer [eVars](evar.md) und [Ereignisse](events/events-overview.md). Bei Verwendung des [**Datenobjekts**](/help/implement/aep-edge/data-var-mapping.md) folgt die Syntax AppMeasurement.

Das XDM-Spiegeln des obigen AppMeasurement-Beispiels würde wie folgt aussehen.

Festlegen der eVar für denselben oder vorherigen Ereignisaufruf:

```json
"_experience": {
  "analytics": {
    "customDimensions": {
      "eVars": {
        "eVar1" : "Aviary"
      }
    }
  }
}
```

Festlegen des Binding-Ereignisses und der Werte für die Produktzeichenfolge:

```json
"commerce": {
  "productViews" : {
    "value" : 1
  }
},
"productListItems": [
  {
    "name": "Canary"
  }
]
```

Die Datenobjekte, die das obige AppMeasurement-Beispiel spiegeln, würden wie folgt aussehen.

Festlegen der eVar für denselben oder vorherigen Ereignisaufruf:

```json
"data": {
  "__adobe": {
    "analytics": {
      "eVar1": "Aviary"
    }
  }
}
```

Festlegen des Binding-Ereignisses und der Werte für die Produktzeichenfolge:

```json
"data": {
  "__adobe": {
    "analytics": {
      "events": "prodView",
      "products": ";Canary"
    }
  }
}
```

