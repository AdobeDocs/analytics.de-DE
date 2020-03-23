---
description: 'null'
title: Übersicht über das Attributionsbedienfeld
uuid: bb345642-4f45-4fb8-82d0-803248dd52ea
translation-type: tm+mt
source-git-commit: 3869385b9ad17cbea5e7a4e09bd06d5f0b53dd3c

---


# Übersicht über das Attributionsbedienfeld

>[!IMPORTANT] Das Attributionsbedienfeld ist für Kunden mit Adobe Analytics Ultimate-, Prime-, Select- und Foundation-SKUs verfügbar.

Das Attributionsbedienfeld ist eine Funktion von [Attribution IQ](../../attribution-iq.md), mit der Sie viele neue Arten von Attributionsmodellen zu Freiformtabellen, Visualisierungen und berechneten Metriken hinzufügen können. Alle Attributionsmodelle weisen zwei Komponenten auf:

* **Attributionsmodell:** Das Modell beschreibt die Verteilung der Konversionen auf die Hits in einer Gruppe. Zum Beispiel Erstkontakt oder Letztkontakt
* **Attributions-Lookback-Fenster:** Das Lookback-Fenster beschreibt, welche Gruppierungen der Hits für das jeweilige Modell berücksichtigt werden. Beispiel: Besuch oder Besucher.

## Attributionsmodelle

