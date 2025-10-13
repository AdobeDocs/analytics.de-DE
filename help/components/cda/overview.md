---
title: Geräteübergreifende Analyse
description: Erfahren Sie, wie Sie Ihre Daten durch Zusammenfügen von Gerätedaten von geräteorientiert zu personenorientiert ändern.
exl-id: e1c0d1e5-399d-45c2-864c-50ef93a77449
feature: CDA
role: Admin
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 59%

---

# Geräteübergreifende Analyse

{{available-existing-customers}}

Die geräteübergreifende Analyse (CDA) ist eine Funktion, mit der Analytics von einer geräteorientierten Ansicht zu einer personenorientierten Ansicht wechselt. Analysten können so das Benutzerverhalten über Browser, Geräte oder Apps hinweg nachvollziehen. Adobe unterstützt zwei übergreifende Workflows zum Verknüpfen von Gerätedaten:

* [**Feldbasiertes Stitching**](field-based-stitching.md): Diese Stitching-Option wird empfohlen, da sie nur deterministische Abgleiche verwendet, um Geräte miteinander zu verknüpfen.
Mit der feldbasierten Zuordnung können Sie eine Analytics-Variable als Basis für die geräteübergreifende Zuordnung in einer Virtual Report Suite auswählen.

* [**Gerätediagramm**](device-graph.md): Die geräteübergreifende Analyse kommuniziert mit einem privaten Diagramm, um Geräte miteinander zu verknüpfen.

Mithilfe der geräteübergreifenden Analyse können Sie Fragen beantworten wie z. B.:

* Wie viele Menschen interagieren mit meiner Marke? Wie viele und welche Gerätetypen verwenden sie? Wie überschneiden sich diese?
* Wie oft beginnen Personen mit einer Aufgabe auf einem Mobilgerät und wechseln dann zu einem Desktop-PC, um die Aufgabe abzuschließen? Führen Kampagnen-Clickthroughs auf einem Gerät zur Konversion auf einem anderen Gerät?
* Wie ändern sich meine Daten zur Wirksamkeit einer Kampagne, wenn ich geräteübergreifende Journeys berücksichtige? Wie ändert sich meine Trichteranalyse?
* Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo schließen sie ihre Aktion erfolgreich ab?
* Wie unterscheidet sich das Verhalten von Benutzern mit mehreren Geräten von Benutzern mit nur einem Gerät?

Beim Zuordnen von Geräten wird die variable Persistenz über Geräte hinweg übernommen. Beispiel: Ein Benutzer besucht Ihre Site zum ersten Mal über eine Werbeanzeige auf seinem Desktop. Der Benutzer findet Ihre Mobile App, installiert sie und tätigt schließlich einen Einkauf auf seinem Mobilgerät. Mit der geräteübergreifenden Analyse können Sie den Umsatz auf dem Mobilgerät einer Anzeige zuordnen, auf die auf dem Desktop-Computer geklickt wurde.

Microsoft Azure wird für geräteübergreifende Analysen verwendet. Adobe verwendet Azur zum Speichern von Gerätediagrammdaten und zum Durchführen geräteübergreifender Zuordnungen. Daher werden Adobe Analytics-Daten zwischen dem Rechenzentrum von Adobe und den von Adobe bereitgestellten Instanzen von Microsoft Azure hin und her übertragen.

