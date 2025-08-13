---
description: Mit dem Importeur können Sie Classification-Daten in großen Mengen in Form einer Classification-Datendatei in die Analytics-Berichterstellung hochladen. Für den Import ist ein besonderes Dateiformat erforderlich, damit die Daten erfolgreich hochgeladen werden.
title: Klassifizierungsdatendateien
feature: Classifications
exl-id: aa919a03-d461-4d12-adc1-6441fb467e63
source-git-commit: 4eea524bf95c9b6bc9ddc878c8c433bc1e60daee
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 90%

---

# Klassifizierungsdatendateien (veraltet)

{{classification-importer-deprecation}}

Mit dem Importeur können Sie Classification-Daten in großen Mengen in Form einer Classification-Datendatei in die Analytics-Berichterstellung hochladen. Für den Import ist ein besonderes Dateiformat erforderlich, damit die Daten erfolgreich hochgeladen werden.

Zum Erstellen gültiger Datendateien können Sie eine Vorlage herunterladen, die Ihnen eine Dateistruktur zur Verfügung stellt, in die Sie die Classification-Daten einfügen können. Weitere Informationen finden Sie unter [Klassifizierungsvorlage herunterladen](/help/components/classifications/importer/c-download-saint-data.md).

Weitere Informationen zu Zeichenbeschränkungen in Klassifizierungen finden Sie unter [Allgemeine Dateistruktur](/help/components/classifications/importer/c-saint-data-files.md).

## Allgemeine Dateistruktur

Die folgende Abbildung zeigt eine Beispieldatendatei:

![](assets/completed-saint-file.png)

Eine Datendatei muss den folgenden Strukturregeln entsprechen:

* Der Wert von Classifications darf nicht 0 (null) sein.
* Adobe empfiehlt, die Anzahl der Spalten für den Import und Export auf 30 zu begrenzen.
* Hochgeladene Dateien sollten die Zeichenkodierung UTF-8 ohne BOM verwenden.
* Sonderzeichen wie Tabulatoren, Zeilenumbrüche und Anführungszeichen können in eine Zelle eingebettet werden, wenn das v2.1-Dateiformat angegeben und die Zelle ordnungsgemäß [auskommentiert](/help/components/classifications/importer/importer-faq.md) ist. Sonderzeichen umfassen:

  ```text
  \t     tab character 
  \r     form feed character 
  \n    newline character 
  "       double quote
  ```

  Das Komma ist kein Sonderzeichen.

