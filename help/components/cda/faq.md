---
title: Häufig gestellte Fragen zur geräteübergreifenden Analyse
description: Häufig gestellte Fragen zur geräteübergreifenden Analyse
exl-id: 7f5529f6-eee7-4bb9-9894-b47ca6c4e9be
feature: CDA
role: Admin
TQID: 'https://experienceleague.adobe.com/tdOmNG-s2F-KOq9fCMILkovykm3gknjnS-8JdxiGnm4'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4
    internal-label: Attribution
  - id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2
    internal-label: VRS
  - id: dcae653e-62c6-4cc8-84e6-ee110b848296
    internal-label: Visualizations
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
    internal-label: Report suites
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
    internal-label: Events
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
  - id: f99536a1-75c7-4151-a2c8-073630632526
    internal-label: CDA
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: c426cc55c1888aa690748fab2c4a7b28fbba8dec
workflow-type: tm+mt
source-wordcount: '1728'
ht-degree: 95%
---
# Häufig gestellte Fragen

{{available-existing-customers}}

+++ Wie kann ich CDA verwenden, um zu sehen, wie Benutzende von einem Gerätetyp zum anderen wechseln?

Sie können eine [!UICONTROL Fluss]-Visualisierung mit der Dimension „Mobilgerätetyp“ verwenden.

1. Melden Sie sich bei Adobe Analytics an und erstellen Sie ein neues leeres Workspace-Projekt.
2. Klicken Sie auf der linken Seite auf die Registerkarte „Visualisierungen“ und ziehen Sie eine Flussvisualisierung in die Arbeitsfläche auf der rechten Seite.
3. Klicken Sie links auf die Registerkarte Komponenten und ziehen Sie die Dimension „Mobilgerätetyp“ an die mittlere Position mit der Bezeichnung &quot;Dimension oder Element“.
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

+++

+++ Kann ich sehen, wie Benutzer zwischen verschiedenen Benutzererlebnissen wechseln (z. B. zwischen Desktop-Browser, mobilem Browser und Mobile App)?

Anhand des Beispiels mit dem oben beschriebenen Mobilgerätetyp können Sie sehen, wie Personen zwischen Mobilgerätetypen und Desktop-Gerätetypen wechseln. Desktop-Browser können jedoch nicht von mobilen Browsern unterschieden werden. Wenn Sie diese Information wünschen, können Sie eine benutzerdefinierte Variable erstellen (z. B. eine Prop oder eVar), die aufzeichnet, ob das Erlebnis in einem Desktop-Browser, einem mobilen Browser oder einer Mobile App stattfand. Anschließend können Sie ein Flussdiagramm wie oben beschrieben erstellen, indem Sie die benutzerdefinierte Variable anstelle der Mobilgerätetyp-Dimension verwenden. Durch diese Methode erhalten Sie eine etwas andere Ansicht des geräteübergreifenden Verhaltens.

+++

+++ Wie weit reicht die Zuordnung der geräteübergreifenden Analyse für Besucher zurück?

Die geräteübergreifende Zuordnung der Cross-Device-Analyse erfolgt in zwei gleichzeitigen Prozessen.

* Das erste Verfahren wird als „Live Stitching“ bezeichnet und läuft ab, wenn die Daten in Adobe Analytics strömen. Während der Live-Zuordnung versucht die Cross-Device-Analyse, die Daten auf Personenebene neu darzustellen. Ist die Person zum Zeitpunkt der Live-Zuordnung jedoch unbekannt, nutzt die Cross-Device-Analyse zur Darstellung der Person die Besucher-ID.

* Der zweite Prozess ist die sogenannte „Wiederholung“. Während der Wiederholung geht die Cross-Device-Analyse in der Zeit zurück und ordnet soweit möglich historische Daten innerhalb eines bestimmten Rückblickfensters neu zu. Dieses Rückblickfenster dauert je nach Konfiguration der Cross-Device-Analyse entweder 1 Tag oder 7 Tage. Während der Wiederholung versucht die Cross-Device-Analyse, Treffer neu darzustellen, bei denen die Person vorher unbekannt war.


+++

+++ Wie behandelt die Cross-Device-Analyse Treffer mit Zeitstempel?

