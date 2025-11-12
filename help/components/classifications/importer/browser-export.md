---
title: Browser-Export
description: Mit dem Browser-Export können Sie die Klassifizierungsdaten in eine mit Tabulatoren getrennte Datei exportieren.
feature: Classifications
exl-id: f4c709b2-f707-4e3c-82ba-6b43def3e698
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 60%

---

# Browser-Export (veraltet)

{{classification-importer-deprecation}}

Mit dem Browser-Export können Sie die Klassifizierungsdaten in eine mit Tabulatoren getrennte Datei exportieren.

[!UICONTROL Admin] > [!UICONTROL Classification Importer]

Die Datensatzdatei ist eine tabulatorgetrennte Datendatei (Dateierweiterung.tab), die von den meisten Tabellenkalkulationsprogrammen unterstützt wird.

>[!NOTE]
>Browser-Exporte sind auf 30 Spalten beschränkt.

## Feldbeschreibungen

| Element | Beschreibungen |
| --- | --- |
| Report Suite auswählen | Wählen Sie die Report Suite aus, aus der Sie die Berichtsdaten exportieren möchten. |
| Datensatz, der klassifiziert werden soll | Wählen Sie aus dem Dropdown-Menü den Datensatz aus, den Sie klassifizieren möchten. |
| Zeilenanzahl auswählen | Geben Sie die Anzahl der zu exportierenden Datenzeilen an.<ul><li>Wählen Sie **[!UICONTROL Alle]**, um alle Berichtsdaten (bis zu 50.000 Zeilen) herunterzuladen. </li><li>Wählen Sie **[!UICONTROL Datenzeilen beschränken auf]**, wenn Sie eine bestimmte Anzahl von Zeilen zum Download festlegen möchten.</li></ul>Wenn Sie mehr als 50.000 Datenzeilen herunterladen möchten, verwenden Sie die FTP-Download-Option. |
| Filtern nach Empfangsdatum | (Optional) Filtern Sie Daten nach dem Empfangsdatum. Geben Sie den Datumsbereich an, für den Sie Daten herunterladen möchten. |
| Anwenden eines Datenfilters | (Optional) Filtern des Datensatzes nach Datenkriterien. Sie können den Download so filtern, dass Datenzeilen mit spezifischen Werten oder nicht zugewiesenen Spalten-Werten (Classification-Werten) einbezogen werden. Beachten Sie beim Anwenden von Datenfiltern die folgenden Probleme:<ul><li>Beim Definieren des Datenfilters können Sie Platzhalter verwenden. Verwenden Sie ein Sternchen als Platzhalter für null oder mehr Zeichen und ein Fragezeichen `?` für genau ein Zeichen. Für ein oder mehrere Zeichen können Sie `?*` eingeben.</li><li>Wenn Sie beide Arten von Datenfiltern auf einen Download anwenden, werden in der Regel nur Zeilen heruntergeladen, die beiden Regeln entsprechen. Es gelten jedoch die folgenden Ausnahmen:<ul><li>Wenn die Bedingung „Zeilen mit leerer Spalte = Alle Spalten“ gilt, werden alle Spalten mit Ausnahme der in der ersten Regel angegebenen Spalte auf ihren leeren Gehalt überprüft. Diese Ausnahme stellt sicher, dass das System jede Zeile mit einer Spalte herunterlädt, die mit der ersten Regel übereinstimmt, bei der auch alle anderen Spalten leer sind.</li><li>Beim Herunterladen von Datenzeilen, die auf leeren Spalten basieren, werden alle Spalten mit Ausnahme der in der ersten Regel angegebenen auf Leere überprüft.</li><li>Wenn dieselbe Spalte für beide Filterregeln angegeben ist (es ist fast unmöglich, beide Kriterien zu erfüllen), werden nur Zeilen heruntergeladen, die der ersten Regel entsprechen.</li></ul></ul> |
| Datenfilter | (Optional) Filtern von Daten nach Kampagnendaten. Sie können Daten nur aus aktiven Kampagnen herunterladen oder Kampagnen auswählen, die in einem bestimmten Datumsbereich begonnen (oder beendet) haben.<br>**Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |
| Export von Numerisch 2 | Mit dem Importer können Sie Numerisch-2-Classifications in das System importieren. Numerisch-2-Classifications sind für Variablen sinnvoll, die sich im Laufe der Zeit für verschiedene Artikel bzw. Einheiten ändern, z. B. Kosten und Budgetwerte im Marketing-Kanal-Bericht. Im Abschnitt „Numerisch-2-Classifications“ finden Sie Informationen zum Hochladen von Daten mithilfe von Numerisch-2-Classifications. |
| Codierung | Wählen Sie die Zeichencodierung für die Datendatei aus. Das Standardcodierungsformat ist entweder UTF-8 oder ISO-8859-1, basierend auf der für die Classification hochgeladenen Codierung. Mit „UTF-8 zu UTF-16“ können Sie UTF-8-codierte Classifications in UTF-16-Codierung konvertieren. ISO-8859-1 in UTF-16 konvertiert Ihre ISO-8859-1-kodierten Klassifizierungen in UTF-16-Kodierung.<br>**Hinweis:** Wenn Sie die Konvertierung in UTF-16 wählen, muss die Quellcodierung mit der Codierung des ursprünglichen Uploads übereinstimmen, da andernfalls unerwartete Ergebnisse auftreten können. Es wird empfohlen, alle hochgeladenen Dateien in UTF-8 ohne BOM zu kodieren. |
| Kursausgabe | Gibt Version 2.1 für die Klassifizierungsdatei an. Bei dieser Einstellung werden Sonderzeichen in Anführungszeichen gesetzt, um sicherzustellen, dass Exporte in Excel funktionieren, wenn die eVar-Werte einen Zeilenumbruch aufweisen. Sie können feststellen, ob es sich bei einer Klassifizierungsdatei um Version 2.1 handelt, indem Sie die heruntergeladene Datei öffnen. In der Kopfzeile wird v2.1 angezeigt. Beispiel: `## SC SiteCatalyst SAINT Import File v:2.1` |

## Exportieren von Classification-Daten über den Browser

1. Klicken Sie auf [!UICONTROL Admin] > [!UICONTROL Classification Importer].
1. Klicken Sie auf die Registerkarte [!UICONTROL Browser-Export].
1. Spezifizieren Sie die Datensatzdetails.
1. Klicken Sie auf [!UICONTROL Datei exportieren].
1. Speichern Sie den Datensatz auf Ihrem lokalen System.
