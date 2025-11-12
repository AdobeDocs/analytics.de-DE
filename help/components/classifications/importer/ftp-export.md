---
title: Export von Klassifizierungsdaten über FTP
description: Der FTP-Export bietet mehr Flexibilität beim Herunterladen von Datensätzen, z. B. die Fähigkeit, Daten aus mehreren Report Suites oder Datensatzdatein mit mehr als 50.000 Datenzeilen herunterzuladen.
feature: Classifications
exl-id: 6f97f0b2-1a04-407f-9df9-8715da52037d
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 68%

---

# FTP-Export (veraltet)

{{classification-importer-deprecation}}

Die FTP-Option bietet mehr Flexibilität beim Herunterladen von Datensätzen, z. B. die Fähigkeit, Daten aus mehreren Report Suites oder Datensatzdateien mit über 50.000 Datenzeilen herunterzuladen. Erstellen Sie vor dem Herunterladen von Klassifizierungsdaten via FTP ein FTP-Konto.

Beachten Sie beim Anwenden von Datenfiltern die folgenden Probleme:

* Beim Definieren des Datenfilters können Sie Platzhalter verwenden. Verwenden Sie ein Sternchen `*` als Platzhalter für null oder mehr Zeichen und ein Fragezeichen `?` für genau ein Zeichen. Für ein oder mehrere Zeichen können Sie `?*` eingeben.
* Wenn Sie beide Arten von Datenfiltern auf einen Download anwenden, werden in der Regel nur Zeilen heruntergeladen, die beiden Regeln entsprechen. Es gelten jedoch die folgenden Ausnahmen:
   * Wenn die Bedingung „Zeilen mit leerer Spalte = Alle Spalten“ gilt, werden alle Spalten mit Ausnahme der in der ersten Regel angegebenen Spalte auf ihren leeren Gehalt überprüft. Diese Ausnahme stellt sicher, dass das Tool jede Zeile mit einer Spalte herunterlädt, die mit der ersten Regel übereinstimmt, bei der auch alle anderen Spalten leer sind.
   * Beim Herunterladen von Datenzeilen, die auf leeren Spalten basieren, werden alle Spalten mit Ausnahme der in der ersten Regel angegebenen auf Leere überprüft.
   * Wenn dieselbe Spalte für beide Filterregeln angegeben ist (es ist fast unmöglich, beide Kriterien zu erfüllen), werden nur Zeilen heruntergeladen, die der ersten Regel entsprechen.
   * FTP-Exporte sind auf 30 Spalten begrenzt.

## Exportieren von Klassifizierungen per FTP

In diesen Schritten wird beschrieben, wie Sie Klassifizierungen aus Adobe Analytics über FTP exportieren (herunterladen).

1. Erstellen Sie ein FTP-Konto.
1. Gehen Sie zu [!UICONTROL Admin] > [!UICONTROL Classification Importer].
1. Klicken Sie auf die Registerkarte **[!UICONTROL FTP-Import]**.
1. Konfigurieren Sie die Felder für den FTP-Export.
1. Klicken Sie auf **[!UICONTROL Datei exportieren]**.
1. Speichern Sie den Datensatz auf Ihrem lokalen System.

## Feldbeschreibungen

| Element | Beschreibungen |
| --- | --- |
| [!UICONTROL Report Suite auswählen] | Wählen Sie die Report Suite aus, aus der Sie die Berichtsdaten exportieren möchten. |
| [!UICONTROL Datensatz, der klassifiziert werden soll] | Wählen Sie aus dem Dropdown-Menü den Datensatz aus, den Sie klassifizieren möchten. |
| [!UICONTROL Zeilenanzahl auswählen] | Geben Sie die Anzahl der zu exportierenden Datenzeilen an.<ul><li>Wählen Sie **[!UICONTROL Alle]**, um alle Berichtsdaten herunterzuladen.</li><li>Wählen Sie **[!UICONTROL Datenzeilen beschränken auf]**, wenn Sie eine bestimmte Anzahl von Zeilen zum Download festlegen möchten.</li></ul> |
| [!UICONTROL Filtern nach Empfangsdatum] | (Optional) Filtern Sie Daten nach dem Empfangsdatum. Geben Sie den Datumsbereich an, für den Sie Daten herunterladen möchten. |
| [!UICONTROL Datenfilter anwenden] | (Optional) Filtern des Datensatzes nach Datenkriterien. Sie können den Download so filtern, dass Datenzeilen mit spezifischen Werten oder nicht zugewiesenen Spalten-Werten (Classification-Werten) einbezogen werden.  |
| [!UICONTROL Datumsfilter] | (Optional) Daten nach Kampagnendatum filtern. Sie können festlegen, dass nur Daten aus aktiven Kampagnen heruntergeladen werden, oder Sie können Kampagnen auswählen, die in einem bestimmten Datumsbereich beginnen (oder enden). |
| [!UICONTROL Export von Numerisch 2] | Mit dem Importer können Sie Numerisch-2-Classifications in das System importieren. Numerisch-2-Classifications sind für Variablen sinnvoll, die sich im Laufe der Zeit für verschiedene Artikel bzw. Einheiten ändern, z. B. Kosten und Budgetwerte im Marketing-Kanal-Bericht. |
| [!UICONTROL FTP-Konto] | Geben Sie die Informationen zum FTP-Server an, auf den Adobe die Datendatei herunterladen soll, inklusive Host-Namen und Port, Pfad des Zielverzeichnisses, Benutzername und Kennwort. |
| [!UICONTROL Benachrichtigung] | Geben Sie die E-Mail-Adresse an, an die Benachrichtigungen zu diesem FTP-Download gesendet werden sollen. |
| [!UICONTROL Codierung] | Wählen Sie die Zeichencodierung für die Datendatei aus. Das Standardcodierungsformat ist entweder UTF-8 oder ISO-8859-1, basierend auf der für die Classification hochgeladenen Codierung. Mit „UTF-8 zu UTF-16“ können Sie UTF-8-codierte Classifications in UTF-16-Codierung konvertieren. ISO-8859-1 in UTF-16 konvertiert Ihre ISO-8859-1-kodierten Klassifizierungen in UTF-16-Kodierung.<br>**Hinweis:** Wenn Sie die Konvertierung in UTF-16 wählen, muss die Quellcodierung mit der Codierung des ursprünglichen Uploads übereinstimmen, da andernfalls unerwartete Ergebnisse auftreten können. Es wird empfohlen, alle hochgeladenen Dateien in UTF-8 ohne BOM zu kodieren. |
