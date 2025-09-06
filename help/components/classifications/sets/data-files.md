---
description: Von Klassifizierungssätzen unterstützte Dateiformate
title: Dateiformate für Klassifizierungssätze
feature: Classifications
source-git-commit: 2d9eb9179ace40a8d333883cea78dd67329078ab
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 1%

---

# Dateiformate für Klassifizierungssätze

Klassifizierungssätze unterstützen mehrere Dateiformate für das Massen-Hochladen von Klassifizierungsdaten. Für jedes Format gelten spezifische Anforderungen für erfolgreiche Daten-Uploads.

Sobald Ihre Datei ordnungsgemäß gemäß diesen Spezifikationen formatiert ist, können Sie sie über die Oberfläche der Klassifizierungssätze oder die API hochladen. Detaillierte Upload-Anweisungen finden Sie unter:

* **Browser-Upload**: Siehe [Schema](manage/schema.md)
* **API-Upload**: Siehe [Analytics Classifications API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/)

Klassifizierungssätze unterstützen die folgenden Dateiformate:

* **JSON**: JavaScript Object Notation-Dateien mit strukturierten Daten
* **CSV**: Dateien mit kommagetrennten Werten
* **TSV/TAB**: Dateien mit tabulatorgetrennten Werten

## Allgemeine Dateianforderungen

Alle Dateiformate müssen die folgenden Anforderungen erfüllen:

* **Dateicodierung**: Verwenden Sie UTF-8 ohne Bytereihenfolgen-Markierungen. Die Latin1-Kodierung wird ebenfalls unterstützt.
* **Zeichenbeschränkungen**: Einzelne Classification-Werte haben eine Obergrenze von 255 Byte.
* **Schlüsselanforderungen**: Schlüsselwerte dürfen nicht leer sein oder nur Leerzeichen enthalten. Wenn doppelte Schlüssel vorhanden sind, wird das letzte Vorkommen verwendet.

+++**Details im JSON-Format**

Das JSON-Dateiformat folgt den Konventionen für JSON-Zeilen (JSON). Die Datei muss ein JSON-Objekt pro Zeile enthalten, wobei jedes Objekt einen einzelnen Klassifizierungseintrag darstellt.

>[!NOTE]
>
>Verwenden Sie trotz der folgenden Konventionen für JSON-Zeilen die Dateierweiterung `.json` für alle Uploads. Die Verwendung der `.jsonl`-Erweiterung kann zu Fehlern führen.

### JSON-Struktur

Jedes JSON-Objekt muss Folgendes enthalten:

* `key` (erforderlich): Die eindeutige Kennung für den Klassifizierungsdatensatz
* `data` (für Aktualisierungen erforderlich): Ein Objekt, das Klassifizierungsspaltennamen und deren Werte enthält
* `action` (optional): Die auszuführende Aktion. Folgende Werte werden unterstützt:
   * `update` (Standard)
   * `delete-field`
   * `delete-key`
* `enc` (optional): Datenkodierungsspezifikation. Folgende Werte werden unterstützt:
   * `utf8` oder `UTF8` (Standard)
   * `latin1` oder `LATIN1`

Bei allen JSON-Feldnamen (`key`, `data`, `action`, `enc`) wird zwischen Groß- und Kleinschreibung unterschieden.

### JSON-Beispiele

**Einfache Update-Aufzeichnung:**

```json
{"key": "product123", "data": {"Product Name": "Basketball Shoes", "Brand": "Brand A", "Category": "Sports"}}
```

**Mit angegebener Kodierung aktualisieren:**

```json
{"key": "product456", "enc": "utf8", "data": {"Product Name": "Running Shoes", "Brand": "Brand B"}}
```

**Bestimmte Felder löschen:**

```json
{"key": "product789", "action": "delete-field", "data": {"Brand": null, "Category": null}}
```

**Gesamten Schlüssel löschen:**

```json
{"key": "product999", "action": "delete-key"}
```

### JSON-Validierungsregeln

* Das `key` ist ein Pflichtfeld und darf weder null noch leer sein.
* Für `update` Aktionen ist das `data` erforderlich und darf nicht leer sein.
* Für `delete-field` Aktionen muss das Feld `data` die zu löschenden Felder enthalten.
* Für `delete-key` Aktionen darf das Feld `data` nicht vorhanden sein.
* Bei den unterstützten Kodierungswerten wird nicht zwischen Groß- und Kleinschreibung unterschieden und es werden standardmäßige Zeichensatznamen einbezogen.

