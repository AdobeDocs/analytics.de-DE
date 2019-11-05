---
description: Sequenzielle Segmente werden über den DANN-Operator anstelle von UND oder ODER erstellt. DANN gibt an, dass ein Segmentkriterium gefolgt von einem anderen auftritt. Standardmäßig identifiziert ein sequenzielles Segment alle übereinstimmenden Daten und zeigt den Filter "Alle einschließen"an. Sequenzielle Segmente können mithilfe der Optionen "Nur vor Sequenz"und "Nur nach Sequenz"weiter zu einer Untergruppe übereinstimmender Treffer gefiltert werden.
seo-description: Sequenzielle Segmente werden über den DANN-Operator anstelle von UND oder ODER erstellt. DANN gibt an, dass ein Segmentkriterium gefolgt von einem anderen auftritt. Standardmäßig identifiziert ein sequenzielles Segment alle übereinstimmenden Daten und zeigt den Filter "Alle einschließen"an. Sequenzielle Segmente können mithilfe der Optionen "Nur vor Sequenz"und "Nur nach Sequenz"weiter zu einer Untergruppe übereinstimmender Treffer gefiltert werden.
seo-title: Sequentielle Segmente erstellen
solution: Analytics
title: Sequentielle Segmente erstellen
topic: Segmente
uuid: 7fb9f1c7-a738-416a-aaa2-d77e40fa7e61
translation-type: tm+mt
source-git-commit: 57fe1f6d613b9f54a5191ac8684d36bccfebf4e5

---


# Sequentielle Segmente erstellen

Sequenzielle Segmente werden über den DANN-Operator anstelle von UND oder ODER erstellt. DANN gibt an, dass ein Segmentkriterium gefolgt von einem anderen auftritt. Standardmäßig identifiziert ein sequenzielles Segment alle übereinstimmenden Daten und zeigt den Filter "Alle einschließen"an. Sequenzielle Segmente können mithilfe der Optionen "Nur vor Sequenz"und "Nur nach Sequenz"weiter zu einer Untergruppe übereinstimmender Treffer gefiltert werden.

![](assets/before-after-sequence.png)

Additionally, you can constrain sequential segments to a specific duration of time, granularity, and counts between checkpoints using the [After and Within operators](/help/components/c-segmentation/c-segmentation-workflow/seg-sequential-build.md).

## Alle einschließen {#section_75ADDD5D41F04800A09E592BB2940B35}

Beim Erstellen eines Segments, bei dem "Alle einschließen"festgelegt ist, identifiziert das Segment Pfade, die dem angegebenen Muster als Ganzes entsprechen. Hier ist ein Beispiel für ein einfaches Sequenzsegment, das nach einem Treffer sucht (Seite A), auf den ein weiterer folgt (Seite B), der vom gleichen Besucher besucht wurde. Das Segment ist so eingestellt, dass es alle einschließt.

![](assets/sequence-filter.png)

| Wenn Ergebnis... | Sequenz |
|--- |--- |
| Stimmt überein | A, dann<br>BA, dann (bei einem anderen Besuch)<br>BA, dann D, dann B |
| Stimmt nicht überein mit | B, dann A |

## „Nur vor Sequenz“ und „Nur nach Sequenz“ {#section_736E255C8CFF43C2A2CAAA6D312ED574}

