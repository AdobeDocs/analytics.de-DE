---
description: In diesem Thema erhalten Sie Antworten auf die am häufigsten gestellten Fragen.
subtopic: Data sources
title: Häufig gestellte Fragen zu Data Sources
topic-fix: Developer and implementation
feature: Data Sources
exl-id: 2a5d38fe-5c5b-4275-bc44-e9cb02ec2f5d
source-git-commit: 18c5f88cef907af1bdb17c99df59dfb46cc859bc
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 94%

---

# Häufig gestellte Fragen zu Data Sources

In diesem Thema erhalten Sie Antworten auf die am häufigsten gestellten Fragen.

## Wie können Offline-Daten mit Online-Ereignissen verknüpft werden? {#offline}

Damit Transaktions-ID-Datenquellen Offline-Daten mit Online-Events verbinden können, müssen Sie die Aufzeichnung der Transaktions-ID aktivieren. Weitere Informationen erhalten Sie unter [Transaktions-ID-Aufzeichnung](/help/import/c-data-sources/datasrc-integrating-offline-data.md#section_30D6D47AEC0F4A36B87EBFE4C858F20C).

## Wie viel kostet die Nutzung der Datenquelle-Funktion? {#cost}

Für die Nutzung der Data Sources-Applikation fallen keine weiteren Gebühren außer dem Standard-Server-Aufruf an. Server-Aufruf-gebühren gelten nur für Datenquellen-Typen mit vollständiger Verarbeitung, bei denen einzelne Treffer als Datenzeilen gesendet werden. Traffic- und Datenquellen auf aggregierter Ebene führen nicht zu zusätzlichen Kosten.

## Wie kann ich in Data Sources-Dateien Kommentare einfügen? {#comments}

Jede Zeile in einer Data Sources-Datei, die mit einem Nummernzeichen (#) beginnt, wird als Kommentar interpretiert.

## Muss ich in meine Tabellendaten eine Datumsspalte einfügen? {#date}

Ja. Da viele Marketingberichte auf der Datumsspalte basieren, benötigt Data Sources eine Datumsspalte.

## Kann ich Daten in bestehenden und bereits verwendeten Variablen speichern? {#variables}

Adobe empfiehlt, dass Sie neue, noch nicht verwendete Variablen auswählen, um Daten mit Data Sources zu importieren. Wenn Sie sich bei der Konfiguration der Datendatei unsicher sind oder die Risiken einer erneuten Nutzung von Variablen besser verstehen möchten, setzen Sie sich mit der Kundenunterstützung in Verbindung.

## Kann ich Daten löschen, die mit Data Sources importiert wurden? {#imported}

Nein. Daten, die mit Data Sources in Berichte hochgeladen wurden, können nach dem Import nicht entfernt werden, auch nicht von Adobe-Mitarbeitern. Sie werden dauerhaft in die bestehenden Daten eingefügt und lassen sich nicht von den mit herkömmlichen Datenerfassungsmaßnahmen (z. B. JavaScript, ActionSource, Data Insertion API) eingegebenen Daten unterscheiden. Daher empfiehlt Adobe dringend, dass Sie Data Sources-Daten in eine Report Suite zum Testen laden, bevor Sie sie in eine Produktionssuite hochladen.

## Wie viele Daten kann ich gleichzeitig importieren? {#amount}

Die Verarbeitung wird angehalten, wenn die Datenmenge 50 MB übersteigt, und wird erst fortgesetzt, wenn die Gesamtmenge unter 50 MB liegt. Um Verzögerungen beim Generieren von Berichten auf ein Minimum zu reduzieren, laden Sie pro Tag nicht mehr als die Daten von 90 Tagen hoch.

## Werden bestehende Daten überschrieben, wenn ich Daten über Data Sources importiere? {#overwrite}

Daten aus Data Sources überschreiben nie bestehende Berichtsdaten. Stattdessen werden die mit Data Sources hochgeladenen Daten den bestehenden Daten hinzugefügt.

## Warum werden nicht auch meine Metriken angezeigt, wenn ich Daten über Data Sources hochladen? {#metrics}

Wenn Sie Daten aus Data Sources hochladen, laden Sie die Metriken hoch, die in der Berichtsoberfläche zur Verfügung stehen werden.

Wenn Sie beispielsweise den Call-Center-Umsatz für Produkte hochladen, die Sie über Ihre Site vertreiben, kann der Call-Center-Umsatz im gleichen Bericht wie der Online-Umsatz angezeigt werden. Sie können sie jedoch nicht zusammen mit Besuchen verwenden, da Sie damit nicht die Anzahl der Besuche hochgeladen haben. Adobe kann nur Berichte für die Metriken und Elemente erstellen, die Sie über Data Sources hochgeladen haben (neben den normalen Marketingberichtsmetriken).

## Was passiert, wenn ich über Data Sources negative Werte in Berichte einfüge? {#negative}

Der Wert wird entsprechend verringert.

## Worin besteht der Unterschied zwischen einer Traffic- und einer (generischen) Konversion-Datenquelle? {#traffic}

Die Traffic-Datenquelle wird sehr viel schneller hochgeladen, da sie nur die zusammenfassenden Werte in den entsprechenden Tabellen aktualisiert. Die generische Datenquelle mit Konversion-Daten (Ereignisse usw.) erstellt für jeden Wert in der Spalte, die verarbeitet werden soll, einen Hit.

Beispieldatei:

<table id="table_D5408E0BDB984229B4C60A66BB53CEBB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code> Date </code> </p> </td> 
   <td colname="col2"> <p> <code> Event15 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code> 01/01/2013 </code> </p> </td> 
   <td colname="col2"> <p> <code> 553 </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

Im oben aufgeführten Beispiel werden 553 Hits erzeugt, die im Cache-System verarbeitet werden sollen.

## Berücksichtigt Data Sources untergeordnete Beziehungen, Korrelationen und Pfade? {#breakdown}

Da der Datenquelle-Prozess („für generische DS, nicht Datenverkehr“) einzelne Hits erstellt, die vom Cache verarbeitet werden, wird der Prozess für untergeordnete Beziehungen und nicht der Korrelationsprozess verwendet. Pfade können potenziell verarbeitet werden, aber jeder Hit würde für einen eigenen Besuch stehen, sodass keine Pfade generiert werden. Pfaddaten werden für Webprotokoll-Importe generiert.

## Muss bei der Dateierweiterung die Groß- und Kleinschreibung für eine Datenquelle-Upload- oder Classification-Datei beachtet werden? {#case}

Wenn die Erweiterungen einer Datenquelle-Upload-Datei oder einer Classification-Datei großgeschrieben sind, werden die Dateien nicht verarbeitet. Erweiterungen einer Datenquelle-Upload-Datei müssen kleingeschrieben werden. So werden beispielsweise [!DNL file.TXT] und [!DNL file.FIN] nicht verarbeitet. Auch [!DNL .TAB] und [!DNL .FIN] werden nicht verarbeitet. [!DNL .txt] und [!DNL .fin] werden jedoch verarbeitet.

## Kann ich weitere Ereignisse zur generierten Vorlage hinzufügen oder liegt das Maximum bei drei? {#template}

Sie können beliebig viele Ereignisse hinzufügen. Der Assistent erlaubt jedoch nur drei Ereignisse. Sobald die Vorlagendatei erstellt wurde, können Sie bei Bedarf weitere Ereignisse hinzufügen.

## Was geschieht mit einer Datenquelle-Datei, in der mindestens einer der Datensätze nicht die gleiche Anzahl Spalten wie der Header-Datensatz hat? {#header}

Bei einer Datenquelle-Datei, in der mindestens einer der Datensätze nicht die gleiche Anzahl Spalten wie der Header-Datensatz hat, passiert Folgendes.

* Der Ersteller der Datenquelle erhält eine E-Mail, in der er auf den Fehler hingewiesen wird.
* Die Datei wird aufgrund der ungleichen Spaltenanzahl nicht verarbeitet.

## Wird mit Data Sources-Informationen eine Datenaggregation durchgeführt? {#rollup}

Mit Data Sources-Informationen kann eine Datenaggregation durchgeführt werden. Die Adobe-Kundenunterstützung muss die Datenaggregation jedoch ab den historischen Daten erneut verarbeiten, um die historischen Daten einzuschließen. Wenn das aktuelle Datum z. B. der 31. Oktober 2015 ist und Sie Daten für den 1. bis 15. August 2015 mit Data Sources hochladen, muss die Datenaggregation so eingerichtet sein, dass eine neue Verarbeitung ab dem 1. August 2015 durchgeführt wird, damit die neu importierten Daten eingeschlossen werden.

Beachten Sie zudem, dass Daten niemals direkt über Data Sources in eine Datenaggregations-Report-Suite hochgeladen werden sollten. Wenn diese Daten in einer Datenaggregation eingeschlossen werden sollen, müssen Sie in eine standardmäßige Report Suite importiert werden, die auch als  *`child suite`* der Datenaggregation bezeichnet wird. Wenden Sie sich an die Adobe-Kundenunterstützung, um weitere Informationen zu erhalten.

## Warum enthält der Seitenansichtsbericht keine Data Sources-Daten für einen einzelnen Tag, sondern die korrekten Daten für eine Woche? {#week}

Data Sources erfasst keine Daten auf Stundenbasis. Wenn Sie einen Bericht für einen bestimmten Tag ausführen möchten, können die Daten nur stundenweise unterteilt werden, sodass nichts im Bericht angezeigt wird. Sie können nur Daten sehen, wenn die Unterteilung auf Tagesbasis oder in einem größeren Zeitraum erfolgt, indem Sie einen Wochen- oder Monatsbericht ausführen.

## Wie werden „Unique Visitors“ in einem Webserver-Protokoll Datenquelle-Upload berechnet? {#unique}

Die Anzahl an Unique Visitors in einem Webserver-Protokoll wird als spezifische Kombination aus *`IP Address`* und *`User Agent`* im Webprotokoll berechnet. Jede einzigartige Kombination dieser beiden Elemente wird als Unique Visitor berechnet. Wenn die Spalte [!UICONTROL Benutzeragent] leer ist (oder nicht im Webprotokoll eingeschlossen ist), können wir nicht die Zahl der Unique Visitors ermitteln, sodass der gesamte Upload als ein Unique Visitor zählt (selbst wenn mehrere IP-Adressen vorliegen).

## Wie kann ich in Data Sources herausfinden, welche Anmeldeinformationen zu welcher Report Suite gehören? {#login}

Die Report Suite-ID ist in Data Sources der erste Teil der Anmeldeinformationen, an den eine zufällige Nummer angehängt wird, die die jeweilige Datenquelle kennzeichnet, die eingerichtet wurde. Beispiel: `RSID-drmossdev5 Login-drmossdev5_0001343430`.

## Wie wirken sich die Version 15 und die Segmentierung auf Datenquellen aus? {#segmentation}

In Version 15 weist Data Sources je nach Quelltyp ein unterschiedliches Verhalten auf:

* Datenquellen mit vollständiger Verarbeitung, Webprotokollen und Transaktions-ID werden normal angezeigt. Wenn Segmente angewendet werden, werden die Daten entsprechend den Segmentregeln gefiltert.
* Standard- oder Konversionsdatenquellen (Werbekampagnen, CRM, Kundenzufriedenheit, Siteperformance, allgemeine Zusammenfassungsdaten, Onlinekäufe, Interessenten und Angebote sowie Offlinekanaldaten) werden in Version 15 angezeigt. Da diese Datenquellen jedoch nicht an Besuche oder Besucher gebunden sind, werden sie beim Anwenden von Segmenten herausgefiltert.

## Sind Metriken, die mit einer Transaktions-ID importiert werden, in Clickstream Data Feeds und Data Warehouse verfügbar? {#clickstream}

Der Data Feed enthält alle Metriken mit Transaktions-IDs, die empfangen wurden. Wenn Sie jedoch Transaktions-ID-Daten für ein Datum in der Vergangenheit hochladen, können diese Daten nur abgerufen werden, indem Sie den Data Feed erneut für diesen Tag herunterladen.

## Sind eVars, die aktuell im Besucherprofil bestehen, Metriken zugeordnet, die mithilfe von Datenquellen hochgeladen wurden? {#visitor}

Im Falle einer vollen Verarbeitung ist dies nicht der Fall, im Falle von Transaktions-IDs trifft dies zu. Datenquellen mit vollständiger Verarbeitung werden mit getrennten Besucherprofilen verarbeitet. Das heißt, selbst wenn die Besucher-IDs übereinstimmen, werden sie aus der Sicht einer eVar-Zuordnung nicht aneinander gebunden. Transaktions-ID-Datenquellen werden an das Hauptbesucherprofil gebunden, sodass bestehende eVars Ereignissen zugeordnet werden, die mit einer Transaktions-ID hochgeladen wurden.

## Beeinflussen die mit Datenquellen hochgeladenen eVars das spätere Online-Verhalten? {#evars}

Nein. Die mit Transaktions-ID-Datenquellen hochgeladenen eVars führen in den gespeicherten Profilinformationen lediglich Lesevorgänge aus, das Profil wird nicht aktualisiert.
Nein. eVars sind die einzigen Variablen, die im Schnappschuss des Besucherprofils gespeichert werden.

## Wie funktionieren numerische und Währungsereignisse mit Datenquellen? {#numeric}

Die Vollverarbeitung unterstützt nur herkömmliche Formate für Ereignislisten mit Ausnahme von Ereigniswerten vom Typ „numerisch“, „Währung“ oder „Zähler“ (größer als 1) direkt in der Ereignisliste, d. h. `"eventNN,eventKK"` und nicht `"eventNN=#.##"`. Dies bedeutet, dass es nur ein Zählerereignis unterstützt, wenn es in der Datenquellendatei in der Ereignisspalte übergeben wird und um 1 inkrementiert wird.

Wenn Ereignisse vom Typ „numerisch“, „Währung“ oder „Zähler“ (größer als 1) erforderlich sind, verwenden Sie die Produktliste:

```js
s.products="Footwear;Running Shoes;1;99.99;event1=4.50";
s.products="Footwear;Running Shoes;1;99.99;event1=4.50|event4=1.99";
```

## Warum wird mein FTP-Upload nicht erfasst?

Nachdem die .fin -Datei hochgeladen wurde, ist es wichtig, dass Sie sich von der Data Sources-FTP-Site abmelden. Analytics verwendet Abmeldeereignisse nämlich als Trigger dafür, dass Dateien zur Verarbeitung bereit sind. Wenn Sie die Dateien programmgesteuert hochladen, ist es wichtig, dass sich Ihr automatisierter Prozess auch nach dem Hochladen der Dateien von der FTP-Site abmeldet.

Überprüfen Sie, ob Ihre Dateinamen das richtige Format aufweisen. Das Anführen oder Anhalten von Leerzeichen im Dateinamen führt dazu, dass die Adobe nicht erkannt wird und nicht vom Aufnahmevorgang erfasst wird.
