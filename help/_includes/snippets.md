---
source-git-commit: 399902152f4882e3953dbb67dd51fd12f46ef773
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 87%

---
# Snippets

## Vorgängerversion von Report Builder {#legacy-arb}

>[!IMPORTANT]
>
>Eine neue und optimierte [Report Builder](/help/analyze/report-builder/rb-overview.md) wurde am 16. Oktober 2024 veröffentlicht. Es wird in Mac, Windows und Webbrowsern unterstützt.
>>Diese alte Add-In-Version von Report Builder funktioniert weiterhin. Sie können [alte Arbeitsmappen) in ](/help/analyze/report-builder/convert-workbooks.md) neue Report Builder konvertieren.

## Mitteilung zum Ende der Nutzungsdauer von Reports &amp; Analytics {#ra-eol}

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

Ein Attributionsmodell bestimmt, welchen Dimensionselementen eine Metrik zugeschrieben wird, wenn im Lookback-Fenster einer Metrik mehrere Werte angezeigt werden. Attributionsmodelle werden nur angewendet, wenn im Lookback-Fenster mehrere Dimensionselemente festgelegt sind. Wenn nur ein einzelnes Dimensionselement festgelegt ist, werden diesem Dimensionselement unabhängig vom verwendeten Attributionsmodell 100 % zugeschrieben.