Die Optionen **[!UICONTROL Nur vor Sequenz]** und **Nur nach Sequenz]filtern das Segment vor oder nach der angegebenen Sequenz nach einer Teilmenge an Daten.[!UICONTROL **

* **Nur vor Sequenz**: Umfasst alle Treffer vor einer Sequenz sowie den ersten Treffer der Sequenz selbst (siehe Beispiel 1 und 3). Wenn eine Sequenz mehrere Male in einem Pfad angezeigt wird, enthält "Nur vor Sequenz"den ersten Treffer des letzten Vorkommens der Sequenz und alle vorherigen Treffer (siehe Beispiel 2).
* **Nur nach Sequenz**: Umfasst alle Treffer nach einer Sequenz sowie den letzten Treffer der Sequenz selbst (siehe Beispiel 1 und 3). Wenn eine Sequenz mehrere Male in einem Pfad angezeigt wird, enthält "Nur nach"den letzten Treffer des ersten Vorkommens der Sequenz und alle nachfolgenden Treffer (siehe Beispiel 2).

Betrachten wir beispielsweise eine Sequenz von B gefolgt von D. Die drei Filter würden die Treffer folgendermaßen identifizieren:

**Beispiel 1: B gefolgt von D kommt einmal vor**

| Beispiel | A | B | C | D | E | F |
|---|---|---|---|---|---|---|
| Alle einschließen | A | B | C | D | E | F |
| Nur vor Sequenz | A | B |  |  |  |  |
| Nur nach Sequenz |  |  |  | D | E | F |

**Beispiel 2: B gefolgt von D kommt mehrmals vor**

| Beispiel | A | B | C | D | B | C | D | E |
|---|---|---|---|---|---|---|---|---|
| Alle einschließen | A | B | C | D | B | C | D | E |
| Nur vor Sequenz | A | B | C | D | B |  |  |  |
| Nur nach Sequenz |  |  |  | D | B | C | D | E |

Lassen Sie uns dieses Konzept auch mit der Dimension "Treffertiefe"umreißen.

**Beispiel 3: Treffertiefe 3 gefolgt von 5**

![](assets/hit-depth.png)

## Dimensionsbegrenzungen {#section_EAFD755F8E674F32BCE9B642F7F909DB}

In einer "Innerhalb"-Klausel können Sie zwischen THEN-Anweisungen beispielsweise "innerhalb 1 Suchbegriffsinstanz", "innerhalb 1 eVar 47-Instanz"hinzufügen. Dadurch wird das Segment auf innerhalb einer Instanz einer Dimension beschränkt.

Durch die Festlegung einer "Innerhalb der Dimension"-Klausel zwischen Regeln kann ein Segment Daten auf Sequenzen beschränken, bei denen diese Klausel erfüllt ist. Siehe untenstehendes Beispiel, in dem die Begrenzung auf „Innerhalb 1 Seite“ festgelegt ist:

![](assets/sequence-filter4.png)

| Wenn Ergebnis... | Sequenz |
|--- |--- |
| Stimmt überein | A, dann B |
| Stimmt nicht überein mit | <br> A, dann C, dann B (da B nicht innerhalb einer Seite von A war)**** Hinweis:  Wenn die Dimensionsbeschränkung entfernt wird, stimmen "A, dann B"und "A, dann C, dann B"überein. |

## Einfache Seitenansichtsreihenfolge

Identifizieren Sie Benutzer, die eine Seite und anschließend eine andere Seite angezeigt haben. Die Daten auf Trefferebene filtern diese Sequenz ungeachtet vorheriger, letzter oder zwischenzeitlicher Besuchssitzungen oder der Zeit oder der Anzahl der Seitenansichten, die zwischenzeitlich vergangen ist bzw. erfolgt sind.

**Beispiel**: Besucher hat Seite A und dann Seite B im selben oder einem anderen Besuch angesehen.

**Anwendungsbeispiele**

Die folgenden Beispiele zeigen, wie dieses Segment verwendet werden kann.

1. Besucher einer Sport-Site sehen sich die Football-Landingpage und dann die Basketball-Landingpage in sequenzieller Reihenfolge an, aber nicht unbedingt während desselben Besuchs. Dies löst eine Kampagne aus, die während der Football-Saison Basketball-Inhalte an Football-Besucher liefert.
1. Der Händler ermittelt die Beziehung zwischen denen, die auf der Kundentreueseite landen und dann zu irgendeinem Zeitpunkt während des Besuchs oder bei einem anderen Besuch zur Videoseite wechseln.

**Dieses Segment erstellen**

Sie verschachteln zwei Seitenregeln in einem [!UICONTROL Besucherbehälter] der obersten Ebene und sequenzieren die Seitentreffer mit dem [!UICONTROL DANN]-Operator.

![](assets/segment_sequential_1.png)

## Besuchersequenz über mehrere Besuche hinweg

Identifizieren Sie die Besucher, die aus einer Kampagne herausgefallen, aber im Rahmen einer anderen Sitzung zur Sequenz der Seitenansichten zurückgekehrt sind.

**Beispiel**: Besucher hat Seite A bei einem Besuch und dann Seite B bei einem anderen Besuch angesehen.

**Nutzungsszenarios**

Die folgenden Beispiele zeigen, wie dieser Segmenttyp verwendet werden kann:

* Besucher der Sportseite eine Nachrichten-Site, die anschließend in einer anderen Sitzung die Sportseite erneut besuchen.
* Ein Bekleidungshändler sieht eine Beziehung zwischen Besuchern, die in einer Sitzung auf einer Landingpage ankommen und dann in einer anderen Sitzung direkt zur Kassenseite gehen.

**Dieses Segment erstellen**

In diesem Beispiel sind zwei **[!UICONTROL Besuchebehälter]** im **[!UICONTROL Besucherbehälter]der obersten Ebene verschachtelt und das Segment ist mit dem[!UICONTROL DANN]-Operator sequenziert.**

![](assets/visitor_seq_across_visits.png)

## Sequenz auf gemischten Ebenen

Erkennen von Besuchern, die bei einer nicht festgelegten Anzahl von Besuchen zwei Seiten ansehen, dann aber bei einem separaten Besuch eine dritte Seite ansehen.

**Beispiel**: Besucher besuchen Seite A und dann Seite B bei einem oder mehreren Besuchen, gefolgt von einem Besuch auf Seite C bei einem separaten Besuch.

**Nutzungsszenarios**

Die folgenden Beispiele zeigen, wie dieser Segmenttyp verwendet werden kann:

* Besucher besuchen zuerst eine Nachrichten-Site und sehen sich dann bei demselben Besuch die Sportseite an. Bei einem anderen Besuch sieht sich der Besucher die Wetterseite an.
* Ein Händler definiert Besucher, die die Hauptseite besuchen und dann zur Seite „Mein Konto“ wechseln. Bei einem anderen Besuch besuchen sie die Seite „Einkaufswagen anzeigen“.

**Dieses Segment erstellen**

1. Legen Sie zwei Seitendimensionen aus den linken Fenstern in einem [!UICONTROL Besucherbehälter] der obersten Ebene ab.
1. Fügen Sie zwischen den beiden den DANN-Operator ein. 
1. Click **[!UICONTROL Options]** &gt; **[!UICONTROL Add container]** and add a [!UICONTROL Visit] container underneath the [!UICONTROL Visitor] level and sequenced using the [!UICONTROL THEN] operator.

![](assets/mixed_level_checkpoints.png)

## Aggregatbehälter

Durch das Hinzufügen mehrerer [!UICONTROL Trefferbehälter] innerhalb eines [!UICONTROL Besucherbehälters] können Sie die entsprechenden Operatoren zwischen identischen Behältertypen anwenden und Regeln und Dimensionen wie Seiten- und Besuchsnummer verwenden, um die Seitenansicht zu definieren und eine Sequenzdefinition innerhalb des [!UICONTROL Trefferbehälters] bereitzustellen. Wenn Sie eine Logik auf Trefferebene anwenden, können Sie Übereinstimmungen einschränken und als Treffer derselben Ebene im [!UICONTROL Besucherbehälter] kombinieren, um eine Vielzahl von Segmenttypen zu erstellen.

**Beispiel**: Die Besucher haben Seite A nach dem ersten Treffer in der Sequenz von Seitenansichten (in diesem Beispiel Seite D) besucht. Anschließend haben sie ungeachtet der Anzahl der Besuche entweder Seite B oder Seite C besucht.

**Nutzungsszenarios**

Die folgenden Beispiele zeigen, wie dieser Segmenttyp verwendet werden kann:

* Erkennen von Besuchern, die während eines Besuchs zur Haupt-Landingpage gelangen, dann bei einem anderen Besuch die Herrenbekleidungsseite ansehen und sich dann bei einem anderen Besuch entweder die Landingpage für Damen- oder Kinderbekleidung ansehen.
* Ein e-Zine erfasst Besucher, die bei einem Besuch die Homepage besuchen, bei einem anderen Besuch die Sportseite und bei einem anderen Besuch die Kommentarseite.

**Dieses Segment erstellen**

1. Wählen Sie den [!UICONTROL Besucherbehälter] als Behälter der obersten Ebene aus.
1. Fügen Sie zwei weitere Behälter der [!UICONTROL Trefferebene] hinzu – eine Dimension mit einer geeigneten numerischen Dimension wurde auf derselben [!UICONTROL Trefferebene] durch die [!UICONTROL UND]- und [!UICONTROL ODER]-Operatoren verknüpft.
1. Fügen Sie im [!UICONTROL Besuchsbehälter] einen weiteren [!UICONTROL Trefferbehälter] hinzu und verschachteln Sie zwei weitere [!UICONTROL Trefferbehälter], die mit einem [!UICONTROL ODER]- oder [!UICONTROL UND]-Operator verknüpft wurden.

   Sequenzieren Sie die verschachtelten [!UICONTROL Trefferbehälter] mit dem [!UICONTROL DANN]-Operator.

![](assets/aggregate_checkpoints2.png)

## "Verschachtelung"in sequenziellen Segmenten

Durch das Positionieren von Checkpoints auf [!UICONTROL Besuchs-] und [!UICONTROL Trefferebene] können Sie das Segment so einschränken, dass Anforderungen innerhalb eines spezifischen Besuchs sowie an einen spezifischen Treffer erfüllt werden.

**Beispiel**: Besucher besuchte Seite A und besuchte dann Seite B im selben Besuch. Bei einem neuen Besuch ist der Besucher dann zur Seite C gewechselt.

**Dieses Segment erstellen**

1. Legen Sie unter einem [!UICONTROL Besuchebehälter] der obersten Ebene zwei Seitendimensionen ab.
1. Multi-select both rules, click **[!UICONTROL Options]** &gt; **[!UICONTROL Add container from selection]** and change it to a [!UICONTROL Visit] container.
1. Verbinden Sie beide mit einem [!UICONTROL DANN]-Operator.
1. Erstellen Sie einen Trefferbehälter, der gleichrangig zum [!UICONTROL Besuchebehälter] ist, und legen Sie darin eine Seitendimension ab.
1. Verknüpfen Sie die verschachtelte Sequenz im [!UICONTROL Besuchsbehälter] mit dem [!UICONTROL Trefferbehälter]. Verwenden Sie dazu einen weiteren [!UICONTROL DANN]-Operator.

![](assets/nesting_sequential_seg.png)

## Treffer ausschließen

Segmentregeln beinhalten alle Daten, es sei denn, Sie schließen mithilfe der Regel zum [!UICONTROL Ausschließen] [!UICONTROL Besucher-], [!UICONTROL Besuchs-] oder [!UICONTROL Trefferdaten] aus. Sie ermöglicht Ihnen das Auslassen allgemeiner Daten und das gezieltere Erstellen von Segmenten. Alternativ ermöglicht sie Ihnen das Erstellen von Segmenten ohne gefundene Gruppen, um den verbleibenden Datensatz zu identifizieren. Sie können beispielsweise eine Regel erstellen, die erfolgreiche Besucher mit aufgegebenen Bestellungen einschließt und diese dann ausschließt, um die „Nicht-Käufer“ zu identifizieren. In den meisten Fällen ist es jedoch besser, Regeln zum Ausschließen umfassender Werte zu erstellen, anstelle zu versuchen, die [!UICONTROL Ausschlussregel] für spezielle Einschlusswerte zu verwenden.

Beispiel:

* **Schließen Sie Seiten aus**. Verwenden Sie eine Segmentregel, um eine spezielle Seite aus einem Bericht zu entfernen (beispielsweise die *`Home Page`*) from a report, create a Hit rule where the page equals "Home Page," and then exclude it. Diese Regel schließt mit Ausnahme der Homepage automatisch alle Werte ein.
* **Schließen Sie die Referrerdomäne aus**. Verwenden Sie eine Regel, die nur Referrerdomänen aus „Google.com“ einschließt und alle anderen Domänen ausschließt.
* **Identifizieren Sie Nicht-Käufer**. Bestimmen Sie, wann Bestellungen größer als null sind, und schließen Sie dann den [!UICONTROL Besucher] aus.

Der [!UICONTROL Ausschlussoperator] kann zum Identifizieren einer Sequenz verwendet werden, in der vom Besucher keine spezifischen Besuche oder Treffer ausgeführt wurden. [!UICONTROL Ausschluss-Checkpoints] können auch in eine [logische Gruppe](/help/components/c-segmentation/c-segmentation-workflow/seg-sequential-build.md).

### Ausschluss zwischen Checkpoints

Erzwingen Sie das Segmentieren von Besuchern mit einer Logik, wenn ein Checkpoint nicht explizit zwischen zwei anderen Checkpoints aufgetreten ist.

**Beispiel**: Besucher, die Seite A und dann Seite C besucht haben, aber Seite B nicht besucht haben.

**Nutzungsszenarios**

Die folgenden Beispiele zeigen, wie dieser Segmenttyp verwendet werden kann:

* Besucher einer Lifestyle-Seite, die direkt den Theaterbereich aufsuchen, ohne die Feuilletonseite zu besuchen.
* Ein Autohändler sieht einen Zusammenhang zwischen denen, die die Haupt-Landingpage besuchen und dann direkt zur „Kein Interesse“-Kampagne wechseln, ohne die Fahrzeugseite zu besuchen.

**Dieses Segment erstellen**

Erstellen Sie ein Segment, wie Sie dies für ein  einfaches oder verschachteltes sequenzielles Segment bzw. ein Segment mit gemischten Ebenen tun würden, und legen Sie dann den [!UICONTROL AUSSCHLIESSEN]-Operator für das Behälterelement fest. Bei dem Beispiel unten handelt es sich um ein aggregiertes Segment, bei dem die drei [!UICONTROL Trefferbehälter] in die Arbeitsfläche gezogen wurden, der [!UICONTROL DANN]-Operator für die Verknüpfung mit der Behälterlogik zugeordnet wurde und dann der mittlere Seitenansichtsbehälter ausgeschlossen wurde, um nur die Besucher aufzunehmen, die in der Sequenz von Seite A zu Seite C gewechselt sind.

![](assets/exclude_between_checkpoints.png)

### Am Anfang der Sequenz ausschließen

Wenn sich der Ausschluss-Checkpoint am Anfang eines sequenziellen Segments befindet, wird sichergestellt, dass vor dem ersten nicht ausgeschlossenen Treffer keine ausgeschlossene Seitenansicht aufgetreten ist.

**Beispiel**: Besucher besuchte Seite A und nicht Seite B.

**Nutzungsszenarios**

Im Folgenden finden Sie Beispiele für Anwendungsfälle, wie dieser Segmenttyp verwendet werden kann:

* Besucher, die Seite A, aber nicht Seite B besucht haben.
* Ein Restaurant möchte treue Benutzer erkennen, die die Haupt-Landingpage umgehen und direkt zur Bestellseite navigieren.

**Dieses Segment erstellen**

Erstellen Sie zwei separate Trefferbehälter in einem Besucherbehälter der obersten Ebene. Legen Sie anschließend den [!UICONTROL AUSSCHLIESSEN]-Operator für den ersten Behälter fest.

![](assets/exclude_beginning_sequence.png)

### Am Ende der Sequenz ausschließen

Wenn der Ausschluss-Checkpoint am Ende einer Sequenz liegt, wird sichergestellt, dass der Checkpoint nicht zwischen dem letzten nicht ausgeschlossenen Checkpoint und dem Ende der Besuchersequenz auftritt.

**Beispiel**: Besucher besuchen Seite A und besuchten dann Seite B bei den aktuellen oder nachfolgenden Besuchen nicht.

**Nutzungsszenarios**

Die folgenden Beispiele zeigen, wie dieser Segmenttyp verwendet werden kann:

* Besucher, die Seite A, aber nicht Seite B besucht haben.
* Ein Restaurant möchte treue Benutzer erkennen, die die Haupt-Landingpage umgehen und direkt zur Bestellseite navigieren.

**Dieses Segment erstellen**

Build a simple sequence segment by dragging two [!UICONTROL Hit] containers to the canvas and connecting them using the [!UICONTROL THEN] operator. Weisen Sie dann den [!UICONTROL AUSSCHLIESSEN]-Operator dem zweiten [!UICONTROL Trefferbehälter] in der Sequenz zu.

![](assets/exclude_end_sequence.png)

## Logische Gruppenbehälter

Logische Gruppenbehälter sind erforderlich, um Bedingungen in einem einzigen sequenziellen Segmentprüfpunkt zu gruppieren. Der spezielle logische Gruppenbehälter ist nur in der sequenziellen Segmentierung verfügbar, um sicherzustellen, dass seine Bedingungen nach einem vorherigen sequenziellen Checkpoint und vor einem nachfolgenden sequenziellen Checkpoint erfüllt werden. Die Bedingungen innerhalb des Checkpoints für logische Gruppen können in beliebiger Reihenfolge erfüllt werden. Dagegen erfordern nicht sequenzielle Behälter (Treffer, Besuch, Besucher) nicht, dass ihre Bedingungen innerhalb der Gesamtsequenz erfüllt werden, was bei Verwendung mit einem DANN-Operator zu intuitiven Ergebnissen führt.
Der [!UICONTROL logische Gruppenbehälter] wurde so konzipiert, dass *mehrere Checkpoints als Gruppe* behandelt werden können, *ohne dass eine Reihenfolge* zwischen den gruppierten Checkpoints erfolgt. Mit anderen Worten, die Reihenfolge der Checkpoints in dieser Gruppe ist uns egal. Sie können beispielsweise einen [!UICONTROL Besucherbehälter] nicht in einem [!UICONTROL Besuchsbehälter] verschachteln. But instead, you can nest a [!UICONTROL Logic Group] container within a [!UICONTROL Visitor] container with specific [!UICONTROL Visit]-level and [!UICONTROL Hit]-level checkpoints.

> [!NOTE] Eine [!UICONTROL logische Gruppe] kann nur in einem sequenziellen Segment definiert werden, d. h. der [!UICONTROL DANN] -Operator wird im Ausdruck verwendet.

| Behälterhierarchie | Illustration | Definition |
|---|---|---|
| Standardbehälterhierarchie | ![](assets/nesting_container.png) | Innerhalb des [!UICONTROL Besuchercontainers] werden die Container für [!UICONTROL Besuche] und [!UICONTROL Treffer] in einer Sequenz verschachtelt, um Segmente basierend auf Treffern, der Anzahl der Besuche und basierend auf dem Besucher zu extrahieren. |
| Logische Behälterhierarchie | ![](assets/logic_group_hierarchy.png) | Die Standardbehälterhierarchie ist auch außerhalb des [!UICONTROL logischen Gruppenbehälters] erforderlich. Innerhalb des [!UICONTROL logischen Gruppenbehälters] ist für die Checkpoints jedoch keine bestimmte Reihenfolge oder Hierarchie erforderlich. Diese Checkpoints müssen einfach vom Besucher in beliebiger Reihenfolge getroffen werden. |

Logische Gruppen mögen abschreckend erscheinen - hier einige Best Practices für ihre Verwendung:

**Logische Gruppe oder Treffer-/Besuchsbehälter?**
Wenn Sie sequenzielle Checkpoints gruppieren möchten, lautet Ihr "Container"logische Gruppe. Müssen diese sequenziellen Checkpoints jedoch innerhalb eines einzelnen Treffers oder Besuchs auftreten, ist ein Treffer oder ein Besuchsbehälter erforderlich. (Natürlich ergibt "Treffer"keinen Sinn für eine Gruppe sequenzieller Checkpoints, wenn einem Treffer nicht mehr als ein Checkpoint gutgeschrieben werden kann).

**Vereinfachen logische Gruppen das Erstellen sequenzieller Segmente?**
Ja, sie können. Nehmen wir einmal an, Sie versuchen, diese Frage zu beantworten: Hat ein Besucher nach Seite A Seite B, Seite C oder Seite D **gesehen?**

Sie können dieses Segment ohne logischen Gruppenbehälter erstellen, es ist jedoch komplex und aufwändig:
* `Visitor Container [Page A THEN Page B THEN Page C THEN Page D] or`
* `Visitor Container [Page A THEN Page B THEN Page D THEN Page C] or`
* `Visitor Container [Page A THEN Page C THEN Page B THEN Page D] or`
* `Visitor Container [Page A THEN Page C THEN Page D THEN Page B] or`
* `Visitor Container [Page A THEN Page D THEN Page B THEN Page C] or`
* `Visitor Container [Page A THEN Page D THEN Page C THEN Page B]`

Ein logischer Gruppenbehälter vereinfacht das Erstellen dieses Segments erheblich, wie im Folgenden gezeigt:

![](assets/logic-grp-example.png)


### Build a Logic Group segment {#section_A5DDC96E72194668AA91BBD89E575D2E}

Wie andere Behälter können auch [!UICONTROL logische Gruppenbehälter] auf mehrere Arten innerhalb des [!UICONTROL Segmentaufbaus]erstellt werden. Hier finden Sie eine bevorzugte Methode zum Verschachteln von [!UICONTROL logischen Gruppenbehältern]:

1. Ziehen Sie Dimensionen, Ereignisse oder Segmente aus den linken Fenstern.
1. Ändern Sie den oberen Behälter in einen [!UICONTROL Besucher]behälter.
1. Ändern Sie den standardmäßig eingefügten [!UICONTROL UND]- oder [!UICONTROL ODER]-Operator in den DANN-Operator.
1. Select the [!UICONTROL Hit] containers (the Dimension, Event, or Item) and click **[!UICONTROL Options]** &gt; **[!UICONTROL Add container from selection]**.
1. Klicken Sie auf das Behältersymbol und wählen Sie **[!UICONTROL Logische Gruppe aus]**.  ![](assets/logic_group_checkpoints.png)
1. Nun können Sie die [!UICONTROL Treffer] im [!UICONTROL logischen Gruppenbehälter] ungeachtet der Hierarchie festlegen.

### Checkpoints für logische Gruppen in beliebiger Reihenfolge

Die Verwendung der [!UICONTROL logischen Gruppe] ermöglicht Ihnen das Erfüllen von Bedingungen innerhalb der jeweiligen Gruppe, die sich außerhalb der Sequenz befinden. Dies ermöglicht Ihnen das Erstellen von Segmenten, in denen ungeachtet der normalen Hierarchie ein [!UICONTROL Besuchs-] oder [!UICONTROL Trefferbehälter] existiert.

**Beispiel**: Besucher, die Seite A und dann Seite B und C in beliebiger Reihenfolge besucht haben.

**Dieses Segment erstellen**

Seite B und C sind in einem [!UICONTROL logischen Gruppenbehälter] innerhalb des äußeren [!UICONTROL Besucherbehälters] verschachtelt. Der [!UICONTROL Trefferbehälter] für A wird anschließend vom [!UICONTROL logischen Gruppenbehälter] gefolgt, wobei B und C mithilfe des [!UICONTROL UND]-Operators identifiziert werden. Because it is in the [!UICONTROL Logic Group], the sequence is not defined and hitting both page B and C in any order makes the argument true.

![](assets/logic_group_any_order2.png)

**Ein weiteres Beispiel**: Besucher, die Seite B oder C und dann Seite A besucht haben:

![](assets/logic_group_any_order3.png)

Das Segment muss mindestens mit einem der Checkpoints der logischen Gruppe (B oder C) übereinstimmen. Auch können die Bedingungen für logische Gruppen im selben Treffer oder über mehrere Treffer hinweg erfüllt werden. &#x200B;

### Erste Übereinstimmung mit der logischen Gruppe

Die Verwendung der [!UICONTROL logischen Gruppe] ermöglicht Ihnen das Erfüllen von Bedingungen innerhalb der jeweiligen Gruppe, die sich außerhalb der Sequenz befinden. In diesem nicht geordneten Segment der ersten Übereinstimmung werden die Regeln der [!UICONTROL logischen Gruppe] zuerst als Seitenansicht von Seite B oder C und dann als erforderliche Ansicht von Seite A identifiziert.

**Beispiel**: Besucher, die Seite B oder C und dann Seite A besucht haben.

**Dieses Segment erstellen**

Die Dimensionen von Seite B und C werden innerhalb eines [!UICONTROL logischen Gruppenbehälters] gruppiert, wobei der [!UICONTROL ODER]-Operator ausgewählt ist. Dann folgt der [!UICONTROL Trefferbehälter], der eine Seitenansicht von Seite A als Wert definiert.

![](assets/logic_group_1st_match.png)

### Logische Gruppe ausschließen UND

Erstellen Sie mithilfe der [!UICONTROL logischen Gruppe] Segmente, wobei mehrere Seitenansichten aggregiert werden, um zu definieren, welche Seiten getroffen werden müssen, während andere Seiten speziell ausgelassen wurden. ****

**Beispiel**: Besucher hat Seite A besucht und dann explizit nicht Seite B oder C besucht, sondern Seite D getroffen.

**Dieses Segment erstellen**

Erstellen Sie dieses Segment, indem Sie Dimensionen, Ereignisse und vorgefertigte Segmente aus den linken Fenstern ziehen. Siehe [Erstellen eines logischen Gruppensegments](/help/components/c-segmentation/c-segmentation-workflow/seg-sequential-build.md).

Klicken Sie nach dem Verschachteln der Werte in der [!UICONTROL logischen Gruppe] im **[!UICONTROL logischen Gruppenbehälter]** auf die Schaltfläche [!UICONTROL Ausschließen].

![](assets/logic_exclude_and.png)

### Logische Gruppe - ODER

Erstellen Sie mithilfe der [!UICONTROL logischen Gruppe] Segmente, wobei mehrere Seitenansichten aggregiert werden, um zu definieren, welche Seiten getroffen werden müssen, während andere Seiten speziell ausgelassen wurden.

**Beispiel**: Besucher, die Seite A, aber vor Seite A weder Seite B noch Seite C besucht haben.

**Dieses Segment erstellen**

Die ursprünglichen Seiten B und C werden in einem ausgeschlossenen [!UICONTROL logischen Gruppenbehälter] identifiziert und werden dann von einem Treffer auf Seite A durch den Besucher gefolgt.

Erstellen Sie dieses Segment, indem Sie Dimensionen, Ereignisse und vorgefertigte Segmente aus den linken Fenstern ziehen.

Klicken Sie nach dem Verschachteln der Werte in der [!UICONTROL logischen Gruppe] im **[!UICONTROL logischen Gruppenbehälter]** auf die Schaltfläche [!UICONTROL Ausschließen].

![](assets/logic_exclude_or.png)

## Erstellen von Zeit- und Nachschlagesegmenten

Mithilfe der in die Kopfzeilen der einzelnen Behälter integrierten [!UICONTROL In]- und [!UICONTROL Nach]-Operatoren können Sie die Zeit, Ereignisse und Anzahl definieren.

![](assets/then_within_operators.png)

Mit den [!UICONTROL In]- und [!UICONTROL Nach]-Behältern und durch Angabe einer Granularität und Anzahl können Sie die Übereinstimmung auf eine angegebene Zeitdauer beschränken. Der [!UICONTROL In]-Operator wird zum Angeben einer maximalen Zeitbegrenzung zwischen zwei Checkpoints verwendet. Mit dem [!UICONTROL Nach]-Operator wird eine minimale Zeitbegrenzung zwischen zwei Checkpoints angegeben.

### Nach- und In-Operatoren {#section_CCAF5E44719447CFA7DF8DA4192DA6F8}

Die Dauer wird durch einen einzelnen Großbuchstaben für die Granularität gefolgt von einer Zahl für die Wiederholungszahl der Granularität angegeben.

**[!UICONTROL In]** schließt den Endpunkt ein (kleiner gleich).

**[!UICONTROL Nach]** schließt den Endpunkt nicht mit en (größer als).

| Operatoren | Beschreibung |
|--- |--- |
| NACH | Der Nach-Operator wird zum Angeben einer minimalen Zeitbegrenzung zwischen zwei Checkpoints verwendet. Beim Festlegen der Nach-Werte beginnt die Zeitbegrenzung mit dem Anwenden des Segments. Wenn der Nach-Operator beispielsweise für einen Behälter festgelegt ist, um Besucher zu identifizieren, die Seite A besuchen, aber erst nach einem Tag zum Besuch von Seite B zurückkehren, beginnt dieser Tag, wenn der Besucher Seite A verlässt.  Damit der Besucher in das Segment einbezogen wird, müssen nach dem Verlassen von Seite A zur Ansicht von Seite B mindestens 1440 Minuten (ein Tag) vergehen. |
| IN | Der In-Operator wird zum Angeben einer maximalen Zeitbegrenzung zwischen zwei Checkpoints verwendet. Wenn der In-Operator beispielsweise für einen Behälter festgelegt ist, um Besucher zu identifizieren, die Seite A besuchen und dann innerhalb eines Tages zurückkehren, um Seite B zu besuchen, beginnt dieser Tag, sobald der Besucher Seite A verlässt. Um in das Segment aufgenommen zu werden, hat der Besucher eine maximale Zeit von einem Tag, bevor er Seite B öffnet.   Damit der Besucher in das Segment eingeschlossen wird, muss der Besuch auf Seite B innerhalb von maximal 1440 Minuten (einen Tag) erfolgen, nachdem die Seite A zur Ansicht von Seite B verlassen wurde. |
| NACH/IN | Beim Verwenden der Nach- und In-Operatoren gilt es zu beachten, dass beide Operatoren parallel und nicht sequenziell beginnen und enden.   For example, if you build a segment with the container set to:<br>`After = 1 Week(s) and Within = 2 Week(s)`<br>Then the conditions to identify visitors in the segment are met only between 1 and 2 weeks. Beide Bedingungen werden vom Zeitpunkt des ersten Seitentreffers an erzwungen. |

### Nach-Operator verwenden

* Der Nach-Zeitoperator ermöglicht Ihnen eine Verfolgung nach Jahr, Monat, Tag, Stunde und Minute, um Besuche zuzuordnen.
* Der Nach-Zeitoperator kann nur auf einen [!UICONTROL Trefferbehälter] angewendet werden, da dies die einzige Ebene ist, für die eine solch feine Granularität definiert ist.

**Beispiel**: Besucher, die Seite A und dann Seite B erst nach 2 Wochen besucht haben.****

![](assets/time_between_after_operator.png)

**Segment** erstellen: Dieses Segment wird durch Hinzufügen eines [!UICONTROL Besucherbehälters] mit zwei [!UICONTROL Trefferbehältern] erstellt. Anschließend können Sie den [!UICONTROL DANN]-Operator festlegen und die Dropdown-Liste für den [!UICONTROL NACH]-Operator öffnen, um die Wochenanzahl festzulegen.

![](assets/after_operator.png)

**Stimmt überein mit**

Wenn „Nach 2 Wochen“ festgelegt ist und am 1. Juni 2019 um 00:01 Uhr auf Seite A ein Treffer stattfindet, stimmt ein darauf folgender Treffer auf Seite B überein, sofern er vor dem 15. Juni 2019 um 00:01 Uhr (14 Tage später) erfolgt. 

| Treffer A | Treffer B | Übereinstimmend |
|--- |--- |--- |
| Treffer **A**: 01. Juni 2019 00:01 | Treffer **B**: 15. Juni 2019 00:01 | **** Sucht: Diese Zeitbeschränkung stimmt überein, da sie nach dem 1. Juni 2019 (zwei Wochen) liegt. |
| Treffer **A**: 01. Juni 2019 00:01 | **Treffer B** : Treffer 8. Juni 2019 00:01 B: 15. Juni 2019 00:01 | **** Stimmt nicht überein: Der erste Treffer auf Seite B stimmt nicht überein, da er mit der Beschränkung in Konflikt steht, die nach zwei Wochen erforderlich ist. |

### Verwenden Sie den In-Operator

* Mit dem [!UICONTROL In]-Operator können Sie eine Verfolgung nach Jahr, Monat, Tag, Stunde und Minute ausführen, um Besuche zuzuordnen.
* Der [!UICONTROL In]-Operator kann nur auf einen [!UICONTROL Trefferbehälter] angewendet werden, da dies die einzige Ebene ist, für die eine solch feine Granularität definiert ist.

>[!IMPORTANT]
>
>In einer "Innerhalb"-Klausel können Sie zwischen THEN-Anweisungen beispielsweise "innerhalb 1 Suchbegriffsinstanz", "innerhalb 1 eVar 47-Instanz"hinzufügen. Dadurch wird das Segment auf innerhalb einer Instanz einer Dimension beschränkt.

**Beispiel**: Besucher, die Seite A und dann innerhalb von 5 Minuten Seite B besucht haben.

![](assets/time_between_within_operator.png)

**Segment** erstellen: Dieses Segment wird erstellt, indem ein [!UICONTROL Besucherbehälter] hinzugefügt und dann mit zwei [!UICONTROL Trefferbehältern] gezogen wird. Dann können Sie den [!UICONTROL DANN]-Operator festlegen und das Dropdown-Feld [!UICONTROL NACH] öffnen, um das Intervall festzulegen: Treffer, Seitenansichten, Besuche, Minuten, Stunden, Tage, Wochen, Monate, Quartale oder Jahre.

![](assets/within_operator.png)

**Stimmt überein mit**

Übereinstimmungen müssen innerhalb der Zeitbeschränkung erfolgen. Wenn ein Besucher bei dem Ausdruck um 00:01 Uhr Seite A trifft, stimmt ein darauf folgender Treffer auf Seite B überein, solange er an oder vor 00:06 Uhr erfolgt (fünf Minuten später, einschließlich derselben Minute). Mit Treffern innerhalb derselben Minuten werden ebenfalls Treffer erzielt.

### Die In- und Nach-Operatoren

Verwenden Sie die [!UICONTROL In]- und [!UICONTROL Nach]-Operatoren zum Bereitstellen eines maximalen und minimalen Endpunkts an beiden Enden eines Segments.

**Beispiel**: Besucher, die Seite A und dann Seite B nach 2 Wochen, aber innerhalb eines Monats besucht haben.

![](assets/time_between_using_both_operators.png)

**Segment** erstellen: Erstellen Sie das Segment, indem Sie zwei [!UICONTROL Trefferbehälter] in einem [!UICONTROL Besucherbehälter] sequenzieren. Legen Sie anschließend die [!UICONTROL Nach]- und [!UICONTROL In]-Operatoren fest.

![](assets/within_after_together.png)

**Stimmt überein mit**

Es werden alle Besucher in das Segment eingeschlossen, die am 1. Juni 2019 auf Seite A einen Treffer erzielen und die nach dem 15. Juni 2019, aber *vor* dem 1. Juli 2019 zurückkehren. Siehe im Vergleich [Zeit zwischen Ausschlüssen](/help/components/c-segmentation/c-segmentation-workflow/seg-sequential-build.md).

Die [!UICONTROL Nach]- und [!UICONTROL In]-Operatoren können zusammen verwendet werden, um ein sequenzielles Segment zu definieren.

![](assets/time_between_within_after.png)

In diesem Beispiel wird ein zweiter Besuch zum Erzielen eines Treffers auf Seite B nach zwei Wochen aber innerhalb eines Monats dargestellt.
