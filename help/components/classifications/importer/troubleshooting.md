---
title: Fehlerbehebung beim Klassifizierungs-Importer
description: Häufige Upload-Probleme bei der Verwendung von Classification Importer.
feature: Classifications
exl-id: de3e9eca-9264-4711-b73a-4a1a3dd16715
TQID: https://experienceleague.adobe.com/YDa--mPqMNfRfRT-xUYTj6jJVEFf2HXWSUtELvuBpy4
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 875
ht-degree: 92%

---

# Fehlerbehebung beim Klassifizierungs-Importer

{{classification-importer-deprecation}}

Die häufigsten Probleme beim Hochladen von Classification-Daten in Adobe.

## Falsches Dateiformat oder falsche Dateierweiterung

Klassifizierungen erfordern einen bestimmten Dateityp und ein bestimmtes Dateiformat, damit sie erfolgreich hochgeladen werden können. Wenn sie nicht im richtigen Format gespeichert wurden, verursacht dies einen Fehler und es werden keine Zeilen verarbeitet. Der zurückgegebene Fehler lautet häufig *„Die erste Spalte muss der Schlüssel sein“*. Es kann sich aber um eine beliebige Anzahl von Fehlern handeln. Überprüfen Sie Folgendes:

* **Hochladen einer Tabelle (.xlsx) anstelle einer tab- oder txt-Datei**: Beim Hochladen von Klassifizierungsdateien in einem falschen Format erhalten Sie die Fehlermeldung *„Die erste Spalte muss der Schlüssel sein“*. Der Klassifizierungs-Importer kann keine xls- oder xlsx-Dateien verarbeiten. Stellen Sie im Excel-Dialogfeld „Speichern unter“ den richtigen Dateityp ein:
   * Verwenden Sie unter Windows das Dateiformat `Text (Tab delimited) (*.txt)`.
   * Verwenden Sie unter Mac das Dateiformat `Windows Formatted Text`.
* **Sie haben die Erweiterung des Dateinamens nach dem Speichern als Arbeitsmappe geändert**: Beim Versuch, eine Dateierweiterung direkt umzubenennen, wird eine ungültige Arbeitsmappe generiert. Verwenden Sie ausschließlich die Excel-Funktion „Speichern unter“ oder nutzen Sie einen Texteditor wie Notepad++.
* **Sie haben Erweiterungen in Großbuchstaben verwendet**: Erweiterungen in Großbuchstaben (z. B. dateiupload.`fileupload.TXT`) funktionieren nicht. Benennen Sie die Datei in eine kleingeschriebene Erweiterung um (`fileupload.txt`).
* **Nicht übereinstimmende Zeichenkodierung**: Stellen Sie sicher, dass die Kodierung des gespeicherten Classification-Uploads mit der ursprünglichen Kodierung beim Herunterladen der Vorlage übereinstimmt. Wenn Sie eine UTF-16-Datei hochladen, obwohl sie ursprünglich in UTF-8 kodiert war, führen Uploads zu unerwarteten Ergebnissen. Adobe empfiehlt das Hochladen von Dateien im UTF-8-Format ohne Byte-Reihenfolge-Markierungen.

## Ungültiger Dateiinhalt

Wenn Ihre Upload-Datei korrekt formatiert ist, versucht der Uploader, so viele gültige Zeilen wie möglich zu importieren. Einige häufig auftretende Probleme mit Classification-Daten:

* **Zeilen, die bereits klassifiziert wurden**: Wenn Sie versuchen, Zeilen hochzuladen, die bereits mit demselben Wert klassifiziert wurden, gibt der Importer Zeilen zurück, die keine Auswirkungen hatten. Dies ist so vorgesehen, da Klassifizierungen einen Schlüsselwert nicht erneut mit derselben Klassifizierung klassifizieren. Es handelt sich um eine Benachrichtigung anstelle eines Fehlers. Sie müssen sich also keine Gedanken darum machen, Zeilen innerhalb einer Exportdatei zu ändern. Adobe empfiehlt, nur geänderte Zeilen hochzuladen.
* **Kopfzeile stimmt nicht mit hochgeladener Variable überein**: Wenn Sie eine Classification-Vorlage für die Trackingcode-Dimension herunterladen und versuchen, sie in eine eVar-Classification hochzuladen, schlägt dies fehl. Verwenden Sie Exportdateien nur für die spezifischen Variablen, aus denen sie exportiert wurden.
* **Schlüssel- oder Classification-Wert enthält 0**: Classifications können den Wert 0 nicht von einer leeren Zeile unterscheiden und können somit diesen Wert nicht klassifizieren. Weitere Informationen finden [ unter Häufig gestellte Fragen ](importer-faq.md) Classification Importer .
* **Die Classification-Datei enthält Kommas oder Sonderzeichen**: Informationen zum Maskieren von Werten finden [ in den ](importer-faq.md) zum Classification Importer .
* **Zusätzliche Tabulatoren in der hochgeladenen Datei**: Manchmal werden beim Bearbeiten von Classification-Dateien versehentlich zusätzliche Tabs hinzugefügt. Jede Zeile erfordert eine identische Anzahl von Tabulatoren, damit sie richtig verarbeitet werden kann. Um zu überprüfen, ob die Datei über zusätzliche Tabulatoren verfügt, markieren Sie den gesamten Text in einem Texteditor und stellen Sie sicher, dass keine Zeilen Leerzeichen am Ende haben.
* **Doppelte Schlüsselwerte in der Datei**: Jeder Schlüsselwert darf nur eine Classification pro Spalte aufweisen. Wenn Sie versuchen, denselben Wert mehrmals zu klassifizieren, gibt der Importer einen Fehler aus.
* **Unterklassifizierungen sind vorhanden und falsch konfiguriert**: Wenn Unterklassifizierungen vorhanden sind, überprüfen Sie Folgendes:
   * Alle Unterklassifizierungswerte haben einen übergeordneten Classification-Wert
   * Keine zwei Unterklassifizierungen verweisen auf denselben übergeordneten Classification-Wert
* **Spaltenabweichung**: Sie können die Fehlermeldung *„Der Schlüssel in der Zeile hat zu viele Spalten“* erhalten, wenn eine Zeile eine ungültige Spaltenanzahl enthält. Das ist beispielsweise der Fall, wenn Sie 3 Spalten in Ihrem Klassifizierungs-Upload haben, die Variable jedoch nur über eine einzelne Klassifizierung verfügt. Überprüfen Sie Ihre Upload-Datei, um sicherzustellen, dass die Anzahl der Spalten nicht größer ist als die Anzahl der für diese Variable konfigurierten Klassifizierungen.

## Fehlerbehebung bei FTP-Importen

Die folgenden Ursachen sind häufig der Grund dafür, dass FTP-Klassifikationen hochgeladene Dateien nicht verarbeiten:

* **Fehlende .fin-Datei**: Erstellen Sie ein leeres Textdokument auf Ihrem Desktop und benennen Sie die Dateinamenerweiterung von .txt in .fin um. Der Name dieser .fin-Datei muss mit dem Namen der betreffenden Classification-Datei übereinstimmen. Wenn Ihr FTP-Dateiname beispielsweise `fileupload.tab` lautet, nennen Sie Ihre .fin-Datei `fileupload.fin`. Nach dem Hochladen der .fin-Datei werden beide Dateien ausgeblendet.
* **Hochladen der .fin-Datei vor der Classification-Datei**: Manchmal wird eine .fin-Datei erstellt, bevor das Hochladen der Classification-Datei auf die FTP-Site abgeschlossen ist. Die Verarbeitung kann fehlschlagen, wenn Dateien nicht in der richtigen Reihenfolge hochgeladen werden. Entfernen Sie beide Dateien, fügen Sie zuerst die Classification-Datei hinzu und dann die .fin-Datei, nachdem die Classification-Datei vollständig hochgeladen wurde.
* **Die Dateigröße ist übermäßig groß**: Adobe empfiehlt, die Größe der Classification-Dateien so gering wie möglich zu halten, um eine zügige Verarbeitung zu gewährleisten.
* **Vorhandene Dateien werden bereits verarbeitet**: Wenn mehrere Dateien für dieselbe Variable und dieselbe Report Suite hochgeladen werden, wird die Verarbeitung der alten Datei zugunsten der neuen Datei eingestellt. Wenn Sie Klassifizierungen mit mehreren Dateien hochladen, warten Sie auf die Bestätigung, dass die Verarbeitung der vorhandenen Dateien abgeschlossen ist, bevor Sie neue hochladen.
* **Hochgeladene Dateien, die nicht im Stammverzeichnis abgelegt sind**: Auf die FTP-Site von Adobe hochgeladene Dateien müssen im Stammverzeichnis abgelegt werden. Wenn Classification-Importdateien in Unterordnern abgelegt werden, werden sie nicht erfasst oder verarbeitet.

Wenn Sie weiterhin Probleme beim Hochladen einer Classification-Datei haben, wenden Sie sich an die Adobe-Kundenunterstützung.
