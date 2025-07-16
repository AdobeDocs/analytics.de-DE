---
title: Hash-Kollisionen
description: Beschreibt, was eine Hash-Kollision ist und wie sie sich manifestieren kann.
feature: Implementation Basics
exl-id: 693d5c03-4afa-4890-be4f-7dc58a1df553
role: Admin, Developer
source-git-commit: c2adf6d2e328378332cc290ba2dfd75ee6587ef6
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 6%

---

# Hash-Kollisionen

Dimensionen in Adobe Analytics erfassen Zeichenfolgenwerte. Manchmal sind diese Zeichenfolgen hunderte von Zeichen lang, während sie andermal kurz sind. Um die Leistung zu verbessern, werden diese Zeichenfolgenwerte bei der Verarbeitung nicht direkt verwendet. Stattdessen wird für jeden Wert ein Hash berechnet, um alle Werte in einer einheitlichen Größe zu halten. Alle Berichte werden mit diesen Hash-Werten ausgeführt, wodurch ihre Leistung drastisch gesteigert wird.

Bei den meisten Feldern wird die Zeichenfolge zuerst in Kleinbuchstaben konvertiert. Die Konvertierung in Kleinbuchstaben reduziert die Anzahl der eindeutigen Werte. Werte werden monatlich gehasht - die Groß-/Kleinschreibung für einen bestimmten Wert verwendet den ersten Wert, der jeden Monat angezeigt wird. Von Monat zu Monat gibt es eine geringe Möglichkeit, dass zwei eindeutige Variablenwerte denselben Wert hashen. Dieses Konzept wird als *Hash-Kollision* bezeichnet.

Hash-Kollisionen können sich in Berichten wie folgt manifestieren:

* Wenn Sie einen Bericht im Zeitverlauf anzeigen und einen unerwarteten Anstieg feststellen, ist es möglich, dass mehrere eindeutige Werte für diese Variable denselben Hash verwenden.
* Wenn Sie ein Segment verwenden und einen unerwarteten Wert sehen, ist es möglich, dass das unerwartete Dimensionselement denselben Hash wie ein anderes Dimensionselement verwendet, das Ihrem Segment entspricht.

## Wahrscheinlichkeit einer Hash-Kollision

Adobe Analytics verwendet für die meisten Dimensionen 32-Bit-Hashes, was bedeutet, dass es 2<sup>32 </sup> Hash-Kombinationen gibt (ca. 4,3 Mrd.). Für jede Dimension wird jeden Monat eine neue Hash-Tabelle erstellt. Die ungefähre Wahrscheinlichkeit, dass eine Hash-Kollision auftritt, basiert auf der Anzahl der eindeutigen Werte wie folgt. Diese Quoten basieren auf einer einzigen Dimension für einen einzelnen Monat.

| Eindeutige Werte | Quoten |
| --- | --- |
| 1.000 | 0,01 % |
| 10.000 | 1 % |
| 50.000 | 26% |
| 100.000 | 71 % |

{style="table-layout:auto"}

Ähnlich wie beim [Geburtstagsparadox](https://en.wikipedia.org/wiki/Birthday_problem) steigt mit zunehmender Anzahl eindeutiger Werte die Wahrscheinlichkeit von Hash-Kollisionen drastisch. Bei 1 Million eindeutigen Werten gibt es wahrscheinlich mindestens 100 Hash-Kollisionen für diese Dimension.

## Hash-Kollisionen minimieren

Die meisten Hash-Kollisionen treten mit zwei ungewöhnlichen Werten auf, die keine bedeutsame Auswirkung auf Berichte haben. Selbst wenn ein Hash mit einem gemeinsamen und einem ungewöhnlichen Wert kollidiert, ist das Ergebnis vernachlässigbar. In seltenen Fällen, in denen zwei beliebte Werte eine Hash-Kollision erleben, ist es jedoch möglich, die Auswirkungen klar zu sehen. Adobe empfiehlt Folgendes, um die Auswirkungen in Berichten zu reduzieren:

* **Ändern des Datumsbereichs**: Hash-Tabellen ändern sich monatlich. Wenn Sie den Datumsbereich so ändern, dass er sich über einen weiteren Monat erstreckt, kann jeder Wert unterschiedliche Hash-Werte erhalten, die nicht kollidieren.
* **Reduzieren der Anzahl eindeutiger Werte**: Sie können Ihre Implementierung anpassen oder [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) verwenden, um die Anzahl eindeutiger Werte zu reduzieren, die eine Dimension erfasst. Wenn Ihre Dimension beispielsweise eine URL erfasst, können Sie Abfragezeichenfolgen oder Protokolle entfernen.

<!-- https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=OmniArch&title=Uniques -->
