---
title: Geräteübergreifende Analyse
description: Erfahren Sie, wie Sie Ihre Daten durch Zusammenfügen von Gerätedaten von geräteorientiert zu personenorientiert ändern.
exl-id: e1c0d1e5-399d-45c2-864c-50ef93a77449
feature: CDA
role: Admin
TQID: https://experienceleague.adobe.com/SEHyUllyHtYjtfpaw9uI64WNytw3MMrR1Np9BN2Ckyk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 837
ht-degree: 54%

---

# Geräteübergreifende Analyse

{{available-existing-customers}}

>[!WARNING]
>
>Das Gerätediagramm in der geräteübergreifenden Analyse ist [veraltet](https://experienceleague.adobe.com/en/docs/discontinued/using/device-graph) und ab dem 31. **2025 nicht mehr**. Wechseln Sie alle aktuellen für Gerätediagramme aktivierten Virtual Report Suites in die [feldbasierte Methode](/help/components/cda/field-based-stitching.md).
>


Die geräteübergreifende Analyse (CDA) ist eine Funktion, mit der Analytics von einer geräteorientierten Ansicht zu einer personenorientierten Ansicht wechselt. Analysten können so das Benutzerverhalten über Browser, Geräte oder Apps hinweg nachvollziehen. Adobe unterstützt [feldbasiertes Stitching](field-based-stitching.md) das nur deterministische Abgleiche verwendet, um Geräte miteinander zu verknüpfen.
Mit der feldbasierten Zuordnung können Sie eine Analytics-Variable als Basis für die geräteübergreifende Zuordnung in einer Virtual Report Suite auswählen.


Mithilfe der geräteübergreifenden Analyse können Sie Fragen beantworten wie z. B.:

* Wie viele Menschen interagieren mit meiner Marke? Wie viele und welche Gerätetypen verwenden sie? Wie überschneiden sich diese?
* Wie oft beginnen Personen mit einer Aufgabe auf einem Mobilgerät und wechseln dann zu einem Desktop-PC, um die Aufgabe abzuschließen? Führen Kampagnen-Clickthroughs auf einem Gerät zur Konversion auf einem anderen Gerät?
* Wie ändern sich meine Daten zur Wirksamkeit einer Kampagne, wenn ich geräteübergreifende Journeys berücksichtige? Wie ändert sich meine Trichteranalyse?
* Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo sind sie erfolgreich?
* Wie unterscheidet sich das Verhalten von Benutzern mit mehreren Geräten von Benutzern mit nur einem Gerät?

Beim Zuordnen von Geräten wird die variable Persistenz über Geräte hinweg übernommen. Beispiel: Ein Benutzer besucht Ihre Site zum ersten Mal über eine Werbeanzeige auf seinem Desktop. Der Benutzer findet Ihre Mobile App, installiert sie und tätigt schließlich einen Einkauf auf seinem Mobilgerät. Mit der geräteübergreifenden Analyse können Sie den Umsatz auf dem Mobilgerät einer Anzeige zuordnen, auf die auf dem Desktop-Computer geklickt wurde.



Weitere [ zu den Funktionen und Leistungsmerkmalen der geräteübergreifenden Analyse finden ](https://express.adobe.com/page/8ZpjsX6Lp5XTM/) auf der Seite „Cross-Device Analytics Spark“.

## Voraussetzungen

Die Verwendung der geräteübergreifenden Analyse erfordert [feldbasiertes Stitching](field-based-stitching.md).

* Es muss ein Vertrag bei Adobe mit Adobe Analytics Ultimate abgeschlossen werden.
* Ihre Organisation wählt die Report Suites aus, die CDA aktivieren sollen. Adobe empfiehlt Report Suites, die geräteübergreifende Daten enthalten, d. h. Daten von mehreren Geräten/Browsern/App-Typen. Einige Unternehmen bezeichnen dieses Konzept als „globale“ Report Suite, obwohl die geräteübergreifende Analyse aus geografischer Sicht nicht unbedingt global sein muss.

## Einschränkungen

Die geräteübergreifende Analyse ist eine innovative und zuverlässige Funktion, die jedoch Einschränkungen hinsichtlich ihrer Verwendung aufweist. [Feldbasiertes Stitching](field-based-stitching.md) weist auch eigene spezifische Einschränkungen auf.

* Die geräteübergreifende Analyse ist nur über Analysis Workspace verfügbar.
* Die geräteübergreifende Analyse funktioniert nicht in allen Report Suites und kombiniert auch keine Daten aus mehreren Report Suites.
* Adobe Analytics-Report Suites können nicht mit mehr als einer Organisations-ID verknüpft werden. Da die geräteübergreifende Analyse Geräte innerhalb einer bestimmten Report Suite zusammenfügt, kann die geräteübergreifende Analyse nicht verwendet werden, um Daten über mehrere Organisations-IDs hinweg zusammenzufügen.
* Die geräteübergreifende Analyse verwendet eine komplexe Verarbeitungs-Pipeline mit mehreren abhängigen Komponenten. Diese Pipeline wird parallel zum Analytics-Basisberichterstellungs-Workflow ausgeführt. Es besteht eine Datenabweichung von etwa 1 % für die Gesamtzahl der Treffer zwischen der ursprünglichen Report Suite und der Virtual Report Suite in Cross-Device Analytics.
* CDA verwendet eine Virtual Report Suite und eine Berichtszeitverarbeitung, die ihre eigenen Einschränkungen haben. Sie unterstützen etwa derzeit keine Marketing-Kanal-Variablen. Weitere Informationen zu diesen Einschränkungen finden Sie unter [Virtual Report Suites](/help/components/vrs/vrs-about.md) und [Berichtszeitverarbeitung](/help/components/vrs/vrs-report-time-processing.md).
* Das private Diagramm nutzt dieselben ID-Synchronisierungen wie die ID-Synchronisierungen, die von der Funktion [Kundenattribute](https://experienceleague.adobe.com/en/docs/core-services/interface/services/customer-attributes/attributes) in CX Enterprise und Adobe Analytics verwendet werden. Virtual Report Suites in Cross-Device Analytics (unabhängig davon, ob sie auf privatem Diagramm oder feldbasierter Zuordnung basieren) sind jedoch nicht mit dem Rest der Funktion „Kundenattribute“ kompatibel. Mit anderen Worten: Kundenattribute-basierte Dimensionen sind nicht für die Verwendung mit Virtual Report Suites in Cross-Device Analytics verfügbar.
* Die geräteübergreifende Analyse ist derzeit nicht mit A4T kompatibel.
* Die 1.4 API wird nicht unterstützt. Power BI-Connectoren und Report Builder basieren beide auf der 1.4 API und sind daher nicht mit der geräteübergreifenden Analyse kompatibel.
* Die aktive Überwachung des Prozesses der geräteübergreifenden Analyse durch Adobe ist auf Report Suites im Produktionsbetrieb beschränkt.
* Die geräteübergreifende Analyse ist derzeit nicht mit der Adobe Analytics (Data [ API) ](https://developer.adobe.com/analytics-apis/docs/2.0/)
* Historische Daten in der Virtual Report Suite ändern sich je nach Erkennung und Zuordnung von Geräten von Adobe. Die Daten in der Quell-Report Suite bleiben unverändert.
* Zugeordnete Daten haben eine Latenz von 8 bis 12 Stunden.
* Die Zuordnung von Verlaufsdaten für ein bestimmtes Gerät wird für bis zu einem Jahr gespeichert.
* Wenn ein Gerät innerhalb eines Jahres eine sehr hohe Anzahl von Zuordnungsverlaufseinträgen erreicht, wird der Zuordnungsverlauf gekürzt. Das genaue Limit hängt von der verwendeten Stitching-Option ab.
