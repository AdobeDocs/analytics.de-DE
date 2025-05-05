---
source-git-commit: 9a2d4c582b6a3946b658924851e5b5ada2f5a7ee
workflow-type: tm+mt
source-wordcount: '2353'
ht-degree: 46%

---
# Snippets

## Vorgängerversion von Report Builder {#legacy-arb}

>[!IMPORTANT]
>
>Eine neue und optimierte [Report Builder](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/rb-overview) wurde am 16. Oktober 2024 veröffentlicht. Es wird in Mac, Windows und Webbrowsern unterstützt.
>Diese alte Add-In-Version von Report Builder funktioniert weiterhin. Sie können [alte Arbeitsmappen) in ](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/convert-workbooks) neue Report Builder konvertieren.

## Mitteilung zum Ende der Nutzungsdauer von Reports & Analytics {#ra-eol}

>[!IMPORTANT]
>
>Mit **17. Januar 2024** Adobe Reports &amp; Analytics und die zugehörigen Berichte und Funktionen eingestellt. Zu diesem Zeitpunkt funktionierten Reports &amp; Analytics und alle zugehörigen Berichte und Zeitpläne nicht mehr. Die Berichte, Visualisierungen und zugrunde liegenden Technologien von Reports &amp; Analytics entsprechen nicht mehr den technologischen Standards von Adobe. Die meisten Reports &amp; Analytics-Funktionen sind in Analysis Workspace verfügbar. Weitere Informationen finden Sie unter [Verwenden von Vorlagen](/help/analyze/analysis-workspace/templates/use-templates.md).
> 
>Seit der Veröffentlichung von Analysis Workspace im Jahr 2015 wurden die Funktionen und Leistungsmerkmale von Reports &amp; Analytics in Analysis Workspace verschoben, und es wurde ein Schwellenwert für die Workflow-Parität erreicht. In dieser Mitteilung wird der End-of-Life-Prozess erläutert.
>
>Erfahren Sie mehr über die [Mitteilung zum Ende der Nutzungsdauer](https://www.adobe.com/go/analytics_rnaeol_de) von Reports &amp; Analytics.

## Sortieroptionen von Komponenten {#components-sort-options}

| Option | Funktion |
|---------|----------|
| [!UICONTROL **Empfohlen**] | Sortiert Komponenten nach den am Anfang der Liste empfohlenen Komponenten. Komponenten, die am häufigsten und zuletzt von Ihnen oder anderen in Ihrem Unternehmen verwendet werden, werden weiter oben in der Liste angezeigt. |
| [!UICONTROL **Alphabetisch**] | Sortiert Komponenten alphabetisch. |
| [!UICONTROL **Kategorisch**] | Sortiert Komponenten nach Komponententyp (Dimension, Metrik, Segment, Datumsbereich). |

{style="table-layout:auto"}

## Eingeschränkte Testphase der Version {#release-limited-testing}

>[!AVAILABILITY]
>
>Die in diesem Artikel beschriebene Funktion befindet sich in der eingeschränkten Testphase der Version und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Analytics-Veröffentlichungsprozess finden Sie unter [Adobe Analytics-Funktionsversionen](/help/release-notes/releases.md).

## Abschnitt zur eingeschränkten Testphase der Veröffentlichung {#release-limited-testing-section}

>[!AVAILABILITY]
>
>Die in diesem Abschnitt beschriebene Funktion befindet sich in der eingeschränkten Testphase der Version und ist möglicherweise noch nicht in Ihrer Umgebung verfügbar. Diese Anmerkung wird entfernt, wenn die Funktion allgemein verfügbar ist. Informationen zum Analytics-Veröffentlichungsprozess finden Sie unter [Adobe Analytics-Funktionsversionen](/help/release-notes/releases.md).


## Plug-in-Haftungsausschluss {#plug-in}

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe bei diesem Plug-in benötigen, wenden Sie sich an das für Ihr Unternehmen zuständige Adobe-Kunden-Team. Sie können ein Treffen mit einer Beraterin oder einem Berater zur Unterstützung arrangieren.


## Nur für Bestandskunden verfügbar {#available-existing-customers}

>[!AVAILABILITY]
>
>Die in diesem Abschnitt beschriebene Funktion steht nur Bestandskunden zur Verfügung, die bereits über eine Lizenz für die Funktion verfügen. Die Funktion wird bestehenden oder neuen Kunden nicht mehr als zusätzliches Add-on angeboten.
>



## Attributionsmodelle {#attribution-models-details}

Ein Attributionsmodell bestimmt, welchen Dimensionselementen eine Metrik gutgeschrieben wird, wenn im Lookback-Fenster einer Metrik mehrere Werte angezeigt werden. Attributionsmodelle werden nur angewendet, wenn im Lookback-Fenster mehrere Dimensionselemente festgelegt sind. Wenn nur ein einzelnes Dimensionselement festgelegt ist, erhält dieses Dimensionselement unabhängig vom verwendeten Attributionsmodell eine 100%ige Gutschrift.

| Symbol | Attributionsmodell | Definition |
| :---: | :--- | --- |
| ![Letztkontakt](/help/assets/icons/AttributeLastTouch.svg) | Letztkontakt | 100 % werden dem Touchpoint zugeschrieben, der zuletzt vor der Konversion aufgetreten ist. Dieses Attributionsmodell ist in der Regel der Standardwert für jede Metrik, bei der kein anderes Attributionsmodell angegeben ist. Unternehmen verwenden dieses Modell in der Regel, wenn die Konversionszeit relativ kurz ist, z. B. bei der Analyse interner Suchbegriffe. |
| ![Erstkontakt](/help/assets/icons/AttributeFirstTouch.svg) | Erstkontakt | Gibt dem Touchpoint, der zuerst im Attributions-Lookback-Fenster angezeigt wird, eine 100%ige Gewichtung. Unternehmen verwenden dieses Modell in der Regel, um Markenwahrnehmung oder Kundenakquise zu verstehen. |
| ![Linear](/help/assets/icons/AttributeLinear.svg) | Linear | Gibt jedem Touchpoint vor der Konversion dieselbe Gewichtung. Dies ist besonders dann nützlich, wenn die Konversionszyklen länger sind oder häufiger Kundeninteraktionen erfordern. Unternehmen verwenden in der Regel dieses Attributionsmodell zur Messung der Effektivität von Mobile-App-Benachrichtigungen oder mit abonnementbasierten Produkten. |
| ![Beitrag](/help/assets/icons/AttributeParticipation.svg) | Beitrag | 100 % Gewichtung für alle eindeutigen Touchpoints. Da jeder Touchpoint zu 100 % angerechnet wird, summieren sich die Daten von Metriken in der Regel auf mehr als 100 %. Wenn ein Dimensionselement mehrmals separat angezeigt wird, was zu einer Konversion führt, werden die Werte auf 100 % dedupliziert. Dieses Attributionsmodell ist ideal in Situationen, in denen Sie verstehen möchten, welche Touchpoints Kundinnen und Kunden am meisten ausgesetzt sind. Medienunternehmen verwenden dieses Modell normalerweise zur Berechnung der Inhaltsgeschwindigkeit. Einzelhandelsorganisationen verwenden dieses Modell in der Regel, um zu verstehen, welche Teile ihrer Site für die Konversion wichtig sind. |
| ![Selber Kontakt](/help/assets/icons/AttributeSameTouch.svg) | Selber Kontakt | Gibt dem Ereignis, bei dem die Konversion stattgefunden hat, eine 100%ige Gutschrift. Wenn ein Touchpoint nicht im selben Ereignis wie eine Konversion auftritt, wird er in Buckets unter „None“ („Keine„) erfasst. Dieses Attributionsmodell wird manchmal damit gleichgesetzt, dass es gar kein Attributionsmodell hat. Dies ist nützlich in Szenarien, in denen Sie keine Werte von anderen Ereignissen wünschen, die beeinflussen, wie eine Metrik Dimensionselementen zuordnet. Produkt- oder Design-Teams können dieses Modell verwenden, um die Effektivität einer Seite zu bewerten, auf der Konversionen stattfinden. |
| ![U-förmig](/help/assets/icons/AttributeUShaped.svg) | U-Form | Der ersten Interaktion werden 40 % zugeschrieben, der letzten Interaktion 40 %. Die verbleibenden 20 % werden auf alle dazwischen liegenden Touchpoints aufgeteilt. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Konversionen mit zwei Touchpoints werden beide mit 50 % angerechnet. Dieses Attributionsmodell eignet sich am besten für Szenarien, in denen Sie die erste und letzte Interaktion am meisten schätzen, aber zusätzliche Interaktionen dazwischen nicht völlig ausschließen möchten. |
| ![J-Kurve](/help/assets/icons/AttributeJCurve.svg) | J-Kurve | Der letzten Interaktion werden 60 % zugeschrieben, der ersten Interaktion werden 20 % zugeschrieben. Die restlichen 20 % werden auf alle dazwischen liegenden Touchpoints aufgeteilt. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Konversionen mit zwei Touchpoints werden der letzten Interaktion 75 % und der ersten 25 % zugeschrieben. Ähnlich wie U-förmig begünstigt dieses Attributionsmodell die erste und die letzte Interaktion, stärker jedoch die letzte Interaktion. |
| ![Umgekehrtes J](/help/assets/icons/AttributeInverseJ.svg) | Umgekehrtes J | Der ersten Interaktion werden 60 % zugeschrieben, der letzten Interaktion 20 %. Die verbleibenden 20 % werden auf alle dazwischen liegenden Touchpoints aufgeteilt. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Konversionen mit zwei Touchpoints werden der ersten Interaktion 75 % und der letzten Interaktion 25 % zugeschrieben. Ähnlich wie J-förmig bevorzugt dieses Attributionsmodell die erste und die letzte Interaktion, stärker jedoch die erste Interaktion. |
| ![Zeitverfall](/help/assets/icons/AttributeTimeDecay.svg) | Zeitabfall | Folgt einem exponentiellen Abfall mit einem benutzerdefinierten Parameter für die Halbwertszeit, wobei der Standardwert 7 Tage ist. Die Gewichtung der einzelnen Kanäle hängt von der Zeit ab, die zwischen dem Beginn des Touchpoints und der letztendlichen Konversion verstrichen ist. Die Formel, die zur Bestimmung der Gewichtung verwendet wird, lautet `2^(-t/halflife)`, wobei `t` die Zeit zwischen einem Touchpoint und einer Konversion ist. Alle Berührungspunkte werden dann auf 100 % normalisiert. Ideal für Szenarien, in denen Sie die Attribution anhand eines bestimmten und signifikanten Ereignisses messen möchten. Je länger nach diesem Ereignis eine Konversion stattfindet, desto weniger Anerkennung wird erhalten. |
| ![Benutzerspezifisch](/help/assets/icons/AttributeCustom.svg) | Anpassen | Hier können Sie die Gewichtungen angeben, die Sie dem ersten Touchpoint, dem letzten Touchpoint und allen dazwischen liegenden Touchpoints zuweisen möchten. Die angegebenen Werte werden auf 100 % normalisiert, selbst wenn die eingegebenen benutzerdefinierten Zahlen zusammen nicht 100 ergeben. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Interaktionen mit zwei Touchpoints wird der mittlere Parameter ignoriert. Der erste und der letzte Berührungspunkt werden dann auf 100 % normalisiert und die Gutschrift wird entsprechend zugewiesen. Dieses Modell eignet sich ideal für Analysten, die die volle Kontrolle über ihr Attributionsmodell haben möchten und spezifische Anforderungen haben, die andere Attributionsmodelle nicht erfüllen. |
| ![Algorithmisch](/help/assets/icons/AttributeAlgorithmic.svg) | Algorithmisch | Verwendet statistische Verfahren, um die optimale Zuordnung von Gutschriften für die ausgewählte Metrik dynamisch zu bestimmen. Der für die Zuordnung verwendete Algorithmus basiert auf der Harsanyi-Dividende aus der kooperativen Spieltheorie. Die Harsanyi-Dividende ist eine Verallgemeinerung der Shapley-Wertlösung (die nach Lloyd Shapley, einem Nobelpreisträger für Ökonomie, benannt wurde) zur Verteilung von Gutschriften unter den Spielern in einem Spiel mit ungleichen Beiträgen zum Ergebnis.<br>Auf hoher Ebene wird die Attribution als eine Koalition von Akteuren berechnet, an die ein Überschuss gerecht verteilt werden muss. Die Überschussverteilung jeder Koalition wird anhand des Überschusses bestimmt, der zuvor von jeder Subkoalition (oder zuvor teilnehmenden Dimensionselementen) rekursiv erzeugt wurde. Weitere Einzelheiten finden Sie in John Harsanyis und Lloyd Shapleys Originaldokumenten: <br>Shapley, Lloyd S. (1953). A value for n-person games. *Contributions to the Theory of Games, 2(28)*, 307-317.<br>Harsanyi, John C. (1963). A simplified bargaining model for the n-person cooperative game. *International Economic Review 4(2)*, 194-220. |

{style="table-layout:auto"}

## Attributions-Lookback-Fenster {#attribution-lookback-window}

Ein Lookback-Fenster ist der Zeitraum, der für eine Konversion rückblickend bei der Erfassung von Touchpoints berücksichtigt werden sollte. Wenn ein Dimensionselement außerhalb des Lookback-Fensters festgelegt wird, wird der Wert in keine Attributionsberechnungen einbezogen.

* **14 Tage**: Schaut bis zu 14 Tage nach dem Zeitpunkt zurück, an dem die Konvertierung stattgefunden hat.
* **30 Tage**: Sieht bis zu 30 Tage nach dem Zeitpunkt der Konvertierung zurück.
* **60 Tage**: Sieht bis zu 60 Tage nach dem Zeitpunkt der Konvertierung zurück.
* **90 Tage**: Sieht bis zu 90 Tage nach dem Zeitpunkt der Konvertierung zurück.
* **Besuch**: Rückblick auf den Beginn des Besuchs, bei dem eine Konversion stattgefunden hat.
* **Besucher (Reporting-Fenster)**: Zeigt alle Besuche bis zum ersten des Monats des aktuellen Datumsbereichs an. Wenn der Datumsbereich des Berichts beispielsweise der 15. September bis zum 30. September ist, umfasst der Datumsbereich des Besucher-Lookback den 1. September bis zum 30. September. Wenn Sie dieses Lookback-Fenster verwenden, können Sie gelegentlich sehen, dass Dimensionselemente Datumsangaben außerhalb Ihres Reporting-Fensters zugeordnet werden.
* **Benutzerdefinierte Zeit:** Ermöglicht es Ihnen, ein benutzerdefiniertes Lookback-Fenster festzulegen, das anzeigt, wann eine Konversion stattgefunden hat. Sie können die Anzahl der Minuten, Stunden, Tage, Wochen, Monate oder Quartale angeben. Wenn beispielsweise am 20. Februar eine Konversion stattgefunden hat, würden in einem Lookback-Fenster von fünf Tagen alle Dimensions-Touchpoints vom 15. bis 20. Februar im Attributionsmodell ausgewertet.

## Attributionsbeispiel {#attribution-example}

Sehen Sie sich folgendes Beispiel an:

1. Am 15. September gelangt eine Person über eine Paid Search-Anzeige zu Ihrer Site und verlässt sie dann.
1. Am 18. September gelangt die Person über einen Link in sozialen Medien, den er von einer Freundin oder einem Freund erhalten hat, erneut auf Ihre Site. Er fügt mehrere Artikel zum Warenkorb hinzu, erwirbt aber nichts.
1. Am 24. September sendet Ihr Marketing-Team eine E-Mail mit einem Coupon für einige der Artikel im Warenkorb. Der Coupon wird angewendet, der Besucher ruft aber mehrere andere Websites auf, um zu sehen, ob andere Coupons verfügbar sind. Er findet einen weiteren über eine Display-Anzeige und kauft dann letztendlich für 50 Euro ein.

Je nach Lookback-Fenster und Attributionsmodell erhalten Kanäle eine unterschiedliche Gewichtung. Im Folgenden finden Sie einige Beispiele:

* Bei Verwendung von **Erstkontakt** und einem **Sitzungs-Lookback-Fenster** betrachtet die Attribution nur den dritten Besuch. E-Mail kam vor Display-Anzeige, sodass E-Mail 100 % des Kaufs von 50 US-Dollar zugeschrieben werden.

* Mithilfe von **Erstkontakt** und einem **Personen-Lookback-Fenster** betrachtet die Attribution alle drei Besuche. Paid Search kam zuerst, sodass Paid Search 100 % des Kaufs von 50 $ zugeschrieben werden.

* Bei Verwendung eines **linearen** Fensters und eines **Sitzungs-Lookback-Fensters** wird die Gewichtung zwischen E-Mail und Display-Anzeige aufgeteilt. Beiden Kanälen werden jeweils 25 $ zugeschrieben. Die Gewichtung wird mithilfe eines **linearen** Fensters und eines **Personen-Lookback-Fensters** zwischen Paid Search, Social Media, E-Mail und Display-Anzeige aufgeteilt. Jedem Kanal werden für diesen Kauf 12,50 $ zugeschrieben.

* Mithilfe des **J-förmigen** Fensters und eines **Personen-Lookback-Fensters** wird die Gewichtung zwischen Paid Search, Social Media und Display-Anzeige aufgeteilt.

   * Der Display-Anzeige werden 60 %, also 30 Euro, zugeschrieben.
   * Paid Search werden 20 %, also 10 Euro, zugeschrieben.
   * Die restlichen 20 % werden zwischen Social Media und E-Mail aufgeteilt (jeweils 5 Euro).

* Bei Verwendung von **Zeitverfall** und einem **Personen-Lookback-Fenster** wird die Gewichtung zwischen Paid Search, Social Media, E-Mail und Display-Anzeige aufgeteilt. Verwendung der standardmäßigen 7-Tage-Halbwertszeit:

   * Abstand von null Tagen zwischen Display-Touchpoint und Konversion. `2^(-0/7) = 1`
   * Abstand von null Tagen zwischen E-Mail-Touchpoint und Konversion. `2^(-0/7) = 1`
   * Abstand von sechs Tagen zwischen Social Media-Touchpoint und Konversion. `2^(-6/7) = 0.552`
   * Abstand von 9 Tagen zwischen Paid Search-Touchpoint und Konversion. `2^(-9/7) = 0.41`
   * Die Normalisierung dieser Werte führt zu Folgendem:

      * Display-Anzeige: 33,8 %, 16,88 Euro
      * E-Mail: 33,8 %, 16,88 Euro
      * Social Media: 18,6 %, 9,32 Euro
      * Paid Search: 13,8 %, 6,92 Euro

Konversionsereignisse, die in der Regel Ganzzahlen aufweisen, werden aufgeteilt, wenn die Gewichtung mehr als einem Kanal zugeschrieben wird. Wenn beispielsweise zwei Kanäle mit einem linearen Attributionsmodell zu einer Bestellung beitragen, erhalten beide Kanäle 0,5 dieser Bestellung. Diese Teilmetriken werden über alle Personen summiert und dann zur Berichterstellung auf die nächste Ganzzahl gerundet.

## Journey-Visualisierungsvergleiche {#journey-visualization-comparisons}

Verschiedene Visualisierungen in Customer Journey Analytics dienen zur Analyse der Journey, die Sie Ihren Kunden bereitstellen.

Verwenden Sie die folgenden Informationen, um die Visualisierung auszuwählen, die Ihren Anforderungen am besten entspricht.

| Funktion | Journey-Arbeitsfläche | Fallout | Fluss |
|---------|----------|---------|---------|
| **Vordefinierte Folge von Seiten** | Ja</br>Kombiniert vordefinierte und explorative Analysen. Der endgültige Pfad wird bei Verwendung vordefinierter Knoten auf dem Pfad verwendet (Besucher werden gezählt, solange sie schließlich von einem vordefinierten Knoten zum anderen wechseln). Die unmittelbar (nicht letztendlich) nächsten Knoten können ebenfalls angezeigt werden. | Ja</br> Der Pfad kann ein möglicher Pfad sein oder auf den nächsten Touchpoint beschränkt sein | Nein |
| **Explorative Sequenz von Seiten (Ad-hoc-Analyse)** | Ja</br>Kombiniert vordefinierte und explorative Analysen. Der endgültige Pfad wird bei Verwendung vordefinierter Knoten auf dem Pfad verwendet (Besucher werden gezählt, solange sie schließlich von einem vordefinierten Knoten zum anderen wechseln). Die unmittelbar (nicht letztendlich) nächsten Knoten können ebenfalls angezeigt werden. | Eingeschränkt</br> Ermöglicht es Ihnen, mit der rechten Maustaste auf einen sofortigen Fallout in einer Freiformtabelle zu klicken und ihn anzuzeigen. | Ja</br> Nur explorative Analyse. Immer innerhalb einer Dimensionsinstanz zwischen Knoten. Das bedeutet, dass jeder Knoten den sofortigen (nicht letzten) nächsten Touchpoint entlang des Pfads anzeigt. |
| **Zeigt an, wo Personen gegangen sind und was passiert ist** | Ja</br>Wird sowohl für vordefinierte als auch für explorative Journey angezeigt | Ja</br>Zeigt vordefinierte Journey an | Ja</br>Shows für explorative Journey |
| **Lineare Journey** | Ja | Ja | Nein |
| **Nichtlineare Journey mit mehreren Einstiegspunkten und Pfaden** | Ja | Nein | Ja |
| **Primäre Metrik** | Jede Metrik, einschließlich berechneter Metriken | Nur Sitzung oder Person | Nur Vorfälle (Pfadansichten) |
| **Sekundäre Metrik** | Ja<p>Jede Metrik, einschließlich berechneter Metriken</p> | Nein | Nein |
| **Komponentenunterstützung in Knoten oder Touchpoints** | Metriken, Dimensionselemente, Filter und Datumsbereiche. | Metriken, Dimensionselemente, Filter und Datumsbereiche. | Nur Dimensionselemente (mit Ausnahme des Start- und Endkontaktpunkts) |
| **Filter vergleichen** | Nein | Ja<p>Eine Gegenüberstellung zweier verschiedener Filter im gleichen Bericht vornehmen.</p> | Nein |
| **Drag-and-Drop-Komponenteninteraktion** | Ja | Ja | Nein |
| **Adobe Journey Optimizer Journey** | Ja</br>Öffnen Sie Journey von Journey Optimizer aus, um sie gründlicher zu analysieren und anzupassen. | Nein | Nein |

{style="table-layout:auto"}