| Benutzeroberflächensymbol | Attributionsmodell | Definition | Verwendungsbereiche |
| --- | --- | --- | --- |
| ![Letztkontakt](assets/last_touch1.png) | Letztkontakt | 100 % werden dem Touchpoint zugeschrieben, der zuletzt vor der Konversion aufgetreten ist. | Das einfachste und gängigste Attributionsmodell. Es wird häufig für Konversionen mit einem kurzen Überlegungszyklus verwendet. Letztkontakt wird häufig durch Teams verwendet, die Suchmaschinen-Marketing verwalten oder Schlüsselwörter für die interne Suche analysieren. |
| ![Erstkontakt](assets/first_touch.png) | Erstkontakt | 100 % werden dem Touchpoint zugeschrieben, der zuerst im Attributions-Lookback-Fenster angezeigt wird. | Ein weiteres allgemeines Attributionsmodell, das sich für die Analyse von Marketing-Kanälen eignet, die das Markenbewusstsein oder die Kundenakquise ankurbeln sollen. Es wird häufig von Teams für Display- oder Social-Media-Marketing verwendet, eignet sich jedoch auch für das Bewerten der Produktempfehlungseffektivität vor Ort. |
| ![Selber Kontakt](assets/same_touch.png) | Selber Kontakt | 100 % werden dem Hit zugeschrieben, bei dem die Konversion erfolgte. Wenn ein Touchpoint nicht bei demselben Hit erfolgt wie eine Konversion, wird er unter „Keine“ zusammengefasst. | Dies ist ein hilfreiches Modell beim Evaluieren des zum Zeitpunkt der Konversion angezeigten Inhalts oder Kundenerlebnisses. Produkt- oder Designteams verwenden dieses Modell oftmals, um die Effektivität einer Seite zu bewerten, auf der die Konversion auftritt. |
| ![Linear](assets/linear.png) | Linear | Ermöglicht dieselbe Gewichtung für jeden Touchpoint, der vor einer Konversion erfolgte. | Dieses Modell eignet sich für Konversionen mit längeren Überlegungszyklen oder Kundenerlebnissen, für die eine häufigere Kundeninteraktion erforderlich ist. Es wird oft von Teams genutzt, die die Benachrichtigungseffektivität von Apps messen, oder mit abonnementbasierten Produkten verwendet. |
| ![U-förmig](assets/u_shaped.png) | U-förmig | Der ersten Interaktion werden 40 % zugeschrieben, der letzten Interaktion 40 %. Die verbleibenden 20 % werden auf alle dazwischen liegenden Touchpoints aufgeteilt. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Konversionen mit zwei Touchpoints werden jedem 50 % zugeschrieben. | Ein passendes Modell für diejenigen, die Interaktionen schätzen, die eine Konversion gestartet oder beendet haben, aber dennoch unterstützende Interaktionen erkennen möchten. Die U-förmige Attribution wird oft durch Teams verwendet, die einen ausgeglicheneren Ansatz verwenden, jedoch Kanälen mehr Gewichtung zuteilen möchten, die eine Konversion gestartet oder beendet haben. |
| ![J-förmig](assets/j_shaped.png) | J-förmig | Der letzten Interaktion werden 60 % zugeschrieben, der ersten Interaktion werden 20 % zugeschrieben. Die restlichen 20 % werden auf alle dazwischen liegenden Touchpoints aufgeteilt. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Konversionen mit zwei Touchpoints der letzten Interaktion 75 % zu geschrieben und der ersten 25 %. | Dieses Modell ist ideal für diejenigen, die Eröffnung und Abschluss priorisieren, sich aber auf den Abschluss konzentrieren möchten. Die J-förmige Attribution wird oft durch Teams verwendet, die einen ausgeglicheneren Ansatz verwenden und Kanälen mehr Gewichtung zuteilen möchten, auf denen eine Konversion abgeschlossen wurde. |
| ![Umgekehrt J-förmig](assets/inverse_j.png) | Umgekehrtes J | Der ersten Interaktion werden 60 % zugeschrieben, der letzten Interaktion 20 %. Die verbleibenden 20 % werden auf alle dazwischen liegenden Touchpoints aufgeteilt. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Konversionen mit zwei Touchpoints der ersten Interaktion 75 % zu geschrieben und der letzten 25 %. | Dieses Modell ist ideal für diejenigen, die Eröffnung und Abschluss priorisieren, sich aber auf die Eröffnung konzentrieren möchten. Die Attribution mit umgekehrtem J wird oft durch Teams verwendet, die einen ausgeglicheneren Ansatz verwenden und Kanälen mehr Gewichtung zuteilen möchten, auf denen eine Konversion begonnen wurde. |
| ![Benutzerspezifisch](assets/custom.png) | Benutzerspezifisch | Ermöglicht Ihnen die Angabe der Gewichtungen, die Sie für Erstkontakt-Punkte, Letztkontakt-Punkte und dazwischen liegende Touchpoints festlegen möchten. Die angegebenen Werte werden auf 100 % normalisiert, selbst wenn die eingegebenen benutzerdefinierten Zahlen zusammen nicht 100 ergeben. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Interaktionen mit zwei Touchpoints wird der mittlere Parameter ignoriert. Die ersten und letzten Touchpoints werden dann auf 100 % normalisiert und die Gewichtung wird entsprechend zugeschrieben. | Dieses Modell ist perfekt für diejenigen, die eine vollständige Kontrolle über ihr Attributionsmodell wünschen und spezielle Bedürfnisse haben, die andere Zuordnungsmodelle nicht erfüllen. |
| ![Zeitverfall](assets/time_decay.png) | Zeitverfall | Folgt einem exponentiellen Abfall mit einem benutzerdefinierten Parameter für die Halbwertszeit, wobei der Standardwert 7 Tage ist. Die Gewichtung der einzelnen Kanäle hängt von der Zeit ab, die zwischen dem Beginn des Touchpoints und der letztendlichen Konversion verstrichen ist. Die Formel, die zur Bestimmung der Gewichtung verwendet wird, lautet `2^(-t/halflife)`, wobei `t` die Zeit zwischen einem Touchpoint und einer Konversion ist. Alle Touchpoints werden dann auf 100 % normalisiert. | Ideal für Teams, die regelmäßig Videowerbung betreiben oder Marketing im Zusammenhang mit Ereignissen mit festem Datum durchführen. Je länger eine Konversion nach einem Marketing-Ereignis erfolgt, desto geringer ist die zugeschriebene Gewichtung. |
| ![Beitrag](assets/participation.png) | Beitrag | 100 % Gewichtung für alle eindeutigen Touchpoints. Die Gesamtanzahl der Konversionen ist im Vergleich zu anderen Attributionsmodellen überhöht. Durch den Beitrag werden Kanäle dedupliziert, die mehrmals angezeigt werden. | Ausgezeichnet, um zu verstehen, wie häufig Kunden einer bestimmten Interaktion ausgesetzt sind. Medienunternehmen verwenden dieses Modell häufig zur Berechnung der Content Velocity. Einzelhandelsunternehmen verwenden dieses Modell oft, um zu verstehen, welche Teile ihrer Site für die Konversion von entscheidender Bedeutung sind. |