Weitere [&#x200B; zu den Funktionen und Leistungsmerkmalen der geräteübergreifenden Analyse finden &#x200B;](https://express.adobe.com/page/8ZpjsX6Lp5XTM/) auf der Seite „Cross-Device Analytics Spark“.

## Voraussetzungen

Die Verwendung der geräteübergreifenden Analyse erfordert [feldbasiertes Stitching](field-based-stitching.md) und [Gerätediagramm](device-graph.md)-Methoden und beide haben ihre eigenen spezifischen Voraussetzungen.

* Es muss ein Vertrag bei Adobe mit Adobe Analytics Ultimate abgeschlossen werden.
* Ihre Organisation wählt die Report Suites aus, die CDA aktivieren sollen. Adobe empfiehlt Report Suites, die geräteübergreifende Daten enthalten, d. h. Daten von mehreren Geräten/Browsern/App-Typen. Einige Unternehmen bezeichnen dieses Konzept als „globale“ Report Suite, obwohl die geräteübergreifende Analyse aus geografischer Sicht nicht unbedingt global sein muss.

## Einschränkungen

Die geräteübergreifende Analyse ist eine innovative und zuverlässige Funktion, die jedoch Einschränkungen hinsichtlich ihrer Verwendung aufweist. Die Methoden zum [feldbasierten Stitching](field-based-stitching.md) und der [Gerätediagrammme](device-graph.md) haben ebenfalls eigene spezifische Einschränkungen.

* Die geräteübergreifende Analyse ist nur über Analysis Workspace verfügbar.
* Die geräteübergreifende Analyse funktioniert nicht in allen Report Suites und kombiniert auch keine Daten aus mehreren Report Suites.
* Adobe Analytics-Report Suites können nicht mit mehr als einer Organisations-ID verknüpft werden. Da die geräteübergreifende Analyse Geräte innerhalb einer bestimmten Report Suite zusammenfügt, kann die geräteübergreifende Analyse nicht verwendet werden, um Daten über mehrere Organisations-IDs hinweg zusammenzufügen.
* Die geräteübergreifende Analyse verwendet eine komplexe Verarbeitungs-Pipeline mit mehreren abhängigen Komponenten. Diese Pipeline wird parallel zum Analytics-Basisberichterstellungs-Workflow ausgeführt. Es besteht eine Datenabweichung von etwa 1 % für die Gesamtzahl der Treffer zwischen der ursprünglichen Report Suite und der Virtual Report Suite in Cross-Device Analytics.
* CDA verwendet eine Virtual Report Suite und eine Berichtszeitverarbeitung, die ihre eigenen Einschränkungen haben. Sie unterstützen etwa derzeit keine Marketing-Kanal-Variablen. Weitere Informationen zu diesen Einschränkungen finden Sie unter [Virtual Report Suites](/help/components/vrs/vrs-about.md) und [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md).
* Das private Diagramm nutzt dieselben ID-Synchronisierungen wie die ID-Synchronisierungen, die von der Funktion [Kundenattribute](https://experienceleague.adobe.com/de/docs/core-services/interface/services/customer-attributes/attributes) in Experience Cloud und Adobe Analytics verwendet werden. Virtual Report Suites in Cross-Device Analytics (unabhängig davon, ob sie auf privatem Diagramm oder feldbasierter Zuordnung basieren) sind jedoch nicht mit dem Rest der Funktion „Kundenattribute“ kompatibel. Mit anderen Worten: Kundenattribute-basierte Dimensionen sind nicht für die Verwendung mit Virtual Report Suites in Cross-Device Analytics verfügbar.
* Die geräteübergreifende Analyse ist derzeit nicht mit A4T kompatibel.
* Die 1.4 API wird nicht unterstützt. Power BI-Connectoren und Report Builder basieren beide auf der 1.4 API und sind daher nicht mit der geräteübergreifenden Analyse kompatibel.
* Die aktive Überwachung des Prozesses der geräteübergreifenden Analyse durch Adobe ist auf Report Suites im Produktionsbetrieb beschränkt.
* Die geräteübergreifende Analyse ist derzeit nicht mit der Adobe Analytics (Data [&#x200B; API) &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/)
* Historische Daten in der Virtual Report Suite ändern sich je nach Erkennung und Zuordnung von Geräten von Adobe. Die Daten in der Quell-Report Suite bleiben unverändert.
* Zugeordnete Daten haben eine Latenz von 8 bis 12 Stunden.
* Die Zuordnung von Verlaufsdaten für ein bestimmtes Gerät wird für bis zu einem Jahr gespeichert.
* Wenn ein Gerät innerhalb eines Jahres eine sehr hohe Anzahl von Zuordnungsverlaufseinträgen erreicht, wird der Zuordnungsverlauf gekürzt. Das genaue Limit hängt von der verwendeten Stitching-Option ab.
