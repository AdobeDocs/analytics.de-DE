---
description: Im Abschnitt „Feed-Informationen“ können Sie den Feed benennen, die Report Suite angeben, für die der Feed ausgeführt werden soll, die Feed-Wiederholung bestimmen und angeben, wann der Feed startet und endet.
keywords: Datenfeed;Informationen;Name;Report Suite;E-Mail bei Abschluss;E-Mail;Intervall;Feed;Verzögerung der Verarbeitung;Verzögerung;Start;Ende;Datum;kontinuierlicher Feed
seo-description: Im Abschnitt „Feed-Informationen“ können Sie den Feed benennen, die Report Suite angeben, für die der Feed ausgeführt werden soll, die Feed-Wiederholung bestimmen und angeben, wann der Feed startet und endet.
seo-title: Feed-Informationen
solution: Analytics
title: Feed-Informationen
uuid: adf92f42-a957-4de0-a5a1-683f2933af04
translation-type: tm+mt
source-git-commit: bc46011a48aa18e33ba6f1912223857f5a664f35

---


# Feed-Informationen

Im Abschnitt „Feed-Informationen“ können Sie den Feed benennen, die Report Suite angeben, für die der Feed ausgeführt werden soll, die Feed-Wiederholung bestimmen und angeben, wann der Feed startet und endet.

![](assets/feed-info.jpg)

<table id="table_C98C7C3CE4194BEF819E792793EBC517">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Feld </th>
   <th colname="col2" class="entry"> Beschreibung </th>
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Name (Erforderlich) </p> </td>
   <td colname="col2"> <p>Geben Sie einen Feed-Namen ein. </p> <p>Der Name muss innerhalb der ausgewählten Report Suite eindeutig sein. Er kann bis zu 255 Zeichen enthalten. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Report Suite (erforderlich) </p> </td>
   <td colname="col2"> <p>Geben Sie die Report Suites für die Feed-Abfrage an. </p> <p>Es muss mindestens eine Report Suite ausgewählt werden. Sie können dieselbe Report Suite nicht zweimal angeben. </p> <p>Alle nicht-virtuellen Report Suites, die dem angemeldeten Benutzer zur Verfügung stehen, sind verfügbar. </p></td>
  </tr>
  <tr>
   <td colname="col1"> <p>E-Mail bei Abschluss versenden (erforderlich) </p> </td>
   <td colname="col2"> <p>Geben Sie den E-Mail-Empfänger an, der die aktualisierten Feed-Bereitstellungen erhält. </p> <p>Dieses Feld darf nicht leer sein. Es muss eine ordnungsgemäß formatierte E-Mail-Adresse enthalten. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Feed-Intervall (erforderlich) </p> </td>
   <td colname="col2"> <p>Geben Sie die Zeitplanwiederholung an. </p> <p>Anmerkung: Stellen Sie aufgrund der potenziellen Größe der Zip-Dateien des Datenfeeds sicher, dass Ihr ETL-Prozess ein 64-Bit-Zip-Dienstprogramm verwendet. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Verarbeitung verzögern (optional) </p> </td>
   <td colname="col2"> <p>Geben Sie die auf die einzelnen Zeitplaninstanzen anzuwendende Verzögerung an. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Start- und Enddatum (erforderlich) </p> <p>Kontinuierlicher Feed (optional) </p> </td>
   <td colname="col2"> <p>Planen Sie die Termine für den Start und das Ende des Feeds. </p> <p>
     <ul id="ul_509977336CD34032924B48E043E8CBC7">
      <li id="li_BFB5B6ADCB184D839C9BA42DB3DCAF32">Startdatum: wird standardmäßig auf das Datum des aktuellen Tags festgelegt </li>
      <li id="li_34F8DB45D9B54076840D1A0B782812D3">Enddatum: wird standardmäßig auf das Datum des folgenden Tags festgelegt </li>
     </ul>
     </p> </td>
  </tr>
 </tbody>
</table>
