---
description: Die Anomalieerkennung in Analysis Workspace setzt eine Reihe statistischer Verfahren ein, um festzustellen, ob eine Beobachtung als anormal anzusehen ist oder nicht.
seo-description: Die Anomalieerkennung in Analysis Workspace setzt eine Reihe statistischer Verfahren ein, um festzustellen, ob eine Beobachtung als anormal anzusehen ist oder nicht.
seo-title: Statistische Verfahren bei der Anomalieerkennung
title: Statistische Verfahren bei der Anomalieerkennung
uuid: b 6 ef 6 a 2 e -0836-4 c 9 a-bf 7 e -01910199 bb 92
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Statistische Verfahren bei der Anomalieerkennung

Die Anomalieerkennung in Analysis Workspace setzt eine Reihe statistischer Verfahren ein, um festzustellen, ob eine Beobachtung als anormal anzusehen ist oder nicht.

Je nach der im Bericht verwendeten Datumsgranularität werden 3 verschiedene statistische Verfahren verwendet - insbesondere für stündliche, tägliche, wöchentliche/monatliche Anomalieerkennung. Die statistischen Verfahren werden nachfolgend beschrieben.

## Anomaly detection for daily granularity {#section_758ACA3C0A6B4D399563ECABFB8316FA}

Für Berichte mit täglicher Granularität berücksichtigt der Algorithmus verschiedene wichtige Faktoren, um Ergebnisse mit höchstmöglicher Genauigkeit bereitzustellen. Zunächst legt der Algorithmus fest, welcher Modelltyp angewendet werden soll, basierend auf den verfügbaren Daten, aus denen wir zwischen zwei Klassen auswählen: ein zeitreihenbasiertes Modell oder ein Ausreißererkennungsmodell (als funktionale Filterung bezeichnet).

