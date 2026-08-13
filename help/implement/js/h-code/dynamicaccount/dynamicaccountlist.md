---
title: dynamicAccountList
description: Legen Sie eine Logik fest, wie Ihre Implementierung die Report Suite bestimmt.
feature: Implementation Basics
exl-id: ccff24a1-4b9a-4f62-adb5-09ab60e9b93e
role: Developer
TQID: https://experienceleague.adobe.com/qqkQoYsBWdTDOIkNfregm4k11CoDEl3dOJ3HNCMIo3s
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 157cc2bde1047063014aff39319d5cfaa1de9b5c
workflow-type: tm+mt
source-wordcount: 268
ht-degree: 89%

---

# s.dynamicAccountList

>[!IMPORTANT]
>
>Dynamische Konten werden nur mit älteren JavaScript-Implementierungen (H-Code) unterstützt. Diese Variablen werden in aktuellen AppMeasurement-Bibliotheken oder der Adobe Experience Platform-Datenerfassung nicht unterstützt.

Die `s.dynamicAccountList`-Variable bestimmt dynamisch den Wert von `s_account`. Ist `dynamicAccountSelection` gleich `true`, wird die `dynamicAccountMatch`-Variable mit `dynamicAccountList` verglichen. Wenn eine Übereinstimmung gefunden wird, wird die entsprechende Report Suite-ID verwendet.

## Syntax

Diese Variable ist eine Zeichenfolge, die automatisch von der JavaScript-Datei analysiert wird.

```JavaScript
s.dynamicAccountList = "[rsid]=[valuetomatch],[rsid2]=[valuetomatch]";
```

Gültige Eingabe ist eine durch Semikolon getrennte Liste von rsid- und value-Paaren. Jede Liste enthält die folgenden Elemente:

* Eine oder mehrere Report Suite-IDs (durch Kommas getrennt)
* Ein Gleichheitszeichen
* Eine oder mehrere übereinstimmende Zeichenfolgen (durch Kommas getrennt)

In der Zeichenfolge sind nur normale ASCII-Zeichen zu verwenden. Fügen Sie keine Leerzeichen ein.

## Beispiele

Bei allen folgenden Beispielen lautet die Seiten-URL `https://example.com/path2/?prod_id=12345`, und die `dynamicAccountSelection`-Variable ist auf `true` und die `s_account`-Variable auf `examplersid` festgelegt.

```js
// In this example, the report suite that receives data is examplersid1.
s.dynamicAccountMatch = "window.location.hostname";
s.dynamicAccountList = "examplersid2=www2.example.com;examplersid1=example.com";

// In this example, the report suite that receives data is examplersid2.
s.dynamicAccountMatch = "window.location.pathname";
s.dynamicAccountList = "examplersid2=path2;examplersid3=path3";

// In this example, no rules match so it resorts to the default rsid in s_account, examplersid.
s.dynamicAccountMatch = "window.location.pathname";
s.dynamicAccountList = "examplersid4=path4;examplersid5=path5";
```

## Probleme, Fragen und Tipps

* Die in dieser Variablen aufgeführten Regeln werden von links nach rechts angewendet. Wenn mehrere Regeln auf eine `dynamicAccountMatch`-Variable zutreffen, wird die Report Suite anhand der Regel ermittelt, die am weitesten links steht. Aus diesem Grund sollten Sie allgemeinere Regeln in der Liste weiter rechts platzieren.
* Wenn keine der Regeln zutrifft, wird die standardmäßige Report Suite in `s_account` verwendet.
* Bei Seiten, die auf einer lokalen Festplatte gespeichert oder über ein Web-basiertes Übersetzungsmodul übersetzt werden (wie z. B. die übersetzten Seiten in Google), funktioniert die dynamische Kontoauswahl wahrscheinlich nicht mehr.
* Die `dynamicAccountSelection`-Regeln gelten nur für den in `dynamicAccountMatch` festgelegten Abschnitt der URL.
* Verwenden Sie den Adobe CX Enterprise-Debugger, um die Ziel-Report-Suite zu testen.
