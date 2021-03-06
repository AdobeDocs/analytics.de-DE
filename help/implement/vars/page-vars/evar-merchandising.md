---
title: eVar-Variablen (Merchandising)
description: Benutzerdefinierte Variablen, die mit Einzelprodukten verknüpft sind.
feature: Variables
exl-id: 26e0c4cd-3831-4572-afe2-6cda46704ff3
mini-toc-levels: 3
source-git-commit: 9a94e910d4e837bb9808b5662beebe6214ed4174
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 72%

---

# eVar (Merchandising)

*Auf dieser Hilfeseite wird die Implementierung von Merchandising-eVars beschrieben. Informationen dazu, wie Merchandising-eVars als Dimension funktionieren, finden Sie unter [eVar (Merchandising)](/help/components/dimensions/evar-merchandising.md) im Komponenten-Benutzerhandbuch.*

Eine ausführliche Erläuterung der Funktionsweise von Merchandising-eVars finden Sie unter [Merchandising-eVars und Methoden zur Produktsuche](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/merchandising-evars.html?lang=de).

## Einrichten von eVars in den Report Suite-Einstellungen

Bevor Sie eVars in Ihrer Implementierung verwenden, stellen Sie sicher, dass Sie die eVar in den Report Suite-Einstellungen auf die gewünschte Syntax konfigurieren. Weitere Informationen finden Sie im Admin-Handbuch unter [Konversionsvariablen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md).

>[!WARNING]
>
>Wenn Merchandising-eVars nicht korrekt konfiguriert werden, führt dies zu unerwarteten Werten oder Datenverlusten für die Variable. Vergewissern Sie sich, dass sie für Ihre Implementierung korrekt konfiguriert ist.

## Implementieren mit der Produktsyntax

Wenn „Produktsyntax“ aktiviert ist, wird die Merchandising-Kategorie direkt innerhalb der `products`-Variablen aufgefüllt. Daher ist es nicht erforderlich, ein Binding-Ereignis auszuwählen und festzulegen. Dies ist die empfohlene Methode und sollte verwendet werden, es sei denn, der in `products` festzulegende Wert ist nicht verfügbar, wenn das Erfolgsereignis stattfindet.

```js
// The bare minimum to set a merchandising eVar with product syntax
s.products = ";Example product;;;;eVar1=Example merchandising value";

// An example single product with product syntax
s.products = "Example category;Example product;1;5.99;event1=1;eVar1=Turtles";

// Tie a merchandising eVar to a different values on two different products
s.products = "Birds;Scarlet Macaw;1;4200;;eVar1=talking bird,Birds;Turtle dove;2;550;;eVar1=love birds";
```

Der Wert für `eVar1` wird dem Produkt zugewiesen. Alle nachfolgenden Erfolgsereignisse, die dieses Ereignis betreffen, werden dem eVar-Wert gutgeschrieben.

### Verwenden von XDM für die Edge-Sammlung

Jedes Feld in der Variable &quot;products&quot;wird durch ein entsprechendes XDM-Feld gefüllt. Sie können eine Liste aller Zuordnungen von XDM zu Analytics-Parametern anzeigen [here](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=en). Nachstehend finden Sie ein Beispiel dafür, wie die productListItems-XDM-Felder kombiniert werden, um eine Produktvariable zu erstellen.

XDM-Struktur:

```js
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

Resultierender Parameter &quot;products&quot;, der an Analytics übergeben wird:

```js
pl = ”;Bahama Shirt;3;12.99;event4|event10=2:abcd;eVar10=green|eVar33=large”
```

## Implementieren mit Syntax der Konversionsvariablen

Die Syntax der Konversionsvariablen wird verwendet, wenn der eVar-Wert nicht in der `products`-Variable gesetzt werden kann. Dieses Szenario bedeutet in der Regel, dass Ihre Seite keinen Kontext für den Merchandising-Kanal oder die Suchmethode hat. In diesen Fällen müssen Sie die Merchandising-Variable festlegen, bevor Sie auf die Produktseite gelangen, wobei der Wert so lange bestehen bleibt, bis das Binding-Ereignis eintritt.

Wenn das bei der Konfiguration ausgewählte Binding-Ereignis eintritt, wird der beibehaltene Wert der eVar dem Produkt zugewiesen. Wenn z. B. `prodView` als Binding-Ereignis ausgewählt wird, wird die Merchandising-Kategorie nur Zeitpunkt des Ereignisses mit der aktuellen Produktliste verknüpft. Eine Merchandising-eVar, die bereits einem Produkt zugewiesen wurde, kann nur von nachfolgenden Binding-Ereignissen aktualisiert werden.

```js
// Place on the same or previous page before the binding event:
s.eVar1 = "Aviary";

// Place on the page where the binding event occurs:
s.events = "prodView";
s.products = ";Canary";
```

Der Wert `"Aviary"` für `eVar1` wird dem Produkt `"Canary"` zugewiesen. Alle nachfolgenden Erfolgsereignisse, die dieses Ereignis betreffen, werden `"Canary"` gutgeschrieben. Des Weiteren wird der aktuelle Wert der Merchandising-Variablen allen nachfolgenden Produkten zugewiesen, bis eine der folgenden Bedingungen erfüllt ist:

* Die eVar läuft ab (basierend auf der Einstellung „Läuft ab nach“).
* Die Merchandising-eVar wird mit einem neuen Wert überschrieben.

### Verwenden von XDM für die Edge-Sammlung

Sie können dieselben Informationen mithilfe von XDM-Feldern angeben, die Analytics-Feldern zugeordnet sind. Sie können eine Liste aller Zuordnungen von XDM zu Analytics-Parametern anzeigen [here](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=en). Das XDM-Spiegeln des obigen Beispiels würde wie folgt aussehen:

Legen Sie die eVar für denselben oder vorherigen Ereignisaufruf fest:

```js
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

Legen Sie das Binding-Ereignis und die Werte für die Produktzeichenfolge fest:

```js
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