Adobe behandelt Treffer mit Zeitstempel so, als wären sie zum Zeitpunkt des Zeitstempels eingegangen, nicht zum Zeitpunkt, zu dem Adobe den Treffer erhalten hat. Treffer mit Zeitstempel, die älter als 1 Monat sind, werden nie gestitcht, da sie außerhalb des Bereichs liegen, den Adobe zum Stitching verwendet.

+++

+++ Wie unterscheidet sich die Cross-Device-Analyse von der benutzerdefinierten Besucher-ID?

Die Verwendung einer benutzerdefinierten Besucher-ID ist eine veraltete Methode, Benutzende geräteübergreifend zu verbinden. Bei einer benutzerspezifischen Besucher-ID verwenden Sie die [`visitorID`](/help/implement/vars/config-vars/visitorid.md)-Variable, um die für die Besucherlogik verwendete ID explizit festzulegen. Die `visitorID`-Variable setzt alle Cookie-basierten IDs außer Kraft, die vorhanden sind.

Benutzerdefinierte Besucher-IDs haben mehrere unerwünschte Seiteneffekte, die durch CDA überwunden oder minimiert werden. Beispielsweise verfügt die Methode der benutzerspezifischen Besucher-ID über keine [Wiederholungsfunktionen](replay.md). Wenn sich ein Benutzer während eines Besuchs authentifiziert, wird der erste Teil des Besuchs mit einer anderen Besucher-ID verknüpft als der letzte Teil des Besuchs. Die separaten Besucher-IDs führen zu Besuchs- und Besucherinflation. CDA stellt historische Daten erneut dar, sodass nicht authentifizierte Treffer der richtigen Person zugeordnet werden.

+++

+++ Kann ich von der benutzerdefinierten Besucher-ID zu CDA wechseln?

Kunden, die bereits eine benutzerdefinierte Besucher-ID verwenden, können auf CDA aktualisieren, ohne dass sich die Implementierung ändert. Die `visitorID`-Variable wird weiterhin in der Quell-Report Suite verwendet. Die geräteübergreifende Analyse ignoriert jedoch die `visitorID`-Variable in der Virtual Report Suite, wenn sich ein Benutzer authentifiziert.

+++



+++ Wie behandelt die geräteübergreifende Analyse Situationen, in denen eine einzelne Person über VIELE Geräte/ECIDs verfügt?

In bestimmten Situationen kann ein einzelner Benutzer mit einer großen Anzahl von ECIDs verknüpft sein. Dies kann vorkommen, wenn der Benutzer eine Vielzahl von Browsern oder Apps verwendet, vor allem dann, wenn er häufig Cookies löscht oder den privaten oder Inkognito-Modus des Browsers verwendet.

* **Bei der Verwendung des feldbasierten Stitching** ist die Anzahl der Geräte für die Prop/eVar, die Sie zur Identifizierung der angemeldeten Benutzer verwenden, irrelevant. Ein einzelner Benutzer oder eine einzelne Benutzerin kann zu einer beliebigen Anzahl von Geräten gehören, ohne dass sich dies auf die Fähigkeit von CDA auswirkt, Daten geräteübergreifend zu verknüpfen.

+++

+++ Was ist der Unterschied zwischen der Metrik „Personen“ in CDA und der Metrik „Unique Visitors“ außerhalb von CDA?

Die Metriken [Personen](/help/components/metrics/people.md) und [Unique Visitors](/help/components/metrics/unique-visitors.md) zählen einzelne Besucher (Einzelpersonen). Beachten Sie jedoch, dass zwei verschiedene Geräte derselben Person gehören können. Cross-Device Analytics (CDA) ordnet die beiden Geräte derselben Person zu, während die zwei Geräte außerhalb von CDA als zwei separate „Unique Visitors“ erfasst werden.

+++

+++ Was ist der Unterschied zwischen der Metrik „Unique Devices“ in CDA und der Metrik „Unique Visitors“ außerhalb von CDA?

Diese beiden Metriken sind in etwa gleich. Unterschiede zwischen diesen beiden Metriken treten auf, wenn:

* Ein gemeinsam genutztes Gerät mehreren Personen zugeordnet wird. In diesem Szenario wird 1 „Unique Visitor“ gezählt, während mehrere „Unique Devices“ gezählt werden.
* Ein Gerät weist sowohl nicht zugeordneten als auch zugeordneten Traffic vom gleichen Besucher oder von der gleichen Besucherin auf. Beispiel: Ein Browser generiert identifizierten zugeordneten Traffic sowie anonymen historischen Traffic, der nicht zugeordnet wurde. In diesem Fall wird 1 „Unique Visitor“ gezählt, während 2 „Unique Devices“ gezählt werden.

Weitere Beispiele und Details zur Funktionsweise finden Sie unter [Eindeutige Geräte](/help/components/metrics/unique-devices.md).

+++

+++ Kann ich CDA-Metriken mithilfe der Adobe Analytics 2.0-API einbeziehen?

Ja. Analysis Workspace verwendet die 2.0-API, um Daten von Adobe-Servern anzufordern. Außerdem können Sie API-Aufrufe anzeigen, die Adobe verwendet, um Ihre eigenen Berichte zu erstellen:

1. Wenn Sie sich bei Analysis Workspace angemeldet haben, gehen Sie zu [!UICONTROL Hilfe] > [!UICONTROL Debugger aktivieren].
2. Klicken Sie im gewünschten Bedienfeld auf das Debugging-Symbol und wählen Sie dann die gewünschte Visualisierung und die Uhrzeit der Anfrage aus.
3. Suchen Sie die JSON-Anfrage, die Sie in Ihrem API-Aufruf an Adobe verwenden können.

+++

+++ Cross-Device Analytics kann „Unique Visitors“ einander zuordnen. Können durch diese Metrik Besuche einander zugeordnet werden?

Ja. Wenn eine Person innerhalb des Besuchs-Timeouts Ihrer Virtual Report Suite (standardmäßig 30 Minuten) Treffer von zwei verschiedenen Geräten sendet, werden sie demselben Besuch zugeordnet.

+++

+++ Was ist die ultimative Besucher-ID, die CDA verwendet? Kann ich sie aus Adobe Analytics exportieren?

* **Bei Verwendung eines Gerätediagramms** ist eine benutzerdefinierte ID, die auf ihrem Cluster basiert, die primäre Kennung.
* **Bei Verwendung des feldbasierten Stitching** ist eine benutzerdefinierte ID, die auf der von Ihnen gewählten Eigenschaft/eVar basiert, die primäre Kennung.

Beide diese Kennungen werden von Adobe zum Zeitpunkt der Berichterstellung berechnet. Dies wird auch als [Berichtszeitverarbeitung](../vrs/vrs-report-time-processing.md) bezeichnet. Aufgrund der Art der Berichtszeitverarbeitung ist diese nicht mit Data Warehouse, Daten-Feeds oder anderen Exportfunktionen von Adobe kompatibel.

+++

+++ Wie kann ich vom Gerätediagramm zum feldbasierten Stitching wechseln oder umgekehrt?

Der Wechsel vom Gerätediagramm zum feldbasierten Stitching oder umgekehrt kann über die Kundenunterstützung angefordert werden. Es kann jedoch einige Wochen oder länger dauern, bis ein solcher Wechsel abgeschlossen ist, und *historische zugeordnete Daten aus der vorherigen Methode gehen verloren*.

+++

+++ Wie geht Adobe mit individuellen Einschränkungen für eine Prop oder eVar um, die beim feldbasierten Stitching verwendet wird?

CDA ruft die Elemente der Kennungsvariablen-Dimension ab, bevor sie für das Reporting optimiert werden. Sie müssen sich für CDA keine Sorgen um eindeutige Grenzwerte machen. Wenn Sie jedoch versucht haben, diese Prop/eVar in einem Workspace-Projekt zu verwenden, wird weiterhin das Dimensionselement [(Geringer Traffic)](/help/technotes/low-traffic.md) angezeigt.

+++

+++ Wie viele Report Suites meines Unternehmens können für die geräteübergreifende Analyse (CDA) aktiviert werden?

Ab dem 1. Mai 2022 wird jede neue Implementierung von CDA auf maximal drei Report Suite-IDs (RSIDs) pro Kunde beschränkt. Die geräteübergreifende Analyse führt Report Suites nicht zusammen. Jede für die geräteübergreifende Analyse aktivierte Report Suite muss geräteübergreifend sein (mit Daten von mehreren Oberflächen wie Desktop-Web, mobilem Web, Mobile App usw.).

