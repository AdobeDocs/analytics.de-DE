---
title: Numbers Suite
description: Generieren und bearbeiten Sie Zahlen zur Verwendung in anderen JavaScript-Variablen.
feature: Variables
exl-id: 7af88dce-baf3-4581-b5b6-0d6e41922266
source-git-commit: bbb138d979968ec2536e53ff07001b43156df095
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 89%

---

# Adobe-Plug-in: Numbers Suite

{{plug-in}}

Numbers Suite bietet eine Reihe von JavaScript-Funktionen. Es enthält die folgenden Plug-ins:

* **`zeroPad`**: Fügen Sie am Anfang einer Zahl eine bestimmte Anzahl von Nullen hinzu. Dieses Plug-in ist nützlich, wenn eine Variable eine bestimmte Anzahl von Ziffern benötigt, z. B. wenn Sie mit JavaScript-Datumsobjekten arbeiten und den Monat und Tag eines Datums mit zwei anstelle von nur einer Ziffer formatieren möchten. Beispiel: `01/09/2020` anstelle von `1/9/2020`.
* **`randomNumber`**: Generieren Sie eine Zufallszahl mit einer bestimmten Anzahl von Ziffern. Dieses Plug-in ist nützlich, wenn Sie Tags von Drittanbietern bereitstellen und eine Cache-Busting-Zufallszahl wünschen.
* **`twoDecimals`**: Runden Sie eine Zahl auf das nächste Hundertstel. Dieses Plug-in eignet sich für Währungszwecke, sodass Sie eine Zahl auf einen gültigen Währungswert runden können.

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
   * Aktionstyp: Numbers Suite initialisieren
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
/* Adobe Consulting Plugin: zeroPad v1.0 */
function zeroPad(num,nod){num=parseInt(num);nod=parseInt(nod);if(isNaN(num)||isNaN(nod))return"";var c=nod-num.toString().length+ 1;return Array(+(0<c&&c)).join("0")+num};

/* Adobe Consulting Plugin: randomNumber v2.0 (zeroPad plug-in optional)*/
function randomNumber(nod){nod="number"===typeof nod?17>Math.abs(nod)?Math.round(Math.abs(nod)):17:10;for(var a="1",c=0;c<nod;c++) a+="0";a=Number(a);a=Math.floor(Math.random().toFixed(nod)*a)+"";a.length!==nod&&"undefined"!==typeof zeroPad&&(a=zeroPad(a,nod)); return a};

/* Adobe Consulting Plugin: twoDecimals v1.0 */
function twoDecimals(v){return"undefined"===typeof v||void 0===v||isNaN(v)?0:Number(Number(v).toFixed(2))};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden der Plug-ins

Die `zeroPad`-Funktion verwendet die folgenden Argumente:

* **num** (erforderlich, Ganzzahl): Die Nummer, die aufgefüllt werden soll. Die Funktion rundet den Wert dieses Arguments ab, wenn es Dezimalstellen enthält.
* **nod** (erforderlich, Ganzzahl): Die Anzahl der Ziffern im endgültigen Rückgabewert. Wenn die Zahl, die aufgefüllt werden soll, weniger Ziffern enthält als die Anzahl der zu verwendenden Ziffern, fügt das Plug-in dem `num`-Argument Nullen am Anfang hinzu.

Die `randomNumber`-Funktion verwendet die folgenden Argumente:

* **nod** (optional, Ganzzahl): Die Anzahl der Ziffern in der Zufallszahl, die Sie generieren möchten. Der Höchstwert beträgt 17 Ziffern. Der Standardwert beträgt 10 Ziffern.

Die `twoDecimals`-Funktion verwendet die folgenden Argumente:

* **val** (erforderlich, Zahl): Eine Zahl (die durch ein Zeichenfolgen- oder Zahlenobjekt dargestellt wird), die auf das nächste Hundertstel gerundet werden soll.

## Rückgaben

* Die Funktion **zeroPad** gibt eine Zeichenfolge zurück, die dem `num`-Argument entspricht, wobei jedoch eine bestimmte Anzahl von Nullen am Anfang des Werts hinzugefügt wird. Dadurch wird sichergestellt, dass der Rückgabewert die richtige Anzahl von Ziffern aufweist.
* Die Funktion **randomNumber** gibt eine Zeichenfolge zurück, die einer Zufallszahl mit der gewünschten Anzahl von Ziffern entspricht.
* Die Funktion **twoDecimals** gibt ein auf das nächste Hundertstel gerundetes Zahlenobjekt zurück.

## Beispielaufrufe

### zeroPad-Beispiele

```js
s.eVar25 = zeroPad(25.5562, 5) //sets eVar25 equal to "00025"

s.prop1 = zeroPad(25, 1) //sets prop1 equal to "25"

s.prop1 = zeroPad(232425235,23) //sets prop1 equal to "00000000000000232425235"
```

### randomNumber-Beispiele

```js
s.eVar65 = randomNumber(15) //sets eVar65 equal to "721759731750342" or some other random 15-digit number

randomNumber() //returns a random 10-digit number but is useless since this isn't used in an expression

var j = randomNumber(35) //sets a variable named j equal to "15476068651810060" or another random 17-digit number
```

### twoDecimals-Beispiele

```js
s.events = "event10=" + twoDecimals("85.4827128694") //sets s.events="event10=85.48"

var fivehundredthirtytwo = twoDecimals(532.000000001) //sets the variable fivehundredthirtytwo equal to 532

s.eVar65 = twoDecimals("672132.9699736457") //sets s.eVar65 equal to 672132.97
```

## Versionsverlauf

### 1.0 (25. Mai 2019)

* Erste Version.
