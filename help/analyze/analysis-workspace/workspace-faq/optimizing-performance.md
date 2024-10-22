---
description: Faktoren, die sich auf die Leistung von Workspace auswirken, und die Optimierungen, die Sie ausführen können
title: Leistungsfaktoren und Optimierung von Analysis Workspace
feature: Workspace Basics
role: User, Admin
exl-id: 7a675f53-2774-4c7b-af1b-79e52e7d5cfb
source-git-commit: 4cbcdc1e1287c301fe4452370e3db1f4b9b3f3a1
workflow-type: tm+mt
source-wordcount: '2548'
ht-degree: 76%

---

# Optimieren der [!UICONTROL Analysis Workspace-Leistung]

Mehrere Faktoren können die Leistung eines Projekts in Analysis Workspace beeinflussen. Damit Sie Ihr Projekt optimal planen und erstellen können, sollten Sie vor Beginn diese Faktoren kennen. Diese Seite enthält eine Liste von Faktoren, die sich auf die Leistung auswirken, sowie Optimierungen, die Sie vornehmen können, um eine optimale Leistung in Analysis Workspace sicherzustellen.

## [!UICONTROL Hilfe] > [!UICONTROL Leistung] in Analysis Workspace

Unter **Analysis Workspace > [!UICONTROL Hilfe] > [!UICONTROL Leistung]** können Sie die Faktoren sehen, die sich auf die Leistung Ihres Projekts auswirken, einschließlich Netzwerk-, Browser- und Projektfaktoren. Um möglichst genaue Ergebnisse zu erzielen, müssen Sie das Projekt vor dem Öffnen der Seite „Leistung“ vollständig laden.

* In der Spalte „Aktuelles Projekt“ werden die Ergebnisse für Ihr aktuelles Projekt und Ihre Umgebung angezeigt.
* In der Spalte „Richtlinie“ wird der von Adobe empfohlene Schwellenwert für jeden Faktor angezeigt.

Darüber hinaus können Sie die Leistungsinhalte **als CSV-Datei herunterladen**, um sie einfach mit der Adobe-Kundenunterstützung oder Ihren IT-Teams zu teilen.

>[!NOTE]
>
>Die Informationen auf der Seite „Leistung“ variieren bei jedem Öffnen des Modells, da sich Faktoren ändern können. Darüber hinaus verfeinert Adobe die bereitgestellten Richtlinien weiter, sobald mehr Daten verfügbar sind.

![](assets/performance-modal.png)

## Netzwerkfaktoren

[!UICONTROL Hilfe] > [!UICONTROL Leistungsnetzwerkfaktoren] beinhalten:

| Faktor | Definition | Beeinflusst durch | Optimierung |
| --- | --- | --- | --- |
| Verbindung mit Adobe | Adobe sendet 10 Testaufrufe, wenn die Leistungsseite geöffnet wird. Dies stellt den Prozentsatz der erfolgreichen Aufrufe zu Adobe dar. | Lokale Netzwerkprobleme oder Probleme mit der Adobe wirken sich auf diesen Faktor aus. | Überprüfen Sie status.adobe.com, ob bekannte Service-Probleme vorliegen. Überprüfen Sie dann Ihre lokale Netzwerkverbindung. |
| Internetbandbreite | Nur für Google Chrome verfügbar. Geschätzte Bandbreite Ihres Browsers an Ihrem Standort. Die Richtlinie ist 2,0 MB/s. | Ihre lokale Netzwerkverbindung wirkt sich auf diesen Faktor aus. | Überprüfen Sie die lokale Netzwerkverbindung. |
| Internetlatenz | Adobe sendet 10 Testaufrufe, wenn die Leistungsseite geöffnet wird. Dies stellt die Zeitdauer dar, die durchschnittlich eine Anfrage an Adobe und deren Antwort benötigt. Einfach gesagt, es ist ein Maß dafür, wie schnell das Internet zwischen Ihrem Standort und Adobe ist. Die Richtlinie ist &lt; 1 Sekunde. | Lokale Netzwerkprobleme, viele offene Browser-Registerkarten oder Probleme bei Adobe wirken sich auf diesen Faktor aus. | Überprüfen Sie status.adobe.com, ob bekannte Service-Probleme vorliegen. Überprüfen Sie dann Ihre lokale Netzwerkverbindung und schließen Sie nicht verwendete Browser-Registerkarten. |