Die Entscheidung für das zeitreihenbasierte Modell beruht auf den folgenden Kombinationen für den Typ ETS (Error, Trend and Seasonality = Fehler, Trend und Saisonabhängigkeit), wie von [Hyndman und Kollegen (2008)](https://www.springer.com/us/book/9783540719168) beschrieben. Dabei versucht der Algorithmus insbesondere die folgenden Kombinationen:

1. ANA (Additive error, No trend, Additive seasonality = Additiver Fehler, Kein Trend, Additive Saisonabhängigkeit)
1. AAA (Additive error, Additive trend, Additive seasonality = Additiver Fehler, Additiver Trend, Additive Saisonabhängigkeit)
1. MNM (Multiplicative error, No trend, Multiplicative seasonality = Multiplikativer Fehler, Kein Trend, Multiplikative Saisonabhängigkeit)
1. MNA (Multiplicative error, No trend, Additive seasonality = Multiplikativer Fehler, Kein Trend, Additive Saisonabhängigkeit)
1. AAN (Additive error, Additive trend, No seasonality = Additiver Fehler, Additiver Trend, Keine Saisonabhängigkeit)

Der Algorithmus testet die Tauglichkeit jeder dieser Kombinationen, indem er die Kombination mit dem besten MAPE-Wert (Mean Absolute Percentage Error, Mittlerer absoluter prozentualer Fehler) auswählt. Liegt jedoch der MAPE-Wert des besten Zeitreihenmodells über 15 %, wird funktionale Filterung angewendet. Bei einem Zeitreihenmodell passen meist Daten mit einem hohen Grad an Wiederholbarkeit am besten (z. B. von Woche zu Woche oder von Monat zu Monat).

Nach Auswahl des Modells passt der Algorithmus die Ergebnisse basierend auf Feiertagen und jährlicher Saisonalität an. Für Feiertage überprüft der Algorithmus, ob einer der folgenden Feiertage im Datumsbereich des Berichts vorhanden ist:

* Memorial Day (nur USA)
* 4. Juli (nur USA)
* Thanksgiving (nur USA)
* Black Friday (nur USA)
* Cyber Monday (nur USA)
* 24.–26. Dezember
* 1. Januar
* 31. Dezember

Diese Feiertage wurden anhand umfangreicher statistischer Analysen einer großen Anzahl von Datenpunkten ausgewählt, um die Feiertage zu ermitteln, die den größten Einfluss in den meisten Kundentrends gezeigt haben. Die Liste ist zwar nicht für alle Kunden oder Geschäftszyklen vollständig, wir haben jedoch festgestellt, dass eine Berücksichtigung dieser Feiertage die Zuverlässigkeit des Algorithmus insgesamt für fast alle Kundendatensätze steigern konnte.

Nach Auswahl des Modells und der Identifizierung der im Berichtszeitraum befindlichen Feiertage fährt der Algorithmus wie folgt fort:

1. Erstellen Sie den Anomaliereferenzzeitraum, der bis zu 35 Tage vor dem Datumsbereich der Berichterstellung umfasst, und einen übereinstimmenden Datumsbereich, der älter ist als ein Jahr (bei Bedarf die Tabellage, wenn erforderlich, und alle anwendbaren Feiertage, die in einem anderen Kalendertag des vorherigen Jahres aufgetreten sein könnten).
1. Er testet, ob im aktuellen Zeitraum (außer dem Vorjahr) Feiertage vorhanden sind, die laut den aktuellsten Daten eine Anomalität darstellen.
1. Wenn der Feiertag im aktuellen Datumsbereich als anormal betrachtet wird, passt der Algorithmus den erwarteten Wert und das Konfidenzintervall des aktuellen Feiertags anhand des Feiertags aus dem Vorjahreszeitraum an (unter Berücksichtigung von 2 Tagen vorher und nachher). Die Korrektur für den aktuellen Feiertag erfolgt auf Grundlage des niedrigsten MAPE-Wertes von:

   1. Additive Effekte
   1. Multiplikative Effekte
   1. Differenz zum Vorjahr

Beachten Sie im folgenden Beispiel die deutliche Verbesserung der Performance an Weihnachten und Neujahr:

![](assets/anomaly_statistics.png)

## Anomaly detection for hourly granularity {#section_014C9E9209AF43F8A03D5D46E3B3AEE7}

Stündliche Daten basieren auf der gleichen Vorgehensweise des zeitreihenbasierten Algorithmus wie beim Algorithmus für tägliche Granularität: Allerdings setzt der Algorithmus hier primär auf zwei Trendmuster: den 24-Stunden-Zyklus sowie den Wochenende-Wochentag-Zyklus. Um diese beiden saisonalen Effekte zu erfassen, erstellt der stündliche Algorithmus zwei separate Modelle (für ein Wochenende und einen Wochentag), wobei er auf die gleiche Weise wie oben beschrieben vorgeht.

Das Trainingfenster für stündliche Trends basiert auf einem 336-Stunden rückwärts gerichteten Fenster.

## Anomaly detection for weekly and monthly granularities {#section_5D421576BFBC4B24A58DFCC0A6407545}

Da wöchentliche und monatliche Trends nicht die gleichen wöchentlichen oder täglichen Trends wie bei täglicher oder stündlicher Granularität aufweisen, wird ein separater Algorithmus verwendet. Für wöchentliche oder monatliche Granularität wird ein aus zwei Schritten bestehender Ausreißererkennungsalgorithmus eingesetzt, der als GESD-Test (Generalized Extreme Studentized Deviate, Generalisierte Extreme Studentisierte Abweichung) bezeichnet wird. Dieser Test betrachtet die maximale Anzahl der zu erwartenden Anomalien kombiniert mit dem angepassten Box-Plot-Ansatz (ein nichtparametrisches Verfahren zur Erkennung von Ausreißern), um die maximale Anzahl von Ausreißern zu ermitteln. Die beiden Schritte sehen wie folgt aus:

1. Angepasste Box-Plot-Funktion: Diese Funktion ermittelt die maximale Anzahl von Anomalien aus den eingegebenen Daten.
1. GESD-Funktion: Wird mit der Ausgabe aus Schritt 1 auf die eingegebenen Daten angewendet.

Dann zieht der Anomalieerkennungsschritt „Feiertag und Vorjahres-Saisonabhängigkeit“ die Daten aus dem Vorjahr von den Daten dieses Jahres ab und geht die Daten dann wiederholt nach dem oben beschriebenen zweistufigen Verfahren durch, um zu überprüfen, dass die Anomalien saisonal korrekt sind. Jede dieser Datumsgranularitäten verwendet ein 15 Zeiträume zurückliegendes Zeitfenster, in dem der für den Bericht ausgewählte Datumsbereich liegt (entweder 15 Monate oder 15 Wochen), sowie einen entsprechenden Datumsbereich, der 1 Jahr vor dem Trainigszeitraum liegt.
