---
title: Hash-Kollisionen
description: Beschreibt, was eine Hash-Kollision ist und wie sie sich manifestieren kann.
feature: Validation
exl-id: 693d5c03-4afa-4890-be4f-7dc58a1df553
role: Admin, Developer
source-git-commit: 06f61fa7b39faacea89149650e378c8b8863ac4f
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 6%

---

# Hash-Kollisionen

Dimensionen in Adobe Analytics erfassen Zeichenfolgenwerte. Manchmal sind diese Zeichenfolgen Hunderte von Zeichen lang, während sie manchmal kurz sind. Zur Leistungsverbesserung werden diese Zeichenfolgenwerte nicht direkt in der Verarbeitung verwendet. Stattdessen wird für jeden Wert ein Hash berechnet, um alle Werte zu einer einheitlichen Größe zu machen. Alle Berichte werden mit diesen Hash-Werten ausgeführt, wodurch ihre Leistung drastisch gesteigert wird.

Bei den meisten Feldern wird die Zeichenfolge zuerst in Kleinbuchstaben umgewandelt. Die niedrigere Konversionsrate reduziert die Anzahl eindeutiger Werte. Die Werte werden monatlich gehasht - der Fall für einen bestimmten Wert verwendet den ersten jeden Monat angezeigten Wert. Von Monat zu Monat besteht ein geringes Risiko, dass zwei eindeutige Variablenwerte auf denselben Wert Hash. Dieses Konzept wird als *Hash-Kollision* bezeichnet.

Hash-Kollisionen können in Berichten wie folgt auftreten:

* Wenn Sie einen Bericht im Zeitverlauf anzeigen und eine unerwartete Spitze feststellen, kann es sein, dass mehrere eindeutige Werte für diese Variable denselben Hash verwenden.
* Wenn Sie ein Segment verwenden und einen unerwarteten Wert anzeigen, kann es sein, dass das unerwartete Dimensionselement denselben Hash als ein anderes Dimensionselement verwendet, das mit Ihrem Segment übereinstimmt.

## Chancen einer Hash-Kollision

Adobe Analytics verwendet für die meisten Dimensionen 32-Bit-Hashes, d. h. es gibt 2<sup>32</sup> mögliche Hash-Kombinationen (ca. 4,3 Mrd.). Jeden Monat wird eine neue Hash-Tabelle für jede Dimension erstellt. Die ungefähren Chancen auf eine Hash-Kollision basierend auf der Anzahl eindeutiger Werte sind wie folgt. Diese Chancen basieren auf einer einzelnen Dimension für einen einzelnen Monat.

| Eindeutige Werte | Quoten |
| --- | --- |
| 1.000 | 0,01 % |
| 10.000 | 1 % |
| 50.000 | 26% |
| 100.000 | 71 % |

{style="table-layout:auto"}

Ähnlich wie bei [Geburtstagsparadox](https://en.wikipedia.org/wiki/Birthday_problem)erhöht sich die Wahrscheinlichkeit von Hash-Kollisionen drastisch, da die Anzahl der eindeutigen Werte zunimmt. Bei 1 Million individuellen Werten ist es wahrscheinlich, dass für diese Dimension mindestens 100 Hash-Kollisionen vorliegen.

## Hash-Kollisionen verringern

Die meisten Hash-Kollisionen treten mit zwei ungewöhnlichen Werten auf, die keine aussagekräftigen Auswirkungen auf Berichte haben. Selbst wenn ein Hash mit einem gemeinsamen und ungewöhnlichen Wert kollidiert, ist das Ergebnis vernachlässigbar. In seltenen Fällen, in denen zwei beliebte Werte eine Hash-Kollision erleben, ist es jedoch möglich, ihre Wirkung deutlich zu erkennen. Adobe empfiehlt Folgendes, um die Wirkung in Berichten zu reduzieren:

* **Datumsbereich ändern**: Hash-Tabellen ändern sich jeden Monat. Wenn Sie den Datumsbereich so ändern, dass er sich über einen weiteren Monat erstreckt, können bei jedem Wert unterschiedliche Hashes auftreten, die nicht kollidieren.
* **Anzahl eindeutiger Werte reduzieren**: Sie können Ihre Implementierung anpassen oder [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) um die Anzahl der eindeutigen Werte zu reduzieren, die eine Dimension erfasst. Wenn Ihre Dimension beispielsweise eine URL erfasst, können Sie Abfragezeichenfolgen oder Protokolle entfernen.

<!-- https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=OmniArch&title=Uniques -->