## Browser-Faktoren

[!UICONTROL Hilfe] > [!UICONTROL Leistungs-Browser-Faktoren] beinhalten:

| Faktor | Definition | Beeinflusst durch | Optimierung |
| --- | --- | --- | --- |
| Berechnungsgeschwindigkeit | Wie schnell Ihr Computer einen Verarbeitungstest durchführt. Die Richtlinie ist &lt; 750 ms. | Ihre Hardware sowie gleichzeitige Programme wirken sich auf diesen Faktor aus. | Öffnen Sie den Task-Manager (PC) bzw. die Aktiviätsanzeige (Mac) Ihres Computers, um zu ermitteln, ob Programme geschlossen werden können. Schließen Sie dann nicht verwendete Browser-Registerkarten oder andere Programme. <br><br>Wenn diese Aktionen nicht hilfreich sind, besprechen Sie Hardware-Details mit Ihrem IT-Team. |
| Speicher verwendet | Nur für Google Chrome verfügbar. Jede Workspace-Registerkarte in einem Google Chrome-Browser verwendet insgesamt 4 GB Arbeitsspeicher. Dies entspricht dem Prozentsatz des Speicherlimits, das vom aktuellen Projekt belegt wird. Die Richtlinie ist 3.500 MB. Dies ist der Punkt, ab dem Workspace Speicherfehler zurückgibt. | Das Arbeiten mit mehreren Registerkarten oder das Herunterladen von 50.000 Zeilen mit Daten bedeutet eine höhere Speicherbelegung. | Wenn Sie einen Speicherfehler erhalten, schließen Sie andere Workspace-Registerkarten und/oder führen Sie 50.000 Zeilen-Downloads einzeln durch. |
| Lokaler Speicher verwendet | Daten, die lokal auf Ihrem Computer zur Verwendung im Browser gespeichert werden. Jede Herkunft (z. B. experience.adobe.com) verfügt über ein Limit von 10 MB. | Analysis Workspace verwendet lokale Datenspeicherung für verschiedene Funktionen, unter anderem zum Speichern automatisch gespeicherter (vorhandener) Projekte, Benutzereinstellungen und Feature Flags. | Um sicherzustellen, dass Analysis Workspace-Funktionen nicht gestört werden, sollten Sie die lokale Datenspeicherung für die Domain „experience.adobe.com“ löschen. |
| Rendering-Geschwindigkeit | FPS steht für Frames pro Sekunde, d. h., wie oft der Browser die Seite auf Ihrem Bildschirm zeichnet. 24 FPS sind häufig das, was das menschliche Auge als Bewegung wahrnimmt. Wenn der FPS-Wert niedriger ist, treten in Workspace Rendering-Probleme auf. | Der FPS-Wert wird durch das gleichzeitige Bearbeiten vieler Workspace-Projekte auf einmal und die Größe des angezeigten Projekts beeinflusst. Andere auf Ihrem Computer ausgeführte Programme können Auswirkungen haben, wie Streaming, Hintergrund-Scanner usw. Darüber hinaus wirkt sich Ihre Hardware auf diesen Faktor aus. | Öffnen Sie den Task-Manager (PC) bzw. die Aktiviätsanzeige (Mac) Ihres Computers, um zu ermitteln, ob Programme geschlossen werden können. Schließen Sie dann nicht verwendete Browser-Registerkarten oder andere Programme. <br><br>Wenn diese Aktionen nicht hilfreich sind, besprechen Sie Hardware-Details mit Ihrem IT-Team. |

## Projektfaktoren

[!UICONTROL Hilfe] > [!UICONTROL Leistungsprojektfaktoren] beinhalten:

| Faktor | Definition | Optimierung |
| --- | --- | --- |
| Anzahl der Anfragen | Die Gesamtzahl der an Adobe gerichteten Anfragen zum Abrufen von Daten, die im Projekt angezeigt werden. Zu den Abfragen gehören Ranganfragen für Tabellen, Anomalieerkennung, Wortgrafiken, Komponenten in der linken Leiste und mehr. Schließt ausgeblendete Bedienfelder und Visualisierungen aus. Die Richtlinie ist 100. | Vereinfachen Sie Ihr Projekt nach Möglichkeit, indem Sie Daten in verschiedene Projekte aufteilen, die einem bestimmten Zweck oder Interessenten dienen. Verwenden Sie Tags, um Projekte in Themen zu organisieren, und verwenden Sie [direkte Verknüpfungen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html?lang=de), um ein internes Inhaltsverzeichnis zu erstellen, damit die Interessierte leichter finden können, wonach sie suchen. |
| Erweiterte Bedienfelder (von der Gesamtzahl der Bedienfelder) | Die Anzahl der erweiterten Bedienfelder von der Gesamtzahl der Bedienfelder im Projekt. Die Richtlinie ist 5. | Nachdem Sie Schritte zur Vereinfachung des Projekts unternommen haben, reduzieren Sie die Bedienfelder im Projekt, die beim Laden nicht angezeigt werden müssen. Wenn das Projekt geöffnet wird, werden nur erweiterte Bedienfelder verarbeitet. Reduzierte Felder werden erst verarbeitet, wenn der Nutzer sie erweitert. |
| Erweiterte Visualisierungen (aus der Gesamtzahl der Visualisierungen) | Die Anzahl der erweiterten Tabellen und Visualisierungen aus der Gesamtsumme im Projekt, einschließlich der ausgeblendeten Datenquellen. Die Richtlinie ist 15. | Nachdem Sie Schritte zur Vereinfachung des Projekts unternommen haben, reduzieren Sie die Visualisierungen in Ihrem Projekt, die beim Laden nicht angezeigt werden müssen. Priorisieren Sie die Visuals, die für den Verbraucher des Berichts am wichtigsten sind, und teilen Sie die unterstützenden Visuals bei Bedarf in ein separates, detaillierteres Bedienfeld oder Projekt auf. |
| Anzahl der Freiformzellen | Die Gesamtzahl der Freiform-Tabellenzellen im Projekt, berechnet durch Zeilen * Spalten in allen Tabellen. Schließt verborgene Datenquellen aus. Die Richtlinie ist 4000. | Reduzieren Sie die Anzahl der Spalten in Ihrer Tabelle auf die relevantesten Datenpunkte. Reduzieren Sie die Anzahl der Zeilen in Ihrer Tabelle, indem Sie die Anzahl der angezeigten Zeilen anpassen, einen Tabellenfilter oder ein Segment anwenden. |
| Verfügbare Komponenten | Die Gesamtzahl der in der linken Leiste des Projekts abgerufenen Komponenten für alle Report Suites im Projekt. Dies wirkt sich auf die Geschwindigkeit aus, mit der die linke Leiste geladen wird und wie schnell Suchergebnisse innerhalb der Leiste zurückgegeben werden. Die Richtlinie ist 2.000. | Sprechen Sie mit Ihrem Produktadministrator über das Erstellen einer kuratierten Virtual Report Suite, die über einen stärker auf Ihre Bedürfnisse zugeschnittenen Satz an Komponenten verfügt. |
| Verwendete Komponenten | Die Gesamtzahl der im Projekt verwendeten Komponenten. Die Richtlinie ist 100. | Die Anzahl der verwendeten Komponenten hat keinen direkten Einfluss auf die Leistung. Die Komplexität dieser Komponenten wird jedoch zur Leistung des Projekts beitragen. Siehe Optimierungen im Abschnitt „Weitere Faktoren“ unten. |
| Längster Datumsbereich | Dieser Faktor zeigt den längsten Datumsbereich an, der für das Projekt verwendet wurde. Die Richtlinie ist ein Jahr. | Rufen Sie möglichst nicht mehr Daten ab, als Sie benötigen. Schränken Sie den Kalender des Bedienfelds auf die relevanten Daten für Ihre Analyse ein oder verwenden Sie Datumsbereichskomponenten (violette Komponenten) in Ihren Freiform-Tabellen. In einer Tabelle verwendete Datumsbereiche überschreiben den Datumsbereich des Bedienfelds. Beispielsweise können Sie den Tabellenspalten „Letzter Monat“, „Letzte Woche“ und „Gestern“ hinzufügen, um diese spezifischen Datenbereiche anzufordern. Weitere Informationen zu Datumsbereichen in Analysis Workspace erhalten Sie in [diesem Video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/date-ranges-and-calendar-in-analysis-workspace.html?lang=de). <br><br>Minimieren Sie außerdem die Anzahl der im Projekt verwendeten Jahresvergleiche. Bei der Berechnung eines Jahresvergleichs werden die gesamten 13 Monate von Daten zwischen den betrachteten Monaten berücksichtigt. Dies hat die gleiche Auswirkung wie die Änderung des Datumsbereichs des Bedienfelds auf 13 Monate. |

