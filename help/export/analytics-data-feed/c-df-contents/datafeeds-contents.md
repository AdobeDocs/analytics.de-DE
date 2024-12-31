---
description: In diesem Abschnitt werden die Dateien beschrieben, die in einer Daten-Feed-Bereitstellung enthalten sind.
keywords: Daten-Feed;Auftrag;Inhalte;Manifest;Datei;Suche;Trefferdaten;Bereitstellungsinhalte
subtopic: data feeds
title: Daten-Feed-Inhalte – Übersicht
feature: Data Feeds
exl-id: 7456ed99-c2f3-4b19-a63e-6b4e457e7d55
source-git-commit: 6b8366b451be1612331f517ee80fd57744deafdc
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 69%

---

# Daten-Feed-Inhalte - Übersicht

In den folgenden Abschnitten wird beschrieben, wie Sie auf die Dateien in einem Daten-Feed-Versand zugreifen und diese verstehen können.

## Zugreifen auf Daten-Feed-Inhalte

So greifen Sie auf die Inhalte eines Daten-Feeds zu:

1. Melden Sie sich bei der Ziel-Site des Daten-Feeds an.

   Dies ist die Ziel-Site, die Sie beim Erstellen des Daten-Feeds eingerichtet haben, z. B. einen Amazon S3- oder Google Cloud Platform-Bucket.

1. Laden Sie die komprimierte Daten-Feed-Datei auf Ihren lokalen Computer herunter.

1. Dekomprimieren Sie die komprimierte Datei mit einem Programm, das `.tar.gz`-Dateierweiterungen unterstützt.

1. Öffnen Sie die `hit_data.tsv`-Datei in einer Tabelle oder in einer Datenbankanwendung Ihrer Wahl, um die Rohdaten für diesen Tag anzuzeigen. —>

## Manifestdatei {#feed-manifest}

Die Manifestdatei enthält folgende Details zu den einzelnen Dateien, die Bestandteil des hochgeladenen Datensatzes sind:

* Dateiname
* Dateigröße
* MD5-Hash
* Anzahl der in der Datei enthaltenen Datensätze

Die Manifestdatei hat dasselbe Format wie eine Java-JAR-Manifestdatei.

Die Manifestdatei wird immer abschließend in Form einer separaten `.txt`-Datei gesendet. Mit der Manifestdatei wird signalisiert, dass der vollständige Datensatz für den Anforderungszeitraum ausgeliefert wurde. Manifestdateien werden nach folgendem Muster benannt:

```text
[rsid]_[YYYY-mm-dd].txt
```

Eine typische Manifestdatei enthält Daten, die folgendem Schema entsprechen:

```text
Datafeed-Manifest-Version: 1.0
 Lookup-Files: 1
 Data-Files: 1
 Total-Records: 611

 Lookup-File: rsid_date-lookup_data.tar.gz
 MD5-Digest: af6de42d8b945d4ec1cf28360085308
 File-Size: 63750

 Data-File: 01-rsid_date.tsv.gz
 MD5-Digest: 9c70bf783cb3d0095a4836904b72c991
 File-Size: 122534
 Record-Count: 611
```

Jede Manifestdatei enthält eine Kopfzeile, in der die Gesamtanzahl der Lookup-Dateien, Datendateien sowie die Gesamtanzahl der Datensätze in allen Datendateien angegeben sind. Nach dieser Kopfzeile folgen verschiedene Abschnitte mit Informationen zu den einzelnen Dateien, die in der Datenfeedauslieferung enthalten sind.

Einige Feeds sind so konfiguriert, dass sie eine `.fin`-Datei anstelle einer `.txt`-Manifestdatei erhalten. Die `.fin` gibt an, dass der Upload abgeschlossen ist, die darin enthaltenen Metadaten jedoch in einem älteren Format.

## Lookup-Dateien

In manchen Daten-Feed-Spalten wird eine Zahl ausgegeben, die einem Wert entspricht. Lookup-Dateien werden verwendet, um diese Zahl in einer Daten-Feed-Spalte einem tatsächlichen Wert zuzuordnen. Beispielsweise bedeutet der Wert „497“ in der Spalte mit den `browser`-Trefferdaten, dass der Treffer von „Microsoft Internet Explorer 8“ stammte, wie in `browser.tsv` ersichtlich ist.

Beachten Sie, dass `column_headers.tsv` und `event_list.tsv` spezifisch für den Daten-Feed und die Report Suite sind. Andere Dateien, z. B. `browser.tsv`, sind hingegen generisch.

Lookup-Dateien werden in einer komprimierten ZIP-Datei bereitgestellt, die nach folgendem Muster benannt ist:

```text
[rsid]_[YYYY-mm-dd]-lookup_data.[compression_suffix]
```

