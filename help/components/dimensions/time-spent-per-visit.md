---
title: Besuchszeit pro Besuch (Dimensionen)
description: Die Gesamtdauer des Besuchs.
feature: Dimensions
exl-id: f241eb2d-7e22-47ee-ade8-8aeb7b2b9694
TQID: 'https://experienceleague.adobe.com/jtBAAq-Pe0PyCQJPwvzwnK9eLv14CxTvrVQP4lvWy7k'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 304
ht-degree: 91%

---

# Zeit pro Besuch

*Auf dieser Hilfeseite wird beschrieben, wie die „pro Besuch verbrachte Zeit“ als ihre jeweiligen [Dimensionen“ &#x200B;](overview.md). Weitere Informationen finden Sie unter der Metrik [Zeit pro Besuch](../metrics/time-spent-per-visit.md).*

Die Dimensionen „Zeit pro Besuch“ geben die Zeit an, die ein Besucher für den gesamten Besuch aufgewendet hat. Zur Berechnung werden die folgenden Schritte verwendet:

1. Sehen Sie sich den Zeitstempel des ersten Treffers des Besuchs an.
2. Vergleichen Sie diesen Treffer mit dem Zeitstempel des letzten Treffers des Besuchs.
3. Die Zeit, die zwischen diesen beiden Treffern verstrichen ist, zählt zur Besuchszeit.

Diese Dimensionen sind nützlich, wenn Sie verstehen möchten, wie lange Besucher mit Ihrer Site im Allgemeinen interagieren.

>[!TIP]
>
>Die Besuchszeit erfordert mindestens zwei Treffer bei einem Besuch, um die Zeit zu messen. Besuche, die aus einem einzelnen Treffer bestehen, werden nicht in dieser Dimension angezeigt.

Diese Dimension basiert auf Besuchen, d. h., der Wert gilt für jeden Treffer innerhalb des Besuchs und ändert sich nicht. Vergleichen Sie diese Dimension mit der [Besuchszeit pro Seite](time-spent-on-page.md), die einer trefferbasierten Dimension entspricht.

Diese Dimension bezieht sich auf die Metriken [Durchschnittliche Besuchszeit pro Site](../metrics/average-time-on-site.md) und [Zeit pro Besuch](../metrics/time-spent-per-visit.md).

## Füllen dieser Dimension mit Daten

Diese Dimensionen sind bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktionieren diese Dimensionen.

## Dimensionselemente

Für die Zeit pro Besuch gibt es mehrere Dimensionen:

* **Zeit pro Besuch – zusammengefasst**: Die Zeitdauer wird zusammengefasst. Dimensionselemente reichen von `"Less than 1 minute"` bis `"More than 15 hours"`. Besuche dauern in der Regel nicht länger als 12 Stunden. Besuche können jedoch 12 Stunden überschreiten, wenn Treffer mit Zeitstempel oder Datenquellen verwendet werden.
* **Zeit pro Besuch – präzise**: Jede Anzahl von Sekunden ist ein eindeutiges Dimensionselement. Diese Dimension ist in Data Warehouse nicht verfügbar.

Allgemeine Informationen zur Besuchszeit finden Sie unter [Besuchszeit – Übersicht](../metrics/time-spent.md).
