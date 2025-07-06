---
title: Anwendungsfälle für Segmentvergleiche
description: Erfahren Sie, wie Sie mithilfe des Segmentvergleichsfelds Einblicke in die Marketing-Strategie gewinnen können.
keywords: Segment IQ
feature: Segmentation
role: User, Admin
exl-id: d7c02e5c-5313-4e12-86cb-d483644ccbc7
source-git-commit: b4c1636bdc9d5be522b16f945a46beabf4f7a733
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 15%

---

# Anwendungsfälle für Segmentvergleiche

Das Bedienfeld für den Segmentvergleich ist eine in Analysis Workspace häufig verwendete Funktion. Kunden entdecken häufig neue Möglichkeiten, Einblicke zu gewinnen, wenn sie das Bedienfeld verwenden. Im Folgenden finden Sie einige typische Anwendungsfälle

## Anwendungsfall 1: Vergleich von Mobile- und Desktop-Implementierungen

> *„Sie haben Treffer von einer Website mit einer anderen verglichen und schnell eine Reihe von Tagging-Inkonsistenzen festgestellt. Auf diese Weise haben Sie Datenprobleme vor der Produktveröffentlichung vermieden.“*

Sie sind für eine mobile Website und eine Desktop-Website zuständig und müssen sicherstellen, dass die Tags auf allen Mobilgeräten und Desktop-Computern einheitlich sind. Um sicherzustellen, dass Sie nichts Wichtiges verpassen, verwenden Sie das Bedienfeld Segmentvergleich , um Treffer auf ihrer mobilen Site mit Treffern auf ihrer Desktop-Site zu vergleichen. Sie werden feststellen, dass es auf der mobilen Website keine Checkout-Ereignisse gibt und Sie die richtigen Tags erhalten, bevor die mobile Website veröffentlicht wird. Dadurch wird ein Datenunglück verhindert, das dadurch entsteht, dass die mobile Site keine Konversionen aufzeichnet.

| Segment 1 | Segment 2 |
|--- |--- |
| Hit-Container, bei dem Mobilgerätetyp gleich Mobiltelefon oder Tablet ist | Alle anderen |

{style="table-layout:fixed"}


## Anwendungsfall 2: Vergleichen von Kunden, die eine bestimmte Funktion verwenden, mit Kunden, die dies nicht tun

> *„Sie haben festgestellt, dass Kunden, die Ihre Funktion zum Produktvergleich nutzen, mit 10 % höherer Wahrscheinlichkeit konvertieren. Sie haben den Produktvergleich an den Anfang der Seite verschoben und die Bestellungen um 4 % gesteigert!“*

Ein Team für die Optimierung von Websites für den Einzelhandel möchte die Benutzer besser verstehen, die mit einer kürzlich veröffentlichten Produktvergleichsfunktion interagieren. Sie verwenden das Bedienfeld „Segmentvergleich“, um Benutzer, die die Funktion „Produktvergleich“ verwenden, mit allen anderen Personen auf der Website zu vergleichen. Sie identifizieren schnell mehrere wichtige Unterschiede, darunter die Tatsache, dass diese Benutzer mit 10 % höherer Wahrscheinlichkeit ein Produkt kaufen. Das Site-Optimierungs-Team entscheidet, die Funktion für den Produktvergleich oben auf der Seite prominenter zu testen.

| Segment 1 | Segment 2 |
|--- |--- |
| Besucher-Container, in dem ein benutzerdefiniertes Ereignis (Preisvergleichswerkzeug) vorhanden ist | Alle anderen |

{style="table-layout:fixed"}


## Anwendungsfall 3: Vergleich zwischen Besuchern der News-Website und Besuchern anderer Website-Abschnitte

> *„Sie haben festgestellt, dass sich Besucher Ihres News-Abschnitts mit doppelt so hoher Wahrscheinlichkeit Videoanzeigen ansehen. Daher haben Sie in diesem Abschnitt mehr Videooptionen hinzugefügt. Die Zahl der angezeigten Videoanzeigen stieg um 7 % an!“*

