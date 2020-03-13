---
title: Datenschicht erstellen
description: Erfahren Sie, was eine Datenschicht in Ihrer Analytics-Implementierung ist und wie sie zur Zuordnung von Variablen in Adobe Analytics verwendet werden kann.
translation-type: tm+mt
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707

---


# Datenschicht erstellen

Eine Datenschicht ist ein Framework von JavaScript-Objekten auf Ihrer Site, die alle in Ihrer Implementierung verwendeten Variablenwerte enthalten. Dadurch erhalten Sie mehr Kontrolle und eine einfachere Wartung Ihrer Implementierung.

## Voraussetzungen

[Erstellen Sie ein Lösungsdesigndesign-Dokument](solution-design.md) - Es ist wichtig, dass Ihr Unternehmen die Anforderungen für die Verfolgung einhält. Stellen Sie sicher, dass Sie mit einem Lösungsdesign-Dokument vorbereitet sind, bevor Sie sich an Entwicklungsteams in Ihrem Unternehmen wenden.

## Arbeitsablauf

Die Implementierung von Adobe Analytics mit einer Datenschicht führt in der Regel folgende Schritte aus:

1. **Arbeiten Sie mit Ihrem Site-Entwicklungsteam zusammen, um eine Datenschicht** zu implementieren: Ihr Site-Entwicklungsteam ist in erster Linie dafür verantwortlich sicherzustellen, dass das Datenschichtobjekt mit korrekten Werten gefüllt wird. Überprüfen Sie diese Seite mit Ihrem Site-Entwicklungsteam, um sicherzustellen, dass die Erwartungen zwischen den Teams übereinstimmen.
   > [!NOTE] Die von Adobe empfohlenen Datenschichtspezifikationen sind optional. Wenn Sie bereits über eine Datenschicht verfügen oder sich anderweitig dafür entscheiden, die Adobe-Spezifikationen nicht einzuhalten, stellen Sie sicher, dass sich Ihr Unternehmen an den zu beachtenden Spezifikationen orientiert.
2. **Validieren Sie Ihre Datenschicht mithilfe einer Browser-Konsole**: Nachdem eine Datenschicht erstellt wurde, können Sie überprüfen, ob sie mit der Entwicklerkonsole eines Browsers funktioniert. Sie können die Entwicklerkonsole in den meisten Browsern mit dem `F12` Schlüssel öffnen. Ein Beispiel für einen Variablenwert wäre `digitalData.page.pageInfo.pageID`.
3. **Verwenden Sie Adobe Experience Platform Launch, um Datenschichtobjekte zu Datenelementen** starten zuzuordnen: Erstellen Sie Datenelemente in Launch und ordnen Sie sie den in Ihrer Datenschicht beschriebenen JavaScript-Attributen zu.
4. **Verwenden Sie die Adobe Analytics-Erweiterung in Launch, um Datenelemente Analytics-Variablen** zuzuordnen: Weisen Sie nach dem Dokument des Lösungsentwurfs jedes Datenelement der entsprechenden Analytics-Variable zu.

## Spezifikationen

