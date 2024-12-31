---
title: Komponentenunterstützung in Data Warehouse
description: Erfahren Sie, welche zusätzlichen Dimensionen und Metriken in Data Warehouse verfügbar sind und was nicht unterstützt wird.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
source-git-commit: d929e97a9d9623a8255f16729177d812d59cec05
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 60%

---

# Unterstützung von Komponenten in Data Warehouse

Die eindeutige Verarbeitung in der Data Warehouse-Architektur ermöglicht einige Komponenten, die normalerweise nicht in anderen Funktionen von Adobe Analytics verfügbar sind. Aufgrund seiner speziellen Architektur stehen einige Komponenten weder für Berichte noch für Segmente zur Verfügung. Auf dieser Seite erfahren Sie, welche Komponenten verwendet werden können und welche nicht.

## Komponenten, die speziell in Data Warehouse verwendet werden

Einige Dimensionen und Metriken, die beim Data Warehouse verwendet werden können, sind nicht verfügbar, wenn andere Funktionen in Adobe Analytics verwendet werden.

### Ausschließlich unterstützte Dimensionen

* **Experience Cloud-ID**: Bei Implementierungen, die den Experience Cloud-ID-Dienst (ECID) verwenden, eine 128-Bit-Zahl, die aus zwei verketteten 64-Bit-Zahlen besteht, die auf 19 Stellen aufgefüllt sind.
* **Seiten-URL**: Die Seiten-URL, auf der der Treffer aufgetreten ist.
* **Kauf-IDs**: Eindeutige Kennung für einen Kauf, die mithilfe der purchaseID-Variablen festgelegt wird.
* **Besucher-ID**: Stellt die eindeutige Kennung für den Besucher bereit. Dieser Wert entspricht dem konkatenierten Wert der Spalten `visid_high` und `visid_low` in Daten-Feeds. Weitere Informationen finden Sie unter in der [Datenspaltenreferenz](../analytics-data-feed/c-df-contents/datafeeds-reference.md) unter Daten-Feeds.

### Ausschließlich unterstützte Metriken

* **Besuche**: Diese Metrik im Kontext des Data Warehouse schließt nicht beständige Cookie-Besuche aus.
* **Besuche - Alle Besucher**: Diese Metrik im Kontext von Data Warehouse entspricht eher der Metrik Besuche in anderen Tools in Adobe Analytics.

## Nicht in Data Warehouse unterstützte Komponenten

Einige Dimensionen und Metriken werden in Data Warehouse nicht unterstützt.

>[!NOTE]
>
>Wenn eine Dimension oder Metrik in Data Warehouse nicht unterstützt wird, werden Segmente, die diese Komponenten verwenden, auch nicht unterstützt. Überprüfen Sie beim Erstellen oder Bearbeiten eines Segments immer die Produktkompatibilität.

### Nicht unterstützte Dimensionen

* Vormittag/Nachmittag
* Einige pfadbasierte Dimensionen, darunter:
   * Alle Entry-Dimensionen, außer Entrypage
   * Alle Exit-Dimensionen, außer Exitpage und Exitlink
   * Treffertiefe
   * Rückkehrhäufigkeit
   * Zeit vor Ereignis
   * Besuchszeit pro Seite – zusammengefasst
   * Zeit pro Besuch – zusammengefasst
* Rangansicht aller Suchseiten
* Hierarchievariablen
* Treffertyp
* Nicht gefundene Seiten (als Dimension verfügbar; nicht unterstützt für Segmentierung)
* Paid Search
* Einzelseitenbesuche
* Nachverfolgen des Abmeldegrunds
* US-Staaten

### Nicht unterstützte Metriken

* Einige pfadbasierte Metriken, darunter:
   * Absprünge
   * Einstiege
   * Ausstiege
   * Neuladungen
   * Einzelzugriff
   * Besuchszeit-Metriken
* Teilnahmemetriken (wie unter [Erstellen einer Metrik „Teilnahme“ beschrieben](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/participation-metric.md))

### Auf andere Weise unterstützte Dimensionen

Die folgenden zeitbasierten Dimensionen werden unterstützt. Bei der Verwendung dieser Dimensionen ist die Ausgabe von Datumsangaben jedoch nicht standardmäßig. Konkret wird das Jahr um 1900 ausgeglichen, und die Monate basieren auf Null.

* Jahr
* Quartal
* Monat
* Woche
* Tag
* Stunde
* Minute

## Segmente als Dimensionen im Data Warehouse

Wenn Sie ein Segment als Dimension in Data Warehouse verwenden, gibt der Bericht eine Spalte zurück, die `"0"` oder `"1"` enthält:

* **`"0"`**: Das Dimensionselement entsprach nicht den Kriterien des Segments.
* **`"1"`**: Das Dimensionselement entsprach den Kriterien des Segments.
