---
title: getPreviousValue
description: Rufen Sie den letzten Wert ab, der an eine Variable übergeben wird.
feature: Appmeasurement Implementation
exl-id: 235c504b-ba97-4399-a07b-b0bfc764f1ba
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 77%

---

# Adobe-Plug-in: getPreviousValue

{{plug-in}}

Mit dem `getPreviousValue`-Plug-in können Sie eine Variable auf einen Wert einstellen, der bei einem vorherigen Treffer festgelegt wurde. Dieses Plug-in ist nicht erforderlich, wenn Ihre Implementierung alle gewünschten Werte im aktuellen Treffer enthält.

## Installieren des Plug-ins mithilfe der Web SDK-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die am häufigsten verwendeten Plug-ins mit dem Web-SDK verwenden können.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie **[!UICONTROL links auf]** Tags“ und dann auf die gewünschte Tag-Eigenschaft.
1. Klicken Sie **[!UICONTROL links auf]** Erweiterungen“ und dann auf die Registerkarte **[!UICONTROL Katalog]**.
1. Suchen Sie die Erweiterung **[!UICONTROL Common Web SDK Plugins]** und installieren Sie sie.
1. Klicken **[!UICONTROL links auf]** Datenelemente“ und dann auf das gewünschte Datenelement.
1. Legen Sie den gewünschten Datenelementnamen mit der folgenden Konfiguration fest:
   * Erweiterung: Common Web SDK Plugins
   * Datenelement: `getPreviousValue`
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
   * Aktionstyp: getPreviousValue initialisieren
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
/* Adobe Consulting Plugin: getPreviousValue v3.0 */
function getPreviousValue(v,c){var k=v,d=c;if("-v"===k)return{plugin:"getPreviousValue",version:"3.0"};var a=function(){if("undefined"!==typeof window.s_c_il)for(var c=0,b;c<window.s_c_il.length;c++)if(b=window.s_c_il[c],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof a&&(a.contextData.getPreviousValue="3.0");window.cookieWrite=window.cookieWrite||function(c,b,f){if("string"===typeof c){var h=window.location.hostname,a=window.location.hostname.split(".").length-1;if(h&&!/^[0-9.]+$/.test(h)){a=2<a?a:2;var e=h.lastIndexOf(".");if(0<=e){for(;0<=e&&1<a;)e=h.lastIndexOf(".",e-1),a--;e=0<e?h.substring(e):h}}g=e;b="undefined"!==typeof b?""+b:"";if(f||""===b)if(""===b&&(f=-60),"number"===typeof f){var d=new Date;d.setTime(d.getTime()+6E4*f)}else d=f;return c&&(document.cookie=encodeURIComponent(c)+"="+encodeURIComponent(b)+"; path=/;"+(f?" expires="+d.toUTCString()+";":"")+(g?" domain="+g+";":""),"undefined"!==typeof cookieRead)?cookieRead(c)===b:!1}};window.cookieRead=window.cookieRead||function(c){if("string"===typeof c)c=encodeURIComponent(c);else return"";var b=" "+document.cookie,a=b.indexOf(" "+c+"="),d=0>a?a:b.indexOf(";",a);return(c=0>a?"":decodeURIComponent(b.substring(a+2+c.length,0>d?b.length:d)))?c:""};var l;d=d||"s_gpv";a=new Date;a.setTime(a.getTime()+18E5);window.cookieRead(d)&&(l=window.cookieRead(d));k?window.cookieWrite(d,k,a):window.cookieWrite(d,l,a);return l};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getPreviousValue`-Funktion verwendet die folgenden Argumente:

* **`v`** (Zeichenfolge erforderlich): Die Variable mit dem Wert, der an die nächste Bildanforderung übergeben werden soll. Eine häufig verwendete Variable ist `s.pageName`, um den Wert der vorherigen Seite abzurufen.
* **`c`** (Zeichenfolge, optional): Der Name des Cookies, in dem der Wert gespeichert wird.  Wenn dieses Argument nicht festgelegt ist, wird standardmäßig `"s_gpv"` verwendet.

Wenn Sie diese Funktion aufrufen, wird der im Cookie enthaltene Zeichenfolgenwert zurückgegeben. Das Plug-in setzt dann das Ablaufdatum des Cookies zurück und weist ihm den Variablenwert aus dem `v`-Argument zu. Das Cookie läuft nach 30 Minuten Inaktivität ab.

## Beispiele

```js
// 1. Sets prop7 to the cookie value contained in gpv_Page
// 2. Resets the gpv_Page cookie value to the page variable
// 3. If the page variable is not set, reset the gpv_Page cookie expiration
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");

// Sets prop7 to the cookie value contained in gpv_Page, but only if event1 is in the events variable.
if(inList(s.events,"event1")) s.prop7 = getPreviousValue(s.pageName,"gpv_Page");

// Sets prop7 to the cookie value contained in gpv_Page, but only if the page variable is currently set on the page
if(s.pageName) s.prop7 = getPreviousValue(s.pageName,"gpv_Page");

// Sets eVar10 equal to the cookie value contained in s_gpv, then sets the s_gpv cookie to the current value of eVar1.
s.eVar10 = getPreviousValue(s.eVar1);
```

## Unwahrscheinliche Eigenheiten

Wenn die mit dem `v`-Argument verknüpfte Variable auf einen neuen Wert eingestellt ist und das `getPreviousValue`-Plug-in ausgeführt wird, aber gleichzeitig KEIN Analytics-Server-Aufruf gesendet wird, wird der neue Wert des `v`-Arguments bei der nächsten Ausführung des Plug-ins weiterhin als „vorheriger Wert“ betrachtet.
Angenommen, der folgende Code wird auf der ersten Seite des Besuchs ausgeführt:

```js
s.pageName = "Home";
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");
s.t();
```

Dieser Code erzeugt einen Server-Aufruf, bei dem `pageName` „Home“ lautet und prop7 nicht festgelegt ist. Der Aufruf von `getPreviousValue` speichert jedoch den Wert von `pageName` im Cookie `gpv_Page`. Angenommen, unmittelbar danach wird auf derselben Seite der folgende Code ausgeführt:

```js
s.pageName = "New value";
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");
```

Da die Funktion `t()` in diesem Code-Block nicht ausgeführt wird, wird keine weitere Bildanforderung gesendet. Wenn der Funktions-Code `getPreviousValue` dieses Mal ausgeführt wird, wird jedoch `prop7` auf den vorherigen Wert von `pageName` („Home“) gesetzt und der neue Wert von `pageName` („New value“) im Cookie `gpv_Page` gespeichert. Nehmen wir nun an, der Besucher navigiert zu einer anderen Seite, und der folgende Code wird auf dieser Seite ausgeführt:

```js
s.pageName = "Page 2";
s.prop7 = getPreviousValue(s.pageName,"gpv_Page");
s.t();
```

Wenn die Funktion `t()` ausgeführt wird, wird eine Bildanforderung erstellt, bei der `pageName` „Page 2“ und `prop7` „New value“ lautet. Dies war der Wert von `pageName`, als der letzte Aufruf von `getPreviousValue` stattfand. Der `prop7`-Wert `"Home"` war nie in einer Bildanforderung enthalten, obwohl „Home“ der erste Wert war, der an `pageName` übergeben wurde.

## Versionsverlauf

### 3.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### v2.0 (7. Oktober 2019)

* Zwischenversion (vollständige Neufassung der Logik).