+++

+++ Wenn meine Organisations-ID mehrere Unternehmen in verschiedenen Regionen enthält, kann ich dann CDA für alle Unternehmen aktivieren?

Nein. Für dieselbe Organisations-ID kann nur eine Region CDA aktiviert werden.

+++

+++ Welche Vor- und Nachteile hat eine Wiederholung über sieben Tage gegenüber einer Wiederholung über einen Tag?

Der Vorteil des siebentägigen Wiederholungs-Lookback-Fensters besteht darin, dass CDA einen längeren Zeitraum nutzen kann, um zu versuchen, zuvor anonyme Ereignisse mit einer Person zu verknüpfen, die sich später innerhalb dieser sieben Tage angemeldet hat. Die Nachteile des 7-Tage-Lookback-Fensters sind: 1) Wiederholungen werden nur einmal pro Woche ausgeführt, und 2) die letzten sieben Tage können sich ändern.

Die Vorteile der Verwendung des eintägigen Wiederholungs-Lookback-Fensters sind: 1) tägliche Wiederholungsläufe und 2) nur gestern kann sich ändern. Der Nachteil des eintägigen Lookback-Fensters besteht darin, dass CDA nur einen Tag zurückgehen kann, um zuvor anonyme Ereignisse mit einer Person zu verknüpfen, die sich gestern angemeldet hat.

+++

+++ Was passiert mit den zugeordneten Daten in meinen virtuellen Report Suites in CDA, wenn mein Unternehmen beschließt, ein Downgrade von Analytics Ultimate durchzuführen?

Wenn ein Kunde oder eine Kundin von Ultimate herabstuft, hat er keinen Zugriff mehr auf zusammengeführte Daten. Alle zuvor zusammengeführten Daten werden entfernt. Das bedeutet, dass die Virtual Report Suites für geräteübergreifende Analyse jetzt keine geräteübergreifende Zuordnung widerspiegeln. Die Daten ähneln der ursprünglichen, nicht zugeordneten Report Suite.

+++

+++ Warum unterscheidet sich die Gesamtzahl der Treffer zwischen meiner Quell-Report Suite und der virtuellen CDA-Report Suite?

CDA verwendet eine komplexe parallele Verarbeitungspipeline mit mehreren abhängigen Komponenten. Eine Datenabweichung von etwa 1 % bei der Gesamtzahl der Treffer zwischen der ursprünglichen Quell-Report Suite und der virtuellen CDA-Report Suite ist zu erwarten.

+++

+++ Warum ist die Metrik „Identifizierte Personen“ überhöht?

Die Metrik „Identifizierte Personen“ kann etwas höher sein, wenn für die Prop//eVar der Kennung eine [Hash-Kollision](/help/implement/validate/hash-collisions.md) besteht.

Bei feldbasiertem Stitching wird bei der benutzerdefinierten Kennungsvariablen zwischen Groß- und Kleinschreibung unterschieden. Die Zahl der Metrik „Identifizierte Personen“ kann erheblich höher sein, wenn die Kennungswerte sich nur in der Groß- und Kleinschreibung unterscheiden. Wenn beispielsweise `bob` und `Bob` gesendet und eigentlich dieselbe Person sind, interpretiert die geräteübergreifende Analyse diese beiden Werte als unterschiedlich.

+++

+++ Warum sehe ich für die Metrik „Nicht identifizierte Personen“ bei der Anzeige der Prop/eVar der Kennung Werte ungleich null?

Diese Situation tritt normalerweise auf, wenn für einen Besucher oder eine Besucherin im Reporting-Zeitraum sowohl authentifizierte als auch nicht authentifizierte Treffer generiert werden. Der Besucher gehört in der Dimension [Identifikationsstatus](/help/components/dimensions/identified-state.md) sowohl zu „Nicht identifiziert“ als auch zu „Identifiziert“, weshalb nicht identifizierte Treffer einer Kennung zugeordnet werden. Dieses Szenario kann sich nach der Ausführung von [Wiederholen](replay.md) ändern, je nach der Wiederholungshäufigkeit und der Erfolgsrate.

+++