| Symbol | Attributionsmodell | Definition |
| :---: | :--- | --- |
| ![Letztkontakt](/help/assets/icons/AttributeLastTouch.svg) | Letztkontakt | 100 % werden dem Touchpoint zugeschrieben, der zuletzt vor der Konversion aufgetreten ist. Dieses Attributionsmodell ist in der Regel der Standardwert für jede Metrik, bei der kein anderes Attributionsmodell angegeben ist. Organisationen verwenden dieses Modell in der Regel, wenn die Konversionszeit relativ kurz ist, z. B. bei der Analyse interner Suchbegriffe. |
| ![Erstkontakt](/help/assets/icons/AttributeFirstTouch.svg) | Erstkontakt | 100 % werden dem Touchpoint zugeschrieben, der zuerst im Attributions-Lookback-Fenster angezeigt wird. Organisationen verwenden dieses Modell in der Regel, um Markenwahrnehmung oder Kundenakquise zu verstehen. |
| ![Linear](/help/assets/icons/AttributeLinear.svg) | Linear | Ermöglicht dieselbe Gewichtung für jeden Touchpoint, der vor einer Konversion erfolgte. Dies ist nützlich, wenn die Konversionszyklen länger sind oder häufiger Kundeninteraktionen erfordern. Organisationen verwenden dieses Attributionsmodell in der Regel zur Messung der Effektivität von App-Benachrichtigungen oder mit abonnementbasierten Produkten. |
| ![Beitrag](/help/assets/icons/AttributeParticipation.svg) | Beitrag | 100 % Gewichtung für alle eindeutigen Touchpoints. Da jedem Touchpoint zu 100 % Gewichtung zugeschrieben werden, summieren sich die Daten von Metriken in der Regel auf mehr als 100 %. Wenn ein Dimensionselement mehrmals separat angezeigt wird, was zu einer Konversion führt, werden die Werte auf 100 % dedupliziert. Dieses Attributionsmodell ist ideal in Situationen, in denen Sie verstehen möchten, welchen Touchpoints Kundinnen und Kunden am meisten ausgesetzt sind. Medienunternehmen verwenden dieses Modell in der Regel zur Berechnung der Inhaltsgeschwindigkeit. Einzelhandelsunternehmen verwenden dieses Modell in der Regel, um zu verstehen, welche Teile ihrer Site für die Konversion von entscheidender Bedeutung sind. |
| ![Selber Kontakt](/help/assets/icons/AttributeSameTouch.svg) | Selber Kontakt | 100 % werden demselben Ereignis zugeschrieben, bei dem die Konversion erfolgte. Wenn ein Touchpoint nicht bei demselben Ereignis erfolgt wie eine Konversion, wird er unter „Keine“ zusammengefasst. Dieses Attributionsmodell wird manchmal damit gleichgesetzt, dass gar kein Attributionsmodell vorhanden ist. Dies ist nützlich in Szenarien, in denen Werte von anderen Ereignissen nicht beeinflussen sollen, wie eine Metrik Dimensionselementen eine Gewichtung zuschreibt. Produkt- oder Design-Teams können dieses Modell verwenden, um die Effektivität einer Seite zu bewerten, auf der die Konversion auftritt. |
| ![U-Form](/help/assets/icons/AttributeUShaped.svg) | U-Form | Der ersten Interaktion werden 40 % zugeschrieben, der letzten Interaktion 40 %. Die verbleibenden 20 % werden auf alle dazwischen liegenden Touchpoints aufgeteilt. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Konversionen mit zwei Touchpoints werden jedem 50 % zugeschrieben. Dieses Attributionsmodell eignet sich am besten für Szenarien, in denen Sie der ersten und letzten Interaktion den höchsten Wert zuweisen, aber zusätzliche Interaktionen dazwischen nicht völlig ausschließen möchten. |
| ![J-Kurve](/help/assets/icons/AttributeJCurve.svg) | J-Kurve | Der letzten Interaktion werden 60 % zugeschrieben, der ersten Interaktion werden 20 % zugeschrieben. Die restlichen 20 % werden auf alle dazwischen liegenden Touchpoints aufgeteilt. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Konversionen mit zwei Touchpoints werden der letzten Interaktion 75 % zugeschrieben und der ersten 25 %. Ähnlich wie „U-Form“ begünstigt dieses Attributionsmodell die erste und die letzte Interaktion, wobei die letzte Interaktion stark bevorzugt wird. |
| ![Umgekehrtes J](/help/assets/icons/AttributeInverseJ.svg) | Umgekehrtes J | Der ersten Interaktion werden 60 % zugeschrieben, der letzten Interaktion 20 %. Die verbleibenden 20 % werden auf alle dazwischen liegenden Touchpoints aufgeteilt. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Konversionen mit zwei Touchpoints werden der ersten Interaktion 75 % zugeschrieben und der letzten 25 %. Ähnlich wie „J-Form“ begünstigt dieses Attributionsmodell die erste und die letzte Interaktion, wobei die erste Interaktion stark bevorzugt wird. |
| ![Zeitverfall](/help/assets/icons/AttributeTimeDecay.svg) | Zeitverfall | Folgt einem exponentiellen Abfall mit einem benutzerdefinierten Parameter für die Halbwertszeit, wobei der Standardwert 7 Tage ist. Die Gewichtung der einzelnen Kanäle hängt von der Zeit ab, die zwischen dem Beginn des Touchpoints und der letztendlichen Konversion verstrichen ist. Die Formel, die zur Bestimmung der Gewichtung verwendet wird, lautet `2^(-t/halflife)`, wobei `t` die Zeit zwischen einem Touchpoint und einer Konversion ist. Alle Touchpoints werden dann auf 100 % normalisiert. Ideal für Szenarien, in denen die Attribution anhand eines bestimmten und bedeutenden Ereignisses gemessen werden soll. Je später eine Konversion nach einem Marketing-Ereignis erfolgt, desto geringer ist die zugeschriebene Gewichtung. |
| ![Benutzerspezifisch](/help/assets/icons/AttributeCustom.svg) | Anpassen | Ermöglicht Ihnen die Angabe der Gewichtungen, die Sie für den ersten Touchpoint, den letzten Touchpoint und dazwischen liegende Touchpoints festlegen möchten. Die angegebenen Werte werden auf 100 % normalisiert, selbst wenn die eingegebenen benutzerdefinierten Zahlen zusammen nicht 100 ergeben. Bei Konversionen mit einem einzigen Touchpoint werden diesem 100 % zugeschrieben. Bei Interaktionen mit zwei Touchpoints wird der mittlere Parameter ignoriert. Die ersten und letzten Touchpoints werden dann auf 100 % normalisiert und die Gewichtung wird entsprechend zugeschrieben. Dieses Modell ist ideal für Analystinnen und Analysten, die eine vollständige Kontrolle über ihr Attributionsmodell wünschen und spezielle Bedürfnisse haben, die andere Zuordnungsmodelle nicht erfüllen. |
| ![Algorithmisch](/help/assets/icons/AttributeAlgorithmic.svg) | Algorithmisch | Verwendet statistische Verfahren, um die optimale Zuordnung für die ausgewählte Metrik dynamisch zu bestimmen. Der für die Zuordnung verwendete Algorithmus basiert auf der Harsanyi-Dividende aus der kooperativen Spieltheorie. Die Harsanyi-Dividende ist eine Verallgemeinerung der Shapley-Wertlösung (die nach Lloyd Shapley, einem Nobelpreisträger für Ökonomie, benannt wurde) zur Verteilung von Gutschriften unter den Spielern in einem Spiel mit ungleichen Beiträgen zum Ergebnis.<br>Auf hoher Ebene wird die Attribution als eine Koalition von Spielenden berechnet, an die ein Überschuss gerecht verteilt werden muss. Die Überschusshöhe jeder Koalition wird nach dem Überschuss bestimmt, der zuvor von jeder Unterkoalition (oder zuvor teilnehmenden Dimensionselementen) rekursiv erzeugt wurde. Weitere Informationen finden Sie in John Harsanyis und Lloyd Shapleys Originaldokumenten: <br>Shapley, Lloyd S. (1953). A value for n-person games. *Contributions to the Theory of Games, 2(28)*, 307-317.<br>Harsanyi, John C. (1963). A simplified bargaining model for the n-person cooperative game. *International Economic Review 4(2)*, 194-220. |

