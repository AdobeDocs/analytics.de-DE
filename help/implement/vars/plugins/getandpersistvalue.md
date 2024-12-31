---
title: getAndPersistValue
description: Speichern Sie einen Wert, der später jederzeit abgerufen werden kann.
feature: Variables
exl-id: b562f9ad-3844-4535-b729-bd3f63f6f0ae
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 70%

---

# Adobe-Plug-in: getAndPersistValue

{{plug-in}}

Mit dem `getAndPersistValue`-Plug-in können Sie einen Wert in einem Cookie speichern, das später während eines Besuchs abgerufen werden kann. Er erfüllt eine ähnliche Rolle wie die Funktion [!UICONTROL Speicherdauer] in der Adobe Analytics-Erweiterung in der Adobe Experience Platform-Datenerfassung. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie eine Analytics-Variable bei nachfolgenden Treffern automatisch auf dem gleichen Wert belassen wollen, nachdem die Variable gesetzt wurde. Dieses Plug-in ist nicht erforderlich, wenn die Funktion [!UICONTROL Speicherdauer] in der Analytics-Erweiterung ausreicht. Es ist auch nicht erforderlich, dieses Plug-in zu verwenden, wenn Sie Variablen in nachfolgenden Treffern nicht auf denselben Wert setzen und beibehalten müssen. Die integrierte Persistenz von eVars erfordert keine Verwendung dieses Plug-ins, da eVars von Adobe Server-seitig persistiert werden.

## Installieren des Plug-ins mithilfe der Web SDK-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die am häufigsten verwendeten Plug-ins mit der Web-SDK verwenden können.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie **[!UICONTROL links auf]** Tags“ und dann auf die gewünschte Tag-Eigenschaft.
1. Klicken Sie **[!UICONTROL links auf]** Erweiterungen“ und dann auf die Registerkarte **[!UICONTROL Katalog]**.
1. Suchen Sie die Erweiterung **[!UICONTROL Common Web SDK Plugins]** und installieren Sie sie.
1. Klicken **[!UICONTROL links auf]** Datenelemente“ und dann auf das gewünschte Datenelement.
1. Legen Sie den gewünschten Datenelementnamen mit der folgenden Konfiguration fest:
   * Erweiterung: Common Web SDK Plugins
   * Datenelement: `getAndPersistValue`
1. Stellen Sie die gewünschten Parameter auf der rechten Seite ein.
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
   * Aktionstyp: getAndPersistValue initialisieren
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
/* Adobe Consulting Plugin: getAndPersistValue v3.0 (Requires AppMeasurement) */
function getAndPersistValue(vtp,cn,ex){var d=vtp,k=cn,l=ex;if("undefined"!==typeof d&&"-v"===d)return{plugin:"getAndPersistValue",version:"3.0"};var a=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof a&&(a.contextData.getAndPersistValue="3.0");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};a=new Date;k=k?k:"s_gapv";(l=l?l:0)?a.setTime(a.getTime()+864E5*l):a.setTime(a.getTime()+18E5);"undefined"!==typeof d&&d||(d=cookieRead(k));cookieWrite(k,d,a);return d};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getAndPersist`-Funktion verwendet die folgenden Argumente:

* **`vtp`** (erforderlich): Der Wert, der von Seite zu Seite beibehalten werden soll
* **`cn`** (optional): Der Name des Cookies, in dem der Wert gespeichert werden soll. Wenn dieses Argument nicht gesetzt ist, heißt Das Cookie `"s_gapv"`
* **`ex`** (optional): Die Anzahl der Tage vor Ablauf des Cookies. Wenn dieses Argument `0` oder nicht gesetzt ist, läuft das Cookie am Ende des Besuchs ab (30 Minuten Inaktivität).

Wenn die Variable im `vtp`-Argument festgelegt ist, setzt das Plug-in das Cookie und gibt dann den Cookie-Wert zurück. Wenn die Variable im `vtp`-Argument nicht festgelegt ist, gibt das Plug-in nur den Cookie-Wert zurück.

## Beispiele

```js
// Sets eVar21 to "raccoon", and sets the ev21gapv cookie to "raccoon" (which expires in 28 days).
s.eVar21 = "raccoon";
s.eVar21 = getAndPersistValue(s.eVar21,"ev21gapv",28);

// Checks the "ev21gapv" cookie for a value and assigns it to eVar21. It does not set a cookie value or reset an existing cookie's expiration since the value is not set on the page.
// If there is a cookie, assigns eVar21 to that value. Otherwise, eVar21 is blank.
s.eVar21 = getAndPersistValue(s.eVar21,"ev21gapv",28);

// Checks the "ev21gapv" cookie for a value and assigns it to prop35. It does not set a cookie value or reset an existing cookie's expiration since eVar21 is not set on the page.
s.prop35 = getAndPersistValue(s.eVar21,"ev21gapv",28);

// Sets eVar21 to "panda", and sets the ev21gapv cookie to "panda" (which expires in 14 days). It then sets prop35 to the value contained in the ev21gapv cookie.
// Ultimately both eVar21 and prop35 contain the value "panda".
s.eVar21 = "panda";
s.prop35 = getAndPersistValue(s.eVar21,"ev21gapv",14);

// Sets eVar30 to "shopping", and sets the s_gapv cookie to "shopping" (which expires at the end of the browser session).
s.eVar30 = "shopping";
s.eVar30 = getAndPersistValue(s.eVar30);
```

## Versionsverlauf

### 3.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 2.0 (16. April 2018)

* Zwischenversion (kleinere Code-Größe)
* Die Übergabe von „0“ in das `ex`-Argument erzwingt nun den Ablauf nach 30 Minuten Inaktivität und nicht mehr den Ablauf am Ende der Browser-Sitzung.

### 1.0 (18. Januar 2016)

* Erste Version.