## Anforderungsfaktoren

[!UICONTROL Hilfe] > [!UICONTROL Leistung] Anforderungsfaktoren

Verwenden Sie das folgende Diagramm und die folgenden Begriffe, um zu erfahren, wie Anforderungen verarbeitet werden und welche Faktoren die Verarbeitungszeiten beeinflussen:

>[!NOTE]
>
>Die empfohlenen Richtlinien für diese Faktoren basieren auf einem Komplexitätswert von Medium für Berichterstellungsanforderungen.


### Anforderungsverarbeitungsdiagramm

![Anforderungsverarbeitung](assets/request-processing.png)

### Verarbeitungsbegriffe anfordern

| Faktor | Definition | Optimierung |
| --- | --- | --- |
| [!UICONTROL **Durchschnittliche Anforderungszeit**] | Die Zeit, die ab dem Initiieren der Anfrage bis zum Abschluss benötigt wird. Die Richtlinie beträgt 15 Sekunden. <p>Im obigen Diagramm [Anforderungsverarbeitung](#request-processing-diagram) stellt die Anforderungszeit den gesamten Prozess dar, von **Analysis Workspace-Anfrage initiiert** bis **Analysis Workspace-Anfrage abgeschlossen**.</p> |  |
| [!UICONTROL **Längste Anforderungszeit**] | Die Zeit, die ab dem Initiieren der Anfrage bis zum Abschluss benötigt wird. <p>Im obigen Diagramm [Anforderungsverarbeitung](#request-processing-diagram) stellt die Anforderungszeit den gesamten Prozess dar, von **Analysis Workspace-Anfrage initiiert** bis **Analysis Workspace-Anfrage abgeschlossen**.</p> |  |
| [!UICONTROL **Durchschnittliche Suchzeit**] | Da Analysis Workspace nur den Hash für alle Zeichenfolgen speichert, die in beliebigen Segmenten verwendet werden, werden bei jeder Projektverarbeitung **Suchen** ausgeführt, um die Hashes mit den entsprechenden Werten abzugleichen. Die Richtlinie liegt unter 2 Sekunden.<p>Dies kann ein ressourcenintensiver Prozess sein, je nachdem, wie viele Werte möglicherweise mit dem Hash übereinstimmen. </p><p>Im obigen Diagramm [Anforderungsverarbeitung](#request-processing-diagram) wird die Suchzeit in der Phase **Suchvorgänge** dargestellt (zum Zeitpunkt der Phase der **Verarbeitung der Anforderungs-Engine**).</p> | Wenn sich die Anforderungen hier verlangsamen, liegt dies wahrscheinlich daran, dass in Ihrem Projekt zu viele Zeichenfolgensegmente vorhanden sind oder Zeichenfolgen mit zu generischen Werten vorhanden sind, die zu viele potenzielle Übereinstimmungen aufweisen. |
| [!UICONTROL **Durchschnittliche Warteschlangenzeit**] | Die Gesamtwartezeit in der Warteschlange, bevor Anforderungen verarbeitet werden. Die Richtlinie beträgt 5 Sekunden.<p>Im obigen Diagramm [Anforderungsverarbeitung](#request-processing-diagram) wird die Warteschlangenzeit in der Phase **Anforderungs-Engine-Warteschlange** und in der Phase **Server-Warteschlange** dargestellt.</p> | Wenn sich die Anforderungen hier verlangsamen, kann dies auf zu viele Anforderungen zurückzuführen sein, die gleichzeitig in Ihrem Unternehmen ausgeführt werden. Versuchen Sie, die Anfrage außerhalb der Spitzenzeiten auszuführen. |
| [!UICONTROL **Durchschnittliche Server-Verarbeitungszeit**] | Die durchschnittliche Zeit, die für die Verarbeitung der Anfrage benötigt wird.<p>Im obigen Diagramm [Anforderungsverarbeitung](#request-processing-diagram) wird die durchschnittliche Serververarbeitungszeit in der Phase **Serverwarteschlange** und in der Phase **Serververarbeitung** dargestellt. Die Richtlinie beträgt 10 Sekunden | Wenn sich die Anforderungen hier verlangsamen, weist das Projekt wahrscheinlich zu lange Datumsbereiche oder komplexe Visualisierungen auf. Versuchen Sie, den Datumsbereich Ihres Projekts zu verkürzen, um die Verarbeitungszeiten zu verkürzen. |
| [!UICONTROL **Komplexität**] | Nicht alle Anforderungen benötigen dieselbe Verarbeitungszeit. Die Anforderungskomplexität kann dabei helfen, eine allgemeine Vorstellung davon zu erhalten, wie viel Zeit für die Verarbeitung der Anfrage erforderlich ist. Die Richtlinie ist Medium oder niedriger. <p>Mögliche Werte:</p> <ul><li>[!UICONTROL **Niedrig**]</li><li>[!UICONTROL **Medium**]</li><li>[!UICONTROL **Hoch**]</li></ul>Dieser Wert wird durch die Werte in den folgenden Spalten beeinflusst:<ul><li>[!UICONTROL **Monatsgrenzen**]</li><li>[!UICONTROL **Spalten**]</li><li>[!UICONTROL **Segmente**]</li></ul> |  |
| [!UICONTROL **Monatsgrenzen**] | Die Anzahl der Monate, die in einer Anfrage enthalten sind. Mehr Monatsgrenzen erhöhen die Komplexität der Anfrage. Die Richtlinie ist 6 oder weniger. | Wenn sich die Anforderungen hier verlangsamen, liegt dies möglicherweise daran, dass die Monatsgrenzen in Ihrem Projekt zu groß sind. Versuchen Sie, die Anzahl der Monate zu reduzieren. |
| [!UICONTROL **Spalten**] | Die Anzahl der Metriken und Aufschlüsselungen in der Anforderung. Mehr Spalten erhöhen die Komplexität der Anforderung. Die Richtlinie ist 10 oder weniger. | Wenn sich die Anforderungen hier verlangsamen, liegt dies möglicherweise daran, dass Ihr Projekt zu viele Spalten enthält. Versuchen Sie, die Anzahl der Spalten zu reduzieren. |
| [!UICONTROL **Segmente**] | Die Anzahl der Segmente, die auf die Anforderung angewendet werden. Weitere Segmente erhöhen die Komplexität der Anforderung. Die Richtlinie ist 5 oder weniger. | Wenn sich die Anforderungen hier verlangsamen, kann dies daran liegen, dass Ihr Projekt zu viele Segmente enthält. Versuchen Sie, die Anzahl der Segmente zu reduzieren. |

## Zusätzliche Faktoren

Zu den weiteren Faktoren, die nicht unter Hilfe > Leistung aufgeführt sind, zählen:

| Faktor | Definition | Beeinflusst durch | Optimierung |
| --- | --- | --- | --- |
| Segmentkomplexität | Komplizierte Segmente können einen erheblichen Einfluss auf die Projektleistung haben. | Zu den Faktoren, die einem Segment Komplexität verleihen (in grober Reihenfolge der Auswirkungen), gehören: <ul><li>Operatoren von „enthält“, „enthält beliebige von“, „stimmt überein mit“, „beginnt mit“ oder „endet mit“ </li><li>Sequentielle Segmentierung, insbesondere wenn Dimensionseinschränkungen (innerhalb/nachher) verwendet werden </li><li>Anzahl der eindeutigen Dimensionselemente innerhalb der Dimensionen, die im Segment verwendet werden (z. B.: Seite = „A“, wenn Seite 10 eindeutige Elemente hat, ist schneller als Seite = „A“, wenn Seite 100000 eindeutige Elemente hat) </li><li>Anzahl der verschiedenen verwendeten Dimensionen (z. B.: Seite = „Startseite“ und Seite = „Suchergebnisse“ sind schneller als eVar 1 = „rot“ und eVar 2 = „blau“)</li><li>Viele OR-Operatoren (anstelle von AND)</li><li>Verschachtelte Container mit unterschiedlichem Umfang (z. B. Hit innerhalb des Besuchs innerhalb des Besuchers)</li></ul> | Während einige der Komplexitätsfaktoren nicht verhindert werden können, sollten Sie nach Möglichkeiten suchen, die Komplexität Ihrer Segmente zu verringern. Generell gilt: Je genauer Sie mit Ihren Segmentkriterien umgehen können, desto besser. Beispiel:<ul><li>Bei Containern ist die Verwendung eines einzelnen Containers am oberen Rand des Segments schneller als die Verwendung einer Reihe verschachtelter Container</li><li>Bei Operatoren ist „stimmt überein mit“ schneller als „enthält“ und „entspricht beliebigen von“ ist schneller als „enthält beliebige von“</li><li>Mit vielen Kriterien sind AND-Operatoren schneller als eine Reihe von OR-Operatoren.</li></ul> Suchen Sie nach Möglichkeiten, viele OR-Anweisungen in eine einzelne Anweisung „entspricht einem von“ zu reduzieren <br><br>[Classifications](/help/components/classifications/c-classifications.md) können auch dazu beitragen, viele Werte in präzisen Gruppen zu bündeln, aus denen Sie dann Segmente erstellen. Segmentierungen und Classification-Gruppen bieten leistungsbezogene Vorteile gegenüber Segmenten mit vielen OR-Anweisungen oder „enthält“-Kriterien. |
| Komplexität der Visualisierung (Segmente, Metriken, Filter) | Die Art der Visualisierung (z. B. Fallout oder Freiformtabelle), die zu einem Projekt hinzugefügt wird, beeinflusst die Leistung selbst nur geringfügig. Die Verarbeitungszeit wird durch die Komplexität der Visualisierung gesteigert. | U. a. machen folgende Faktoren eine Visualisierung komplexer:<ul><li>Angeforderter Datenbereich</li><li>Anzahl der angewandten Segmente, z. B. als Zeilen verwendete Segmente in einer Freiformtabelle</li><li>Verwendung von komplexen Segmenten</li><li>[Statische Element](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.html?lang=de) zeilen oder Spalten in Freiformtabellen</li><li>Auf Zeilen angewandte Filter in Freiformtabellen</li><li>Anzahl verwendeter Metriken, insbesondere berechneter Metriken, die Segmente verwenden</li></ul> | Wenn Sie bemerken, dass Ihre Projekte langsamer als gewünscht geladen werden, sollten Sie nach Möglichkeit einige Segmente durch eVars und Filter ersetzen.<br><br>Wenn Sie ständig Segmente und berechnete Metriken für Datenpunkte verwenden, die für Ihr Unternehmen wichtig sind, sollten Sie versuchen, Ihre Implementierung zu verbessern, um diese Datenpunkte direkter zu erfassen. Durch die Verwendung von Tags in Adobe Experience Platform und die Verarbeitungsregeln von Adobe können Änderungen an der Implementierung schnell und einfach umgesetzt werden. |
| Größe der Report Suite | Die Menge der in Ihrer Report Suite erfassten Daten. | – | Wenden Sie sich an Ihr Implementierungs-Team oder einen Adobe-Experten, um festzustellen, ob es Verbesserungen bei der Implementierung gibt, die zur Verbesserung des Gesamterlebnisses mit Adobe Analytics beitragen können. |
| Gleichzeitige Abfragen | Die Anzahl der Abfragen, die Ihre Organisation gleichzeitig von Adobe anfordert. Jede Organisation hat Anspruch auf mindestens 5 gleichzeitige Abfragen. | Wenn ein Bericht lange dauert, liegt dies in der Regel daran, dass er sich in einer Warteschlange mit anderen Berichten befindet. Das heißt, dass Ihre Organisation versucht, zu viele Anfragen gleichzeitig für eine bestimmte Report Suite auszuführen. Abfragen können von API-Anfragen, Reporting-Benutzeroberflächen (Analysis Workspace, Report Builder usw.), geplanten Projekten, terminierten Berichten, terminierten Warnhinweisen und gleichzeitig von Benutzenden gestellten Anfragen stammen. | Verteilen Sie Ihre Anfragen und Zeitpläne für die Report Suite gleichmäßig über den Tag. Verlagern Sie außerdem Ihre Anforderungen nach Möglichkeit auf Nebenzeiten. Montagmorgen, Dienstagmorgen und der erste Tag eines Monats sind Spitzenzeiten für das Reporting. |

## Tipps zur Produktivitätssteigerung in Analysis Workspace

Im Folgenden finden Sie ein Video zum Thema:

>[!VIDEO](https://video.tv.adobe.com/v/31157/?quality=12)
