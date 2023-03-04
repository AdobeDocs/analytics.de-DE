---
title: getResponsiveLayout
description: Ermitteln Sie, welches Layout einer Website gerade angezeigt wird.
feature: Variables
exl-id: 5b192d02-fc3c-4b82-acb4-42902202ab5f
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 100%

---

# Adobe-Plug-in: getResponsiveLayout

{{plug-in}}

Mit dem `getResponsiveLayout`-Plug-in können Sie verfolgen, welche Version Ihrer auf einem responsiven Design basierenden Website aktuell von einem Besucher angesehen wird. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Ihre Website ein responsives Design verwendet und Sie die Version der von einem Besucher angezeigten Website verfolgen möchten. Dieses Plug-in ist nicht erforderlich, wenn Ihre Website kein responsives Design verwendet.

<!--## Install the plug-in using the Web SDK or the Adobe Analytics extension

Adobe offers an extension that allows you to use most commonly-used plug-ins.

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/data-collection) using your AdobeID credentials.
1. Click the desired tag property.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. If you haven't already, create a rule labeled "Initialize Plug-ins" with the following configuration:
    * Condition: None
    * Event: Core – Library Loaded (Page Top)
1. Add an action to the above rule with the following configuration:
    * Extension: Common Analytics Plugins
    * Action Type: Initialize getResponsiveLayout
1. Save and publish the changes to the rule.-->

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

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
/* Adobe Consulting Plugin: getResponsiveLayout v1.1 (Requires AppMeasurement) */
var getResponsiveLayout=function(ppw,plw,tw){var c=ppw,b=plw,e=tw;if("-v"===c)return{plugin:"getResponsiveLayout",version:"1.1"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.getResponsiveLayout="1.1");if(!(isNaN(c)||isNaN(b)||isNaN(e)||b<c||e<b))return a=window.innerWidth||document.documentElement.clientWidth||document.body.clientWidth,(c<b&&a<=b?a<=c?"phone portrait layout":"phone landscape layout":a<=b?"phone layout":a<=e?"tablet layout":"desktop layout")+":"+a+"x"+(window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight)};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getResponsiveLayout`-Funktion verwendet die folgenden Argumente:

* **`ppw`** (erforderlich, Ganzzahl): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Smartphone-Hochformat-Layout zu einem Smartphone-Querformat-Layout wechselt
* **`plw`** (Erforderlich, Ganzzahl): Die maximale Breite von Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Smartphone-Querformat-Layout zu einem Tablet-Layout wechselt
* **`tw`** (erforderlich, Ganzzahl): Die maximale Breite in Pixeln, die ein Browser-Fenster haben kann, bevor die Seite von einem Tablet-Layout zu einem Desktop-Layout wechselt

Der Aufruf dieser Funktion gibt eine Zeichenfolge zurück, die zwei durch einen Doppelpunkt (`:`) getrennte Teile enthält. Der erste Teil der Zeichenfolge enthält einen der folgenden Werte, je nach Browser-Breite und den obigen Argumenten:

* `"phone portrait layout"`
* `"phone landscape layout"`
* `"phone layout"` (für Websites ohne Layouts im Hoch- und Querformat)
* `"tablet layout"`
* `"desktop layout"`

Der zweite Teil der zurückgegebenen Zeichenfolge ist die Breite und Höhe des Browsers. Beispiel: `"desktop layout:1243x700"`.

## Beispiele

```js
// A visitor accesses your site on their laptop. The browser window is maximized.
// * Your site switches from phone portrait mode to phone landscape mode when the browser width is greater than 500 pixels
// * Your site switches from phone landscape mode to tablet mode when the browser width is greater than 700 pixels
// * Your site switches from tablet mode to desktop mode when the browser width is greater than 1000 pixels
// Sets eVar10 to "desktop layout:1920x937".
s.eVar10 = getResponsiveLayout(500, 700, 1000);

// A visitor accesses your site on their phone.
// * Your site has only a phone mode, a tablet mode, and a desktop mode
// * Your site switches from phone mode to tablet mode when the browser width is greater than 800 pixels
// * Your site switches from tablet mode to desktop mode when the browser width is greater than 1,100 pixels
// Sets eVar10 to "phone portrait layout:720x1280"
s.eVar10 = getResponsiveLayout(800, 800, 1100);
```

## Versionsverlauf

### 1.1 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 1.0 (2. Mai 2018)

* Erste Version.
