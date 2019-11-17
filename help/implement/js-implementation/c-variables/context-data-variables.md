---
description: Mithilfe von Kontextdatenvariablen können Sie für jede Seite benutzerdefinierte Variablen definieren, die von Verarbeitungsregeln gelesen werden können.
keywords: Analytics Implementation;contextdata;s.contextdata
solution: Analytics
subtopic: Variables
title: Kontextdatenvariablen
topic: Developer and implementation
uuid: 4b215803-99d4-46f2-b3c1-e78558987764
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Kontextdatenvariablen

Mithilfe von Kontextdatenvariablen können Sie für jede Seite benutzerdefinierte Variablen definieren, die von Verarbeitungsregeln gelesen werden können.

Statt Props und eVars in Ihrem Code explizit Werte zuzuweisen, können Sie die Daten in Kontextdatenvariablen senden, die mithilfe von Verarbeitungsregeln zugeordnet werden. Verarbeitungsregeln bieten eine leistungsfähige grafische Benutzeroberfläche, in der Sie Änderungen an Daten bei deren Erhalt vornehmen können. Auf Grundlage der in Kontextdaten gesendeten Werte können Sie Ereignisse festlegen, Werte in eVars und Eigenschaftsvariablen kopieren und zusätzliche bedingte Anweisungen ausführen.

> [!NOTE] Bei Kontextvariablen wird die Schreibweise nicht beachtet. Die beiden folgenden Variablen sind beispielsweise im Prinzip identisch:
>```
>s.contextData['article_title'] = 'Weekend Concert Controversy'; 
>```
>und
>```
>s.contextData['ARTICLE_TITLE'] = 'Weekend Concert Controversy';
>```

Die Verwendung von Kontextdaten hilft zu vermeiden, dass Sie Codeaktualisierungen durchführen, um verschiedene Report Suite-Konfigurationen zu unterstützen.

So können Sie zum Beispiel die folgende Variable *`s.contextData`* festlegen:

```
s.contextData['myco.rsid'] = 'value'
```

Mithilfe von Verarbeitungsregeln können Sie eine Bedingung hinzufügen, die nach einer `myco.rsid`-Kontextdatenvariablen sucht. Für den Fall, dass diese Variable gefunden wird, können Sie eine Aktion hinzufügen, die den Wert der Variablen in eine Prop oder eVar kopiert.

Kontextdatenvariablen können auch direkt in der Benutzeroberfläche für Verarbeitungsregeln definiert werden, um einen Wert temporär zu speichern oder um Werte aus einer Kontextdatenvariablen zu erfassen, von der Sie wissen, dass sie in der Report Suite verwendet wird. Wenn zum Beispiel zwei Werte getauscht werden sollen, können Sie eine Kontextdatenvariable erstellen, in der ein Wert während des Tauschs gespeichert wird.

Da Verarbeitungsregeln nur bei der Erfassung von Daten angewendet werden, müssen Sie diese Regeln festlegen, bevor Sie mit dem Versenden von Kontextdaten beginnen. Kontextdatenwerte, die bei der Verarbeitung eines Hits nicht von Verarbeitungsregeln gelesen werden, werden verworfen.

## Regeln {#section_2229739F6B1A4C1CAD7140BDF4687523}

<table id="table_4433A32A952340699B189CAEAF158B06"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Regel </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Unterstützte Namen und Zeichen </p> </td> 
   <td colname="col2"> <p>Namen von Kontextdatenvariablen dürfen nur alphanumerische Zeichen, Unterstriche und Punkte enthalten. Alle anderen Zeichen werden entfernt. Kontextdatenvariablen dienen nicht numerischen Zwecken, sondern als Benennungen. </p> <p>For example, the context data variable <code> login_page-home </code> automatically becomes <code> login_pagehome </code>. All data sent to the <code> login_page-home </code> variable is allocated under <code> login_pagehome </code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Namespace </p> </td> 
   <td colname="col2"> <p>Damit Variablennamen in der gesamten Report Suite eindeutig sind, empfiehlt es sich, den Namen des eigenen Unternehmens, Standorts o. Ä. als Präfix für die Variablen zu verwenden. </p> <p>Kontextdatenvariablen können ähnlich wie andere JavaScript-Variablen benannt werden. Be aware that the namespace <code> a.* </code> is reserved for use by Adobe products in context variable names. So verwendet die AppMeasurement-Bibliothek für iOS zum Beispiel <code> a.InstallEvent </code>, um Installationen von Anwendungen zu messen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>URL-Beschränkungen für Internet Explorer </p> </td> 
   <td colname="col2"> <p>Sie werden möglicherweise auf ältere URL-Beschränkungen für Internet Explorer 6 und 7 stoßen, bei denen URLs bei 2000 Byte gekürzt wurden. Mit dem <span class="keyword">DigitalPulse Debugger</span> können Sie die Größe einer URL-Zeichenfolge bestimmen. </p> <p>Seit den kürzlich erfolgten Aktualisierungen für AppMeasurement (September 2014) wird für Internet Explorer 8 und höher HTTP POST verwendet, wodurch keine Schwierigkeiten mit Verkürzungen mehr auftreten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Unterstützte AppMeasurement-Version </p> </td> 
   <td colname="col2"> <p>Für Kontextdatenvariablen ist mindestens H23-Code (oder höher) erforderlich. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Senden von Kontextdaten in einem Nachverfolgungslink-Aufruf {#section_35EBE5D1CF29427598BD4B2165CE64FC}

Beziehen Sie `ContextData` und den Namen der Variablen ein, die in `s.linkTrackVars` integriert werden soll:

```
s.contextData['myco.value'] = "some value"; 
s.linkTrackVars = "contextData.myco.value"; 
s.tl(true,"o","Link Name"); 
```

## Beispiele {#section_A16AD9E6E0E84F6A85CA4F08512480B3}

Mögliche Methoden, die Implementierung der Variable *`s.pageName`* zu ersetzen, vorausgesetzt, die Verarbeitungsregeln sind für jede Variable korrekt eingerichtet:

```
s.contextData['page'] = "Home Page" 
s.contextData['pagename'] = document.title // Takes the web page's title and passes it into the pageName context data variable 
s.contextData['pagevar'] = s.pageName // This example would be considered redundant, as both the pageName and contextData variable are available in Processing rules
```

Andere Beispiele zur Implementierung von Kontextdatenvariablen:

```
s.contextData['owner'] = "Jesse" 
s.contextData['campaign'] = "Campaign A" 
s.contextData['author'] = "Sheridan Andrius"
```

Ein Beispiel finden Sie in der Analytics-Referenz unter [Copy a Context Data Variable to an eVar](https://marketing.adobe.com/resources/help/en_US/reference/processing_rules_copy_context_data.html) (Kopieren einer Kontextdatenvariablen in eine eVar).
