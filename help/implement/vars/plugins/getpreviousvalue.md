---
title: getPreviousValue
description: Rufen Sie den letzten Wert ab, der an eine Variable übergeben wird.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-Plug-in: getPreviousValue

>[!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getPreviousValue`-Plug-in können Sie eine Variable auf einen Wert einstellen, der bei einem vorherigen Treffer festgelegt wurde. Dieses Plug-in ist nicht erforderlich, wenn Ihre Implementierung alle gewünschten Werte im aktuellen Treffer enthält.

## Installieren des Plug-ins mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: getPreviousValue initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor in Launch

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under the Adobe Analytics extension.
1. Erweitern Sie das [!UICONTROL Configure tracking using custom code] Akkordeon, das die [!UICONTROL Open Editor] Schaltfläche einblendet.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getPreviousValue v2.0 */
s.getPreviousValue=function(v,c){var s=this,d;c=c||"s_gpv";var b=new Date;b.setTime(b.getTime()+18E5);s.c_r(c)&&(d=s.c_r(c)); v?s.c_w(c,v,b):s.c_w(c,d,b);return d};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getPreviousValue`-Methode verwendet die folgenden Argumente:

* **`v`** (Zeichenfolge erforderlich): Die Variable mit dem Wert, der an die nächste Bildanforderung übergeben werden soll. Eine häufig verwendete Variable ist `s.pageName`, um den Wert der vorherigen Seite abzurufen.
* **`c`** (Zeichenfolge, optional): Der Name des Cookies, in dem der Wert gespeichert wird.  Wenn dieses Argument nicht festgelegt ist, wird standardmäßig `"s_gpv"` verwendet.

Wenn Sie diese Methode aufrufen, wird der im Cookie enthaltene Zeichenfolgenwert zurückgegeben. Das Plug-in setzt dann das Ablaufdatum des Cookies zurück und weist ihm den Variablenwert aus dem `v`-Argument zu. Das Cookie läuft nach 30 Minuten Inaktivität ab.

## Beispielaufrufe

### Beispiel 1

Der folgende Code ...

```js
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

* setzt zuerst s.prop7 auf den Wert, der in der vorherigen Bildanforderung an s.pageName übergeben wurde (d. h. den Wert, der im Cookie „gpv_Page“ gespeichert wurde)
* Der Code setzt dann das Cookie „gpv_Page“ zurück, sodass es dem aktuellen Wert von s.pageName entspricht
* Wenn s.pageName nicht zum Zeitpunkt der Ausführung dieses Codes gesetzt ist, setzt der Code die Gültigkeit für den aktuellen Wert des Cookies zurück

### Beispiel 2

Der folgende Code setzt s.prop7 auf den letzten Wert, der an s.pageName übergeben wird, aber nur, wenn event1 zum Zeitpunkt des Aufrufs auch in s.events enthalten ist, wie über das inList-Plug-in bestimmt wird.

```js
if(s.inList(s.events,"event1")) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### Beispiel 3

Der folgende Code setzt s.prop7 auf den letzten Wert, der an s.pageName übergeben wird, aber nur, wenn s.pageName derzeit gleichzeitig auf der Seite gesetzt ist.

```js
if(s.pageName) s.prop7=s.getPreviousValue(s.pageName,"gpv_Page");
```

### Beispiel 4

Der folgende Code setzt s.eVar10 auf den Wert, der in der vorherigen Bildanforderung an s.eVar1 übergeben wurde.   Der vorherige eVar1-Wert wäre im Cookie „s_gpv“ enthalten.  Der Code setzt dann das Cookie „s_gpv“ auf den aktuellen Wert von s.eVar1.

```js
s.eVar10 = s.getPreviousValue(s.eVar1)
```

## Unwahrscheinliche Eigenheiten

Wenn die mit dem v-Argument verknüpfte Variable auf einen neuen Wert eingestellt ist und das getPreviousValue-Plug-in ausgeführt wird, aber gleichzeitig KEIN Analytics-Server-Aufruf gesendet wird, wird der neue v-Argumentwert bei der nächsten Ausführung des Plug-ins weiterhin als „vorheriger Wert“ betrachtet.
Angenommen, der folgende Code wird auf der ersten Seite des Besuchs ausgeführt:

```js
s.pageName="home"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

Dieser Code erzeugt einen Server-Aufruf, bei dem das pageName-Argument mit „home“ identisch ist und das p7-Argument (prop7) nicht gesetzt ist.  Der Aufruf von s.getPreviousValue speichert jedoch den Wert von s.pageName (d. h. „home“) in dem im Aufruf angegebenen Cookie (d. h. das „gpv_Page“-Cookie).
Nehmen Sie jetzt an, dass unmittelbar danach auf derselben Seite der folgende Code ausgeführt wird (aus welchem Grund auch immer):

```js
s.pageName="happy value"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
```

Da die Funktion s.t() in diesem Codeblock nicht ausgeführt wird, wird keine weitere Bildanforderung erstellt.  Wenn jedoch der Funktionscode s.getPreviousValue() dieses Mal ausgeführt wird, wird s.prop7 gleich dem vorherigen Wert von s.pageName (d. h. „home“) und speichert dann den neuen Wert von s.pageName (d. h. „happy value“) im Cookie „gpv_Page“.
Angenommen, der Besucher navigiert zu einer anderen Seite und der folgende Code wird auf dieser Seite ausgeführt:

```js
s.pageName="page 2"
s.prop7=s.getPreviousValue(s.pageName,"gpv_Page")
s.t();
```

Wenn die Aufruffunktion s.t() ausgeführt wird, wird eine Bildanforderung erstellt, bei der s.pageName=„Seite 2“ und s.prop7 gleich „happy value“ sind. Dies war der Wert von s.pageName, als der letzte Aufruf von getPreviousValue stattfand.   Der s.prop7-Wert „home“ war nie in einer echten Bildanforderung enthalten, obwohl „home“ der erste Wert war, der an s.pageName übergeben wurde.

## Versionsverlauf

### v2.0 (7. Oktober 2019)

* Zwischenversion (vollständige Neufassung der Logik).
