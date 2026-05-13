---
description: Erfahren Sie, welche statistischen Verfahren zum Erkennen von Anomalien verwendet werden.
title: In der Anomalieerkennung verwendete statistische Verfahren
feature: Anomaly Detection
role: User, Admin
exl-id: e9868296-e453-45ec-b874-b2aa1b37a1bf
TQID: https://experienceleague.adobe.com/4DIICc89-1ppuJWmUpJBrDrOU7MH78dYBTCHTqkBE2E
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 1101
ht-degree: 37%

---

# Statistische Verfahren

Die Anomalieerkennung in Analysis Workspace setzt eine Reihe statistischer Verfahren ein, um festzustellen, ob eine Beobachtung als anormal anzusehen ist oder nicht.

Je nach der im Bericht verwendeten Datumsgranularität werden 3 verschiedene statistische Verfahren eingesetzt – für stündliche, tägliche, wöchentliche/monatliche Anomalieerkennung. Die statistischen Verfahren werden nachfolgend beschrieben.

## Anomalieerkennung für Granularität „Täglich“

Für Berichte mit täglicher Granularität berücksichtigt der Algorithmus verschiedene wichtige Faktoren, um Ergebnisse mit höchstmöglicher Genauigkeit bereitzustellen. Zunächst bestimmt der Algorithmus anhand der verfügbaren Daten, welche Modellart angewendet werden soll, und wählt dabei eine von zwei Klassen aus: ein zeitreihenbasiertes Modell oder ein Modell zur Ausreißererkennung (funktionale Filterung genannt).

