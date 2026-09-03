---
title: Gezielte Prüfung (nach jeder Website-Veröffentlichung)
description: Führen Sie diese Schritte aus, um sicherzustellen, dass Ihre Implementierung fehlerfrei und im Einklang mit Ihren KPIs ausgeführt wird.
feature: Implementation Basics
exl-id: e38f92b6-bd6e-4835-a8e5-0f29ac962066
role: Admin, Leader
TQID: https://experienceleague.adobe.com/C57qRRa4-WDgJDgvtLebgy-0DAPvMUreSrGfuA67N4o
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: e93b8c4c-c5f7-45f8-9abe-9b710f53f502
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
topic_v2:
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 535
ht-degree: 62%

---

# Gezielte Prüfung (nach jeder Website-Veröffentlichung)

Warum sollten Sie Ihre Implementierung alle paar Monate prüfen? So können Sie alle Probleme mit der Datenqualität lösen, solange sie noch klein sind. Wenn Sie diese fokussierte Überprüfung nach jeder Website-Veröffentlichung konsequent durchführen, werden Sie feststellen, dass Ihre halbjährlichen [vollständigen Überprüfungen](/help/implement/review/full-review.md) viel einfacher sind. Außerdem werden Sie verhindern, dass aus kleinen Problemen Big-Data-Probleme werden, die das Vertrauen der Stakeholder untergraben könnten.

## &#x200B;1. Beginnen Sie mit Ihren fünf wichtigsten KPIs

Die Kenntnis der 5 wichtigsten Leistungsindikatoren (Key Performance Indicators, KPIs) hilft Ihnen bei der Bestimmung der zugehörigen Kennzahlen und Dimensionen, die Sie untersuchen müssen. Wenn Sie Ihre KPIs in den letzten 6 Monaten nicht aktualisiert haben oder Ihr Unternehmen noch keine KPIs erstellt hat, befolgen Sie [diese Anweisungen](/help/implement/review/define-kpis.md).

## &#x200B;2. Stellen Sie sicher, dass Ihre KPI-Metriken und -Variablen weiterhin ihre Aufgabe gut erfüllen

Hin und wieder stattfindende Code-Aktualisierungen können unbeabsichtigte Auswirkungen haben. Sie sollten sicherstellen, dass alle Metriken und Dimensionen, die Ihren [wichtigsten 5 KPIs](/help/implement/review/define-kpis.md) zugeordnet sind, weiterhin ihre Aufgabe korrekt erfüllen. Idealerweise erfolgt dies unmittelbar nach einer Website-Veröffentlichung. Falls Sie es in den letzten Monaten nicht getan haben, tun Sie es *jetzt*. Gehen Sie folgendermaßen vor:

* Erstellen Sie Dashboards, um stündliche Trend-Ansichten dieser kritischen Metriken und Variablen anzuzeigen (oder richten Sie [Warnhinweise](/help/components/alerts/alerts-overview.md) für jede Metrik ein). Überwachen Sie sie dann ein oder zwei Tage lang, um sicherzustellen, dass Sie die erwarteten Daten erhalten und die Daten korrekt sind. Suchen Sie nach Wendepunkten. Seien Sie bereit, alle wichtigen Probleme sofort zu beheben. Wenn Sie Abweichungen feststellen, sollten Sie sich Ihre Datenschicht, Tag-Manager-Regeln und Verarbeitungsregeln ansehen, um den Grund herauszufinden.
* Führen Sie [Analytics Health Dashboard](https://express.adobe.com/page/tnNQGNlfzta3b/) erneut aus, um allgemeine Trends Ihrer KPI-Metriken und -Variablen zu überwachen.

*Weitere Informationen dazu, wie Sie sicherstellen können, dass Ihre Metriken und Variablen ihre Aufgabe ordnungsgemäß erfüllen, finden Sie in [diesen Tipps](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/my-five-best-tips-for-keeping-adobe-analytics-humming/td-p/388608) von der Adobe Analytics-Expertin Sarah Owen.*

## &#x200B;3. Prüfen Sie die Daten aus dem aktualisierten Abschnitt Ihrer Site sorgfältig

Stellen Sie sicher, dass die letzte Site-Veröffentlichung die Datenerfassung für diesen Abschnitt der Site nicht negativ beeinflusst hat: Prüfen Sie den gesamten Code und alle Variablen in diesem Abschnitt, um sicherzustellen, dass das neue Tracking wunschgemäß funktioniert.

## &#x200B;4. Dokumentation aktualisieren

Wenn Sie kürzlich Kennzahlen oder Variablen hinzugefügt oder geändert haben, müssen Sie Ihr Unternehmensanforderungsdokument (Business Requirement Document, BRD) und Ihre Lösungs-Design-Referenz (Solution Design Reference, SDR) aktualisieren.

Wenn Sie nicht über die Dokumentation Ihrer Implementierung verfügen, exportieren Sie eine Liste von Variablen und erstellen Sie Ihre BRD oder SDR mithilfe [dieser Vorlage](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=de#implementation).

## &#x200B;5. Schließen Sie sofort alle Lücken in Ihrer Datenqualität

Beurteilen Sie die Situation und erstellen Sie einen Plan zur Berichtigung der Daten. Nehmen Sie dann die erforderlichen Änderungen vor, aktualisieren Sie Ihre Dokumentation und informieren Sie Ihre Stakeholder über die vorgenommenen Änderungen.

*Sehen Sie sich dieses 2-minütige Video von Adobe Analytics Champion Sarah Owen darüber an, wann Sie Prüfungen Ihrer Implementierung auf sehr praktische Weise in Ihren vollen Zeitplan integrieren können:*


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Überprüfen der Implementierung](https://video.tv.adobe.com/v/328340?quality=12&learn=on){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


