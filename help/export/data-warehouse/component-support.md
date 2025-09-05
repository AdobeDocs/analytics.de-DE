---
title: Komponentenunterstützung in Data Warehouse
description: Erfahren Sie, welche zusätzlichen Dimensionen und Metriken in Data Warehouse verfügbar sind und was nicht unterstützt wird.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
source-git-commit: 665319bdfc4c1599292c2e7aea45622d77a291a7
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 45%

---

# Unterstützung von Komponenten in Data Warehouse

Die eindeutige Verarbeitung in der Data Warehouse-Architektur ermöglicht einige Komponenten, die normalerweise nicht in anderen Funktionen von Adobe Analytics verfügbar sind. Aufgrund seiner speziellen Architektur stehen einige Komponenten weder für Berichte noch für Segmente zur Verfügung. Auf dieser Seite erfahren Sie, welche Komponenten verwendet werden können und welche nicht.

## Komponenten, die speziell in Data Warehouse verwendet werden

Einige Dimensionen und Metriken, die in Data Warehouse verwendet werden können, sind nicht verfügbar, wenn andere Funktionen in Adobe Analytics verwendet werden.

### Ausschließlich unterstützte Dimensionen

* **Experience Cloud ID**: Für Implementierungen, die den Experience Cloud ID Service (ECID) verwenden, eine 128-Bit-Zahl, die aus zwei verketteten 64-Bit-Zahlen besteht, die auf 19 Stellen aufgefüllt sind.
* **Seiten-URL**: Die Seiten-URL, auf der der Treffer aufgetreten ist.
* **Kauf-IDs**: Eindeutige Kennung für einen Kauf, die mithilfe der purchaseID-Variablen festgelegt wird.
* **Besucher-ID**: Stellt die eindeutige Kennung für den Besucher bereit. Dieser Wert entspricht dem konkatenierten Wert der Spalten `visid_high` und `visid_low` in Daten-Feeds. Weitere Informationen finden Sie unter in der [Datenspaltenreferenz](../analytics-data-feed/c-df-contents/datafeeds-reference.md) unter Daten-Feeds.

### Ausschließlich unterstützte Metriken

* **Besuche**: Diese Metrik im Kontext von Data Warehouse schließt nicht beständige Cookie-Besuche aus.
* **Besuche - Alle Besucher**: Diese Metrik im Kontext von Data Warehouse ähnelt stärker der Metrik Besuche in anderen Tools in Adobe Analytics.

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
* Teilnahmemetriken (wie unter [Erstellen einer Metrik „Teilnahme“ beschrieben](/help/components/calculated-metrics/workflow/c-build-metrics/participation-metric.md))

### Auf andere Weise unterstützte Dimensionen (nicht standardmäßige Datumsformatierung)

Die folgenden zeitbasierten Dimensionen werden unterstützt:

* Jahr
* Quartal
* Monat
* Woche
* Tag
* Stunde
* Minute

Die Ausgabe von Datumsangaben ist jedoch bei Verwendung dieser Dimensionen nicht standardmäßig.

Beachten Sie bei der Berechnung der Ausgabe von Datumsangaben in Data Warehouse Folgendes:

* Datumsdimensionen werden im folgenden Format angezeigt: `1YYMMDDHHMM`

* Das Jahr (JJ) wird um 1900 versetzt. Dies bedeutet, dass Sie den ersten drei Werten des Datumsfelds `1900` hinzufügen.

  Wenn beispielsweise der Wert des Felds Datumsbereich Woche in Data Warehouse `1250901` ist, würden Sie 1900 bis 125 hinzufügen, was zum Jahr 2025 führt.

* Alle Monate sind nullbasiert, wobei Januar durch 00, Februar durch 01 und so weiter wie folgt dargestellt wird:

   * 00: Januar
   * 01: Februar
   * 02: März
   * 03: April
   * 04: Mai
   * 05: Juni
   * 06: Juli
   * &#x200B;7. August
   * 08: September
   * &#x200B;9. Oktober
   * &#x200B;10. November
   * &#x200B;11. Dezember

  Wenn beispielsweise der Wert des Felds Datumsbereich Woche in Data Warehouse `1250901` ist, wird der Monat als 09 dargestellt, was Oktober bedeutet.




## Segmente als Dimensionen in Data Warehouse

Wenn Sie ein Segment als Dimension in Data Warehouse verwenden, gibt der Bericht eine Spalte zurück, die `"0"` oder `"1"` enthält:

* **`"0"`**: Das Dimensionselement entsprach nicht den Kriterien des Segments.
* **`"1"`**: Das Dimensionselement entsprach den Kriterien des Segments.
