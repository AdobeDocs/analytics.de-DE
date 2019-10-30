---
description: 'null'
seo-description: 'null'
seo-title: Häufig gestellte Fragen
title: Häufig gestellte Fragen
uuid: 05724f56-cf98-4ad8-ad0d-83a5a4b1944a
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Häufig gestellte Fragen

## Zugriff/Berechtigungen {#section_5F558C5981F747F0AF375A9E4B75C93C}

<table id="table_6713C3B0B6734F768370F974EB5AC5E8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Q: Do I need to be an <b>Adobe Advertising Cloud or Adobe Advertising Cloud (AMO) customer</b> to access this functionality? </p> </td> 
   <td colname="col2"> <p>A: Nein, diese Funktion steht auch Kunden ohne Advertising Cloud und AMO zur Verfügung. </p> <p>AMO-Kunden können die bestehende Analytics-AMO-Integration nutzen, jedoch nicht Advertising Analytics verwenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Welche <b>Adobe Analytics-SKUs</b> berechtigen zur Verwendung von Advertising Analytics? </p> </td> 
   <td colname="col2"> <p>A: Advertising Analytics steht für die Adobe Analytics-SKUs <a href="https://www.adobe.com/data-analytics-cloud/analytics/select.html" format="html" scope="external">Select</a>, <a href="https://www.adobe.com/data-analytics-cloud/analytics/prime.html" format="html" scope="external">Prime</a> und <a href="https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html" format="html" scope="external">Ultimate</a> zur Verfügung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Müssen wir eine <b>Zusatzgebühr</b> für die Verwendung von Advertising Analytics bezahlen? </p> </td> 
   <td colname="col2"> <p>A: Nein, abgesehen von der ordnungsgemäßen SKU-Bereitstellung verursacht Advertising Analytics keine zusätzlichen Kosten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Wird Advertising Analytics bei meiner <b>Serveraufruf-Nutzung</b> angerechnet? </p> </td> 
   <td colname="col2"> <p>A: Nein, Advertising Analytics verwendet einen speziellen Datenquellentyp, der keine zusätzlichen Kosten für Serveraufrufe verursacht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Wenn ich <b>bereits Advertising Cloud/AMO verwende</b>, kann ich dennoch die Advertising Analytics-Funktionen nutzen? </p> </td> 
   <td colname="col2"> <p>A: Jedes kompatible Suchmaschinenkonto wird an Advertising Analytics übergeben und schreibgeschützt angezeigt. Sämtliche Bearbeitungen oder Aktualisierungen müssen in Advertising Cloud/AMO vorgenommen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Ich besitze die richtige SKU, aber kann <b>nicht auf Advertising Analytics zugreifen</b>. Woran liegt das? </p> </td> 
   <td colname="col2"> <p>A: Advertising Analytics ist nur für Adobe Analytics-Administratoren verfügbar, die jedoch auch anderen Benutzern Zugriff gewähren können. Wenden Sie sich also an Ihren Administrator, um Zugriffsrechte zu erhalten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Verwenden von Advertising Analytics {#section_3A70C6C4D5A842B2981F0257A01F95FF}

<table id="table_4EC69262B7AB4DF49E736CF3B0362302"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>F: Welche <b>Suchmaschinenkonten</b> sind in Advertising Analytics enthalten? </p> </td> 
   <td colname="col2"> <p>A: Die Suchmaschinenkonten Google AdWords und Microsoft Bing sind enthalten. </p> <p>Hinweis: Yahoo Gemini wurde am 31. März 2019 von Microsoft Bing übernommen. Daher ist die Anzeigen-Kontenoption „Yahoo Gemini“ nicht mehr verfügbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Wo <b>greife ich auf Advertising Analytics zu</b>? </p> </td> 
   <td colname="col2"> <p>A: Öffnen Sie nach der Anmeldung bei Adobe Analytics das Menü <span class="uicontrol">Admin</span>. Wählen Sie dann die neue Menüoption <span class="uicontrol">Advertising Analytics</span> aus, um Suchmaschinenkonten hinzuzufügen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Wie werden die <b>Daten erfasst und an Analytics übergeben</b>? </p> </td> 
   <td colname="col2"> <p>A: Advertising Analytics nutzt eine Reihe spezieller APIs, um Daten über die Adobe Advertising Cloud von Suchmaschinen an Analytics zu übertragen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Welche <b>Suchdaten</b> erhalte ich mit dieser Integration? </p> </td> 
   <td colname="col2"> <p>A: Sie erhalten 1) Impressionen, 2) Klicks, 3) Kosten, 4) Qualitätsbewertung, 5) Durchschnittliche Position direkt aus Suchmaschinen und 6) AMO-ID-Instanzen (Klickinstanzen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Kann ich meine <b>Advertising Analytics-Daten nach anderen Analytics-Daten aufschlüsseln</b> (Metriken/Dimensionen)? </p> </td> 
   <td colname="col2"> <p>A: Nein, die Rohdaten der Suche gehen als unabhängiger Datensatz ein. Es gibt jedoch eine Instanzenversion der Klickdaten, die nach anderen Analytics-Daten aufgeschlüsselt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Wie lautet die Definition der verschiedenen <b>Statusanzeigen</b> für meine Konten (ausstehend, aktiv, angehalten usw.)? </p> </td> 
   <td colname="col2"> <p>A: Jede dieser Statusanzeigen gibt die Phase im Lebenszyklus der einzelnen Suchmaschinenkonten an. </p> 
    <ul id="ul_F68AD377B2F04A47B20355B2FF4CF345"> 
     <li id="li_05F8D7C6D00E4742A65373BE6FAA0448"><b>Ausstehend</b> bedeutet, dass das Konto eingerichtet wurde, aber noch keine Daten abgerufen werden. </li> 
     <li id="li_42B1557A8AEC41008B85AF6E3F625CAB"><b>Angehalten</b> bedeutet, dass das Konto zuvor eingerichtet wurde, aber inaktiv ist. </li> 
     <li id="li_30B72CC171874F308A2B8CE552EA6930"><b>Aktiv</b> bedeutet, dass das Konto vollständig eingerichtet wurde und Suchdaten abruft. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Ich möchte <b>meine Advertising Analytics-Konten einer bestimmten Report Suite zuordnen</b>, aber sie ist nicht im Report Suite-Dialog verfügbar. Warum? </p> </td> 
   <td colname="col2"> <p>A: Bevor Sie einem Advertising Analytics-Konto eine Report Suite zuweisen können, muss die entsprechende Suite <a href="../../integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md#concept_BE491B2A2CAE4D818C218033B985A0FB" format="dita" scope="local">für Advertising Analytics-Reporting bereitgestellt</a> werden . </p> <p>This is done through a separate Admin page that is accessible from: <span class="ignoretag"> <span class="uicontrol"> Admin </span>  &gt; <span class="uicontrol"> Report Suites </span>  &gt; <span class="uicontrol"> [select Experience Cloud-enabled report suite] </span>  &gt; <span class="uicontrol"> Edit Settings </span>  &gt; <span class="uicontrol"> Advertising Analytics Configuration </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Ist es möglich, einem Advertising Analytics-Konto eine <b>Virtual Report Suite</b> (VRS) zuzuweisen? </p> </td> 
   <td colname="col2"> <p>A: Virtual Report Suites erfassen keine Daten. Deshalb können Sie ein Advertising Analytics-Konto nicht direkt einer VRS zuweisen. </p> <p>Sie können das Advertising Analytics-Konto jedoch der übergeordneten Report Suite der VRS zuweisen, zu der die Daten hinzugefügt werden sollen. </p> <p>Die Suchmaschinenmetriken (Klick-/Kosten-/Impressionen) werden möglicherweise nicht in der VRS angezeigt, es sei denn, Sie fügen Ihrer Segmentlogik eine "oder"-Bedingung basierend auf der AMO-ID (oder deren Klassifizierung) hinzu. Beispiel: Wenn Sie "alle Treffer, bei denen eine AMO-ID vorhanden ist"hinzufügen, werden die Suchmaschinenmetriken in das Segment einbezogen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Können Advertising Analytics-Metriken zum Bericht <b>Marketingkanäle</b> hinzugefügt werden? </p> </td> 
   <td colname="col2"> <p>A: Nein, sie sind nicht im Marketingkanalbericht enthalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: <b>Wann</b> werden die Suchdaten in Analytics abgerufen? </p> </td> 
   <td colname="col2"> <p>A: Die Suchdaten werden um ca. 6:00 Uhr in der Zeitzone Ihres Analytics-Rechenzentrums von den Suchmaschinen abgerufen. Zu diesem Zeitpunkt werden die AMO-Daten erfasst und in die Report Suite eingefügt. Diese Daten werden dann im Rahmen ihrer Einfügung in Analytics in die Report Suite-Zeitzonen umgewandelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Was kann <b>vor dem Klick erfasst</b> werden? Werden Impressionen, Kosten, durchschnittliche Position usw. auch ohne Klick erfasst? </p> </td> 
   <td colname="col2"> <p>A: Über die AMO-ID werden die Metriken der Suchmaschine erfasst: „Impressionen“, „Kosten“, „Klicks“, „Durchschnittliche Position“ und „Durchschnittliche Qualitätsbewertung“. Sind keine Klicks aber Impressionen vorhanden, werden die Daten zu Impression/Position/Qualität dennoch an Analytics gesendet. In der Regel entstehen keine Kosten, wenn keine Klicks vorhanden sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Auf welcher Ebene werden die Daten erfasst? <b>Besucher? Treffer?</b> </p> </td> 
   <td colname="col2"> <p>A: Die Suchmaschinen-Metriken werden auf der Trefferebene erfasst und mit der AMO-ID (und den zugehörigen Klassifizierungen) verknüpft. Dabei handelt es sich um Daten der Zusammenfassungsebene, die nicht mit Besuchen/Besuchern verbunden sind. Daher können die Suchmaschinen-Metriken nur in Segmenten verwendet werden, die sich im Umfang der Trefferebene befinden und die auf der AMO-ID (oder zugehörigen Klassifizierungen) basieren. </p> <p>Die AMO-ID wird auch auf der Landingpage im Treffer für die betreffende Seite (über die die Verbindung zum Besuch/Besucher hergestellt wird) erfasst. Sie bleibt in der absteigenden Hierarchie bestehen, um für andere Analytics-Metriken berücksichtigt zu werden (bis sie abläuft oder durch eine neue AMO-ID überschrieben wird). Sie ist wie jede andere eVar vollständig in den Datensatz integriert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Werden derzeit nur Daten von google.com erfasst oder auch von den <b>Länderversionen</b> (wie google.co.uk, google.it, google.fr oder google.de)? </p> </td> 
   <td colname="col2"> <p>A: Die Anzeigenplattformklassifizierung erfasst folgende Werte: "Google Adwords" und "Bing Ads". </p> <p>Als gängige Best Practice sollte der Ländercode bei der Benennung der Kampagnen eingefügt werden. Sie können dann nach unten oder nach Segment filtern (z. B. wenn alle Kampagnen mit countryCode_ beginnen, und dann ein Segment erstellen, bei dem Kampagnen (AMO-ID) mit "UK_"beginnen, würde Ihnen nur Daten für das Vereinigte Königreich liefern). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Die Metrik „AMO-Kosten“ bezeichnet die Kosten pro Keyword/Werbeanzeige gemäß den Daten der Suchmaschine. Handelt es sich hierbei um Netto- oder Bruttokosten? </p> </td> 
   <td colname="col2"> <p>A: „AMO-Kosten“ sind lediglich die Kosten, die an die Suchmaschinen gezahlt wurden. Sie enthalten keinerlei Gebühren für Agenturen oder Suchoptimierungs-/Verwaltungsplattformen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Sollen weitere Werbekanäle wie z. B. <b>Display</b> oder <b>Social</b> hinzugefügt werden? </p> </td> 
   <td colname="col2"> <p>A: Nein, aktuell sind diese anderen Kanäle nicht Teil unserer Roadmap. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Automatisches Tracking im Vergleich zu manuellem Tracking {#section_7437C4698A6D482EB7ED94A948390119}

<table id="table_9738FF8459574ED2937A860A665BE739"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>F: Bei der Einrichtung meines Werbekontos erhalte ich die Meldung, dass <b>Automatisches Tracking</b> ungewollte Folgen nach sich ziehen kann. Welche Art von Folgen sind hier gemeint? </p> </td> 
   <td colname="col2"> <p>A: 
     <ul id="ul_59EFF4A2ECE947EBBDB6A9FF6D072FE0"> 
      <li id="li_8731E4B7D6ED4F0996B3630A35D5BAC4">Der Auto-Modus versucht, URL-Parameter im richtigen Format an die Tracking-Vorlagen- bzw. Ziel-URLs anzuhängen. <b>Sie müssen jedoch sicherstellen, dass die hinzugefügten URL-Parameter ordnungsgemäß und persistent auf die richtige Landingpage verweisen. </b> </li> 
      <li id="li_1202FE1FC88342378A60E8FE65E5426B">Der Auto-Modus kann Keywords in die Landing-URL einfügen, die möglicherweise Sonderzeichen enthalten, die Ihr Webserver nicht unterstützt. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F: Wenn ich zunächst manuelles oder automatisches Tracking konfiguriere, kann ich dann später in den jeweils anderen Trackingmodus <b>wechseln</b>? Was sind die Auswirkungen? </p> </td> 
   <td colname="col2"> <p>A: Ja, Sie können wechseln, doch Sie müssen die alte Trackinglogik entfernen, bevor Sie den Wechsel vornehmen. Dies kann zu Ausfallzeiten beim Tracking am Tag des Wechsels führen (insbesondere beim Wechsel vom manuellen zum automatischen Tracking). Daher ist es empfehlenswert, einen Wechsel nur dann vorzunehmen, wenn es absolut notwendig ist. </p> 
    <ul id="ul_3F3CADD1C97B4947A13837CEE63A599D"> 
     <li id="li_CB9265951FD040388AEAB9EAD790A36E"><b>Wechsel vom manuellen zum automatischen Tracking</b>: Entfernen Sie die manuellen Ergänzungen der Tracking-Vorlagen. Ändern Sie dann die entsprechende Option in der Advertising Analytics-Benutzeroberfläche von „Manuell“ zu „Automatisch“ und speichern Sie die Einstellung. Beachten Sie, dass es bis zu x Stunden dauern kann, bis das System die automatischen Trackingcodes bereitstellt. </li> 
     <li id="li_2B6ED1342E2D443B8AF26D03532AB8E4"><b>Wechsel vom automatischen zum manuellen Tracking</b>: Aktualisieren Sie die entsprechende Option in der Setup-Benutzeroberfläche von Advertising Analytics von „Automatisch“ auf „Manuell“ und stellen Sie dann die manuellen Trackingcodes so schnell wie möglich bereit. Wenn Sie während der Bereitstellung der manuellen Trackingcodes die automatischen Trackingcodes in den Tracking-Vorlagen der Suchmaschine sehen, entfernen Sie sie. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

