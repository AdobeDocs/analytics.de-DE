---
title: cleanStr
description: Entfernen oder ersetzen Sie alle unnötigen Zeichen aus einer Zeichenfolge.
feature: Appmeasurement Implementation
exl-id: d699dcd4-5e0a-40d3-b345-e5b1a077d393
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 68%

---

# Adobe-Plug-in: cleanStr

{{plug-in}}

Das `cleanStr`-Plug-in entfernt oder ersetzt alle unnötigen Zeichen aus einer Zeichenfolge, einschließlich HTML-Tag-Zeichen, zusätzliche Leerzeichen, Tabulatoren und Zeilenumbrüche/Zeilenumschalter. Es ersetzt auch einfache linke/rechte Anführungszeichen durch einfache gerade Anführungszeichen (`'`). Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie unnötige Zeichen aus Variablenwerten entfernen möchten und die Funktion „Text bereinigen“ in der Adobe Experience Platform-Datenerfassung Ihre Implementierungsanforderungen nicht erfüllt. Dieses Plug-in ist nicht erforderlich, wenn die erfassten Daten keine unnötigen Zeichen enthalten oder die Funktion „Text bereinigen“ in der Adobe Experience Platform-Datenerfassung ausreicht.

## Installieren des Plug-ins über die Web SDK- oder Web SDK-Erweiterung

Dieses Plug-in wird noch nicht für die Verwendung in der Web-SDK unterstützt.

## Installieren des Plug-ins über die Adobe Analytics-Erweiterung

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
   * Aktionstyp: cleanStr initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung Common Analytics Plugins nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

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
/* Adobe Consulting Plugin: cleanStr v2.0 (No Prerequisites Required) */
function cleanStr(str){var a=str;if("-v"===a)return{plugin:"cleanStr",version:"2.0"};a:{if("undefined"!==typeof window.s_c_il){var b=0;for(var c;b<window.s_c_il.length;b++)if(c=window.s_c_il[b],c._c&&"s_c"===c._c){b=c;break a}}b=void 0}"undefined"!==typeof b&&(b.contextData.cleanStr="2.0");if("string"===typeof a){a=a.replace(/<\/?[^>]+(>|$)/g,"");a=a.trim();a=a.replace(/[\u2018\u2019\u201A]/g,"'");a=a.replace(/\t+/g,"");for(a=a.replace(/[\n\r]/g," ");-1<a.indexOf("  ");)a=a.replace(/\s\s/g," ");return a}return""}
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `cleanStr`-Funktion verwendet die folgenden Argumente:

* **`str`** (erforderlich, Zeichenfolge): Der Wert, den Sie von der HTML-Codierung, zusätzlichen Leerzeichen, Tabulatoren oder anderen unnötigen Zeichen bereinigen möchten.

Die Funktion gibt den Wert des `str`-Arguments zurück, wobei alle unnötigen Zeichen entfernt werden.

## Beispiele

```js
// Returns the value "this is a messystring". Note that both tabs and extra spaces are present in the original string.
// Multiple spaces are reduced to one, while tabs are omitted entirely.
s.eVar1 = "  this  is a      messy  string    ";
s.eVar1 = cleanStr(s.eVar1)

// This function call does not do anything because the code does not assign the returned value to a variable.
s.eVar1 = "  this  is a      messy  string    ";
cleanStr(s.eVar1);
```

## Versionsverlauf

### 2.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 1.0 (15. April 2018)

* Erste Version.
