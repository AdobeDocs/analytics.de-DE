---
title: Komponentenunterstützung in Data Warehouse
description: Erfahren Sie, welche Dimensionen und Metriken beim Erstellen einer Data Warehouse-Anfrage verfügbar sind, welche nicht verfügbar sind und welche sich anders verhalten.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
TQID: https://experienceleague.adobe.com/NhSEyPN3093B9M0SngJluJdZScI2lXvRyHkXQd8gg-4
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 362
ht-degree: 11%

---

# Unterstützung von Komponenten in Data Warehouse

Auf dieser Seite werden die Dimensionen und Metriken beschrieben, die Sie beim Erstellen einer Data Warehouse-Anfrage verwenden können. Abschnitte enthalten, welche Komponenten verfügbar sind, welche nicht verfügbar sind und welche sich anders verhalten als in anderen Adobe Analytics-Tools.

## Dimensionen exklusiv in Data Warehouse

Die folgenden Dimensionen können in Data Warehouse verwendet werden, sind jedoch nicht in anderen Adobe Analytics-Funktionen verfügbar.

* [[!UICONTROL Experience Cloud-Besucher-ID]](/help/components/dimensions/experience-cloud-visitor-id.md)
* [[!UICONTROL IP-Adresse]](/help/components/dimensions/ip-address.md)
* [[!UICONTROL Seiten-URL]](/help/components/dimensions/page-url.md)
* [[!UICONTROL Kauf-ID]](/help/components/dimensions/purchase-id.md)
* [[!UICONTROL Besucher-ID]](/help/components/dimensions/visitor-id.md)

## Nicht unterstützte Dimensionen

Die folgenden Dimensionen sind in Data Warehouse-Berichten oder -Segmenten nicht verfügbar:

* [[!UICONTROL Vormittag/Nachmittag]](/help/components/dimensions/am-pm.md)
* Alle Dimensionen des Eintrags, mit Ausnahme [[!UICONTROL Einstiegsseite]](/help/components/dimensions/entry-dimensions.md) und [[!UICONTROL Einstiegsseite original]](/help/components/dimensions/entry-dimensions.md), die zulässig sind
* Alle Ausstiegsdimensionen, mit Ausnahme von [[!UICONTROL Ausstiegsseite]](/help/components/dimensions/exit-dimensions.md) und [[!UICONTROL Ausstiegs-Link]](/help/components/dimensions/exit-link.md), die zulässig sind
* [[!UICONTROL Treffertiefe]](/help/components/dimensions/hit-depth.md)
* [[!UICONTROL Rückkehrhäufigkeit]](/help/components/dimensions/return-frequency.md)
* [[!UICONTROL Zeit vor Ereignis]](/help/components/dimensions/time-prior-to-event.md)
* [[!UICONTROL Besuchszeit pro Seite - Behälter]](/help/components/dimensions/time-spent-on-page.md)
* [[!UICONTROL Besuchszeit pro Besuch - in Buckets]](/help/components/dimensions/time-spent-per-visit.md)
* [[!UICONTROL Ranking aller Suchseiten]](/help/components/dimensions/all-search-page-rank.md)
* [[!UICONTROL Hierarchie]](/help/components/dimensions/overview.md#retired-dimensions) Variablen
* [[!UICONTROL Treffertyp]](/help/components/dimensions/hit-type.md)
* [[!UICONTROL Paid Search]](/help/components/dimensions/paid-search.md)
* [[!UICONTROL Einzelseitenbesuche]](/help/components/dimensions/single-page-visits.md)
* [[!UICONTROL Tracking des Abmeldegrundes]](/help/components/dimensions/tracking-opt-out-reason.md)
* [[!UICONTROL US-Bundesstaaten]](/help/components/dimensions/us-states.md)

Einige Dimensionen sind in einer Data Warehouse-Anfrage verfügbar, können jedoch nicht innerhalb eines Segments verwendet werden. Weitere Informationen finden Sie unter {](segment-compatibility.md)}Segmentkompatibilität mit Data Warehouse .[

## Dimensionen mit nicht standardmäßiger Datumsformatierung

Die folgenden zeitbasierten Dimensionen werden in Data Warehouse-Berichten unterstützt, ihre Ausgabe verwendet jedoch ein nicht standardmäßiges Format:

* [[!UICONTROL Jahr]](/help/components/dimensions/year.md)
* [[!UICONTROL Quartal]](/help/components/dimensions/quarter.md)
* [[!UICONTROL Monat]](/help/components/dimensions/month.md)
* [[!UICONTROL Woche]](/help/components/dimensions/week.md)
* [[!UICONTROL Tag]](/help/components/dimensions/day.md)
* [[!UICONTROL Stunde]](/help/components/dimensions/hour.md)
* [[!UICONTROL Minute]](/help/components/dimensions/minute.md)

Datumswerte werden im `1YYMMDDHHMM` Format ausgegeben:

* **Jahr (JJ)**: Versatz um 1900. Die ersten drei Ziffern um `1900`. Beispiel: `125` = Jahr **2025**.
* **Monat**: Null-basiert. Januar = `00`, Februar = `01`, …, Dezember = `11`.

Wenn beispielsweise im Feld Datumsbereich Woche der Wert `1260901` angezeigt wird, lautet das Jahr 1900 + 126 = **2026** und der Monat ist 09 = **Oktober**.

## In Data Warehouse anders definierte Metriken

* **[[!UICONTROL Besuche]](/help/components/metrics/visits.md)**: Schließt nicht persistente Cookie-Besuche aus, im Gegensatz zur Besuchsmetrik in anderen Adobe Analytics-Tools.
* **[[!UICONTROL Besuche - Alle Besucher]](/help/components/metrics/visits.md)**: Zählt alle Besucher, einschließlich der Besucher mit nicht beständigen Cookies, wodurch es näher an die Standardmetrik [!UICONTROL Besuche] herankommt, die an anderer Stelle in Adobe Analytics verwendet wird.

## Nicht unterstützte Metriken

Die folgenden Metriken sind in Data Warehouse nicht verfügbar:

* [[!UICONTROL Bounces]](/help/components/metrics/bounces.md)
* [[!UICONTROL Einträge]](/help/components/metrics/entries.md)
* [[!UICONTROL Ausstiege]](/help/components/metrics/exits.md)
* [[!UICONTROL Neuladungen]](/help/components/metrics/reloads.md)
* [[!UICONTROL Einzelzugriff]](/help/components/metrics/single-access.md)
* Beliebige [[!UICONTROL Besuchszeit]](/help/components/metrics/time-spent.md) Metriken
* Beliebige Metriken, die ein Attributionsmodell [Teilnahme](/help/components/calculated-metrics/workflow/c-build-metrics/participation-metric.md) verwenden
