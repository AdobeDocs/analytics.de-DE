---
title: getNewRepeat
description: Verfolgen Sie die Aktivitäten neuer oder wiederkehrender Besucher.
feature: Appmeasurement Implementation
exl-id: 8f64e176-1926-4cb1-bfae-09d7e2c015ae
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 74%

---

# Adobe-Plug-in: getNewRepeat

{{plug-in}}

Mit dem `getNewRepeat`-Plug-in können Sie innerhalb einer gewünschten Anzahl von Tagen feststellen, ob es sich bei einem Besucher um einen neuen Besucher oder einen wiederkehrenden Besucher handelt. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie Besucher anhand einer benutzerdefinierten Anzahl von Tagen als „neu“ identifizieren möchten. Dieses Plug-in ist nicht erforderlich, wenn die Besucherdimensionen „Neu“/„Wiederkehrend“ in Analysis Workspace den Anforderungen Ihres Unternehmens entsprechen.

## Installieren des Plug-ins mithilfe der Web SDK-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die am häufigsten verwendeten Plug-ins mit dem Web-SDK verwenden können.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie **[!UICONTROL links auf]** Tags“ und dann auf die gewünschte Tag-Eigenschaft.
1. Klicken Sie **[!UICONTROL links auf]** Erweiterungen“ und dann auf die Registerkarte **[!UICONTROL Katalog]**.
1. Suchen Sie die Erweiterung **[!UICONTROL Common Web SDK Plugins]** und installieren Sie sie.
1. Klicken **[!UICONTROL links auf]** Datenelemente“ und dann auf das gewünschte Datenelement.
1. Legen Sie den gewünschten Datenelementnamen mit der folgenden Konfiguration fest:
   * Erweiterung: Common Web SDK Plugins
   * Datenelement: `getNewRepeat`
1. Stellen Sie den `daysBeforeReset` Parameter auf der rechten Seite ein.
1. Speichern und veröffentlichen Sie die Änderungen am Datenelement.

## Manuelle Installation des Plug-ins durch Implementierung der Web-SDK

Dieses Plug-in wird noch nicht für die Verwendung in einer manuellen Implementierung der Web-SDK unterstützt.

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
   * Aktionstyp: getNewRepeat initialisieren
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
/* Adobe Consulting Plugin: getNewRepeat v3.0 (Requires AppMeasurement) */
function getNewRepeat(d){var a=d;if("-v"===a)return{plugin:"getNewRepeat",version:"3.0"};var d=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof d&&(d.contextData.getNewRepeat="3.0");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};a=a?a:30;d="s_nr"+a;var k=new Date,m=cookieRead(d),n=m.split("-"),l=k.getTime();k.setTime(l+864E5*a);if(""===m||18E5>l-n[0]&&"New"===n[1])return cookieWrite(d,l+"-New",k),"New";cookieWrite(d,l+"-Repeat",k);return"Repeat"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getNewRepeat`-Funktion verwendet die folgenden Argumente:

* **`d`** (Ganzzahl, optional): Die erforderliche Mindestanzahl von Tagen zwischen Besuchen, die Besucher auf `"New"` zurücksetzt. Wenn dieses Argument nicht festgelegt ist, wird der Standardwert 30 Tage verwendet.

Diese Funktion gibt den Wert von `"New"` zurück, wenn das vom Plug-in eingestellte Cookie nicht vorhanden oder abgelaufen ist. Gibt den Wert von `"Repeat"` zurück, wenn das vom Plug-in eingestellte Cookie vorhanden ist und die Zeit seit dem aktuellen Treffer und die im Cookie festgelegte Zeit länger als 30 Minuten sind. Diese Funktion gibt denselben Wert für den gesamten Besuch zurück.

Dieses Plug-in verwendet ein Cookie mit dem Namen `"s_nr[LENGTH]"`, bei dem `[LENGTH]` mit dem `d`-Argument übereinstimmt. Das Cookie enthält einen Unix-Zeitstempel, der die aktuelle Zeit und den aktuellen Status des Besuchers (`"New"` oder `"Repeat"`) darstellt.

## Beispiele

```js
// Sets eVar1 to "New" if it is the visitor's first visit to the site, or they have not visited in at least 30 days. Otherwise, sets eVar1 to "Repeat".
s.eVar1 = getNewRepeat();

// Sets eVar2 to "New" if it is the visitor's first visit to the site, or they have not visited in at least a year (365 days). Otherwise, sets eVar2 to "Repeat".
s.eVar2 = getNewRepeat(365);
```

## Versionsverlauf

### 3.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 2.1 (30. September 2019)

* Neuanordnung der JavaScript-Logik zur Reduzierung der Plug-in-Größe

### 2.0 (16. April 2018)

* Neu kompiliert mit kleinerer Code-Größe
* Die Möglichkeit, das Cookie zum Speichern der Besuchsinformationen zu benennen, wurde entfernt. Das Plug-in benennt das Cookie nun dynamisch basierend auf dem Wert, der an das `d`-Argument übergeben wird.
