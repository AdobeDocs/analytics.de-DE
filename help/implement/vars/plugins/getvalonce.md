---
title: getValOnce
description: Verhindern Sie, dass eine Analytics-Variable zweimal hintereinander auf denselben Wert gesetzt wird.
feature: Variables
exl-id: 23bc5750-43a2-4693-8fe4-d6b31bc34154
source-git-commit: b8640d1387a475e2a9dd082759f0514bd18c1b6e
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 98%

---

# Adobe-Plug-in: getValOnce

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getValOnce`-Plug-in verhindert, dass eine Variable mehrmals auf denselben Wert gesetzt wird. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie Vorkommnisse deduplizieren möchten, bei denen ein Besucher eine Seite aktualisiert oder eine bestimmte Seite mehrmals besucht. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht an der Metrik „Vorkommnisse“ in Analysis Workspace interessiert sind.

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
    * Action Type: Initialize getValOnce
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
/* Adobe Consulting Plugin: getValOnce v3.1 */
function getValOnce(vtc,cn,et,ep){var e=vtc,i=cn,t=et,n=ep;  if(arguments&&"-v"===arguments[0])return{plugin:"getValOnce",version:"3.1"};var o=function(){if(void 0!==window.s_c_il){for(var e,i=0;i<window.s_c_il.length;i++)if((e=window.s_c_il[i])._c&&"s_c"===e._c)return e}}();if(void 0!==o&&(o.contextData.getValOnce="3.1"),window.cookieWrite=window.cookieWrite||function(e,i,t){if("string"==typeof e){var n=window.location.hostname,o=window.location.hostname.split(".").length-1;if(n&&!/^[0-9.]+$/.test(n)){o=2<o?o:2;var r=n.lastIndexOf(".");if(0<=r){for(;0<=r&&1<o;)r=n.lastIndexOf(".",r-1),o--;r=0<r?n.substring(r):n}}if(g=r,i=void 0!==i?""+i:"",t||""===i){if(""===i&&(t=-60),"number"==typeof t){var f=new Date;f.setTime(f.getTime()+6e4*t)}else f=t}return!!e&&(document.cookie=encodeURIComponent(e)+"="+encodeURIComponent(i)+"; path=/;"+(t?" expires="+f.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!=typeof cookieRead)&&cookieRead(e)===i}},window.cookieRead=window.cookieRead||function(e){if("string"!=typeof e)return"";e=encodeURIComponent(e);var i=" "+document.cookie,t=i.indexOf(" "+e+"="),n=0>t?t:i.indexOf(";",t);return(e=0>t?"":decodeURIComponent(i.substring(t+2+e.length,0>n?i.length:n)))?e:""},e){var i=i||"s_gvo",t=t||0,n="m"===n?6e4:864e5;if(e!==cookieRead(i)){var r=new Date;return r.setTime(r.getTime()+t*n),cookieWrite(i,e,0===t?0:r),e}}return""}
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getValOnce`-Funktion verwendet die folgenden Argumente:

* **`vtc`** (erforderlich, Zeichenfolge): Die Variable, die daraufhin geprüft werden soll, ob sie gerade zuvor auf einen identischen Wert gesetzt wurde
* **`cn`** (optional, Zeichenfolge): Der Name des Cookies, das den zu prüfenden Wert enthält. Die Standardeinstellung ist `"s_gvo"`
* **`et`** (optional, Ganzzahl): Der Ablauf des Cookies in Tagen (oder Minuten, je nach dem `ep`-Argument). Die Standardeinstellung ist `0`, die am Ende der Browser-Sitzung abläuft
* **`ep`** (optional, Zeichenfolge): Legen Sie dieses Argument nur fest, wenn das `et`-Argument ebenfalls festgelegt ist. Setzen Sie dieses Argument auf `"m"`, wenn Sie möchten, dass das `et`-Argument in Minuten statt in Tagen abläuft. Die Standardeinstellung ist `"d"`, die das `et`-Argument in Tagen festlegt.

Wenn das Argument `vtc` und der Cookie-Wert übereinstimmen, gibt diese Funktion eine leere Zeichenfolge zurück. Wenn das Argument `vtc` und der Cookie-Wert nicht übereinstimmen, gibt die Funktion das Argument `vtc` als Zeichenfolge zurück.

## Beispiele

```js
// Prevent the same value from being passed in to the campaign variable more than once in a row for next 30 days
s.campaign = getValOnce(s.campaign,"s_campaign",30);

// Prevent the same value from being passed in to eVar2 more than once in a row for the browser session
s.eVar2 = getValOnce(s.eVar2,"s_ev2");

// Prevent the same value from being passed in to eVar8 more than once in a row for 10 minutes
s.eVar8 = getValOnce(s.eVar8,"s_ev8",10,"m");
```

## Versionsverlauf

### 3.1 (22. September 2022)

* Fehler für Ablauf behoben

### 3.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 2.01

* Es wurde ein Problem beim Schreiben von Cookies behoben.

### 2.0

* Zwischenversion (neu kompiliert, kleinere Code-Größe).

### 1.1

* Es wurde die Option hinzugefügt, über den `t`-Parameter Minuten oder Tage für den Ablauf auszuwählen.
* Der Umfang der verwendeten `k`-Variablen wurde korrigiert, um sie auf das Plug-in zu beschränken. Diese Änderung verhindert mögliche Interferenzen mit anderen Code auf der Seite.