+++

+++**Details zum CSV-Format**

CSV-Dateien (kommagetrennte Werte) verwenden Kommas, um Klassifizierungsdatenfelder zu trennen.

### CSV-Struktur

* **Kopfzeile**: Die erste Zeile muss Spaltenüberschriften enthalten, und die erste Spalte muss die Schlüsselspalte sein. Die nachfolgenden Spalten sollten mit den Namen Ihres Klassifizierungssatz-Schemas übereinstimmen.
* **Datenzeilen**: Jede nachfolgende Zeile enthält Klassifizierungsdaten
* **Trennzeichen**: Felder werden durch Kommas getrennt
* **Anführungszeichen**: Felder mit Kommas, Anführungszeichen oder Zeilenumbrüchen sollten in doppelte Anführungszeichen gesetzt werden

### CSV-Beispiele

**Grundlegende Klassifizierungsdaten:**

```csv
Key,Product Name,Brand,Category,Price
product123,"Basketball Shoes",Brand A,Sports,89.99
product456,"Running Shoes",Brand B,Sports,79.99
product789,"Winter Jacket",Brand C,Clothing,149.99
```

**Gesamten Schlüssel löschen:**

```csv
Key,Product Name,Brand,Category,Price
product999,~deletekey~,,,
```

**Bestimmte Felder löschen (mit Aktualisierungen gemischt):**

```csv
Key,Product Name,Brand,Category,Price
product123,"Updated Product Name",Brand A,Sports,89.99
product456,,~empty~,~empty~,79.99
```

### CSV-Formatierungsregeln

* Felder mit Kommas müssen in doppelte Anführungszeichen gesetzt werden
* Felder, die doppelte Anführungszeichen enthalten, müssen Anführungszeichen umgehen, indem sie sie verdoppeln (`""`)
* Leere Felder stellen Null-Werte für diese Klassifizierung dar
* Führende und nachfolgende Leerzeichen um Felder werden automatisch abgeschnitten
* Sonderzeichen (Tabulatoren, Zeilenumbrüche) in Anführungszeichen werden beibehalten

**Löschvorgänge:**
* Verwenden Sie `~deletekey~` in einem beliebigen Feld, um den gesamten Schlüssel und alle zugehörigen Klassifizierungsdaten zu löschen
* Verwenden Sie `~empty~` in bestimmten Feldern, um nur diese Classification-Werte zu löschen (andere Felder bleiben intakt)
* Bei Verwendung von `~empty~` können Sie Löschungen mit Aktualisierungen in derselben Datei kombinieren

+++

+++**Details zum TSV/TAB-Format**

TSV- (Tabulatorgetrennte Werte) und TAB-Dateien verwenden Tabulatorzeichen, um Klassifizierungsdatenfelder zu trennen.

### TSV/TAB-Struktur

* **Kopfzeile**: Die erste Zeile muss Spaltenüberschriften enthalten, und die erste Spalte muss die Schlüsselspalte sein. Die nachfolgenden Spalten sollten mit den Namen Ihres Klassifizierungssatz-Schemas übereinstimmen.
* **Datenzeilen**: Jede nachfolgende Zeile enthält Klassifizierungsdaten
* **Trennzeichen**: Felder werden durch Tabulatorzeichen getrennt (`\t`)
* **Anführungszeichen**: Im Allgemeinen ist keine Anführungszeichen erforderlich, aber einige Implementierungen unterstützen zitierte Felder

### TSV/TAB-Beispiele

**Grundlegende Klassifizierungsdaten:**

```tsv
Key    Product Name    Brand    Category    Price
product123    Basketball Shoes    Brand A    Sports    89.99
product456    Running Shoes    Brand B    Sports    79.99
product789    Winter Jacket    Brand C    Clothing    149.99
```

**Gesamten Schlüssel löschen:**

```tsv
Key    Product Name    Brand    Category    Price
product999    ~deletekey~            
```

**Bestimmte Felder löschen (mit Aktualisierungen gemischt):**

```tsv
Key    Product Name    Brand    Category    Price
product123    Updated Product Name    Brand A    Sports    89.99
product456        ~empty~    ~empty~    79.99
```

### TSV/TAB-Formatierungsregeln

* Felder werden durch einzelne Tabulatorzeichen getrennt
* Leere Felder (aufeinander folgende Registerkarten) stellen Null-Werte dar
* Normalerweise ist kein spezielles Angebot erforderlich
* Leerzeichen am Anfang und Ende bleiben erhalten
* Zeilenumbrüche innerhalb von Feldern sollten vermieden werden

