---
title: addProductEvar
description: Fügt der Variable „products“ Merchandising-eVars hinzu.
feature: Variables
exl-id: 6be94a15-78c9-4cbc-8b33-4a16f1b73b96
source-git-commit: bbb138d979968ec2536e53ff07001b43156df095
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 87%

---

# Adobe-Plug-in: addProductEvar

{{plug-in}}

Mit dem `addProductEvar`-Plug-in können Sie einfach eine Adobe Analytics-Merchandising-eVar hinzufügen, die die Produktsyntax verwendet, ohne sich Gedanken darüber machen zu müssen, ob die bereits vorhandenen Inhalte der Variablen „products“ geändert/verschoben/gelöscht werden. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie der [`products`](../page-vars/products.md)-Variablen einfach Merchandising-eVars mit Produktsyntax hinzufügen möchten. Sie müssen das `addProductEvar`-Plug-in nicht verwenden, wenn Sie keine Merchandising-eVars mit Produktsyntax verwenden.

>[!NOTE]
>
>Dieses Plug-in ersetzt keine eVars, die bereits in einem Produkteintrag vorhanden sind. Es werden nur Werte angehängt, die Sie mit diesem Plug-in festlegen. Seien Sie vorsichtig, wenn Sie eVars anhängen, die bereits für dieses Produkt existieren.

## Installieren des Plug-ins mit der Web SDK- oder Web SDK-Erweiterung

Dieses Plug-in wird noch nicht für die Verwendung im Web SDK unterstützt.

## Installieren des Plug-ins mit der Adobe Analytics-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die am häufigsten verwendeten Plug-ins mit Adobe Analytics verwenden können.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: addProductEvar initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung &quot;Common Analytics Plugins&quot;nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: addProductEvar v2.0 */
function addProductEvar(en,ev,ap){var e=en,f=ev,d=ap;if("-v"===e)return{plugin:"addProductEvar",version:"2.0"};a:{if("undefined"!==typeof window.s_c_il){var b=0;for(var c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c){b=c;break a}}b=void 0}if("undefined"!==typeof b&&(b.contextData.addProductEvar="2.0","string"===typeof e&&"string"===typeof f&&""!==f))if(d=d||!1,b.products){c=b.products.split(",");var g=c.length;d=d?0:g-1;for(var a;d<g;d++)a=c[d].split(";"),a[5]&&-1<a[5].toLowerCase().indexOf("evar")?a[5]=a[5]+"|"+e+"="+f:a[5]?a[5]=e+"="+f:a[5]||(a[4]||(a[4]=""),a[3]||(a[3]=""),a[2]||(a[2]=""),a[1]||(a[1]=""),a[5]=e+"="+f),c[d]=a.join(";");b.products=c.join(",")}else b.products=";;;;;"+e+"="+f};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Das `addProductEvar`-Plug-in verwendet die folgenden Argumente:

* **`en`** (erforderlich, Zeichenfolge): Die eVar, die zum letzten Eintrag hinzugefügt werden soll, der derzeit in der Variablen „products“ enthalten ist. Wenn die Variable „products“ leer ist, erstellt das Plug-in einen „leeren“ Produkteintrag mit dem eVar-Wert am Ende des Eintrags.
* **`ev`** (Erforderlich, Zeichenfolge): Der der eVar zugewiesene Wert.
* **`ap`** (optional, boolesch): Wenn die Variable „products“ derzeit mehr als einen Produkteintrag enthält, wird mit dem Wert „true“ (oder „1“) die eVar zu **allen** Produkteinträgen hinzugefügt.  Der Standardwert ist „false“ (oder „0“), wodurch die eVar nur dem **letzten** Eintrag in der Variablen „products“ hinzugefügt wird.

Das `addProductEvar`-Plug-in gibt nichts zurück. Stattdessen wird die im `en`- und `ev`-Argument angegebene eVar (und der eVar-Wert) zur `products`-Variablen hinzugefügt.

## Beispiele

```js
// Set a merchandising eVar to blue on the last product. The output for the products variable is ";product1;3;300,;product2;2;122,;product3;1;25;;eVar1=blue"
s.products=";product1;3;300,;product2;2;122,;product3;1;25";
addProductEvar("eVar1", "blue");

// Set a merchandising eVar to blue on all products. The output for the products variable is ";product1;3;300;;eVar1=blue,;product2;2;122;;eVar1=blue,;product3;1;25;;eVar1=blue"
s.products=";product1;3;300,;product2;2;122,;product3;1;25";
addProductEvar("eVar1", "blue", true);

// Set multiple merchandising eVars to the last product in the string. The output for the products variable is ";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue,;product2;2;122,;product3;1;25;;eVar23=medium|eVar24=women|eVar1=red"
s.products=";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue,;product2;2;122,;product3;1;25";
addProductEvar("eVar23", "medium");
addProductEvar("eVar24", "women");
addProductEvar("eVar1", "red");

// Set multiple merchandising eVars to all products in the string. The output for the products variable is ";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue|eVar23=medium|eVar24=women|eVar1=red,;product2;2;122;;eVar23=medium|eVar24=women|eVar1=red,;product3;1;25;;eVar23=medium|eVar24=women|eVar1=red"
s.products=";product1;3;300;event2=10;eVar23=large|eVar24=men|eVar1=blue,;product2;2;122,;product3;1;25";
addProductEvar("eVar23", "medium", true);
addProductEvar("eVar24", "women", true);
addProductEvar("eVar1", "red", true);

// If the products variable is not set, the plug-in creates an empty product string correctly delimited to the merchandising eVar. The output for the products variable is ";;;;;eVar1=blue"
addProductEvar("eVar1", "blue");
```

## Versionsverlauf

### 2.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 1.0 (7. Oktober 2019)

* Erste Version.