> [!NOTE] Das folgende algorithmische Zuordnungsmodell ist derzeit in [Adobe Analytics Labs](https://docs.adobe.com/content/help/en/analytics/analyze/tech-previews/overview.html) verfügbar und wird möglicherweise Teil einer allgemeinen Version sein.

| Benutzeroberflächensymbol | Attributionsmodell | Definition | Verwendungsbereiche |
| --- | --- | --- | --- |
| ![Algorithmisch](assets/algorithmic.png) | [Algorithmisch](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/algorithmic.md) | Verwendet statistische Verfahren, um die optimale Zuordnung der Gutschrift für die ausgewählte Metrik dynamisch zu bestimmen. | Nützlich, um bei der Auswahl des richtigen Zuordnungsmodells für Ihr Unternehmen Ratschläge oder Heuristik zu vermeiden. |

## Lookback-Fenster

Ein Lookback-Fenster ist der Zeitraum, der für eine Konversion rückblickend bei der Erfassung von Touchpoints berücksichtigt werden sollte. Attributionsmodelle, die der ersten Interaktion mehr Gewicht zuschreiben, sehen bei der Anzeige verschiedener Lookback-Fenster größere Unterschiede.

* **Besuchs-Lookback-Fenster:** Sieht bis zum Beginn eines Besuchs zurück, bei dem eine Konversion stattgefunden hat. Besuchs-Lookback-Fenster sind klein, da sie nicht über den Besuch hinausblicken. Besuchs-Lookback-Fenster berücksichtigen die geänderte Besuchsdefinition in Virtual Report Suites.

* **Besucher-Lookback-Fenster:** Betrachtet alle Besuche bis zum 1. des Monats des aktuellen Datumsbereichs. Besucher-Lookback-Fenster sind groß, da sie viele Besuche umfassen können. Wenn der Berichts-Datumsbereich beispielsweise zwischen dem 15. September und dem 30. September liegt, liegt der Besucher-Lookback-Datumsbereich zwischen dem 1. September und dem 30. September.

## Beispiel

Siehe folgendes Beispiel:

1. Am 15. September gelangt ein Besucher über Paid Search zu Ihrer Site und verlässt sie dann.
2. Am 18. September gelangt der Besucher erneut über einen Link in sozialen Medien zu Ihrer Site, den er von einem Freund erhalten hat. Er fügt mehrere Artikel zum Warenkorb hinzu, erwirbt aber nichts.
3. Am 24. September sendet Ihr Marketing-Team eine E-Mail mit einem Coupon für einige der Artikel im Warenkorb. Der Coupon wird angewendet, der Besucher ruft aber mehrere andere Websites auf, um zu sehen, ob andere Coupons verfügbar sind. Er findet einen weiteren über eine Display-Anzeige und kauft dann letztendlich für 50 Euro ein.

Je nach Lookback-Fenster und Attributionsmodell erhalten Kanäle eine unterschiedliche Gewichtung. Im Folgenden finden Sie einige interessante Beispiele:

* Bei Verwendung von **Erstkontakt** und einem **Besuchs-Lookback-Fenster** betrachtet die Attribution nur den dritten Besuch. E-Mail kam vor Display-Anzeige, sodass E-Mail 100 % des Kaufs von 50 Euro zugeschrieben werden.
* Mithilfe von **Erstkontakt** und einem **Besucher-Lookback-Fenster** betrachtet die Attribution alle drei Besuche. Paid Search kam zuerst, sodass Paid Search 100 % des Kaufs von 50 Euro zugeschrieben werden.
* Bei Verwendung eines **linearen** Fensters und eines **Besuchs-Lookback-Fensters** wird die Gewichtung zwischen E-Mail und Display-Anzeige aufgeteilt. Beiden Kanälen werden jeweils 25 Euro zugeschrieben.
* Die Gewichtung wird mithilfe eines **linearen** Fensters **und eines** Besucher-Lookback-Fensters zwischen Paid Search, Social Media, E-Mail und Display-Anzeige aufgeteilt. Jedem Kanal werden für diesen Kauf 12,50 Euro zugeschrieben.
* Mithilfe des **J-förmigen** Fensters und eines **Besucher-Lookback-Fensters** wird die Gewichtung zwischen Paid Search, Social Media und Display-Anzeige aufgeteilt.
   * Der Display-Anzeige werden 60 %, also 30 Euro, zugeschrieben.
   * Paid Search werden 20 %, also 10 Euro, zugeschrieben.
   * Die restlichen 20 % werden zwischen Social Media und E-Mail aufgeteilt (jeweils 5 Euro).
* Bei Verwendung von **Zeitverfall** und einem **Besucher-Lookback-Fenster** wird die Gewichtung zwischen Paid Search, Social Media, E-Mail und Display-Anzeige aufgeteilt. Verwendung der standardmäßigen 7-Tage-Halbwertszeit:
   * Abstand von 0 Tagen zwischen Display-Touchpoint und Konversion. `2^(-0/7) = 1`
   * Abstand von 0 Tagen zwischen E-Mail-Touchpoint und Konversion. `2^(-0/7) = 1`
   * Abstand von 6 Tagen zwischen Social-Media-Touchpoint und Konversion. `2^(-6/7) = 0.552`
   * Abstand von 9 Tagen zwischen Paid-Search-Touchpoint und Konversion. `2^(-9/7) = 0.41`
   * Die Normalisierung dieser Werte führt zu Folgendem:
      * Display-Anzeige: 33,8 %, 16,88 Euro
      * E-Mail: 33,8 %, 16,88 Euro
      * Social Media: 18,6 %, 9,32 Euro
      * Paid Search: 13,8 %, 6,92 Euro

> [!TIP] Andere Konversionsereignisse wie Bestellungen oder benutzerspezifische Ereignisse werden ebenfalls aufgeteilt, wenn die Gewichtung für mehrere Kanäle erfolgt. Wenn beispielsweise zwei Kanäle mit einem linearen Attributionsmodell zu einem benutzerspezifischen Ereignis beitragen, erhalten beide Kanäle 0,5 des benutzerspezifischen Ereignisses. Diese Ereignis-Teilbereiche werden über alle Besuche summiert und dann zur Berichterstellung auf die nächste Ganzzahl gerundet.

## Attribution für Marketing-Kanäle

Als Marketing-Kanäle eingeführt wurden, hatten sie nur die Dimensionen „Erstkontakt“ und „Letztkontakt“. Mit diesen zusätzlichen Attributionsmodellen sind explizite Dimensionen für Erst- und Letztkontakt nicht mehr erforderlich. Adobe bietet allgemeine **Marketing-Kanal**-Dimensionen, damit diese mit Ihrem bevorzugten Attributionsmodell verwendet werden können. Diese allgemeinen Dimensionen der Marketing-Kanäle verhalten sich identisch mit den Dimensionen des Letztkontakt-Kanals, sind jedoch anders gekennzeichnet, um Verwirrung bei der Verwendung von Marketing-Kanälen mit einem anderen Attributionsmodell zu vermeiden.

Da die Marketing-Kanal-Dimensionen von einer traditionellen Besuchsdefinition abhängen (wie in den Verarbeitungsregeln definiert), kann ihre Besuchsdefinition nicht mit Virtual Report Suites geändert werden.

## Attribution mit Variablen mit mehreren Werten

Einige Dimensionen in Analytics können bei einem einzelnen Hit mehrere Werte enthalten. Häufige Beispiele sind Listenvariablen und die Produktvariable.

Wenn die Attribution auf Hits mit mehreren Werten angewendet wird, erhalten alle Werte im selben Hit dieselbe Gewichtung. Da viele Werte diese Gewichtung erhalten können, kann sich die Berichtssumme von der Summe der einzelnen Zeileneinträge unterscheiden. Die Berichtssumme wird dedupliziert, während jeder einzelne Dimensionswert korrekt gewichtet wird.

## Attribution mit Segmentierung

Die Attribution wird immer vor der Segmentierung ausgeführt und die Segmentierung wird ausgeführt, bevor Berichtsfilter angewendet werden. Dieses Konzept gilt auch für Virtual Report Suites, die Segmente verwenden.

Wenn Sie z. B. eine VRS mit angewendetem Segment „Hits anzeigen“ erstellen, können Sie mithilfe einiger Attributionsmodelle andere Kanäle in einer Tabelle sehen.

![Schreibgeschützte Virtual Report Suite](assets/vrs-aiq-example.png)

> [!NOTE] Wenn ein Segment Treffer unterdrückt, die Ihre Metrik enthalten, werden diese Metrikinstanzen keiner Dimension zugeordnet. Bei einem ähnlichen Berichtsfilter werden jedoch lediglich einige Dimensionswerte ausgeblendet, ohne dass dies Auswirkungen auf die pro Zuordnungsmodell verarbeiteten Metriken hat. Daher können Segmente und Filter mit vergleichbaren Definitionen manchmal niedrigere Werte für das Segment zurückgeben.
