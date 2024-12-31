---
description: Sie können Dimensionen filtern, die Sie dem Raster „Zeilenbezeichnungen“ hinzugefügt haben. Filter engen die von Anforderungen zurückgegebenen Daten ein und können sowohl auf Pivot- als auch auf benutzerdefinierte Layouts angewendet werden. Wenn Sie die Filterung von Dimensionen im Pivot-Layout konfigurieren, können Sie zusätzlich die Anzahl der Einträge von einer Zelle angeben.
title: Übersicht über Filterdimensionen
uuid: c54d5add-f278-476d-8f14-73f1c2e37671
feature: Report Builder
role: User, Admin
exl-id: eded07d5-3c06-419b-92fd-1a48856ac293
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 73%

---

# Übersicht über Filterdimensionen

{{legacy-arb}}

Sie können Dimensionen filtern, die Sie dem Raster „Zeilenbezeichnungen“ hinzugefügt haben. Filter engen die von Anforderungen zurückgegebenen Daten ein und können sowohl auf Pivot- als auch auf benutzerdefinierte Layouts angewendet werden. Wenn Sie die Filterung von Dimensionen im Pivot-Layout konfigurieren, können Sie zusätzlich die Anzahl der Einträge von einer Zelle angeben.

Das ausgewählte Filterformular wird basierend auf dem Element und der Metrik ausgefüllt, die in der Report Builder-Anfrage ausgewählt wurden.

## Filter definieren – Werte und Sonderzeichen {#section_15840216A4044C40974945FAA435AD93}

Informationen über Filter im Bereich **[!UICONTROL Am meisten bevorzugte Filter]** > **[!UICONTROL Filter definieren]**.

![Screenshot mit dem Dialogfeld „Filter definieren“ mit Optionen zum Filtern nach Anwendung, Benutzer und Projekt.](/help/admin/admin/assets/filter.png)

Die folgenden Tabellen enthalten Beispiele und Informationen über Filter:

<table id="table_8AC3A26FF02143DBA949B30F2A46CF11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Filter </th> 
   <th colname="col02" class="entry"> Beschreibung </th> 
   <th colname="col2" class="entry"> Beispielfilter </th> 
   <th colname="col3" class="entry"> Übereinstimmungsergebnisse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Enthält alle Begriffe </p> </td> 
   <td colname="col02"> <p>Enthält jeden durch Leerzeichen getrennten Wert in jeder beliebigen Reihenfolge. </p> </td> 
   <td colname="col2"> <p>a b c </p> </td> 
   <td colname="col3"> <p>Stimmt <span class="term"> a b </span> und <span class="term"> b a </span> usw. überein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enthält einen der Begriffe </p> </td> 
   <td colname="col02"> <p>Enthält mindestens einen der Filter (durch Leerzeichen getrennt). </p> </td> 
   <td colname="col2"> <p>A B C </p> </td> 
   <td colname="col3"> <p>Entspricht <span class="term"> A1</span>, <span class="term"> B2</span>, <span class="term"> C3</span>, jedoch nicht <span class="term"> D4</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enthält die Wortgruppe </p> </td> 
   <td colname="col02"> <p>Enthält den Suchfilter und mögliche andere Begriffe. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>Entspricht <span class="term"> abc</span> und <span class="term"> abc def</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enthält keine Begriffe </p> </td> 
   <td colname="col02"> <p>Gibt alles zurück, sofern es keinen von Ihnen eingegebenen Wert enthält. </p> </td> 
   <td colname="col2"> <p>a b c </p> </td> 
   <td colname="col3"> <p>Entspricht <span class="term"> d e f</span>, aber nicht <span class="term"> c d e f</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enthält nicht die Wortgruppe </p> </td> 
   <td colname="col02"> <p>Gibt alles zurück, das nicht Ihre Wortgruppe enthält. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>Schließt <span class="term"> abc</span>, <span class="term"> abc def</span> aus und stimmt mit <span class="term"> def überein</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gleich </p> </td> 
   <td colname="col02"> <p>Gibt einen exakten Treffer zurück. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p> <span class="term"> abc</span> wird zurückgegeben, nichts anderes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ist nicht gleich </p> </td> 
   <td colname="col02"> <p>Gibt alles zurück, das nicht genau Ihrem Eintrag entspricht. </p> </td> 
   <td colname="col2"> <p>a </p> </td> 
   <td colname="col3"> <p>Entspricht nicht <span class="term"> a</span>. </p> <p>Stimmt überein mit<span class="term"> a b c</span>. </p> <p>Stimmt überein mit<span class="term"> abc</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beginnt mit </p> </td> 
   <td colname="col02"> <p>Gibt Ergebnisse zurück, die mit einem bestimmten Wert beginnen. </p> </td> 
   <td colname="col2"> <p>abc </p> </td> 
   <td colname="col3"> <p>Entspricht <span class="term"> abcd</span> aber nicht <span class="term"> 1abc</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Endet mit </p> </td> 
   <td colname="col02"> <p>Gibt Ergebnisse zurück, die mit einem bestimmten Wert enden. </p> </td> 
   <td colname="col2"> <p>xyz </p> </td> 
   <td colname="col3"> <p>Stimmt überein mit <span class="term">wxyz</span>, aber nicht mit <span class="term"> wxyz0</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Erweitert (Sonderzeichen) </p> </td> 
   <td colname="col02"> <p>Ermöglicht die Suche nach Zeichen in regulären Ausdrücken: </p> <p> <code> "", ^, -, *, $, | </code> </p> </td> 
   <td colname="col2"> <p>"^Home*Page$" | Sport </p> </td> 
   <td colname="col3"> <p> Dadurch wird ein Filter definiert, der mit <span class="term"> Startseite</span> beginnt, dann nach null oder mehr Zeichen sucht und dann mit <span class="term"> Seite </span>. </p> <p>Auch jede Seite mit <span class="term">Sport</span> darin wird erfasst. </p> <p>Beispiele für Treffer sind: </p> 
    <ul id="ul_72D76C5AFEAF405E8A0E4E3C604D10AE"> 
     <li id="li_4D490059B667450DA8A0103167C7B391">HomePage </li> 
     <li id="li_1351619156274092AEB2771D882AD357">Home und (andere Zeichen) Page </li> 
     <li id="li_940EAA99A8CF49308E8471065EB317B1">Home Sport </li> 
     <li id="li_50A895F14A454BE9BF06EE0F07F99B3B">Sport Page </li> 
     <li id="li_F3CE0D07941D4C2485D2DE0B73E00677">Sport </li> 
     <li id="li_E84C15C061824A5D922D9900392F2996">xyz Sport abc </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_8BBB06C8860745DEA41B39673699DC0F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Sonderzeichen </th> 
   <th colname="col2" class="entry"> Zweck </th> 
   <th colname="col3" class="entry"> Hinweise </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> "" </td> 
   <td colname="col2"> Gleich </td> 
   <td colname="col3"> <p>Nicht mit einem Escapezeichen versehen, sofern es nicht mit einem anderen Anführungszeichen verwendet wird. <span class="term"> 17-Zoll-Display</span> ist beispielsweise keine Wortgruppe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> * </td> 
   <td colname="col2"> Platzhalterzeichen </td> 
   <td colname="col3"> <p>Entspricht dem Sternchen in einem regulären Ausdruck. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ^ </td> 
   <td colname="col2"> Beginnt mit </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> $ </td> 
   <td colname="col2"> Endet mit </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> – </td> 
   <td colname="col2"> Nicht </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> | </td> 
   <td colname="col2"> Oder </td> 
   <td colname="col3"> <p>Wird nur im Filter <span class="term"> Erweitert (Sonderzeichen) </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
