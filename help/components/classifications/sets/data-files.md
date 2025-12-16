---
description: Machen Sie sich mit den verschiedenen Dateiformaten vertraut, die Klassifizierungssätze unterstützen
title: Dateiformate für Klassifizierungssätze
feature: Classifications
exl-id: f3d429be-99d5-449e-952e-56043b109411
source-git-commit: 0f80bb314c8e041a98af26734d56ab364c23a49b
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 1%

---

# Dateiformate für Klassifizierungssätze

Klassifizierungssätze unterstützen verschiedene Dateiformate zum Hochladen von Klassifizierungsdaten. Für jedes Format gelten spezifische Anforderungen für erfolgreiche Daten-Uploads.

Sobald Ihre Datei entsprechend diesen Spezifikationen formatiert ist, können Sie die Daten über die Oberfläche der Klassifizierungssätze oder die -API hochladen. Detaillierte Upload-Anweisungen finden Sie unter:

* **Browser-Upload**: Siehe [Hochladen](manage/schema.md#upload) in der [Schema](manage/schema.md)-Oberfläche für einen Klassifizierungssatz.
* **API-Upload**: Siehe die [Analytics Classifications-API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/)

Klassifizierungssätze unterstützen die folgenden Dateiformate:

* **JSON**: JavaScript Object Notation-Dateien mit strukturierten Daten
* **CSV**: Dateien mit kommagetrennten Werten
* **TSV oder TAB**: Dateien mit tabulatorgetrennten Werten

## Allgemeine Dateianforderungen

Alle Dateiformate müssen die folgenden Anforderungen erfüllen:

* **Dateicodierung**: Verwenden Sie UTF-8 ohne Bytereihenfolgen-Markierungen. Die Latin1-Kodierung wird ebenfalls unterstützt.
* **Zeichenbeschränkungen**: Einzelne Classification-Werte haben eine Obergrenze von 255 Byte.
* **Schlüsselanforderungen**: Schlüsselwerte dürfen nicht leer sein oder nur Leerzeichen enthalten. Wenn doppelte Schlüssel vorhanden sind, wird das letzte Vorkommen verwendet.

+++ Details zum JSON-Format

Das JSON-Dateiformat folgt den Konventionen für JSON-Zeilen (JSON). Die Datei muss ein JSON-Objekt pro Zeile enthalten, wobei jedes Objekt einen einzelnen Klassifizierungseintrag darstellt.

>[!NOTE]
>
>Verwenden Sie trotz Befolgung der Konventionen für JSON-Zeilen die Dateierweiterung `.json` für alle Uploads. Die Verwendung der `.jsonl`-Erweiterung kann zu Fehlern führen.

### JSON-Struktur

Jedes JSON-Objekt muss Folgendes enthalten:

* `key` (erforderlich): Die eindeutige Kennung für den Klassifizierungsdatensatz
* `data` (für Aktualisierungen erforderlich): Ein Objekt, das Klassifizierungsspaltennamen und deren Werte enthält
* `action` (optional): Die auszuführende Aktion. Folgende Werte werden unterstützt:
   * `update` (die Standardaktion, wenn keine Aktion angegeben ist)
   * `delete-field`
   * `delete-key`
* `enc` (optional): Datenkodierungsspezifikation. Folgende Werte werden unterstützt:
   * `utf8` oder `UTF8` (Standard)
   * `latin1` oder `LATIN1`

Bei allen JSON-Feldnamen (`key`, `data`, `action`, `enc`) wird zwischen Groß- und Kleinschreibung unterschieden.

### JSON-Validierungsregeln

* Das `key` ist ein Pflichtfeld und darf weder null noch leer sein.
* Für `update` Aktionen ist das `data` erforderlich und darf nicht leer sein.
* Für `delete-field` Aktionen muss das Feld `data` die zu löschenden Felder enthalten.
* Für `delete-key` Aktionen darf das Feld `data` nicht vorhanden sein.
* Bei den unterstützten Kodierungswerten wird nicht zwischen Groß- und Kleinschreibung unterschieden und es werden standardmäßige Zeichensatznamen einbezogen.

### JSON-Beispiele

Beispiele für JSON-Einträge in einer JSON-Datei

#### Einfache Aktualisierung des Datensatzes

```json
{"key": "product123", "data": {"Product Name": "Basketball Shoes", "Brand": "Brand A", "Category": "Sports"}}
```

#### Mit angegebener Kodierung aktualisieren

```json
{"key": "product456", "enc": "utf8", "data": {"Product Name": "Running Shoes", "Brand": "Brand B"}}
```

#### Bestimmte Felder löschen

```json
{"key": "product789", "action": "delete-field", "data": {"Brand": null, "Category": null}}
```

#### Gesamten Schlüssel löschen

```json
{"key": "product999", "action": "delete-key"}
```


+++

+++ CSV-Formatdetails

CSV-Dateien (kommagetrennte Werte) verwenden Kommas, um Klassifizierungsdatenfelder zu trennen.

### CSV-Struktur

* **Kopfzeile**: Die erste Zeile muss Spaltenüberschriften enthalten, und die erste Spalte muss die Schlüsselspalte sein. Die nachfolgenden Spalten sollten mit den Namen Ihres Klassifizierungssatz-Schemas übereinstimmen.
* **Datenzeilen**: Jede nachfolgende Zeile enthält Klassifizierungsdaten
* **Trennzeichen**: Felder werden durch Kommas getrennt
* **Anführungszeichen**: Felder mit Kommas, Anführungszeichen oder Zeilenumbrüchen sollten in doppelte Anführungszeichen gesetzt werden

### CSV-Formatierungsregeln

* Felder, die Kommas enthalten, müssen in doppelte Anführungszeichen gesetzt werden.
* Felder, die doppelte Anführungszeichen enthalten, müssen die Anführungszeichen durch Verdoppelung umgehen (`""`).
* Leere Felder stellen Null-Werte für diese Klassifizierung dar.
* Führende und nachfolgende Leerzeichen um Felder werden automatisch abgeschnitten.
* Sonderzeichen (Tabulatoren, Zeilenumbrüche) in Anführungszeichen werden beibehalten.

### CSV-Löschvorgänge

* Verwenden Sie `~deletekey~` in einem beliebigen Feld, um den gesamten Schlüssel und alle zugehörigen Klassifizierungsdaten zu löschen
* Verwenden Sie `~empty~` in bestimmten Feldern, um nur diese Classification-Werte zu löschen (andere Felder bleiben intakt)
* Bei Verwendung von `~empty~` können Sie Löschungen mit Aktualisierungen in derselben Datei kombinieren

### CSV-Beispiele

Beispiele für CSV-Einträge in einer CSV-Datei

#### Grundlegende Klassifizierungsdaten

```csv
Key,Product Name,Brand,Category,Price
product123,"Basketball Shoes",Brand A,Sports,89.99
product456,"Running Shoes",Brand B,Sports,79.99
product789,"Winter Jacket",Brand C,Clothing,149.99
```

#### Gesamten Schlüssel löschen

```csv
Key,Product Name,Brand,Category,Price
product999,~deletekey~,,,
```

#### Bestimmte Felder löschen (mit Aktualisierungen gemischt)

```csv
Key,Product Name,Brand,Category,Price
product123,"Updated Product Name",Brand A,Sports,89.99
product456,,~empty~,~empty~,79.99
```

+++

+++ Details zum TSV- und TAB-Format

TSV- (Tabulatorgetrennte Werte) und TAB-Dateien verwenden Tabulatorzeichen, um Klassifizierungsdatenfelder zu trennen.

### TSV- und TAB-Struktur

* **Kopfzeile**: Die erste Zeile muss Spaltenüberschriften enthalten, und die erste Spalte muss die Schlüsselspalte sein. Die nachfolgenden Spalten sollten mit den Namen Ihres Klassifizierungssatz-Schemas übereinstimmen.
* **Datenzeilen**: Jede nachfolgende Zeile enthält Klassifizierungsdaten.
* **Trennzeichen**: Felder werden durch Tabulatorzeichen (`\t`) getrennt.
* **Anführungszeichen**: Im Allgemeinen ist keine Anführungszeichen erforderlich, aber einige Implementierungen unterstützen zitierte Felder.

### TSV- und TAB-Formatierungsregeln

* Felder werden durch einzelne Tabulatorzeichen getrennt.
* Leere Felder (aufeinander folgende Registerkarten) stellen Null-Werte dar.
* Normalerweise ist kein spezielles Angebot erforderlich.
* Leerzeichen am Anfang und Ende bleiben erhalten.
* Zeilenumbrüche innerhalb von Feldern sollten vermieden werden.

### TSV- und TAB-Löschvorgänge

* Verwenden Sie `~deletekey~` in einem beliebigen Feld, um den gesamten Schlüssel und alle zugehörigen Klassifizierungsdaten zu löschen.
* Verwenden Sie `~empty~` in bestimmten Feldern, um nur diese Classification-Werte zu löschen (andere Felder bleiben intakt).
* Bei Verwendung von `~empty~` können Sie Löschungen mit Aktualisierungen in derselben Datei mischen.

### TSV- und TAB-Beispiele

Beispiele für TSV- oder TAB-getrennte Datensätze in einer TSV- oder TAB-Datei.

#### Grundlegende Klassifizierungsdaten

```tsv
Key    Product Name    Brand    Category    Price
product123    Basketball Shoes    Brand A    Sports    89.99
product456    Running Shoes    Brand B    Sports    79.99
product789    Winter Jacket    Brand C    Clothing    149.99
```

#### Gesamten Schlüssel löschen

```tsv
Key    Product Name    Brand    Category    Price
product999    ~deletekey~            
```

#### Bestimmte Felder löschen (mit Aktualisierungen gemischt)

```tsv
Key    Product Name    Brand    Category    Price
product123    Updated Product Name    Brand A    Sports    89.99
product456        ~empty~    ~empty~    79.99
```

+++

## Umgang mit Fehlern

Häufige Probleme und Lösungen beim Hochladen von Dateien:

### Allgemeine Dateiformatfehler

* **Ungültiges Dateiformat**: Stellen Sie sicher, dass Ihre Dateierweiterung dem Inhaltsformat (`.json`, `.csv`, `.tsv` oder `.tab`) entspricht.
* **Unbekannter Header**: Spaltennamen müssen mit Ihrem Klassifizierungssatz-Schema übereinstimmen (gilt für alle Formate).

### JSON-spezifische Fehler

* **Schlüssel ist ein erforderliches Feld**: Alle JSON-Datensätze müssen über ein nicht leeres `"key"`-Feld verfügen (bei Kleinbuchstaben wird zwischen Groß- und Kleinschreibung unterschieden).
* **Daten sind ein erforderliches Feld bei Verwendung von action=update**: JSON-Aktualisierungsaktionen müssen ein `"data"` Feld enthalten.
* **Daten sind ein erforderliches Feld bei Verwendung von action=delete-field**: Bei JSON-Löschfeldaktionen muss angegeben werden, welche Felder im `"data"` Feld gelöscht werden sollen.
* **Bei Verwendung von action=delete-key dürfen keine Daten vorhanden sein** JSON-Löschschlüsselaktionen können kein `"data"`-Feld enthalten.
* **Nicht unterstützte Kodierung**: Verwenden Sie nur unterstützte Kodierungswerte im `"enc"` (`utf8`, `UTF8`, `latin1`, `LATIN1`).
* **Ungültige JSON-Syntax**: Stellen Sie sicher, dass die JSON-Datei gemäß den JSONL-Konventionen korrekt formatiert ist. Überprüfen Sie auch auf allgemeine JSON-Formatierung, fehlende Anführungszeichen, Kommas, Klammern usw.


### CSV- und TSV-spezifische Fehler

* **Die erste Spalte muss der Schlüssel sein**: Stellen Sie sicher, dass Ihre CSV- oder TSV-Datei über eine geeignete Kopfzeile mit der ersten Schlüsselspalte verfügt.
* **Mindestens zwei Kopfzeilenelemente sind erforderlich**: CSV- oder TSV-Dateien müssen mindestens eine `Key` und eine Classification-Spalte aufweisen.
* **Die erste Kopfzeilenspalte muss „Schlüssel“ heißen** Die erste Spaltenüberschrift muss genau `Key` sein (`K`, Groß-/Kleinschreibung beachten).
* **Leere Kopfzeilen sind nicht zulässig**: Alle CSV/TSV-Spaltenkopfzeilen müssen Namen haben.
* **Die Anzahl der Spalten stimmte nicht mit den Kopfzeilen überein**: Jede CSV- oder TSV-Datenzeile muss dieselbe Anzahl von Feldern enthalten wie die Kopfzeile.
* **Falsch formatiertes Dokument**: Überprüfen Sie CSV-Anführungszeichen, ordnungsgemäße Tab-Trennung in TSV-Dateien und mehr.


### Fehler bei der Größenbeschränkung

* **Schlüssel überschreitet die maximale**: Einzelne Schlüssel dürfen 255 Byte nicht überschreiten.
* **Spaltenwert überschreitet die maximale Größe**: Einzelne Classification-Werte dürfen 255 Byte nicht überschreiten.

## Best Practices

* **Dateigröße**: 50 MB ist die maximale Dateigröße für Browser- und API-Uploads.
* **Batch-Verarbeitung**: Bei großen Datensätzen sollten Sie die Aufteilung in kleinere Dateien erwägen.
* **Datenvalidierung**: Testen Sie mit einer kleinen Beispieldatei, bevor Sie große Datensätze hochladen.
* **Backup**: Kopien der Quelldatendateien beibehalten.
* **Inkrementelle Aktualisierungen**: Verwenden Sie das JSON-Format, um die Aktualisierung und Löschung einzelner Datensätze präzise steuern zu können.
