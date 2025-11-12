---
description: Beispiele, Hinweise und Syntaxhinweise zur Verwendung von Datumsbereichen in benutzerdefinierten Ausdrücken.
title: Beispiele für Datumsbereiche mit benutzerdefinierten Ausdrücken
uuid: 3f46816d-9eee-4b2d-83be-bf1c9fb97fcf
feature: Report Builder
role: User, Admin
exl-id: d936dd4e-d330-4ed9-a979-3273397d7d92
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 13%

---

# Beispiele für Datumsbereiche mit benutzerdefinierten Ausdrücken

{{legacy-arb}}

Beispiele, Hinweise und Syntaxhinweise zur Verwendung von Datumsbereichen in benutzerdefinierten Ausdrücken.

In der Tabelle wird davon ausgegangen, dass das heutige Datum Montag, der 10. November 2011 ist, wobei der gregorianische Kalender verwendet wird.

| Beispiel | Datumsbereich | Ausdruck anpassen | Datumsbereich des Berichts |
|---|---|---|---|
|  | | **Von** | **Bis** |
| 1 | Vor zwei Wochen | `cw-2w  \| cw-1w-1d` | &#x200B;26. Oktober bis 1. November |
| 2 | Erste 3 Tage des fünften Monats des letzten Jahres | `cy-1y+4m  \| cy-1y+4m+2d` | 1 Mai bis 3 Mai 2010 |
| 3 | Eine volle Woche, beginnend vor 4 Wochen | `cw-4w  \| cw-3w-1d` | &#x200B;12. Oktober bis 18. Oktober |
| 4 | Letzte Woche im Vorjahr | `cw-53w  \| cw-52w-1d` | November bis 9. November 2010 |
| 5 | 1 Monat beginnend vor 2 Monaten | `cm-2m  \| cm-1m-1d` | 1 Sept. bis 30 Sept. |
| 6 | Vor 12 Monaten im Vorjahr | `cm-12m  \| cm-11m-1d` | &#x200B;1. November bis 30. November 2010 |

## Hinweise zu Beispielen {#section_37801B0D6D364ABAA8DCE3A4C0123B2C}

**Beispiel 1**

Wenn heute Montag, der 10. November 2011 ist, nehmen Sie das aktuelle Datum und ziehen Sie eine Woche ab, um die letzte vollständige Oktoberwoche zu erhalten.

**Beispiel 2**

Fügen Sie vier Monate zu Beginn des Jahres (den Monat Januar) hinzu, um den Monat Mai abzurufen. Fügen Sie zwei Tage zum ersten Tag des Monats hinzu, um den dritten Tag des Monats zu erhalten.

## Hinweise zur Syntax {#section_555D6563B2D94FA3BDD801DC0B8C289D}

Benutzerdefinierte Ausdrücke, die die meisten Datumsbereiche abdecken, können erstellt werden, indem zwei Begriffe mit einem Operator verknüpft werden. Ein Begriff ist eine Kombination aus einem ganzzahligen Multiplikator und einer Periodenabkürzung. Ein Beispiel für einen Begriff ist 18d. Ein Beispiel für einen -Operator ist +.

* Leerzeichen zwischen Operatoren und Begriffen sind nicht zulässig.
* Verwenden Sie nur diese Abkürzungen: cd cw cm cq cy d w m q y
* Es empfiehlt sich, im Start- und Enddatum denselben Datumsverweis zu verwenden: cd, cd oder cw, cw oder cy, cy. Verweise auf gemischte Datumsangaben können zu bestimmten Zeiten im Jahr zu ungültigen Datumsangaben führen.
* Gültige Vielfache der Abkürzungen d w m q y werden durch der Abkürzung vorangestellte ganze Zahlen ( 1 2 3 … ) gebildet, z. B. 53d 3w 5q 9m 2y
* Nicht ganzzahlige Zahlen sind nicht zulässig.
* Stellen Sie der Abkürzung nicht nur eine Null voran. Zum Beispiel ist 0w nicht zulässig.
* Die folgenden Operatoren werden zum Verketten von Abkürzungen verwendet: + -
* Da Datumsbereiche relativ zum aktuellen Zeitraum berücksichtigt werden müssen, beginnt der erste Begriff in einem Ausdruck immer mit c.