Adobe empfiehlt, der [Customer Experience Digital Data Layer](https://www.w3.org/2013/12/ceddl-201312.pdf) zu folgen, die von der [Customer Experience Digital Data Community Group](https://www.w3.org/community/custexpdata/)beschrieben wird. In den folgenden Abschnitten erfahren Sie, wie Datenschichtelemente mit Adobe Analytics interagieren.

Das zu verwendende übergreifende Datenschichtobjekt wird empfohlen `digitalData`. Im folgenden Beispiel wird ein etwas umfangreiches JSON-Objekt der Datenschicht mit Beispielwerten Liste:

```js
digitalData = {
    pageInstanceID: "Example page - production",
    page: {
        pageInfo: {
            pageID: "5093",
            pageName: "Example page",
            destinationURL: "https://example.com/index.html",
            referringURL: "https://example.com/referrer.html",
            sysEnv: "desktop",
            variant: "2",
            version: "1.14",
            breadCrumbs: ["Home","Example group","Example page"],
            author: "J Smith",
            issueDate: "Example date",
            effectiveDate: "Example date",
            expiryData: "Example date",
            language: "en-US",
            geoRegion: "US",
            industryCodes: "Example industry codes",
            publisher: "Example publisher"
        },
        category: {
            primaryCategory: "Example page category",
            subCategory1: "Sub-category example"
        },
        attributes: {
            country: "US",
            language: "en-US"
        }
    },
    product1: {
        productInfo: {
            productID: "4859",
            productName: "Example product",
            description: "Example description",
            productURL: "https://example.com/product.html",
            productImage: "https://example.com/product_image.png",
            productThumbnail: "https://example.com/product_thumbnail.png",
            manufacturer: "Example manufacturer",
            size: "Product size"
        },
        category: {
            primaryCategory: "Example product category",
            subCategory: "Example sub-category"
        }
    },
    cart: {
        cartID: "934856",
        price: {
            basePrice: 200.00,
            voucherCode: "EXAMPLEVOUCHER1",
            voucherDiscount: 0.50,
            currency: "USD",
            taxRate: 0.20,
            shipping: 5.00,
            shippingMethod: "UPS",
            priceWithTax: 120,
            cartTotal: 125
        }
    },
    transaction: {
        transactionID: "694025",
        profile: {
            profileInfo: {
                profileID: "exampleprofile",
                userName: "exampleusername",
                email: "user@example.com"
            },
            address: {
                line1: "123 Vague Street",
                line2: "Apt 1",
                city: "Austin",
                stateProvince: "TX",
                postalCode: "78610",
                country: "USA"
            },
            shippingAddress: {
                line1: "123 Vague Street",
                line2: "Apt 1",
                city: "Austin",
                stateProvince: "TX",
                postalCode: "78610",
                country: "USA"
            }
        }
    },
    event1: {
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    },
    component1: {
        componentInfo: {
            componentID: "4921",
            componentName: "Example component"
        },
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    },
    user1: {
        segment: "Premium membership",
        profile1: {
            profileInfo: {
                profileID: "exampleprofile",
                userName: "exampleusername",
                email: "user@example.com",
                language: "en-US",
                returningStatus: "New"
            },
            social: {
                facebook: "examplefacebookid",
                twitter: "exampletwitterhandle"
            }
        }
    },
    privacy: {
        accessCategories1: {
            categoryName: "Default",
            domains: "adobedtm.com"
        }
    },
    version: "1.0"
}
```

Verwenden Sie den Bericht &quot; [Customer Experience Digital Data Layer](https://www.w3.org/2013/12/ceddl-201312.pdf) &quot;für Details zu den einzelnen Objekten und Unterobjekten. Nicht alle Websites verwenden alle Objekte. Wenn Sie beispielsweise eine News-Site hosten, ist es unwahrscheinlich, dass Sie diese für das `digitalData.product` Objekt verwenden.

Datenschichten sind erweiterbar. Wenn Sie unternehmensspezifische Anforderungen haben, können Sie Objekte in Ihre Datenschicht aufnehmen, um diese Anforderungen zu erfüllen.

## Festlegen von Datenschichtwerten

Datenschichten generieren in der Regel serverseitig und beziehen sich dabei auf dieselben Objekte, die zum Erstellen des Site-Inhalts verwendet werden. Stellen Sie die Datenschicht der Site auf der Grundlage der im [Lösungsdesign-Dokument](solution-design.md)Ihres Unternehmens festgelegten Tracking-Anforderungen ein.

## Nächste Schritte

[Ordnen Sie Datenschichtobjekte Datenelementen](../launch/layer-to-elements.md)zu: Verwenden Sie die Datenschicht Ihrer Site im Adobe Experience Platform Launch.