Die Entscheidung für das zeitreihenbasierte Modell beruht auf den folgenden Kombinationen für den Typ ETS (Error, Trend and Seasonality = Fehler, Trend und Saisonabhängigkeit), wie von [Hyndman und Kollegen (2008)](https://link.springer.com/book/10.1007/978-3-540-71918-2). Insbesondere versucht der Algorithmus die folgenden Kombinationen:

1. ANA (additiver Fehler, kein Trend, additive Saisonabhängigkeit)
1. AAA (additiver Fehler, additiver Trend, additive Saisonabhängigkeit)
1. MNM (multiplikativer Fehler, kein Trend, multiplikative Saisonabhängigkeit)
1. MNA (multiplikativer Fehler, kein Trend, additive Saisonabhängigkeit)
1. AAN (additiver Fehler, additiver Trend, keine Saisonabhängigkeit)

Der Algorithmus testet die Eignung jeder der Kombinationen, indem er die Kombination mit dem besten mittleren absoluten Prozentfehler (MAPE) auswählt. Wenn der MAPE-Wert des besten Zeitreihenmodells jedoch größer als 15 % ist, wird eine funktionale Filterung angewendet. In der Regel passen Daten mit einem hohen Wiederholungsgrad (z. B. Woche über Woche oder Monat über Monat) am besten zu einem Zeitreihenmodell.

Nach der Modellauswahl passt der Algorithmus die Ergebnisse dann an Feiertagen und der Saisonabhängigkeit von einem Jahr zum anderen an. Für Feiertage prüft der Algorithmus, ob einer der folgenden Feiertage im Datumsbereich des Berichts vorhanden ist:

* Gedenktag
* 4. Juli
* Erntedankfest
* Black Friday
* Cyber Monday
* &#x200B;24. bis 26. Dezember
* 1. Januar
* 31. Dezember

Diese Feiertage wurden anhand umfangreicher statistischer Analysen einer großen Anzahl von Datenpunkten ausgewählt, um die Feiertage zu ermitteln, die den größten Einfluss in den meisten Kunden-Trends gezeigt haben. Obwohl die Liste sicherlich nicht für alle Kunden oder Geschäftszyklen vollständig ist, verbessert die Anwendung dieser Feiertage die Leistung des Algorithmus insgesamt für fast alle Datensätze der Kunden erheblich.

Nach Auswahl des Modells und der Identifizierung der im Berichtszeitraum befindlichen Feiertage fährt der Algorithmus wie folgt fort:

1. Konstruiert den Referenzzeitraum der Anomalie. Dieser Zeitraum umfasst bis zu 35 Tage vor dem Berichtsdatumsbereich und einen übereinstimmenden Datumsbereich 1 Jahr davor. und berücksichtigt Schalttage, sofern erforderlich, und alle anwendbaren Feiertage, die an einem anderen Kalendertag im Vorjahr stattgefunden haben könnten.
1. Er testet, ob im aktuellen Zeitraum (außer dem Vorjahr) Feiertage vorhanden sind, die laut den aktuellsten Daten eine Anomalität darstellen.
1. Wenn der Feiertag im aktuellen Datumsbereich als anormal betrachtet wird, passt der Algorithmus den erwarteten Wert und das Konfidenzintervall des aktuellen Feiertags an die Werte des Feiertags aus dem vergangenen Jahr an (unter Betrachtung von zwei Tagen vorher und nachher). Die Korrektur für den aktuellen Feiertag basiert auf dem niedrigsten absoluten Mittelwert des Fehlers in Prozent von:

   1. Additive Wirkungen
   1. Multiplikative Effekte
   1. Differenz gegenüber dem Vorjahr

Beachten Sie im folgenden Beispiel die deutliche Verbesserung der Performance an Weihnachten und Neujahr:

![](assets/anomaly_statistics.png)

## Anomalieerkennung für Granularität „Stündlich“

Stündliche Daten basieren auf demselben Zeitreihen-Algorithmus wie der tägliche Granularitätsalgorithmus. Sie beruht jedoch stark auf zwei Trendmustern: dem 24-Stunden-Zyklus sowie dem Wochenende-/Wochentagszyklus. Um diese beiden saisonalen Effekte zu erfassen, erstellt der stündliche Algorithmus mithilfe des oben beschriebenen Ansatzes zwei separate Modelle für ein Wochenende und einen Wochentag.

Die Schulungsfenster für stündliche Trends basieren auf einem 336-Stunden-Lookback-Fenster.

## Anomalieerkennung für die Granularitäten „Wöchentlich“ und „Monatlich“

Wöchentliche und monatliche Trends weisen nicht dieselben wöchentlichen oder täglichen Trends auf, die bei täglichen oder stündlichen Granularitäten gefunden werden, sodass ein solcher separater Algorithmus verwendet wird. Bei wöchentlichen und monatlichen Tests wird ein zweistufiger Ansatz zur Erkennung von Ausreißern als Generalized Extreme Studentized Deviate (GESD) Test bezeichnet. Dieser Test berücksichtigt die maximale Anzahl erwarteter Anomalien in Kombination mit dem angepassten Boxplot-Plot-Ansatz (eine nicht parametrische Methode zur Ausreißererkennung), um die maximale Anzahl von Ausreißern zu bestimmen. Die beiden Schritte sind:

1. Angepasste Boxplot-Plot-Funktion: Diese Funktion bestimmt die maximale Anzahl von Anomalien bei den Eingabedaten.
1. GESD-Funktion: wird auf die Eingabedaten mit der Ausgabe aus Schritt 1 angewendet.

Der Schritt zur Anomalieerkennung für Feiertag und Jahreszeit zieht dann die Daten des letzten Jahres von den diesjährigen Daten ab. Anschließend werden die Daten erneut mithilfe des oben beschriebenen zweistufigen Prozesses iteriert, um zu überprüfen, ob Anomalien saisonal relevant sind. Jede dieser Datumsgranularitäten verwendet ein 15 Zeiträume zurückliegendes Zeitfenster, in dem der für den Bericht ausgewählte Datumsbereich liegt (entweder 15 Monate oder 15 Wochen), sowie einen entsprechenden Datumsbereich, der 1 Jahr vor dem Trainingszeitraum liegt.

## In der Beitragsanalyse verwendete statistische Verfahren

Die Beitragsanalyse ist ein intensiver maschineller Lernprozess, mit dem Beitragende zu einer in Adobe Analytics beobachteten Anomalie aufgedeckt werden sollen. Damit soll Benutzenden geholfen werden, lohnenswerte Bereiche oder Gelegenheiten für weitere Analysen viel schneller zu identifizieren.

Die Beitragsanalyse führt einen zweiteiligen Algorithmus für jedes einzelne Dimensionselement durch, das für den Bericht zur Beitragsanalyse des Benutzers verfügbar ist. Dabei geht der Algorithmus in der folgenden Reihenfolge vor:

1. Er berechnet für jede Dimension die V-Test-Statistik nach Cramer. Im folgenden Beispiel sehen Sie eine Kontingenztabelle mit Seitenansichten nach Ländern über zwei Zeitperioden:

   ![](assets/contingency_table.png)

   In Tabelle 1 kann Cramers V verwendet werden, um die Verknüpfung zwischen den Seitenansichten nach Ländern für den Zeitraum 1 (z. B. historisch) und den Zeitraum 2 (z. B. den Tag, an dem die Anomalie auftritt) zu messen. Ein niedriger Wert für Cramers V bedeutet einen niedrigen Grad an Zusammenhang. Werte für Cramers V liegen zwischen 0 (kein Zusammenhang) und 1 (vollständiger Zusammenhang). Die Cramer-V-Statistik kann wie folgt berechnet werden:

   ![](assets/cramers-v.png)

1. Für jedes Dimensionselement wird der PR-Wert (Pearson-Residuum) verwendet, um den Zusammenhang zwischen der anormalen Metrik und jedem Dimensionselement zu messen. PR folgt einer Standardnormalverteilung, die es dem Algorithmus ermöglicht, die PRs zweier Zufallsvariablen zu vergleichen, selbst wenn die Abweichungen nicht vergleichbar sind. In der Praxis ist der Fehler nicht bekannt und wird durch endliche Probenkorrektur geschätzt.

   Im vorherigen Beispiel in Tabelle 1 wird der PR mit endlicher Stichprobenkorrektur für Land i und Zeitraum 2 wie folgt angegeben:

   ![](assets/persons-residual.png)

   wobei

   ![](assets/pr-example.png)

   (Für den Zeitraum 1 kann eine ähnliche Formel erhalten werden.)

   Für die Endergebnisse wird die Bewertung von jedem Dimensionselement dann mit dem Cramer-V-Messwert gewichtet und in einen Wert zwischen 0 und 1 skaliert, um den Verteilungswert zu erhalten.
