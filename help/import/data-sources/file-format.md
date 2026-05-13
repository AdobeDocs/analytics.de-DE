---
title: Format der Datenquellendatei
description: Richtige Generierung einer Datei zur Verwendung in Datenquellen.
exl-id: 6632b970-e931-4272-a69b-c1130ad6475f
feature: Data Sources
role: Admin
TQID: https://experienceleague.adobe.com/aOyIlKV8OwvmigJ7RFcNQsrsBiHbrC0a-IPN4xR0OZc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 546
ht-degree: 7%

---

# Format der Datenquellendatei

Datenquellendateien haben die folgenden Eigenschaften:

* Die Datei liegt im `.txt`-Format vor.
* Kommentare zu Zeilen beginnen mit &quot;`#`&quot; und sind optional.
* Die erste nicht kommentierte Zeile enthält die Kopfzeilen der Datei.
* Der erste Wert jeder Zeile ist das Datum, das das Format `MM/DD/YYYY` oder `MM/DD/YYYY/HH/mm/SS` verwendet.
* Die Werte in jeder Zeile, einschließlich der Kopfzeilen, werden durch Tabulatoren getrennt.
* Jede Zeile muss mindestens eine Dimension und eine Metrik aufweisen.

## Kommentare

Jede Zeile, die mit &quot;`#`&quot; beginnt, ist ein Kommentar. Beim Herunterladen einer Datenquellenvorlagendatei sind die ersten beiden Zeilen Kommentare.

* Der erste Kommentar gibt den Typ der Vorlage an, die Sie für die Datenquelle konfiguriert haben, die Backend-Benutzer-ID, die die Datenquelle erstellt hat, und die Datenquellen-ID.
* Der zweite Kommentar liefert benutzerfreundliche Namen für jede der Kopfzeilen, die in der Vorlagendatei enthalten sind.

Alle Kommentarzeilen werden von Adobe bei der Verarbeitung der Datei ignoriert, sodass Sie die Vorlagenkommentare entfernen oder eigene in der gesamten Datei hinzufügen können. Es können nur vollständige Zeilen kommentiert werden. Einzelne Felder oder Teilzeilen können nicht auskommentiert werden.

## Kopfzeilen

Beim Hochladen von Datenquellendateien sind Spaltenüberschriften erforderlich. Bei diesen Spaltenüberschriften wird nicht zwischen Groß- und Kleinschreibung unterschieden, aber erforderliche Leerzeichen sind erforderlich (z. B. ist `eVar1` eine ungültige Kopfzeile, während `EVAR 1` gültig ist). Spaltenüberschriften gelten für alle Report Suites. Verwenden Sie die folgenden Tabellen, um sicherzustellen, dass jede Kopfzeile in Ihrer Datenquellendatei korrekt festgelegt ist.

>[!TIP]
>
>Sie können eine Datenquellendatei von Grund auf neu erstellen, wenn Sie die richtigen Kopfzeilen in Ihre Datenquellendatei einschließen. Die Anzahl der Kopfzeilen, die Sie in eine einzelne Datei aufnehmen können, ist unbegrenzt. Jede Zeile darf jedoch nur maximal 4.096 Byte enthalten.

| Dimension | Datenquellen-Header |
| --- | --- |
| [Kategorie](/help/components/dimensions/category.md) | `Category` |
| [eVar1 - eVar250](/help/components/dimensions/evar.md) | `Evar 1` - `Evar 250` |
| [Marketing-](/help/components/dimensions/marketing-channel.md) | `Marketing Channel` |
| [Details zum Marketing-Kanal](/help/components/dimensions/marketing-detail.md) | `Marketing Channel Detail` |
| [Produkt](/help/components/dimensions/product.md) | `Product` |
| [Trackingcode](/help/components/dimensions/tracking-code.md) | `Tracking Code` |
| [Transaktions-ID](/help/implement/vars/page-vars/transactionid.md) | `transactionID` |
| [Postleitzahl](/help/components/dimensions/zip-code.md) | `Zip` |

{style="table-layout:auto"}

Dimensionen und Metriken werden in dieselbe Kopfzeile eingefügt.

| Metrik | Datenquellen-Header |
| --- | --- |
| [Zusatz zum Warenkorb](/help/components/metrics/cart-additions.md) | `Cart Adds` |
| [Entnahme aus Warenkorb](/help/components/metrics/cart-removals.md) | `Cart Removes` |
| [Warenkorbansichten](/help/components/metrics/cart-views.md) | `Cart Views` |
| [Warenkorb](/help/components/metrics/carts.md) | `Cart Opens` |
| [Checkouts](/help/components/metrics/checkouts.md) | `Checkouts` |
| [Benutzerspezifische Ereignisse](/help/components/metrics/custom-events.md) | `Event 1` - `Event 1000` |
| [Bestellungen](/help/components/metrics/orders.md) | `Orders` |
| [Umsatz](/help/components/metrics/revenue.md) | `Price` |
| [Einheiten](/help/components/metrics/units.md) | `Quantity` |

{style="table-layout:auto"}

Adobe unterstützt keine Datenquellen für andere Dimensionen oder Metriken. Wenn Variablen erforderlich sind, die über die in den obigen Tabellen aufgeführten hinausgehen, sollten Sie stattdessen die [Bulk Data Insertion API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/) verwenden.

## Datum

Der erste Wert in jeder Zeile **muss** das Datum sein. Das Datumsformat muss eines der folgenden Formate aufweisen:

* **`MM/DD/YYYY/HH/mm/SS`**
* **`MM/DD/YYYY`**

Wenn Sie die Stunden/Minuten/Sekunden auslassen, wird der Zeitstempel automatisch auf 12 Uhr für diesen Tag festgelegt.

Eine einzelne Datenquellendatei unterstützt bis zu 90 eindeutige Tage. Wenn Sie mehr als 90 eindeutige Tage in einen Upload einbeziehen möchten, teilen Sie Ihre Daten in mehrere Dateien auf.

## Dimension- und Metrikdaten

Nachfolgende Werte nach dem Datum in jeder Zeile enthalten die Daten, die Sie hochladen möchten. Jede Zeile entspricht diesem entsprechenden Zeitstempel. Stellen Sie sicher, dass in jeder Zeile dieselbe Anzahl von Registerkarten vorhanden ist. Die Spalten können in beliebiger Reihenfolge angeordnet werden. Stellen Sie sicher, dass die Daten in jeder Zeile mit den Kopfzeilen oben ausgerichtet sind. Die maximale Datenmenge, die eine einzelne Zeile haben kann, beträgt 4096 Byte.

Dimension-Daten dürfen keine Semikolons (`;`) enthalten. Zeilen mit Semikolons werden übersprungen.

## Nächste Schritte

[Datei-Upload](file-upload.md): Erfahren Sie, wie Sie eine Datenquellendatei zur Aufnahme durch Adobe hochladen.
