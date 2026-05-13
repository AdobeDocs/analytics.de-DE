---
title: Hash-Kollisionen
description: Beschreibt, was eine Hash-Kollision ist und wie sie sich manifestieren kann.
feature: Implementation Basics
exl-id: 693d5c03-4afa-4890-be4f-7dc58a1df553
role: Admin, Developer
TQID: https://experienceleague.adobe.com/yjYX-h-8jJA7k-jzRMOJ0l2BxN5-no2kCfySkGYss8w
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 9b4525e014170b72688044a6ead344b1bde8c39b
workflow-type: tm+mt
source-wordcount: 539
ht-degree: 5%

---

# Hash-Kollisionen

Dimensionen in Adobe Analytics erfassen Zeichenfolgenwerte. Manchmal sind diese Zeichenfolgen hunderte von Zeichen lang, während sie andermal kurz sind. Um die Leistung zu verbessern, werden diese Zeichenfolgenwerte nicht direkt in der Berichtszeitverarbeitung verwendet. Stattdessen wird für jeden Wert ein Hash berechnet, wodurch eine Kennung in einheitlicher Größe erzeugt wird. Bei den meisten Feldern wird der Wert vor dem Hashing in Kleinbuchstaben umgewandelt, wodurch die Gesamtzahl der eindeutigen Werte reduziert wird. Alle Berichte werden mit diesen Hash-Werten ausgeführt, was ihre Leistung drastisch steigert.

Adobe Analytics verwaltet für jede Variable eine separate Hash-Tabelle, und jede Tabelle wird monatlich neu erstellt. Innerhalb einer dieser Tabellen können gelegentlich zwei verschiedene Quellwerte denselben Hash erzeugen, der als „Hash *Kollision“ bezeichnet*.

Hash-Kollisionen können sich in Berichten wie folgt manifestieren:

* Wenn Sie einen Bericht im Zeitverlauf anzeigen und einen unerwarteten Anstieg feststellen, ist es möglich, dass mehrere eindeutige Werte für diese Variable denselben Hash verwenden.
* Wenn Sie ein Segment verwenden und einen unerwarteten Wert sehen, ist es möglich, dass das unerwartete Dimensionselement denselben Hash wie ein anderes Dimensionselement verwendet, das Ihrem Segment entspricht.

## Wahrscheinlichkeit einer Hash-Kollision

Adobe Analytics verwendet für die meisten Dimensionen 32-Bit-Hashes, was bedeutet, dass es 2<sup>32 </sup> Hash-Kombinationen gibt (ca. 4,3 Mrd.). Die ungefähre Wahrscheinlichkeit, dass eine Hash-Kollision auftritt, basiert auf der Anzahl der eindeutigen Werte wie folgt. Diese Quoten basieren auf einer einzigen Dimension für einen einzelnen Monat.

| Eindeutige Werte | Quoten |
| --- | --- |
| 1.000 | 0.01% |
| 10.000 | 1% |
| 50.000 | 26% |
| 100.000 | 71% |

Ähnlich wie beim [Geburtstagsparadox](https://en.wikipedia.org/wiki/Birthday_problem) steigt mit zunehmender Anzahl eindeutiger Werte die Wahrscheinlichkeit von Hash-Kollisionen drastisch. Bei 1 Million eindeutigen Werten gibt es wahrscheinlich mindestens 100 Hash-Kollisionen für diese Dimension.

## Hash-Kollisionen minimieren

Hash-Kollisionen können nicht vollständig beseitigt werden, aber ihre Auswirkungen auf Berichte können abgeschwächt werden. Die meisten Hash-Kollisionen treten mit zwei ungewöhnlichen Werten auf, die keine bedeutsame Auswirkung auf Berichte haben. Selbst wenn ein Hash mit einem gemeinsamen und einem ungewöhnlichen Wert kollidiert, ist das Ergebnis vernachlässigbar. In seltenen Fällen, in denen zwei beliebte Werte eine Hash-Kollision erleben, ist es jedoch möglich, die Auswirkungen klar zu sehen. Adobe empfiehlt Folgendes, um die Auswirkungen in Berichten zu reduzieren:

* **Ändern des Datumsbereichs**: Hash-Tabellen ändern sich monatlich. Wenn Sie den Datumsbereich so ändern, dass er sich über einen weiteren Monat erstreckt, kann jeder Wert unterschiedliche Hash-Werte erhalten, die nicht kollidieren. In der Regel ist dies die schnellste Möglichkeit, eine sichtbare Anomalie aus einem bestimmten Bericht zu entfernen.
* **Reduzieren der Anzahl eindeutiger Werte**: Sie können Ihre Implementierung anpassen oder [Verarbeitungsregeln](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md) verwenden, um die Anzahl eindeutiger Werte zu reduzieren, die eine Dimension erfasst. Wenn Ihre Dimension beispielsweise eine URL erfasst, können Sie Abfragezeichenfolgen oder Protokolle entfernen.
* **Verwenden von [Data Warehouse](/help/export/data-warehouse/data-warehouse.md) oder [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md)**: Diese Tools basieren nicht auf Hash-Tabellen.
* **Wechseln zu [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html?lang=de)**: Customer Journey Analytics hat keine Hash-Ebene und [keine Kardinalitätsbeschränkungen für Dimensionen](https://experienceleague.adobe.com/docs/analytics-platform/using/components/dimensions/high-cardinality.html). Erwägen Sie, zu diesem Produkt zu wechseln, wenn Hash-Kollisionen oder [[!UICONTROL Geringer Traffic]](/help/technotes/low-traffic.md) Ihre Berichte häufig beeinträchtigen.

>[!MORELIKETHIS]
>
>* [[!UICONTROL Geringer Traffic]-Wert in Adobe Analytics](/help/technotes/low-traffic.md)
>* [Übersicht über Verarbeitungsregeln](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)

<!-- https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=OmniArch&title=Uniques -->