* **`column_headers.tsv`**: Eine einzelne Zeile, die die Spaltenüberschriften für die `hit_data.tsv` enthält.
* **`browser.tsv`**: Ordnet die Browser-ID (die `browser` Feed-Spalte) dem Anzeigenamen des Browsers zu.
* **`browser_type.tsv`**: Ordnet die Browser-ID (die Spalte &quot;`browser` Feed„) dem Browser-Typ zu.
* **`color_depth.tsv`**: Ordnet die Farbtiefe-ID (die Spalte für den `color`-Feed) der Farbtiefe zu.
* **`connection_type.tsv`**: Ordnet die Verbindungstyp-ID (die Spalte &quot;`connection_type` Feed„) dem Verbindungstyp zu.
* **`country.tsv`**: Ordnet die Länder-ID (die `country` Feed-Spalte) dem Ländernamen zu.
* **`javascript_version.tsv`**: Ordnet die JavaScript-Versions-ID (die `javascript` Feed-Spalte) der JavaScript-Version zu.
* **`languages.tsv`**: Ordnet die Sprach-ID (die `language` Feed-Spalte) der Sprache zu.
* **`operating_systems.tsv`**: Ordnet die Betriebssystem-ID (die Spalte &quot;`os` Feed„) dem Betriebssystemnamen zu.
* **`plugins.tsv`**: Ordnet die Plug-in-IDs (die Spalte &quot;`plugin` Feed„) den jeweiligen Plug-in-Namen zu.
* **`resolution.tsv`**: Ordnet die Auflösungs-ID (die `resolution` Feed-Spalte) der Monitorauflösung zu.
* **`referrer_type.tsv`**: Ordnet die Referrer-Typ-ID (die Spalte &quot;`ref_type` Feed„) dem Referrer-Typ zu.
* **`search_engines.tsv`**: Ordnet die Suchmaschinen-ID (die Spalte &quot;`search_engine` Feed„) dem Suchmaschinennamen zu.
* **`event.tsv`**: Ordnet jede Ereignis-ID (die `event_list` Feed-Spalte) dem entsprechenden Ereignisnamen zu.

## Trefferdatendateien

Die Trefferdaten werden in der Datei `hit_data.tsv` bereitgestellt. Die Menge an Daten in dieser Datei richtet sich nach dem Auslieferungsformat (stündlich oder täglich sowie danach, ob die Auslieferung in einer oder in mehreren Dateien erfolgt). Diese Datei enthält nur die Trefferdaten. Die Spaltenkopfzeilen werden separat mit den Lookup-Dateien geliefert. Jede Zeile in dieser Datei entspricht einem einzelnen Server-Aufruf.

Die von Adobe bereitgestellten Dateien variieren je nach Art des konfigurierten Daten-Feeds. Alle Dateien sind ISO-8859-1-kodiert.

* `[rsid]` Bezeichnet die Report Suite-ID, aus der der Daten-Feed stammt.
* `[index]` wird nur bei mehreren Datei-Feeds verwendet und bezieht sich auf die richtige Reihenfolge paginierter Dateien.
* `[YYYY-mm-dd]` bezeichnet den Starttag des Daten-Feed.
* `[HHMMSS]` wird nur in stündlichen Feeds verwendet und bezeichnet den Startzeitpunkt des Daten-Feed.
* `[compression_suffix]` bezeichnet die Art der verwendeten Komprimierung. Normalerweise werden Daten-Feeds in `tar.gz`- oder `zip`-Dateien komprimiert.
* `[format_suffix]` bezieht sich auf den Typ des Dateiformats. Normalerweise ist das Format der Daten-Feed-Datei `.tsv`.

### Täglich; einzelne Datei

Nachdem die Daten einen Tag lang erfasst wurden, erhalten Sie eine einzelne komprimierte Datendatei und eine Manifestdatei. Die Datendatei hat den Namen:

`[rsid]_[YYYY-mm-dd].[compression_suffix]`

Nach dem Extrahieren enthält die Datendatei eine einzelne `hit_data.tsv`-Datei, die alle Daten für diesen Tag beinhaltet, sowie Lookup-Dateien für alle erforderlichen Spalten.

### Täglich; mehrere Dateien

Nachdem die Daten einen Tag lang erfasst wurden, erhalten Sie eine oder mehrere komprimierte Datendateien und eine Manifestdatei. Die Datendatei hat den Namen:

`[index]-[rsid]_[YYYY-mm-dd].[compression_suffix]`

Nach dem Extrahieren enthält jede Datendatei eine einzelne `[index]-[rsid]_[YYYY-mm-dd].[format_suffix]`-Datei, die ca. 2 GB unkomprimierte Daten beinhaltet, sowie Lookup-Dateien für alle erforderlichen Spalten.

### Stündlich; einzelne Datei

Nachdem die Daten eine Stunde lang erfasst wurden, erhalten Sie eine einzelne komprimierte Datendatei und eine Manifestdatei. Die Datendatei hat den Namen:

`[rsid]_[YYYYmmdd]-[HHMMSS].[compression_suffix]`

Nach dem Extrahieren enthält die Datendatei eine einzelne `hit_data.tsv`-Datei, die alle Daten für diese Stunde beinhaltet, sowie Lookup-Dateien für alle erforderlichen Spalten.

### Stündlich; mehrere Dateien

Nachdem die Daten eine Stunde lang erfasst wurden, erhalten Sie eine oder mehrere komprimierte Datendateien und eine Manifestdatei. Die Datendateien werden folgendermaßen benannt:

`[index]-[rsid]_[YYYYmmdd]-[HHMMSS].[format_suffix].[compression_suffix]`

Nach der Extraktion enthält jede Datendatei eine einzelne `[index]-[rsid]_[YYYYmmdd]-[HHMMSS].[format_suffix]`, die etwa 2 GB unkomprimierte Daten enthält, sowie Lookup-Dateien für alle erforderlichen Spalten.

## Größe der Datendatei

Die Größe der Trefferdatei kann in Abhängigkeit von der Anzahl der aktiv genutzten Variablen und dem Traffic an die Report Suite stark variieren. Eine Datenzeile ist durchschnittlich 500 B (komprimiert) oder 2 KB (unkomprimiert) groß. Dieser Wert multipliziert mit der Anzahl der Server-Aufrufe ergibt einen ungefähren Schätzwert zur Größe einer Daten-Feed-Datei. Sobald Ihr Unternehmen Daten-Feed-Dateien empfängt, können Sie eine genauere Zahl feststellen, indem Sie die Anzahl der Zeilen in `hit_data.tsv` durch die Gesamtdateigröße dividieren.