{style="table-layout:auto"}

## Attributions-Container {#attribution-container}

Ein Attributions-Container definiert den gewünschten Umfang für die Attribution. Mögliche Optionen sind:

* **Besuch**: Betrachtet Konversionen aus dem Umfang des Besuchs-Containers. Wenn **[!UICONTROL Besuch]** ausgewählt ist, wird das [Attributions-Lookback-Fenster](#atribution-lookback-window) automatisch auf **[!UICONTROL Reporting-Fenster]** festgelegt und kann nicht geändert werden.
* **Besucher**: Betrachtet Konversionen aus dem Umfang des Besucher-Containers.

## Attributions-Lookback-Fenster {#attribution-lookback-window}

Ein Lookback-Fenster ist der Zeitraum, der für eine Konversion rückblickend bei der Erfassung von Touchpoints berücksichtigt werden sollte. Wenn ein Dimensionselement außerhalb des Lookback-Fensters festgelegt wird, wird der Wert in keine Attributionsberechnungen einbezogen.

* **[!UICONTROL Reporting-Fenster]**: Sucht nach dem Beginn des Reporting-Fensters zum Zeitpunkt der Konvertierung.
* **14 Tage**: Blickt bis zu 14 Tage nach dem Zeitpunkt zurück, an dem die Konversion stattgefunden hat.
* **30 Tage**: Blickt bis zu 30 Tage nach dem Zeitpunkt zurück, an dem die Konversion stattgefunden hat.
* **60 Tage**: Blickt bis zu 60 Tage nach dem Zeitpunkt zurück, an dem die Konversion stattgefunden hat.
* **90 Tage**: Blickt bis zu 90 Tage nach dem Zeitpunkt zurück, an dem die Konversion stattgefunden hat.
* **Benutzerdefinierte Zeit:** Ermöglicht es Ihnen, ein benutzerdefiniertes Lookback-Fenster ab dem Zeitpunkt festzulegen, an dem eine Konversion stattgefunden hat. Sie können die Anzahl der Minuten, Stunden, Tage, Wochen, Monate oder Quartale angeben. Beispiel: Bei einer Konversion am 20. Februar würde ein Lookback-Fenster von fünf Tagen alle Touchpoints der Dimension vom 15. bis 20. Februar im Attributionsmodell auswerten.

## Attributionsbeispiel {#attribution-example}

Sehen Sie sich folgendes Beispiel an:

1. Am 15. September gelangt ein Besucher über Paid Search zu Ihrer Site und verlässt sie dann.
1. Am 18. September gelangt der Besucher erneut über einen Link in sozialen Medien zu Ihrer Site, den er von einem Freund erhalten hat. Er fügt mehrere Artikel zum Warenkorb hinzu, erwirbt aber nichts.
1. Am 24. September sendet Ihr Marketing-Team eine E-Mail mit einem Coupon für einige der Artikel im Warenkorb. Der Coupon wird angewendet, der Besucher ruft aber mehrere andere Websites auf, um zu sehen, ob andere Coupons verfügbar sind. Er findet einen weiteren über eine Display-Anzeige und kauft dann letztendlich für 50 Euro ein.

Je nach Attributionsmodell erhalten Container und Kanäle unterschiedliche Gewichtungen. Beispiele finden Sie in der unten stehenden Tabelle:

| Modell | Container | Lookback-Fenster | Erklärung |
|---|---|---|---|
| Erstkontakt | Besuch | 30 Tage | Die Attribution untersucht nur den dritten Besuch. E-Mail kam vor Display-Anzeige, sodass E-Mail 100 % des Kaufs in Höhe von 50 Euro zugeschrieben werden. |
| Erstkontakt | Besucher | 30 Tage | Die Attribution untersucht alle drei Besuche. Paid Search kam zuerst, sodass Paid Search 100 % des Kaufs in Höhe von 50 Euro zugeschrieben werden. |
| Linear | Besuch | 30 Tage | Die Gewichtung wird zwischen E-Mail und Display-Anzeige aufgeteilt. Beiden Kanälen werden jeweils 25 Euro zugeschrieben. |
| Linear | Besucher | 30 Tage | Die Gewichtung wird zwischen Paid Search, Social Media, E-Mail und Display-Anzeige aufgeteilt. Jedem Kanal werden für diesen Kauf 12,50 Euro zugeschrieben. |
| J-förmig | Besucher | 30 Tage | Die Gewichtung wird zwischen Paid Search, Social Media, E-Mail und Display-Anzeige aufgeteilt.<ul><li>Der Display-Anzeige werden 60 %, also 30 Euro, zugeschrieben.</li><li>Paid Search werden 20 %, also 10 Euro, zugeschrieben.</li><li>Die restlichen 20 % werden zwischen Social Media und E-Mail aufgeteilt (jeweils 5 Euro).</li></ul> |
| Zeitverfall | Besucher | 30 Tage | <ul><li>Abstand von null Tagen zwischen Display-Touchpoint und Konversion. `2^(-0/7) = 1`</li><li>Abstand von null Tagen zwischen E-Mail-Touchpoint und Konversion. `2^(-0/7) = 1`</li><li>Abstand von sechs Tagen zwischen Social Media-Touchpoint und Konversion. `2^(-6/7) = 0.552`</li><li>Abstand von 9 Tagen zwischen Paid Search-Touchpoint und Konversion. `2^(-9/7) = 0.41`</li>Die Normalisierung dieser Werte führt zu Folgendem:<ul><li>Display-Anzeige: 33,8 %, 16,88 Euro</li><li>E-Mail: 33,8 %, 16,88 Euro</li><li>Social Media: 18,6 %, 9,32 Euro</li><li>Paid Search: 13,8 %, 6,92 Euro</li></ul></li></ul> |

Konversionsereignisse, die in der Regel Ganzzahlen aufweisen, werden aufgeteilt, wenn die Gewichtung mehr als einem Kanal zugeschrieben wird. Wenn beispielsweise zwei Kanäle mit einem linearen Attributionsmodell zu einer Bestellung beitragen, erhalten beide Kanäle 0,5 dieser Bestellung. Diese Teilmetriken werden über alle Personen summiert und dann zur Berichterstellung auf die nächste Ganzzahl gerundet.

## Vergleiche der Journey-Visualisierungen {#journey-visualization-comparisons}

In Customer Journey Analytics werden verschiedene Visualisierungen generiert, um die Journeys zu analysieren, die Sie Ihren Kundinnen und Kunden bereitstellen.

Verwenden Sie die folgenden Informationen, um die Visualisierung auszuwählen, die Ihren Anforderungen am besten entspricht.

| Funktion | Journey-Arbeitsfläche | Fallout | Fluss |
|---------|----------|---------|---------|
| **Vordefinierte Seitensequenz** | Ja</br>Kombiniert vordefinierte und explorative Analysen. Der endgültige Pfad wird bei Verwendung vordefinierter Knoten auf dem Pfad verwendet (Besuchende werden gezählt, solange sie schließlich von einem vordefinierten Knoten zum anderen wechseln). Die unmittelbar (nicht letztendlich) nächsten Knoten können ebenfalls angezeigt werden. | Ja</br>Der Pfad kann ein endgültiger Pfad oder auf den nächsten Touchpoint beschränkt sein | Nein |
| **Explorative Sequenz von Seiten (Ad-hoc-Analyse)** | Ja</br>Kombiniert vordefinierte und explorative Analysen. Der endgültige Pfad wird bei Verwendung vordefinierter Knoten auf dem Pfad verwendet (Besuchende werden gezählt, solange sie schließlich von einem vordefinierten Knoten zum anderen wechseln). Die unmittelbar (nicht letztendlich) nächsten Knoten können ebenfalls angezeigt werden. | Eingeschränkt</br>Ermöglicht es Ihnen, mit der rechten Maustaste auf einen sofortigen Fallout in einer Freiformtabelle zu klicken und ihn anzuzeigen. | Ja</br>Nur explorative Analysen. Immer innerhalb einer Dimensionsinstanz zwischen Knoten. Das bedeutet, dass jeder Knoten den sofortigen (nicht endgültigen) nächsten Touchpoint entlang des Pfads anzeigt. |
| **Zeigt an, wo Personen eine Site verlassen haben und wo sie passiert sind (d. h., wo sie verblieben sind).** | Ja</br>Wird sowohl für vordefinierte als auch für explorative Journey angezeigt | Ja</br>Zeigt vordefinierte Journeys an | Ja</br>Zeigt explorative Journeys an |
| **Lineare Journeys** | Ja | Ja | Nein |
| **Nichtlineare Journeys mit mehreren Einstiegspunkten und Pfaden** | Ja | Nein | Ja |
| **Primäre Metrik** | Jede Metrik, einschließlich berechneter Metriken | Nur Sitzung oder Person | Nur Vorkommnisse (Pfadansichten) |
| **Sekundäre Metrik** | Ja<p>Jede Metrik, einschließlich berechneter Metriken</p> | Nein | Nein |
| **Komponentenunterstützung in Knoten oder Touchpoints** | Metriken, Dimensionselemente, Filter und Datumsbereiche. | Metriken, Dimensionselemente, Filter und Datumsbereiche. | Nur Dimensionselemente (mit Ausnahme des Start- und End-Touchpoints) |
| **Filter vergleichen** | Nein | Ja<p>Eine Gegenüberstellung zweier verschiedener Filter im gleichen Bericht vornehmen.</p> | Nein |
| **Drag-and-Drop-Komponenteninteraktion** | Ja | Ja | Nein |
| **Adobe Journey Optimizer-Journeys** | Ja</br>Öffnen Sie Journey von Journey Optimizer aus, um sie gründlicher zu analysieren und anzupassen. | Nein | Nein |

{style="table-layout:auto"}



## Abschnitt zu Tag-Filtern {#tagfiltersection}

| Tags | Beschreibung |
|---|---|
| ![Tags](/help/assets/filter-tag.png){width="300"} | Im Abschnitt **[!UICONTROL Tags]** können Sie nach Tags filtern. <ul><li>Mit ![Suchen](/help/assets/icons/Search.svg) *Tags suchen* können Sie nach Tags suchen, die Sie zum Filtern verwenden können.</li><li>Sie können auch mehr als ein Tag auswählen. Die verfügbaren Tags hängen von der Auswahl ab, die in anderen Abschnitten im Panel „Filter“ vorgenommen wurde.</li><li>Die Zahlen geben Folgendes an:<ul><li>**(1)**: Die Anzahl der ausgewählten Tags (wenn mindestens ein Tag ausgewählt ist).</li><li>**2︎⃣**: Die Anzahl der Tags, die für die aus dem aktuellen Filter resultierenden Elemente verfügbar sind.</li><li>7︎⃣: Die Anzahl der Elemente, die mit dem jeweiligen Tag verknüpft sind.</li></ul></li></ul> |


## Report Suite-Filterabschnitt {#reportsuitefiltersection}

| Report Suite | Beschreibung |
|---|---|
| ![Repost Suite](/help/assets/filter-reportsuite.png){width="300"} | Im **[!UICONTROL Report Suite]** können Sie nach Report Suites filtern. <ul><li>Sie können ![Suche](/help/assets/icons/Search.svg) *Report Suites durchsuchen* um nach Report Suites zu suchen, die Sie zum Filtern verwenden können.</li><li>Sie können mehrere Report Suites auswählen. Die verfügbaren Report Suites hängen von der Auswahl ab, die in anderen Abschnitten im Filterbedienfeld vorgenommen wurde.</li><li>Die Zahlen geben Folgendes an:<ul><li>**(2)**: Die Anzahl der ausgewählten Report Suites (wenn eine oder mehrere Report Suites ausgewählt sind).</li><li>**3︎⃣**: Die Anzahl der Report Suites, die für die aus dem aktuellen Filter resultierenden Elemente verfügbar sind.</li><li>4︎⃣: Die Anzahl der Elemente, die mit der bestimmten Report Suite verknüpft sind.</li></ul></li></ul> |

## Abschnitt zu Filtern nach aktivierten Status {#enabledstatusfiltersection}

| Aktivierter Status | Beschreibung |
|---|---|
| ![Aktivierter Status](/help/assets/filter-enabledstatus.png){width="300"} | Im Abschnitt **[!UICONTROL Aktivierter Status]** können Sie nach dem aktivierten Status filtern. <ul><li>Sie können auch mehrere Status auswählen.</li><li>Die Zahlen geben Folgendes an:<ul><li>**(2)**: Die Anzahl der ausgewählten Status (wenn mindestens ein Status ausgewählt ist).</li><li>**2︎⃣**: Die Anzahl der Status, die für die aus dem aktuellen Filter resultierenden Elemente verfügbar sind.</li><li>1︎⃣: Die Anzahl der Elemente, die mit dem jeweiligen Status verknüpft sind.</li></ul></li></ul> |

## Abschnitt zu Typenfiltern {#typefiltersection}

| Typ | Beschreibung |
|---|---|
| ![Typ](/help/assets/filter-type.png){width="300"} | Im Abschnitt **[!UICONTROL Typ]** können Sie nach dem Typ filtern. <ul><li>Sie können auch mehrere Typen auswählen.</li><li>Die Zahlen geben Folgendes an:<ul><li>**(2)**: Die Anzahl der ausgewählten Typen (wenn mindestens ein Typ ausgewählt ist).</li><li>**1︎⃣**: Die Anzahl der Typen, die für die aus dem aktuellen Filter resultierenden Elemente verfügbar sind.</li><li>3︎⃣: Die Anzahl der Elemente, die mit dem jeweiligen Typ verknüpft sind.</li></ul></li></ul> |

## Abschnitt zu Filtern von Inhaberinnen bzw. Inhabern {#ownerfiltersection}

| Inhaberin oder Inhaber | Beschreibung |
|---|---|
| ![Inhaberinnen oder Inhaber](/help/assets/filter-owners.png){width="300"} | Im Abschnitt **[!UICONTROL Inhaberin oder Inhaber]** können Sie nach Inhaberinnen und Inhabern filtern. <ul><li>Mit ![Suchen](/help/assets/icons/Search.svg) *Verantwortliche(n) suchen* können Sie nach Inhaberinnen bzw. Inhabern suchen, die Sie zum Filtern verwenden können.</li><li>Sie können mehr als eine Inhaberin bzw. einen Inhaber auswählen. Die verfügbaren Inhaberinnen und Inhaber hängen von der Auswahl ab, die in anderen Abschnitten im Panel „Filter“ vorgenommen wurde.</li><li>Die Zahlen geben Folgendes an:<ul><li>**(2)**: Die Anzahl der ausgewählten Inhaberinnen bzw. Inhaber (wenn mindestens eine Inhaberin bzw. ein Inhaber ausgewählt ist).</li><li>**3︎⃣**: Die Anzahl der Inhaberinnen und Inhaber, die für die aus dem aktuellen Filter resultierenden Elemente verfügbar sind.</li><li>4︎⃣: Die Anzahl der Elemente, die mit der jeweiligen Inhaberin bzw. dem jeweiligen Inhaber verknüpft sind.</li></ul></li></ul> |

## Abschnitt zu Filtern von anderen Filtern {#otherfiltersfiltersection}

| Andere Filter | Beschreibung |
|---|---|
| ![Sonstige Filter](/help/assets/filter-other.png){width="300"} | Im Abschnitt **[!UICONTROL Andere Filter]** können Sie nach anderen vordefinierten Filtern filtern.<ul><li>Sie können eine oder mehrere der folgenden Optionen auswählen:<ul><li> **[!UICONTROL Alle anzeigen]**</li><li>**[!UICONTROL Mit mir geteilt]**</li><li>**[!UICONTROL Meine]**</li><li>**[!UICONTROL Genehmigt]**</li><li>**[!UICONTROL Favoriten]**</li></ul> Was Sie auswählen können, hängt von Ihrer Rolle und Ihren Berechtigungen ab.</li><li>Sie können mehr als einen Filter auswählen. Die anderen verfügbaren Filter hängen von der Auswahl ab, die in anderen Abschnitten im Panel „Filter“ vorgenommen wurde.</li><li>Die Zahlen geben Folgendes an:<ul><li>**(1)**: Die Anzahl der ausgewählten anderen Filter (wenn mindestens ein Filter ausgewählt ist).</li><li>**5︎⃣**: Die Anzahl weiterer Filter, die für die aus dem aktuellen Filter resultierenden Elemente verfügbar sind.</li><li>4︎⃣: Die Anzahl der Elemente, die mit dem jeweiligen anderen Filter verknüpft sind.</li></ul></li></ul> |

## Abschnitt zum Datumsbereichsfilter  {#daterangefiltersection}

| Angewendeter Datumsbereich | Beschreibung |
|---|---|
| ![Datumsbereich](/help/assets/filter-daterange.png){width="300"} | Im Abschnitt „Angewendeter Datumsbereich“ können Sie nach einem Datumsbereich filtern, der auf die Elemente anwendbar ist.<ol><li>Wählen Sie einen Datumsbereich aus.</li><li>Definieren Sie im Kalender-Popup einen Datumsbereich oder wählen Sie eine der verfügbaren Voreinstellungen aus.<br>Alternativ können Sie einen Datumsbereich auch direkt im Abschnitt „Datumsbereich“ des Panels „Filter“ angeben.</li></ol><ul><li>Die Zahlen geben Folgendes an:<ul><li>**(1)**: Die Anzahl der geänderten Datumsbereiche, die von den Standardvorgaben geändert wurden.</li><li>**5︎⃣**: Die Anzahl der Datumsbereiche, die für die aus dem aktuellen Filter resultierenden Elemente verfügbar sind.</li></ul> |


## Einstellung des Classification Importers {#classification-importer-deprecation}

>[!WARNING]
>
>Das Classification Importer wird nicht mehr unterstützt und ist nach dem 31. **2026 nicht mehr**. Wechseln Sie zum Erlebnis [Klassifizierungssätze](/help/components/classifications/sets/overview.md), um den Fortbestand der Funktionalität sicherzustellen.
>



## Einstellung des Classification Rule Builders {#classification-rulebuilder-deprecation}

>[!WARNING]
>
>Der Classification Rule Builder wird nicht mehr unterstützt und ist nach dem 31. **2026 nicht mehr**. Wechseln Sie zum Erlebnis [Klassifizierungssätze](/help/components/classifications/sets/overview.md), um den Fortbestand der Funktionalität sicherzustellen.
>