Ein großes Medienunternehmen untersucht in seinem News-Bereich, wie sich die Interaktion der Zielgruppen mit Inhalten verbessern lässt. Sie erstellen ein Segment von Besucherinnen und Besuchern, die den Bereich „Nachrichten-Website“ besuchen, um die Nachrichten-Zielgruppe besser zu verstehen. Sie stellen sofort fest, dass diese Benutzer mit doppelt so hoher Wahrscheinlichkeit Videoanzeigen ansehen als Besucher anderer Site-Bereiche. Das Video-Team hat einen empfohlenen Videoabschnitt auf seiner News-Seitenleiste zusammengestellt und erreicht eine Steigerung der angezeigten Videoanzeigen um 7 %.

| Segment 1 | Segment 2 |
|--- |--- |
| Besucher-Container, bei dem der Website-Bereich „News“ entspricht | Alle anderen |

{style="table-layout:fixed"}


## Anwendungsfall 4: Vergleich zwischen Besuchern aus Paid Search und allen anderen

> *„Bei Besuchern, die über Suchmaschinen auf Ihre Website kamen, war die Wahrscheinlichkeit eines Upsell dreimal höher als bei allen anderen Besuchern. Infolgedessen haben Sie Ihre Ausgaben für bestimmte Keywords erhöht und eine Steigerung der Upsell-Werte um 56 % erzielt.*

Ein großes B2B-Dienstleistungsunternehmen möchte den Traffic verstehen, den Paid Search-Keywords auf seine Site bringen. Paid Search hat nicht zu zahlreichen Konversionen direkt geführt, und der Marketing-Manager erwägt, das Budget dafür zu reduzieren. Das Marketing-Team erstellt ein Segment von Besuchern, die über die gebührenpflichtige Suche auf die Website kommen, und vergleicht dieses Segment mithilfe des Bedienfelds für den Segmentvergleich mit allen anderen Besuchern. Sie stellen fest, dass diese Besucher zwar mit geringerer Wahrscheinlichkeit direkt konvertieren, aber mit dreimal höherer Wahrscheinlichkeit einen zuvor erworbenen Service anbieten. Das Marketing-Team konzentriert sein Budget nur auf die Schlüsselwörter im Zusammenhang mit dem Upsell und verzeichnet eine Steigerung von 56 % bei den Service-Upsells.

| Segment 1 | Segment 2 |
|--- |--- |
| Besucher-Container, bei dem der Typ der verweisenden Stelle „Paid Search“ ist | Alle anderen |

{style="table-layout:fixed"}


## Anwendungsfall 5: Vergleich zwischen Käufern von Fitbit und allen anderen

> *„Sie haben herausgefunden, dass Kunden, die Fitbits kauften, mit 6-mal höherer Wahrscheinlichkeit eine „nicht vorrätige“ Nachricht erhalten als alle anderen. Sie haben schnell mehr Fitbits bestellt und haben es vermieden, nicht mehr vorrätig zu sein!“*

**Szenario:** Ein großes Online-retailer interessiert sich dafür, wie eines der beliebtesten Ferienprodukte - Fitbit - verkauft wird und was Fitbit-Käufer unter anderen Kunden einzigartig macht. Das Marketing-Team kann den Fitbit-Zeileneintrag in seinem Produktbericht auswählen und schnell eine Segmentvergleichsanalyse über das Kontextmenü durchführen. Sie stellen fest, dass Benutzer, die Fitbits kaufen, mit 6-mal höherer Wahrscheinlichkeit eine „nicht vorrätige“ Nachricht erhalten als andere Kunden. Nach weiterer Analyse kann das Marketing-Team diese Besucher zu ihren stationären Läden leiten, während sie in ihrer Einkaufsabteilung warten, um weitere Fitbits zum Versand zu bestellen. Dadurch vermeidet der retailer mehr „nicht vorrätige“ Nachrichten und kann einen größeren Teil der Urlaubsnachfrage befriedigen.

| Segment 1 | Segment 2 |
|--- |--- |
| Besucher-Container, in dem Bestellungen vorhanden sind und benutzerdefinierte Dimension „Marke“ gleich „FitBit“ | Alle anderen |

{style="table-layout:fixed"}