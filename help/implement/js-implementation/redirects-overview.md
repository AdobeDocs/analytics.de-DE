---
description: Weiterleitungen verweisen den Browser ohne Benutzerinteraktion zu einem neuen Standort. Sie werden entweder auf Webbrowser-Ebene (clientseitige Umleitungen) oder Webserver-Ebene (serverseitige Umleitungen) durchgeführt.
keywords: Analytics Implementation
solution: Analytics
subtopic: Redirects
title: Umleitungen und Aliase
topic: Developer and implementation
uuid: 11f9ad7a-5c45-410f-86dd-b7d2cec2aae3
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Umleitungen und Aliase

Weiterleitungen verweisen den Browser ohne Benutzerinteraktion zu einem neuen Standort. Sie werden entweder auf Webbrowser-Ebene (clientseitige Umleitungen) oder Webserver-Ebene (serverseitige Umleitungen) durchgeführt.

## Umleitungen und Aliase {#concept_F4F1D53D473947FE8554897332545763}

Weiterleitungen verweisen den Browser ohne Benutzerinteraktion zu einem neuen Standort. Sie werden entweder auf Webbrowser-Ebene (clientseitige Umleitungen) oder Webserver-Ebene (serverseitige Umleitungen) durchgeführt.

Da bei Umleitungen keine Interaktion des Benutzers erforderlich ist, werden Umleitungen häufig durchgeführt, ohne dass der Benutzer dies bemerkt. Der einzige Hinweis auf eine Umleitung findet sich in der Adressleiste des Browsers. Die Adressleiste zeigt eine URL an, die sich von dem ursprünglich im Browser angefragten Link unterscheidet.

Obwohl es nur zwei Typen von Umleitungen gibt, können sie auf verschiedene Arten implementiert werden. Clientseitige Umleitungen können beispielsweise auftreten, da die Webseite, auf die ein Benutzer seinen Browser verwiesen hat, Scripting oder einen speziellen HTML-Code enthält, der den Browser auf eine andere URL verweist. Serverseitige Umleitungen können auftreten, da die Seite serverseitiges Scripting enthält oder da der Webserver zum Verweisen des Benutzers auf eine andere URL konfiguriert wurde.

## Analytics und Umleitungen {#concept_F9132879D0CB4AC1BE7AF45E388A47F7}

[!DNL Analytics] erfasst einige Daten aus dem Browser und ist auf bestimmte Browsereigenschaften angewiesen. Zwei dieser Eigenschaften, die „Verweisende URL“ (oder „Verweis“) und die „Aktuelle URL“, können durch eine serverseitige Umleitung geändert werden. Da der Browser erkennt, dass eine URL abgefragt wurde, jedoch eine andere URL zurückgegeben wurde, wird die verweisende URL entfernt. Demzufolge ist die verweisende URL leer, und [!DNL Analytics] würde dann melden, dass zu der Seite kein Referrer vorhanden wäre.

<!-- 

redirects_sc.xml

 -->

Die folgenden Beispiele veranschaulichen, wie das Browsen ohne und mit Umleitungen beeinflusst wird:

* [Beispiel: Browsen ohne Umleitungen](/help/implement/js-implementation/redirects-overview.md#section_5C835A4D665A4625A23333C2C21F152D)
* [Beispiel: Browsen mit Umleitungen](/help/implement/js-implementation/redirects-overview.md#section_921DDD32932847848C4A901ACEF06248)

## Beispiel: Browsen ohne Umleitungen {#section_5C835A4D665A4625A23333C2C21F152D}

Betrachten wir das folgende hypothetische Szenario, in dem der Benutzer nicht umgeleitet wird:

1. Der Benutzer verweist seinen Browser auf `www.google.com`, gibt „Discount-Airline Tickets“ in das Suchfeld ein und klickt anschließend auf die Schaltfläche **[!UICONTROL Suchen]**.
1. Der Browser zeigt die Suchergebnisse einschließlich einem Link zu Ihrer Site [!DNL https://www.flywithus.com/] / an. Nach der Anzeige der Suchergebnisse zeigt die Adressleiste des Browsers die vom Benutzer ins Suchfeld eingegebenen Suchbegriffe an ( `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`). Beachten Sie, dass die Suchbegriffe in die URL-Abfragestringparameter einbezogen werden, die auf `https://www.google.com/search?` ? folgen.
1. Der Benutzer klickt auf den Link zu Ihrer hypothetischen Site [!DNL https://www.flywithus.com/]. Wenn der Benutzer auf diesen Link klickt und auf die Website [!DNL flywithus.com] gelangt, erfasst [!DNL Analytics] mithilfe von JavaScript die verweisende URL (`https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets`) und die aktuelle URL ( `https://www.flywithus.com/`).
1. [!DNL Analytics] präsentiert die während dieser Interaktion gesammelten Informationen in verschiedenen Berichten z. B. [!UICONTROL Verweisende Domänen], [!UICONTROL Suchmaschinen] und [!DNL Search Keywords].

## Beispiel: Browsen mit Umleitungen {#section_921DDD32932847848C4A901ACEF06248}

Umleitungen können dazu führen, dass der Browser die eigentliche verweisende URL ausblendet. Betrachten wir das folgende Szenario:

1. Der Benutzer verweist seinen Browser auf `https://www.google.com`, gibt *Discount-Airline Tickets* in das Suchfeld ein und klickt anschließend auf die Schaltfläche **[!UICONTROL Suchen]**.
1. Die Adressleiste des Browser-Fensters zeigt die vom Benutzer ins Suchfeld eingegebenen Suchbegriffe `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets` an. Beachten Sie, dass die Suchbegriffe in die URL-Abfragestringparameter einbezogen werden, die auf `https://www.google.com/search?` ? folgen. Der Browser zeigt auch eine Seite an, die die Suchergebnisse einschließlich einem Link zu einem Ihrer Domänennamen enthält: [!DNL https://www.flytohawaiiforfree.com/]. Diese *Vanity*-Domäne ist konfiguriert, um den Benutzer auf `https://www.flywithus.com/` / umzuleiten.
1. Der Benutzer klickt auf den Link `https://www.flytohawaiiforfree.com/` und wird vom Server auf Ihre Hauptseite `https://www.flywithus.com` umgeleitet. Wenn die Weiterleitung erfolgt, gehen die für die Datenerfassung in [!DNL Analytics] wichtigen Daten verloren, da der Browser die verweisende URL löscht. Somit sind die ursprünglichen Suchinformationen nicht mehr vorhanden, die in den [!DNL Analytics]-Berichten (z. B. [!UICONTROL Verweisende Domänen], [!UICONTROL Suchmaschinen], [!UICONTROL Keywords]) verwendet wurden.

[Implementierung von Weiterleitungen](/help/implement/js-implementation/redirects-overview.md#concept_5EC2EE9677A44CC5B90A38ECF28152E7) – In diesem Abschnitt wird erklärt, wie [!DNL Analytics]-Variablen eingesetzt werden können, um die bei einer Weiterleitung verlorenen Daten zu erfassen. Der Abschnitt erläutert insbesondere, wie die oben beschriebene Situation mit „Discount-Airline Tickets“ beseitigt werden kann.

## Umleitungen implementieren {#concept_5EC2EE9677A44CC5B90A38ECF28152E7}

Damit [!DNL Analytics] Daten aus Weiterleitungen erfasst werden können, müssen vier kleinere Änderungen an dem Code, der die Weiterleitung erstellt, und an der [!DNL AppMeasurement] für JavaScript-Datei vorgenommen werden.

<!-- 

redirects_implement.xml

 -->

Mit Durchführung der folgenden Schritte werden die Informationen erhalten, die der ursprüngliche Verweis (zum Beispiel `https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets` im obigen Szenario) an Ihre Site weitergibt:

## Konfiguration von JavaScript-Code zum Außerkraftsetzen des Verweises {#section_87BB1D47D9C345C18339078824645CC4}

<!-- 

redirects_js_override.xml

 -->

Der nachstehende Codeabschnitt zeigt zwei JavaScript-Variablen, *`s_referrer`* und *`s_pageURL`*. Dieser Code wird auf der endgültigen Landingpage der Weiterleitung platziert.

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
>Stellen Sie *`s.referrer`* nur einmal auf der Seite ein. Wenn Sie die Variable bei jedem Tracking-Aufruf oder jedem Klick festlegen, wird sie vom Referrer und ähnlichen Dimensionen wie Suchmaschinen und Schlüsselwörtern doppelt gezählt.

## Weiterleitungen mittels getQueryParam {#section_EE924E399F7A431C8FC8E8A2BEF84DEC}

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

## Ändern des Weiterleitungsmechanismus {#section_2FF9921E8FCA4440B6FF90F15386E548}

<!-- 

redirects_modify_mechanism.xml

 -->

Da der Browser die verweisende URL abdeckt, müssen Sie den Mechanismus konfigurieren, der die Weiterleitung durchführt (zum Beispiel den Webserver, den serverseitigen Code, den clientseitigen Code), um die Informationen zum ursprünglichen Verweis weiterzugeben. Wenn Sie auch die Link-URL des Alias aufzeichnen möchten, muss dies auch auf die endgültige Landingpage übertragen werden. Verwenden Sie die Variable *`s_pageURL`* zum Überschreiben der aktuellen URL.

Da viele Möglichkeiten zur Implementierung einer Weiterleitung bestehen, müssen Sie ggf. mit Ihrer Web Operations-Gruppe oder Ihrem Online-Werbepartner die spezifischen Mechanismen bestimmen, die Weiterleitungen auf Ihrer Website ausführen.

## Erfassung der ursprünglich verweisenden Stelle {#section_7F1A77F447CF485385B456A64B174050}

<!-- 

redirects_referrer.xml

 -->

Für gewöhnlich ruft [!DNL Analytics] die verweisende URL aus der Eigenschaft [!UICONTROL document.referrer] und die aktuelle URL aus der Eigenschaft [!UICONTROL document.location] des Browsers ab. Durch Übergabe von Werten an die Variablen *`referrer`* und *`pageURL`* können Sie die Standardverarbeitung überschreiben. Durch Übergabe eines Werts an die Variable „referrer“ teilen Sie [!DNL Analytics] mit, dass die Referrer-Information in der Eigenschaft [!UICONTROL document.referrer] ignoriert und stattdessen ein anderer, von Ihnen definierter Wert verwendet werden soll.

Daher muss die finale Version der Landingpage den folgenden Code enthalten, damit die Fehler im Szenario „Discount-Airline Tickets“ korrigiert werden können.

```js
<script language="JavaScript" src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"></script> 
<script language="JavaScript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.campaign="" 
s.referrer="https://www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets" 
// Setting the s.pageURL variable is optional.
s.pageURL="https://www.flytohawaiiforfree.com"
```

## Überprüfen des Referrers mit dem Adobe Debugger {#section_B3E85941982E4E1698B271375AD669B9}

<!-- 

redirects_verify_referrer.xml

 -->

Führen Sie einen Test durch, um zu überprüfen, dass die verweisende Stelle, die Quell-URL (*`s_server`*) und die Kampagnenvariablen erfasst werden.

These variables will be represented as the following parameters in the [Experience Cloud Debugger](https://marketing.adobe.com/resources/help/en_US/experience-cloud-debugger/).

<table id="table_5F3B987D4D514CA283F7B9F52EBC2301"> 
 <thead> 
  <tr> 
   <th class="entry"> </th> 
   <th class="entry"> <b>URL oder Query String-Wert</b> </th> 
   <th class="entry"> <b>Im DigitalPulse-Debugger angezeigter Wert</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Ursprünglich verweisende Stelle </p> </td> 
   <td> <p> <span class="filepath"> https://www.google.com/search%3F hl%3Den %26ie%3DUTF826q%3 Ddiscount%2Bairline%2Btickets </span> </p> </td> 
   <td> <p> <span class="filepath"> r=https:/ref=www.google.com/search?hl=en&amp;ie=UTF -8&amp;q=discount+airline+tickets </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>„Seiten-URL“ </p> </td> 
   <td> <p> <span class="filepath"> https://www.flytohawaiiforfree.com </span> </p> </td> 
   <td> <p> <span class="filepath"> g=https://www.flytohawaiiforfree.com </span> </p> <p>Dieser Wert wird im DigitalPulse-Debugger angezeigt, wenn die Variable <span class="varname"> pageURL</span> verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Endgültige Landingpage-URL </p> </td> 
   <td> <p> <span class="filepath"> https://www.flywithus.com </span> </p> </td> 
   <td> <p>Dieser Wert wird NICHT im DigitalPulse-Debugger angezeigt, wenn die Variable <span class="varname">pageURL</span> verwendet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

Im Debugger wird Folgendes angezeigt:

```
Image 
 
https://flywithuscom.112.2o7.net/b/ss/flywithuscom/1/JS-1.4/s61944015791667?[AQB] 
ndh=1 
t=4/8/2014 13:34:28 4 360 
pageName=Welcome to FlyWithUs.com 
r=https://ref=www.google.com/search?hl=en&ie=UTF-8&q=discount+airline+tickets 
cc=USD 
g=https://www.flytohawaiiforfree.com 
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

Nachdem Sie überprüft haben, ob der Adobe [!UICONTROL Debugger] diese Variablen anzeigt, sollten Sie sich immer vergewissern, dass die Suchbegriffe und die ursprünglich (vor der Umleitung) verweisende Domäne in Berichten Traffic verzeichnen.