* Klassifizierungsnamen dürfen kein Caret (^) enthalten, da dieses Zeichen eine Unterklassifizierung bezeichnet.
* Vorsicht bei der Verwendung von Bindestrichen. Wenn Sie beispielsweise einen Bindestrich (-) in einem sozialem Begriff verwenden, erkennt Social ihn als [!DNL Not]-Operator (Minuszeichen). Wenn Sie beispielsweise mit dem Import *`fragrance-free`* als Begriff angeben, interpretiert Social den Begriff folgendermaßen: Parfüm *`minus`* frei. Dadurch werden Wortlaute mit den Begriffen *`fragrance`*, jedoch nicht *`free`* erfasst.
* Zeichenbeschränkungen werden erzwungen, um Berichtdaten zu klassifizieren. Wenn Sie beispielsweise eine Klassifizierungstextdatei für Produkte (*`s.products`*) mit Produktnamen mit mehr als 100 Zeichen (Byte) hochladen, werden die Produkte nicht in den Berichten angezeigt. Für Trackingcodes und für alle benutzerdefinierten Konversionsvariablen (eVars) sind jeweils 255 Byte zulässig. Diese Richtlinie erstreckt sich auch auf Spaltenwerte für Klassifizierungs- und Unterklassifizierungen, für die dieselbe Beschränkung von 255 Byte gilt.
* Tabulatorgetrennte Datendatei (Sie können die Vorlagendatei mit jeder Tabellenkalkulationsanwendung oder einem Texteditor erstellen).
* Die Dateierweiterung muss entweder `.tab` oder `.txt` lauten.
* Ein Rautenzeichen (#) kennzeichnet eine Zeile als Benutzerkommentar. Sämtliche mit # beginnenden Zeilen werden von Adobe ignoriert.
* Ein Doppelpfund-Zeichen gefolgt von SC (`## SC`) kennzeichnet die Zeile als Vorab-Header-Kommentar, der vom Reporting verwendet wird. Löschen Sie diese Zeilen nicht.
* Classification-Exporte können aufgrund von Zeilenumbruchzeichen im Schlüssel doppelte Schlüssel aufweisen. Bei einem FTP- oder Browser-Export können Sie dies vermeiden, indem Sie Anführungszeichen für das FTP-Konto aktivieren. Dadurch wird jeder Schlüssel mit Zeilenumbruchzeichen in Anführungszeichen gesetzt.
* Die Zelle C1 in der ersten Zeile der Importdatei enthält eine Versionskennung, die festlegt, wie Classifications die Verwendung von Anführungszeichen im Rest der Datei handhaben.

   * v2.0 ignoriert Anführungszeichen und nimmt an, dass sie alle Bestandteil der angegebenen Schlüssel und Werte sind. Beachten Sie z. B. diesen Wert: &quot;Dies ist &quot;&quot;irgendein Wert&quot;&quot;&quot;. v2.0 würde dies wörtlich wie folgt interpretieren: &quot;Dies ist &quot;&quot;irgendein Wert&quot;&quot;&quot;.
   * v2.1 teilt Classifications mit, dass sie Anführungszeichen als Bestandteil der in Excel-Dateien verwendeten Dateiformatierungen betrachten sollen. Daher würde v2.1 das obenstehende Beispiel wie folgt umformatieren: Dies ist &quot;irgendein Wert&quot;.
   * Es kann zu Problemen kommen, wenn in der Datei v2.1 angegeben ist, jedoch tatsächlich v2.0 gewünscht wurde – und zwar, wenn Anführungszeichen auf eine Weise verwendet werden, die bei Excel-Formatierung nicht zulässig wäre. Z. B., wenn folgender Wert vorliegt: „VP NO REPS“ S/l Dress w/ Overlay. Im Fall von v2.1 ist diese Formatierung nicht korrekt (der Wert sollte von öffnenden und schließenden Anführungszeichen eingeschlossen sein, und Anführungszeichen, die Bestandteil des eigentlichen Werts sind, müssen von Anführungszeichen umgeben sein), und Classifications funktionieren über diesen Punkt hinaus nicht.
   * Vergewissern Sie sich, dass Sie eine der folgenden Aktionen durchführen: Ändern Sie das Dateiformat in v2.0, indem Sie die Kopfzeile (Zelle C1) in den Dateien ändern, die Sie hochladen, ODER setzen Sie die Anführungszeichen für Excel in allen Ihren Dateien korrekt um.

* Die erste (Nicht-Kommentar)-Zeile der Datendatei enthält die Spaltenüberschriften, die die Classification-Daten in der Spalte bezeichnen. Für Spaltenüberschriften ist im Importeur ein bestimmtes Format erforderlich. Weitere Informationen finden Sie unter [Format der Spaltenüberschrift](/help/components/classifications/importer/c-saint-data-files.md).
* Unmittelbar auf die Überschriftenzeile in einer Datendatei folgen die Datenzeilen. Jede Zeile mit Daten sollte ein Datenfeld für jede Spaltenüberschrift enthalten.
* Die Datendatei unterstützt die folgenden Steuercodes, die von Adobe genutzt werden, um die Datei zu strukturieren und Classification-Daten korrekt zu importieren:

<table id="table_0548F2E58B6644208147434EB9B3C21B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> STEUERCODE </th> 
   <th colname="col2" class="entry"> BESCHREIBUNG </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>&lt;Neue Zeile&gt; </p> </td> 
   <td colname="col2"> <p>Ein Neue-Zeile-Zeichen ist das einzig unterstützte Trennzeichen zwischen Datenzeilen/Datensätzen in der Datendatei. In der Regel müssen Sie diese Zeichen nur spezifisch einfügen, wenn Sie ein Programm zur automatischen Erzeugung von Datendateien schreiben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~autogen~ </p> </td> 
   <td colname="col2"> <p>Fordert an, dass Adobe automatisch eine eindeutige ID für dieses Element erzeugt. </p> <p>In Zusammenhang mit Kampagnen weist dieser Steuercode Adobe an, jedem kreativen Element eine Kennzeichnung zuzuweisen. Weitere Informationen finden Sie unter <a href="/help/components/classifications/importer/c-saint-data-files.md"  >Schlüssel</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~period~ </p> </td> 
   <td colname="col2"> <p>Zeigt an, dass die Datenspalte den dem Element zugeordneten Datenbereich widerspiegelt. Weitere Informationen finden Sie unter <a href="/help/components/classifications/importer/c-saint-data-files.md"  >Datum</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Leeres Feld </p> </td> 
   <td colname="col2"> <p>Repräsentiert einen NULL-Wert für das aktuelle Feld. Verwenden Sie dies, wenn eine bestimmte Datenspalte nicht für den aktuellen Datensatz einbezogen werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PRO-Modifizierer </p> </td> 
   <td colname="col2"> <p>Zeigt an, dass die Datenspalte <span class="wintitle">PER-Modifizierer</span>-Felder repräsentiert. Weitere Informationen finden Sie unter <a href="/help/components/classifications/importer/c-saint-data-files.md"  >PER-Modifizierer-Überschriften</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Format der Spaltenüberschrift

>[!NOTE]
>
>Adobe empfiehlt, die Anzahl der Spalten für den Import und Export auf 30 zu begrenzen.

Classification-Datendateien unterstützen die folgenden Überschriften:

### Schlüssel

Jeder Wert muss innerhalb des Systems eindeutig sein. Der Wert in diesem Feld entspricht einem Wert, den Sie im [!DNL JavaScript]-Beacon für Ihre Website der [!DNL Analytics]-Variablen zugewiesen haben. Daten in dieser Spalte können ~autogen~ oder einen beliebigen anderen eindeutigen Trackingcode beinhalten.

### Überschrift einer Klassifizierungsspalte

>[!NOTE]
>
>Die Werte in der Überschrift der Spalte [!UICONTROL Klassifizierungen] müssen die Namenskonvention für Klassifizierungen exakt erfüllen, da sonst der Import fehlschlägt. Wenn die Administratorin oder der Administrator beispielsweise im [!UICONTROL Campaign Set-up Manager] den Wert [!UICONTROL Campaigns] in [!UICONTROL Internal Campaign Names] ändert, muss dies ebenfalls in die Spaltenüberschrift übernommen werden. „Schlüssel“ ist ein reservierter Klassifizierungswert (Kopfzeile). Neue Klassifizierungen mit dem Namen „Schlüssel“ werden nicht unterstützt.

Darüber hinaus unterstützt die Datendatei die folgenden zusätzlichen Überschriftenkonventionen zum Identifizieren von Unterklassifizierungen und anderen spezialisierten Datenspalten:

### Untergliederungsüberschrift

Beispiel: `Campaigns^Owner` ist eine Spaltenüberschrift für die Spalte, die `Campaign Owner` enthält. `Creative Elements^Size` ist auch eine Spaltenüberschrift für die Spalte, die die `Size` Unterklassifizierung der `Creative Elements` enthält.

## Fehlerbehebung für Classifications

* [Häufige Probleme beim Hochladen von](https://helpx.adobe.com/de/analytics/kb/common-saint-upload-issues.html): Knowledge Base-Artikel, in dem Probleme aufgrund von falschen Dateiformaten und Dateiinhalten beschrieben werden.
