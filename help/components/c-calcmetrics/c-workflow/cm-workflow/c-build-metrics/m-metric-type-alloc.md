---
description: Informationen
title: Metriktyp und Attribution
feature: Calculated Metrics
exl-id: 3fb98227-e2ef-4829-ae84-812f845470ee
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 69%

---

# Metriktyp und Attribution

Beim [Erstellen einer berechneten Metrik](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) können Sie den Metriktyp und das Attributionsmodell angeben.

## Metriktyp

So geben Sie den Metriktyp beim Erstellen einer berechneten Metrik an:

1. Wählen Sie das Zahnradsymbol neben der Metrik aus, deren Typ Sie auswählen möchten.

   ![](assets/cm_type_alloc.png)

1. Wählen Sie aus den folgenden Optionen:

   | Metriktyp | Definition |
   |---|---|
   | Standard | Diese Metriken sind dieselben, die auch in der Standard-[!DNL Analytics]-Berichterstellung verwendet werden. Wenn eine Formel aus einer einzelnen Standardmetrik besteht, zeigt sie die gleichen Daten wie das nicht berechnete Metrikgegenstück an. Standardmetriken eignen sich zum Erstellen berechneter Metriken, die speziell für die einzelnen Einzelposten gelten. Beispiel: [Bestellungen]/[Besuche] teilt die Bestellungen für diesen Einzelposten durch die Anzahl der Besuche für den Posten. |
   | Gesamtsumme | Verwenden Sie für jeden Zeileneintrag die Gesamtsumme für den Berichtszeitraum. Wenn eine Formel aus einer einzelnen Gesamtsummen-Metrik bestand, wurde für jeden Zeileneintrag dieselbe Gesamtanzahl angezeigt. Gesamtmetriken sind nützlich, um berechnete Metriken zu erstellen, die mit den Gesamtdaten der Site verglichen werden. Beispiel: [Bestellungen]/[Gesamtbesuche] zeigt den Anteil der Bestellungen für ALLE Site-Besuche und nicht nur die Besuche für den speziellen Zeileneintrag. |

## Funktionsweise der linearen Zuordnung

[Attribution](/help/analyze/analysis-workspace/attribution/overview.md) wird anhand der Zuordnungsmodelle in berechneten Metriken bewertet.

Eine vollständige Liste der nicht standardmäßigen Attributionsmodelle und unterstützten Lookback-Fenster finden Sie unter [Attributionsmodelle und Lookback-Fenster](/help/analyze/analysis-workspace/attribution/models.md).

Das folgende Beispiel zeigt, wie berechnete Metriken mit linearer Zuordnung in Berichten funktionieren:

| | Treffer 1 | Treffer 2 | Treffer 3 | Treffer 4 | Treffer 5 | Treffer 6 | Treffer 7 |
|--- |--- |--- |--- |--- |--- |--- |--- |
| Eingereichte Daten | PROMO A | – | PROMO A | PROMO B | – | PROMO C | 10$ |
| Letztkontakt-eVar | PROMO A | PROMO A | PROMO A | PROMO B | PROMO B | PROMO C | 10$ |
| Erstkontakt-eVar | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | PROMO A | 10$ |
| Beispieleigenschaft | PROMO A | – | PROMO A | PROMO B | – | PROMO C | 10$ |

In diesem Beispiel wurden die Werte A, B und C in eine Variable für die Treffer 1, 3, 4 und 6 gesendet, bevor ein Kauf in Höhe von 10 USD bei Treffer 7 getätigt wurde. In der zweiten Zeile werden dieses Werte bei Treffern auf Grundlage von Letztkontaktbesuchen gespeichert. In der dritten Zeile wird das Speichern auf Grundlage des Erstkontaktbesuchs dargestellt. Zu guter Letzt stellt die letzte Zeile dar, wie Daten aus einer Eigenschaft aufgezeichnet würden, bei denen kein Speichern vorgesehen ist.