**Löschvorgänge:**
* Verwenden Sie `~deletekey~` in einem beliebigen Feld, um den gesamten Schlüssel und alle zugehörigen Klassifizierungsdaten zu löschen
* Verwenden Sie `~empty~` in bestimmten Feldern, um nur diese Classification-Werte zu löschen (andere Felder bleiben intakt)
* Bei Verwendung von `~empty~` können Sie Löschungen mit Aktualisierungen in derselben Datei kombinieren

+++

## Umgang mit Fehlern

Häufige Upload-Probleme und -Lösungen:

### Allgemeine Dateiformatfehler

* **Ungültiges Dateiformat**: Stellen Sie sicher, dass Ihre Dateierweiterung dem Inhaltsformat (.json, .csv, .tsv oder .tab) entspricht.
* **„Unbekannter Header“**: Spaltennamen müssen mit Ihrem Klassifizierungssatz-Schema übereinstimmen (gilt für alle Formate).

### CSV-/TSV-spezifische Fehler

* **„Die erste Spalte muss der Schlüssel sein“**: Stellen Sie sicher, dass Ihre CSV-/TSV-Datei über eine geeignete Kopfzeile mit der ersten Schlüsselspalte verfügt.
* **„Mindestens zwei Kopfzeilenelemente sind erforderlich“**: CSV-/TSV-Dateien müssen mindestens eine Spalte „Schlüssel“ und eine Classification-Spalte aufweisen.
* **„Die erste Kopfzeilenspalte muss &#39;Schlüssel&#39; heißen“**: Die erste Spaltenüberschrift muss genau &#39;Schlüssel&#39; sein (Groß-/Kleinschreibung beachten).
* **„Leere Kopfzeilen sind nicht zulässig“**: Alle CSV/TSV-Spaltenüberschriften müssen Namen haben.
* **„Die Anzahl der Spalten stimmte nicht mit den Kopfzeilen überein“**: Jede CSV-/TSV-Datenzeile muss dieselbe Anzahl von Feldern enthalten wie die Kopfzeile.
* **„Fehlerhaftes Dokument“**: CSV-Anführungszeichen überprüfen, ordnungsgemäße Tab-Trennung in TSV-Dateien usw.

### JSON-spezifische Fehler

* **„Schlüssel ist ein erforderliches Feld“**: Alle JSON-Datensätze müssen über ein nicht leeres `"key"`-Feld verfügen (Groß-/Kleinschreibung beachten).
* **„Daten sind ein erforderliches Feld bei Verwendung von action=update“**: JSON-Aktualisierungsaktionen müssen ein `"data"` Feld enthalten.
* **„Daten sind ein erforderliches Feld bei Verwendung von action=delete-field“**: JSON-Löschfeld-Aktionen müssen angeben, welche Felder im `"data"` Feld gelöscht werden sollen.
* **„Bei Verwendung von action=delete-key dürfen keine Daten vorhanden sein“**: Aktionen mit JSON-Löschschlüsseln können kein `"data"` enthalten.
* **„Nicht unterstützte Kodierung“**: Verwenden Sie nur unterstützte Kodierungswerte im `"enc"` (utf8, UTF8, latin1, LATIN1).
* **Ungültige JSON-Syntax**: Stellen Sie sicher, dass die JSON-Datei gemäß den JSONL-Konventionen korrekt formatiert ist. Überprüfen Sie auch auf allgemeine JSON-Formatierung, fehlende Anführungszeichen, Kommas, Klammern usw.

### Fehler bei der Größenbeschränkung

* **„Key exceeded maximum size“**: Einzelne Schlüssel dürfen 255 Byte nicht überschreiten.
* **„Spaltenwert überschreitet die maximale Größe“**: Einzelne Classification-Werte dürfen 255 Byte nicht überschreiten.

## Best Practices

* **Dateigröße**: 50 MB ist die maximale Dateigröße für Browser- und API-Uploads.
* **Batch-Verarbeitung**: Bei großen Datensätzen sollten Sie die Aufteilung in kleinere Dateien erwägen.
* **Datenvalidierung**: Testen Sie mit einer kleinen Beispieldatei, bevor Sie große Datensätze hochladen.
* **Backup**: Kopien der Quelldatendateien beibehalten.
* **Inkrementelle Aktualisierungen**: Verwenden Sie das JSON-Format, um die Aktualisierung und Löschung einzelner Datensätze präzise steuern zu können.
