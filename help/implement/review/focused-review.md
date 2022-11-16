---
title: Gezielte Prüfung (nach jeder Website-Veröffentlichung)
description: Führen Sie diese Schritte aus, um sicherzustellen, dass Ihre Implementierung fehlerfrei und im Einklang mit Ihren KPIs ausgeführt wird.
feature: Implementation Basics
exl-id: e38f92b6-bd6e-4835-a8e5-0f29ac962066
source-git-commit: ac9e4934cee0178fb00e4201cc3444d333a74052
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 98%

---

# Gezielte Prüfung (nach jeder Website-Veröffentlichung)

Warum sollten Sie Ihre Implementierung alle paar Monate prüfen? So können Sie alle Probleme mit der Datenqualität lösen, solange sie noch klein sind. Wenn Sie diese gezielte Prüfung nach jeder Website-Veröffentlichung durchgängig durchführen, werden Sie feststellen, dass Ihre halbjährlichen [vollständigen Prüfungen](/help/implement/review/full-review.md) viel einfacher sind. Sie werden auch verhindern, dass kleine Probleme zu großen Datenproblemen werden, die das Vertrauen der Stakeholder untergraben könnten.

## 1. Beginnen Sie mit Ihren wichtigsten 5 KPIs

Die Kenntnis der 5 wichtigsten Leistungsindikatoren (Key Performance Indicators, KPIs) hilft Ihnen bei der Bestimmung der zugehörigen Kennzahlen und Dimensionen, die Sie untersuchen müssen. Wenn Sie Ihre KPIs in den letzten 6 Monaten nicht aktualisiert haben oder wenn Ihr Unternehmen noch keine KPIs erstellt hat, folgen Sie [diesen Anweisungen](/help/implement/review/define-kpis.md).

## 2. Stellen Sie sicher, dass Ihre KPI-Metriken und -Variablen weiterhin ihre Aufgabe gut erfüllen

Hin und wieder stattfindende Code-Aktualisierungen können unbeabsichtigte Auswirkungen haben. Sie sollten sicherstellen, dass alle Metriken und Dimensionen, die Ihren [wichtigsten 5 KPIs](/help/implement/review/define-kpis.md) zugeordnet sind, weiterhin ihre Aufgabe korrekt erfüllen. Idealerweise erfolgt dies unmittelbar nach einer Website-Veröffentlichung. Falls Sie es in den letzten Monaten nicht getan haben, tun Sie es *jetzt*. Gehen Sie folgendermaßen vor:

* Erstellen Sie Dashboards, um die Trendansicht der Ansichten dieser wichtigen Metriken und Variablen anzuzeigen (oder richten Sie [intelligente Warnhinweise](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/intellligent-alerts.html?lang=de#analysis-workspace) für jede Metrik ein). Überwachen Sie sie dann für ein oder zwei Tage, um sicherzustellen, dass Sie die erwarteten Daten erhalten und dass die Daten korrekt sind. Suchen Sie nach Wendepunkten. Seien Sie bereit, alle wichtigen Probleme sofort zu beheben. Wenn Sie Abweichungen feststellen, sollten Sie sich Ihre Datenschicht, Tag-Manager-Regeln und Verarbeitungsregeln ansehen, um den Grund herauszufinden.
* Führen Sie [Analytics Health Dashboard](https://assets.adobe.com/public/9549dbe7-765a-4899-77b8-85cbba1a4252) erneut aus, um allgemeine Trends Ihrer KPI-Metriken und -Variablen zu überwachen.

*Weitere Informationen dazu, wie Sie sicherstellen können, dass Ihre Metriken und Variablen ihre Aufgabe ordnungsgemäß erfüllen, finden Sie in [diesen Tipps](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/my-five-best-tips-for-keeping-adobe-analytics-humming/td-p/388608) von der Adobe Analytics-Expertin Sarah Owen.*

## 3. Überprüfen Sie sorgfältig die Daten aus dem aktualisierten Abschnitt Ihrer Site

Stellen Sie sicher, dass die letzte Site-Veröffentlichung die Datenerfassung für diesen Abschnitt der Site nicht negativ beeinflusst hat: Prüfen Sie den gesamten Code und alle Variablen in diesem Abschnitt, um sicherzustellen, dass das neue Tracking wunschgemäß funktioniert.

## 4. Aktualisieren Sie Ihre Dokumentation

Wenn Sie kürzlich Kennzahlen oder Variablen hinzugefügt oder geändert haben, müssen Sie Ihr Unternehmensanforderungsdokument (Business Requirement Document, BRD) und Ihre Lösungs-Design-Referenz (Solution Design Reference, SDR) aktualisieren.

Wenn Sie keine Dokumentation Ihrer Implementierung haben, exportieren Sie eine Liste von Variablen und erstellen Sie Ihr BRD oder Ihre SDR mit [dieser Vorlage](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html#implementation).

## 5. Beheben Sie sofort alle Lücken in Ihrer Datenqualität

Beurteilen Sie die Situation und erstellen Sie einen Plan zur Berichtigung der Daten. Nehmen Sie dann die erforderlichen Änderungen vor, aktualisieren Sie Ihre Dokumentation und informieren Sie Ihre Stakeholder über die vorgenommenen Änderungen.

*Sehen Sie sich dieses 2-minütige Video von Adobe Analytics Champion Sarah Owen darüber an, wann Sie Prüfungen Ihrer Implementierung auf sehr praktische Weise in Ihren vollen Zeitplan integrieren können:*

>[!VIDEO](https://video.tv.adobe.com/v/328340/?quality=12&learn=on)
