---
description: Leitet den Browser an einen neuen Speicherort ohne Benutzerinteraktion weiter. Sie werden entweder im Webbrowser (Client-seitige Weiterleitung) oder auf dem Webserver (Server-seitige Weiterleitung) ausgeführt.
keywords: Analytics-Implementierung
title: Umleitungen und Aliase
feature: Implementation Basics
exl-id: 0ed2aa9b-ab42-415d-985b-2ce782b6ab51
TQID: https://experienceleague.adobe.com/iDwKqSKsjzEvgVCNKdTwDZHN2cPDmsuM1SV7PLisw3g
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 1139
ht-degree: 68%

---

# Umleitungen und Aliase

Leitet den Browser an einen neuen Speicherort ohne Benutzerinteraktion weiter. Sie werden entweder im Webbrowser (Client-seitige Weiterleitung) oder auf dem Webserver (Server-seitige Weiterleitung) ausgeführt.

## Umleitungen und Aliase {#aliases}

Leitet den Browser an einen neuen Speicherort ohne Benutzerinteraktion weiter. Sie werden entweder im Webbrowser (Client-seitige Weiterleitung) oder auf dem Webserver (Server-seitige Weiterleitung) ausgeführt.

Da Umleitungen keine Benutzerinteraktion erfordern, werden Umleitungen oft ausgeführt, ohne dass der Benutzer es bemerkt. Das einzige, was darauf hinweist, dass eine Umleitung stattgefunden hat, ist die Adressleiste des Browsers. In der Adressleiste wird eine URL angezeigt, die sich von dem Link unterscheidet, den der Browser ursprünglich angefordert hat.

Es gibt zwar nur zwei Arten von Umleitungen, sie können jedoch auf verschiedene Arten implementiert werden. Client-seitige Weiterleitungen können beispielsweise auftreten, weil die Web-Seite, auf die ein Benutzer verwiesen hat, Skripte oder speziellen HTML-Code enthält, der den Browser zu einer anderen URL umleitet. Server-seitige Weiterleitungen können auftreten, weil die Seite Server-seitige Skripterstellung enthält oder weil der Webserver so konfiguriert wurde, dass der Benutzer auf eine andere URL verweist.

## Analytics und Umleitungen {#aa-redirects}

[!DNL Analytics] erfasst einige Daten aus dem Browser und ist auf bestimmte Browsereigenschaften angewiesen. Zwei dieser Eigenschaften, die „verweisende URL“ (oder „verweisende URL„) und die „aktuelle URL“ können durch eine Server-seitige Umleitung geändert werden. Da der Browser erkennt, dass eine URL angefordert, aber eine andere URL zurückgegeben wurde, wird die verweisende URL gelöscht. Demzufolge ist die verweisende URL leer, und [!DNL Analytics] würde dann melden, dass zu der Seite kein Referrer vorhanden wäre.

## Beispiel: Browsen ohne Umleitungen {#browse-without}

Betrachten wir das folgende hypothetische Szenario, in dem der Benutzer nicht umgeleitet wird:

1. Der Benutzer verweist seinen Browser auf `www.google.com`, gibt „Discount-Airline Tickets“ in das Suchfeld ein und klickt anschließend auf die Schaltfläche **[!UICONTROL Suchen]**.
1. Der Browser zeigt die Suchergebnisse einschließlich einem Link zu Ihrer Site [!DNL https://www.example.com/] / an. Nach der Anzeige der Suchergebnisse zeigt die Adressleiste des Browsers die vom Benutzer ins Suchfeld eingegebenen Suchbegriffe an ( `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`). Beachten Sie, dass die Suchbegriffe in die URL-Abfragestringparameter einbezogen werden, die auf `https://www.google.com/search?` ? folgen.
1. Der Benutzer klickt auf den Link zu Ihrer hypothetischen Site [!DNL https://www.example.com/]. Wenn der Benutzer auf diesen Link klickt und auf die Website [!DNL example.com] gelangt, erfasst [!DNL Analytics] mithilfe von JavaScript die verweisende URL (`https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`) und die aktuelle URL ( `https://www.example.com/`).
1. [!DNL Analytics] präsentiert die während dieser Interaktion gesammelten Informationen in verschiedenen Berichten z. B. [!UICONTROL Verweisende Domänen], [!UICONTROL Suchmaschinen] und [!DNL Search Keywords].

## Beispiel: Browsen mit Umleitungen {#browse-with}

Umleitungen können dazu führen, dass der Browser die wahre verweisende URL ausblendet. Betrachten wir das folgende Szenario:

1. Der Benutzer verweist seinen Browser auf `https://www.google.com`, gibt *Discount-Airline Tickets* in das Suchfeld ein und klickt anschließend auf die Schaltfläche **[!UICONTROL Suchen]**.
1. Die Adressleiste des Browser-Fensters zeigt die vom Benutzer ins Suchfeld eingegebenen Suchbegriffe `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets` an. Beachten Sie, dass die Suchbegriffe in die URL-Abfragestringparameter einbezogen werden, die auf `https://www.google.com/search?` ? folgen. Der Browser zeigt auch eine Seite an, die die Suchergebnisse einschließlich einem Link zu einem Ihrer Domänennamen enthält: [!DNL https://www.flytohawaii.example/]. Diese *Vanity*-Domain ist konfiguriert, um den Benutzer auf `https://www.example.com/` / umzuleiten.
1. Der Benutzer klickt auf den Link `https://www.flytohawaii.example/` und wird vom Server auf Ihre Hauptseite `https://www.example.com` umgeleitet. Wenn die Weiterleitung erfolgt, gehen die für die Datenerfassung in [!DNL Analytics] wichtigen Daten verloren, da der Browser die verweisende URL löscht. Somit sind die ursprünglichen Suchinformationen nicht mehr vorhanden, die in den [!DNL Analytics]-Berichten (z. B. [!UICONTROL Verweisende Domänen], [!UICONTROL Suchmaschinen], [!UICONTROL Keywords]) verwendet wurden.

## Umleitungen implementieren {#implement}

Damit [!DNL Analytics] Daten aus Weiterleitungen erfasst werden können, müssen vier kleinere Änderungen an dem Code, der die Weiterleitung erstellt, und an der [!DNL AppMeasurement] für JavaScript-Datei vorgenommen werden.

Mit Durchführung der folgenden Schritte werden die Informationen erhalten, die der ursprüngliche Verweis (zum Beispiel `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets` im obigen Szenario) an Ihre Site weitergibt:

## Konfiguration von JavaScript-Code zum Außerkraftsetzen des Verweises {#override}

Der nachstehende Codeabschnitt zeigt zwei JavaScript-Variablen, `s.referrer` und `s.pageURL`. Dieser Code wird auf der endgültigen Landingpage der Weiterleitung platziert.

```js
<script language="JavaScript" src="//INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"></script> 
<script language="JavaScript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.campaign="" 
s.referrer="" 
s.pageURL=""
```

>[!IMPORTANT]
>
>Stellen Sie *`s.referrer`* nur einmal auf der Seite ein. Wenn Sie die Variable bei jedem Tracking-Aufruf oder jedem Link-Klick festlegen, wird sie vom Referrer und ähnlichen Dimensionen wie Suchmaschinen und Schlüsselwörtern doppelt gezählt.

## Weiterleitungen mittels getQueryParam {#getqueryparam}

[!UICONTROL getQueryParam] stellt eine einfache Möglichkeit dar, [!DNL Analytics]-Variablen mit Abfragezeichenfolgen-Werten aufzufüllen. Es muss jedoch in Verbindung mit einer temporären Variablen implementiert werden, damit bei einer leeren Abfragezeichenfolge keine legitimen Referrer überschrieben werden. Die beste Möglichkeit, [!UICONTROL getQueryParam] zu verwenden, erfolgt in Kombination mit dem [!UICONTROL getValue]-Plug-in, wie im folgenden Beispielcode gezeigt wird.

```js
// AppMeasurement 1.x 
var tempVar=s.Util.getQueryParam('origref') 
if(tempVar) 
  s.referrer=tempVar;
```

```js
// H Code 
var tempVar=s.getQueryParam('origref') 
if(tempVar) 
  s.referrer=tempVar;
```

## Ändern des Weiterleitungsmechanismus {#modify}

Da der Browser die verweisende URL abschneidet, müssen Sie den Mechanismus konfigurieren, der die Weiterleitung verarbeitet (z. B. Webserver, Server-seitiger Code, Client-seitiger Code), um die ursprünglichen Verweisinformationen weiterzugeben. Wenn Sie auch die URL des Alias-Links aufzeichnen möchten, muss diese ebenfalls an die endgültige Landingpage weitergeleitet werden. Verwenden Sie die Variable *`s_pageURL`* , um die aktuelle URL zu überschreiben.

Da viele Möglichkeiten zur Implementierung einer Weiterleitung bestehen, müssen Sie ggf. mit Ihrer Web Operations-Gruppe oder Ihrem Online-Werbepartner die spezifischen Mechanismen bestimmen, die Weiterleitungen auf Ihrer Website ausführen.

## Erfassung der ursprünglich verweisenden Stelle {#original}

Für gewöhnlich ruft [!DNL Analytics] die verweisende URL aus der Eigenschaft [!UICONTROL document.referrer] und die aktuelle URL aus der Eigenschaft [!UICONTROL document.location] des Browsers ab. Durch Übergabe von Werten an die Variablen *`referrer`* und *`pageURL`* können Sie die Standardverarbeitung überschreiben. Durch Übergabe eines Werts an die Variable „referrer“ teilen Sie [!DNL Analytics] mit, dass die Referrer-Information in der Eigenschaft [!UICONTROL document.referrer] ignoriert und stattdessen ein anderer, von Ihnen definierter Wert verwendet werden soll.

Daher muss die finale Version der Landingpage den folgenden Code enthalten, damit die Fehler im Szenario „Discount-Airline Tickets“ korrigiert werden können.

```js
<script language="JavaScript" src="AppMeasurement.js"></script> 
<script language="JavaScript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.campaign="" 
s.referrer="https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets" 
// Setting the s.pageURL variable is optional.
s.pageURL="https://www.flytohawaii.example"
```

## Überprüfen des Referrers mit dem Adobe Debugger {#verify}

Führen Sie einen Test durch, um zu überprüfen, dass die verweisende Stelle, die Quell-URL (*`s_server`*) und die Kampagnenvariablen erfasst werden.

Diese Variablen werden im [CX Enterprise Debugger) als die folgenden Parameter ](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de).

<table id="table_5F3B987D4D514CA283F7B9F52EBC2301"> 
 <thead> 
  <tr> 
   <th class="entry"> </th> 
   <th class="entry"> <b>URL- oder Abfragezeichenfolgenwert</b> </th> 
   <th class="entry"> <b>Wert wie im DigitalPulse Debugger gezeigt</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Ursprünglicher Referrer </p> </td> 
   <td> <p> <span class="filepath">https://www.google.com/search%3F hl%3Den %26ie%3DUTF826q%3 Ddiscount%2Bairline%2Btickets</span> </p> </td> 
   <td> <p> <span class="filepath"> r=https:/ref=www.google.com/search?hl=en&amp;ie=UTF -8&amp;q=discount+airline+tickets </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Seiten-URL </p> </td> 
   <td> <p> <span class="filepath"> https://www.flytohawaii.example </span> </p> </td> 
   <td> <p> <span class="filepath"> g=https://www.flytohawaii.example </span> </p> <p>Dieser Wert wird im DigitalPulse-Debugger angezeigt, wenn die Variable <span class="varname"> pageURL</span> verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Endgültige Landingpage-URL </p> </td> 
   <td> <p> <span class="filepath">https://www.example.com</span> </p> </td> 
   <td> <p>Dieser Wert wird NICHT im DigitalPulse-Debugger angezeigt, wenn die Variable <span class="varname">pageURL</span> verwendet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

Im Debugger wird Folgendes angezeigt:

```
Image 
 
https://examplecom.112.2o7.net/b/ss/examplecom/1/JS-1.4/s61944015791667?[AQB] 
ndh=1 
t=4/8/20XX 13:34:28 4 360 
pageName=Welcome to example.com 
r=https://ref=www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets 
cc=USD 
g=https://www.flytohawaii.example 
s=1280x1024 
c=32 
j=1.3 
v=Y 
k=Y 
bw=1029 
bh=716 
ct=lan 
hp=N 
[AQE]
```

Nachdem Sie überprüft haben, ob der Adobe [!UICONTROL Debugger] diese Variablen anzeigt, sollten Sie sich immer vergewissern, dass die Suchbegriffe und die ursprünglich (vor der Umleitung) verweisende Domain in Berichten Traffic verzeichnen.
