---
title: Berechnung der Besuchszeit in Adobe Analytics
description: Eine aggregierte Seite mit Dimensionen und Metriken zur Besuchszeit.
feature: Metrics
exl-id: 71e9b856-8a0a-47be-a73f-4dc7d639a5de
source-git-commit: 75ae77c1da1b578639609888e794e13d965ef669
workflow-type: tm+mt
source-wordcount: '1744'
ht-degree: 72%

---

# Besuchszeit – Übersicht

Für Adobe Analytics-Produkte stehen verschiedene [!UICONTROL &#39;Besuchszeit&#39;] [Metriken](overview.md) und Dimensionen zur Verfügung.

## Besuchszeit-Metriken

| Metrik | Definition | Verfügbar in |
|---|---|---|
| [!UICONTROL Gesamtbesuchszeit in Sekunden] | Zeigt den Zeitraum an, über den Besucher insgesamt mit einem bestimmten Dimensionselement agieren. Enthält die Instanz eines Wertes sowie die Persistenz über alle folgenden Treffer hinweg. Bei Props wird die Besuchszeit auch über die nachfolgenden Verknüpfungsereignisse hinweg berechnet. | Analysis Workspace, Report Builder (als &quot;Gesamtbesuchszeit&quot;bezeichnet), Data Warehouse |
| [!UICONTROL Zeit pro Besuch] (Sekunden) | Ungefähr *Gesamtbesuchszeit in Sekunden/(Besuchsabsprünge)*<br> Stellt die durchschnittliche Zeit dar, die Besucher während jedes Besuchs mit einem bestimmten Dimensionselement interagieren. **Hinweis**: Diese Metrik kann nicht unabhängig berechnet werden, da der Nenner dieser Funktion eine interne Metrik ist. | Analysis Workspace |
| [!UICONTROL Besuchszeit pro Besucher] (Sekunden) | Ungefähr *Gesamtbesuchszeit/Unique Visitor in Sekunden*<br> Stellt die durchschnittliche Zeit dar, die Besucher über die Lebensdauer des Besuchers (Cookie-Länge) mit einem bestimmten Dimensionselement interagieren. **Hinweis**: Diese Metrik kann nicht unabhängig berechnet werden, da der Nenner dieser Funktion eine interne Metrik ist. | Analysis Workspace |
| [!UICONTROL Besuchszeit/Benutzer (Status)] | Ungefähr *Gesamtbesuchszeit für die mobile App in Sekunden/Unique Mobile-App-Besucher*<br> Stellt die durchschnittliche Zeit dar, die Besucher der mobilen App über die Lebensdauer des Besuchers (Cookie-Länge) mit einem bestimmten Dimensionselement interagieren. **Hinweis**: Diese Metrik kann nicht unabhängig berechnet werden, da der Nenner dieser Funktion eine interne Metrik ist. | Analysis Workspace |
| [!UICONTROL Durchschnittliche Besuchszeit pro Site] (Sekunden) | Stellt die gesamte Zeit dar, die Besucher pro Dimensionselement-Sequenz mit einem bestimmten Dimensionselement interagieren. Es ist nicht nur auf &quot;Site&quot;-Durchschnittswerte beschränkt, wie der Name nahe legt. Weitere Informationen über Sequenzen finden Sie im Bereich „Berechnung der Besuchszeit“.<br>**Hinweis**: Diese Metrik unterscheidet sich auf der Dimensionselement-Ebene mit hoher Wahrscheinlichkeit von „Zeit pro Besuch“, da bei der Berechnung ein anderer Nenner verwendet wird. | Analysis Workspace, Report Builder (in Minuten angezeigt) |
| [!UICONTROL Durchschnittliche Besuchszeit pro Site] | Dies ist dieselbe Metrik wie *Durchschnittliche Besuchszeit pro Site (Sekunden)*, mit Ausnahme der Formatierung als Zeit (`hh:mm:ss`) | Analysis Workspace |
| [!UICONTROL Durchschnittliche Besuchszeit pro Site] | Veraltete Metrik.<br> Stattdessen empfiehlt Adobe, dass Sie &quot;Durchschnittliche Besuchszeit pro Site&quot;verwenden, wenn die durchschnittliche Besuchszeit für ein Dimensionselement erforderlich ist. | Report Builder (wenn sich eine Dimension in der Anforderung befindet) |
| [!UICONTROL Gesamtsitzungslänge], also [!UICONTROL Frühere Sitzungslänge] | Nur SDK für Mobilanwendungen. <br>Wird beim nächsten Start der App für die vorangegangene Sitzung bestimmt. Diese Metrik wird in Sekunden berechnet. Allerdings zählt sie nicht, wenn sie im Hintergrund ausgeführt wird, sondern nur, wenn sie direkt verwendet wird. Es handelt sich um eine Metrik auf Sitzungsebene.<br>Beispiel: Wir installieren die App ABC, starten die App und verwenden sie 2 Minuten lang, bevor wir die App schließen. Es werden keine Daten über diese Sitzungsdauer gesendet. Wenn wir die App das nächste Mal starten, wird die [!UICONTROL Frühere Sitzungslänge] mit einem Wert von 120 gesendet. | Analysis Workspace, Report Builder, Mobile Services-Benutzeroberfläche |
| [!UICONTROL Durchschnittliche Sitzungslänge] (Mobil) | *Gesamtsitzungslänge/(Starts – Erste Starts)*<br> Nur Mobile-App-SDK. Es handelt sich um eine Metrik auf Sitzungsebene. | Report Builder, Benutzeroberfläche von Mobile Services |

## Besuchszeit-Dimensionen

| Dimension | Definition | Verfügbar in |
| --- | --- | --- |
| [!UICONTROL Zeit pro Besuch – präzise] | Die gesamte bei einem Besuch verbrachte Zeit, die auf die nächste Sekunde gekürzt und auf alle Treffer angewendet wird, die Teil des Besuchs waren. Es handelt sich um eine Dimension auf Besuchsebene. | Analysis Workspace |
| [!UICONTROL Zeit pro Besuch – zusammengefasst] | Die präzise Dimension, die in 9 verschiedene Bereiche zusammengefasst wird. Es handelt sich um eine Dimension auf Besuchsebene. Die Bereiche sind:<ul><li>Weniger als 1 Minute</li><li>1–5 Minuten</li><li>5–10 Minuten</li><li>10–30 Minuten</li><li>30–60 Minuten</li><li>1–2 Stunden</li><li>2–5 Stunden</li><li>5–10 Stunden</li><li>10–15 Stunden</li></ul>**Anmerkung**: Längere Zeiträume können nicht erfasst werden, da ein Besuch nach einer Aktivitätsdauer von 12 Stunden abläuft. | Analysis Workspace, Report Builder |
| [!UICONTROL Besuchszeit pro Seite – präzise] | Die gesamte bei einem Treffer verbrachte Zeit, gekürzt auf die letzte ganze Sekunde. Hierbei handelt es sich um eine Dimension auf Trefferebene, die sowohl Seitenansichten als auch Verknüpfungs-Ereignisse enthält. Trotz seines Namens ist sie nicht auf die Dimension &quot;Seite&quot;beschränkt. | Analysis Workspace |
| [!UICONTROL Besuchszeit pro Seite – zusammengefasst] | Die präzise Dimension, die in 10 verschiedene Bereiche zusammengefasst wird; die zusammengefasste Dimension zählt jedoch nur Seitenansichten (und schließt Verknüpfungs-Ereignisse aus). Es handelt sich um eine Dimension auf Trefferebene. Die Bereiche sind:<ul><li>weniger als 15 Sekunden</li><li>15–29 Sekunden</li><li>30–59 Sekunden</li><li>1–3 Minuten</li><li>3–5 Minuten</li><li>5–10 Minuten</li><li>10–15 Minuten</li><li>15–20 Minuten</li><li>20–30 Minuten</li><li>Mehr als 30 Minuten</li></ul> | Analysis Workspace |

## Berechnung der Besuchszeit

Adobe Analytics verwendet explizite Werte (einschließlich Verknüpfungs-Ereignissen und Videoaufrufen) zur Berechnung der [!UICONTROL Besuchszeit].

>[!NOTE]
>
>Ohne Verknüpfungsereignisse wie [!UICONTROL Videoaufrufe] oder [!UICONTROL Exitlinks] kann die Besuchszeit für den letzten Treffer eines Besuchs nicht ermittelt werden. Aus ähnlichen Gründen wird [!UICONTROL Absprung-Besuchen] (d. h. Besuchen mit einem einzelnen Treffer) keine Besuchszeit zugewiesen.

Der **Zähler** ist in allen Besuchszeit-Berechnungen die Gesamtbesuchszeit in Sekunden.

Der **Nenner** ist in Adobe Analytics nicht als separate Metrik verfügbar. Bei Besuchszeit-Metriken auf Trefferebene besteht der Nenner in Sequenzen. Eine Sequenz ist ein Satz aufeinanderfolgender Treffer, in dem eine beliebige Variable denselben Wert enthält (egal, ob festgelegt, nach vorne verteilt oder permanent gespeichert). „Nach vorne verteilt“ bezieht sich auf die Persistenz von Eigenschaften zwischen Seitenansichten (d. h. über aufeinanderfolgende Verknüpfungs-Ereignisse hinweg). Dies dient der Berechnung der Besuchszeit.

* Zum Beispiel ist der Nenner im Falle des [!UICONTROL Seitennamens] oder einer anderen Dimension auf der Trefferebene vor allem [!UICONTROL Instanzen] oder [!UICONTROL Seitenansichten], für die ein Neuladen und nicht festgelegte Werte (z. B. Verknüpfungs-Ereignisse) jedoch als einzelne Interaktion (eine Sequenz) gezählt werden.

* Treffer mit Absprung und Ausstieg werden auch aus dem Nenner entfernt, da die Besuchszeit nicht ermittelt werden kann.

## Häufig gestellte Fragen (FAQ)

+ + + Können alle Besuchszeitmetriken auf eine Dimension angewendet werden?

Die Besuchszeit-Metriken, die auf jede Dimension angewendet werden können, sind:

* [!UICONTROL Gesamtbesuchszeit in Sekunden]

* [!UICONTROL Zeit pro Besuch] (Sekunden)

* [!UICONTROL Besuchszeit pro Besucher] (Sekunden)

* [!UICONTROL Durchschnittliche Besuchszeit pro Site] (Sekunden)

+++

+++ Welche Besuchszeitdimension wird am besten in Aufschlüsselungen mit anderen Dimensionen verwendet?

Die Dimension [!UICONTROL Besuchszeit pro Seite - präzise] ist eine Dimension auf Trefferebene. Wenn Sie diese Dimension anhand einer anderen Dimension aufschlüsseln, können Sie die Sekunden ermitteln, über die sich ein Treffer erstreckt hat, von dem auch die Aufschlüsselungsdimension betroffen war.
Im folgenden Beispiel ist der Suchbegriff &quot;classifieds&quot;mit Trefferzeiten von 54 Sekunden, 59 Sekunden usw. verknüpft, was möglicherweise anzeigt, dass Besucher Zeit mit dem Lesen von Inhalten verbringen, die für diesen Begriff zurückgegeben werden.

![](assets/time-spent1.png)

+++

+++ Welche Metrik eignet sich für die Dimension [!UICONTROL Besuchszeit pro Seite - präzise]?

Jede beliebige Metrik. Die Dimension zeigt die Besuchszeit für den Treffer an, bei dem es zu dem Ereignis kam. Eine längere Besuchszeit bedeutet, dass ein Besucher mehr Zeit auf einer Seite (Treffer) verbracht hat, auf der es zu dem Ereignis kam.

![](assets/time-spent2.png)

+++

+++Wie unterscheidet sich [!UICONTROL Durchschnittliche Besuchszeit pro Site] von [!UICONTROL Zeit pro Besuch]?

Der Unterschied ist der in der Metrik verwendete Nenner:

* [!UICONTROL Durchschnittliche Besuchszeit pro Site] verwendet die Sequenzen, die ein Dimensionselement enthalten.

* [!UICONTROL Besuchsdauer pro Besuch] verwendet die Besuchsanzahl.

Aus diesem Grund geben diese Metriken möglicherweise ähnliche Ergebnisse auf Besuchsebene zurück, unterscheiden sich aber auf einer Trefferebene.

+++

+++ Warum stimmen Aufschlüsselungssummen mit [!UICONTROL Durchschnittliche Besuchszeit pro Site] nicht mit dem übergeordneten Zeileneintrag überein?

Da [!UICONTROL Durchschnittliche Besuchszeit pro Site] von ununterbrochenen Sequenzen einer Dimension abhängt und der innere Bericht bei der Berechnung dieser Ausführungen nicht vom äußeren Bericht abhängt.

Betrachten Sie beispielsweise den folgenden Besuch.

| Treffernummer | 1 | 2 | 3 |
|---|---|---|---|
| **Besuchszeit in Sekunden** | 30 | 100 | 10 |
| **Seitenname** | Startseite | Produkt | Startseite |
| **Datum** | 1. Januar | 1. Januar | 1. Januar |

Bei der Berechnung der Besuchszeit für die Startseite würde die Rechnung (30+10)/2=20 lauten, aber eine Aufschlüsselung nach Tag würde (30+10)/1=40 ergeben, da am 1. Januar ein einziger ununterbrochenen Durchlauf erfolgte.

Aus diesem Grund geben diese Metriken möglicherweise ähnliche Ergebnisse auf Besuchsebene zurück, unterscheiden sich aber auf einer Trefferebene.

+++

## Beispiele für die Berechnung der [!UICONTROL Besuchszeit]

Angenommen, der folgende Satz von Server-Aufrufen gilt für einen einzigen Besucher mit einem einzigen Besuch:

| Besuch – Trefferanzahl | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|---|---|---|---|---|---|---|
| **Besuch – vergangene Zeit (in Sek.)** | 0 | 30 | 80 | 180 | 190 | 230 | 290 |
| **Besuchszeit in Sekunden** | 30 | 50 | 100 | 10 | 40 | 60 | – |
| **Treffertyp** | Seite | Link | Seite | Seite | Seite | Seite | Seite |
| **Seitenname** | Startseite | – | Produkt | Startseite | Startseite (neu laden) | Korb | Bestellungsbestätigung |
|  |  |  |  |  |  |  |  |
| **prop1** | A (festgelegt) | A (nach vorne verteilt) | nicht festgelegt | B (festgelegt) | B (festgelegt) | A (Set) | C (festgelegt) |
| **prop1 – Besuchszeit in Sekunden** | 30 | 50 | – | 10 | 40 | 60 | – |
|  |  |  |  |  |  |  |  |
| **eVar1** | Rot (festgelegt) | Rot (beibehalten) | (abgelaufen) | Blau (festgelegt) | Blau (festgelegt) | Blau (beibehalten) | Rot (festgelegt) |
| **eVar1 – Besuchszeit in Sekunden** | 30 | 50 | – | 10 | 40 | 60 | – |

Basierend auf der obigen Tabelle werden Besuchszeitmetriken wie folgt berechnet:

| prop1 | Gesamtbesuchszeit in Sekunden | Zeit pro Besuch | Besuchszeit pro Besucher | Sequenzanzahl | Durchschnittliche Besuchszeit pro Site |
|---|---|---|---|---|---|
| A | 30 + 50 + 60 = 140 | 140 / 1 = 140 | 140 / 1 = 140 | 2 | 140 / 2 = 70 |
| B | 10 + 40 = 50 | 50 / 1 = 50 | 50 / 1 = 50 | 1 | 50 / 1 = 50 |
| C | 0 | 0 | 0 | 0 | 0 |
| Nicht zugewiesene Zeit | 100 | – | – | – | – |

| eVar1 | Gesamtbesuchszeit in Sekunden | Zeit pro Besuch | Besuchszeit pro Besucher | Sequenzanzahl | Durchschnittliche Besuchszeit pro Site |
|---|---|---|---|---|---|
| Rot | 30 + 50 = 80 | 80 / 1 = 80 | 80 / 1 = 80 | 1 | 80 / 1 = 80 |
| Blau | 10 + 40 + 60 = 110 | 110 / 1 = 110 | 110 / 1 = 110 | 1 | 110 / 1 = 110 |
| Nicht zugewiesene Zeit | 100 | – | – | – | – |

Zeit pro Besuch (präzise): 290
Besuchszeit pro Seite (präzise): 10, 30, 40, 50, 60, 100

Einige zusätzliche Hinweise, um das Beispiel deutlicher zu machen:

* Alle Besuchszeitberechnungen basieren auf „Besuch – vergangene Zeit“. Dieser Wert beginnt beim ersten Treffer des Besuchs bei null.

* &quot;Besuchszeit in Sekunden&quot;ist die Differenz zwischen dem Zeitstempel des aktuellen Treffers und dem Zeitstempel des nächsten Treffers. Aus diesem Grund gibt es für den letzten Treffer des Besuchs (sowie die Absprünge) keine Besuchszeit.

* Eine &quot;Sequenz&quot;ist ein Satz aufeinander folgender Treffer, bei dem eine bestimmte Variable denselben Wert enthält (egal, ob festgelegt, nach vorne verteilt oder beibehalten). Beispielsweise hat prop1 &quot;A&quot;zwei Sequenzen: Treffer 1 und 2 und Treffer 6. Werte des letzten Treffers eines Besuchs beginnen keine neue Sequenz, da es für den letzten Treffer keine Besuchszeit gibt. „Durchschnittliche Besuchszeit pro Site“ verwendet Sequenzen im Nenner.

   * Für die Besuchszeit werden Props von Seitentreffern auf nachfolgende Link-Treffer &quot;nach vorne verteilt&quot;, wie oben für prop1 bei Treffer 2 gezeigt. Dadurch kann der Wert, der für prop1 bei Treffer 1 (&quot;A&quot;) festgelegt wurde, die bei Treffer 2 verbrachte Zeit sammeln.

   * eVars sammeln die Besuchszeit für jeden Treffer, bei dem der eVar festgelegt oder permanent gespeichert ist. Die eVar-Persistenz wird durch die eVar-Einstellungen unter „Analytics > „Admin“ definiert.
