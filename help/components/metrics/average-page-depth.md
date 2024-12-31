---
title: Durchschnittliche Klicktiefe
description: Gibt an, bei wie vielen Seiten die Dimension im Durchschnitt vorhanden ist.
feature: Metrics
exl-id: 6625405a-bda5-4723-8d22-4bc5b7e44d4e
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 55%

---

# Durchschnittliche Klicktiefe

Die „Metrik [ durchschnittliche Seitentiefe“ ](overview.md) an, wie weit ein Dimensionselement sich im Durchschnitt bis zu einem bestimmten Besuch erstreckt. Beispielsweise zeigt Ihre Startseite (die ein Dimensionselement für die Dimension Seite ist) in der Regel eine kleinere durchschnittliche Seitentiefe als Ihre Kaufbestätigungsseite, die wahrscheinlich weiter in einen Besuch hineinreicht. Sie können diese Informationen verwenden, um bestimmte Seiten für neue Besucher zu optimieren, wenn die Seite im Durchschnitt eine niedrige Tiefe aufweist.

>[!TIP]
>
>Verwenden Sie diese Metrik zusammen mit einer anderen Metrik, z[ B. „Besuche](visits.md), um bessere Einblicke zu erhalten. Wenn Sie diese Metrik allein verwenden, erhalten Sie möglicherweise Dimensionselemente mit anomalen Seitentiefen, was in der Regel keine wertvolle Erkenntnis ist.

## Berechnung dieser Metrik

Die erste Seite eines Besuchs hat eine Klicktiefe von `0`. Die nächste Seite hat eine Klicktiefe von 1, usw. bis zum Ende des Besuchs. Diese Metrik erhöht sich nur bei Aufrufen der Seitenansicht ([`t()`](/help/implement/vars/functions/t-method.md)) und nicht bei Aufrufen des Linktrackings ([`tl()`](/help/implement/vars/functions/tl-method.md)).

Fügen Sie für ein bestimmtes Dimensionselement alle Klicktiefen für dieses Dimensionselement hinzu und teilen Sie es durch Besuche. Die resultierende Zahl ist die durchschnittliche Klicktiefe, gerundet auf die nächste Ganzzahl. Wenn Dimensionselemente eine durchschnittlichen Klicktiefe von `0` haben, bedeutet das, dass sie auf der ersten Seite des Besuchs vorkamen.

Betrachten Sie beispielsweise den folgenden Besuch:

```text
Page1 > Page2 > Page2 > Page3 > Page4 > Page2
```

Wenn Sie die durchschnittliche Klicktiefe für das Dimensionselement `Page2` wünschen, würde diese wie folgt berechnet:

```text
If 'Count repeat instances' is enabled:
(1 + 2 + 5) / 3 = 2.67, rounded up to 3

If 'Count repeat instances' is disabled:
(1 + 4) / 2 = 2.5, rounded up to 3
```

>[!TIP]
>
>Wenn Sie die durchschnittliche Klicktiefe mit einer Dezimalstelle anzeigen möchten, erstellen Sie eine berechnete Metrik mit dieser Metrik als einziges Element in der Formel. Erhöhen Sie die Dezimalstellen in der berechneten Metrik auf die gewünschte Dezimalstelle.

## Prozentsätze über 100 %

Diese Metrik enthält häufig Prozentsätze über 100 %. Der Nenner ist die durchschnittliche Seitentiefe der gesamten Dimension und der Zähler die durchschnittliche Seitentiefe des Dimensionselements.

Wenn die durchschnittliche Seitentiefe der gesamten Dimension geringer ist als die durchschnittliche Seitentiefe eines bestimmten Dimensionselements, werden Prozentsätze über 100 % angezeigt. Bei der Sortierung von Rangberichten nach dieser Metrik werden anormale Werte für die durchschnittliche Klicktiefe angezeigt, was normalerweise nicht nützlich ist. Adobe empfiehlt, in Rangberichten nach einer anderen Metrik wie z. B. [Besuche](visits.md) zu sortieren.
