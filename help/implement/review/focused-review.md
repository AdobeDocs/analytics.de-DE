---
title: Fokussierte Überprüfung (nach jeder Website-Version)
description: Führen Sie diese Schritte aus, um sicherzustellen, dass Ihre Implementierung fehlerfrei und im Einklang mit Ihren KPIs ausgeführt wird.
translation-type: tm+mt
source-git-commit: a7f1da79bd5a6f78ed1a706ccae01b03a2f5665c
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---


# Fokussierte Überprüfung (nach jeder Website-Version)

Warum sollten Sie Ihre Implementierung alle paar Monate überprüfen? So können Sie alle Probleme mit der Datenqualität lösen, solange sie noch klein sind. Wenn Sie diese Fokusüberprüfung nach jeder Website-Version durchgängig durchführen, werden Sie feststellen, dass Ihre halbjährlichen [Vollständigen Reviews](/help/implement/review/full-review.md) viel einfacher sind. Sie werden auch verhindern, dass kleine Themen zu Big-Data-Problemen werden, die das Vertrauen der Interessenträger untergraben könnten.

## 1. Beginn mit Ihren Top 5 KPIs.

Die Kenntnis der fünf wichtigsten Leistungsindikatoren (KPIs) hilft Ihnen bei der Ermittlung der zugehörigen Metriken und Dimensionen, die Sie untersuchen müssen. Wenn Sie Ihre KPIs in den letzten 6 Monaten nicht aktualisiert haben oder wenn Ihr Unternehmen noch keine KPIs erstellt hat, befolgen Sie [diese Anweisungen](/help/implement/review/define-kpis.md).

## 2. Stellen Sie sicher, dass Ihre KPI-Metriken und -Variablen weiterhin gut funktionieren.

Codeaktualisierungen im Laufe der Zeit können unbeabsichtigte Auswirkungen haben. Sie möchten sicherstellen, dass alle Metriken und Dimensionen, die [Ihren Top-5-KPIs](/help/implement/review/define-kpis.md) zugeordnet sind, weiterhin korrekt funktionieren. Idealerweise sollte dies unmittelbar nach der Veröffentlichung einer Website erfolgen. Wenn Sie dies in den letzten Monaten nicht getan haben, führen Sie *jetzt* durch. Gehen Sie folgendermaßen vor:

* **Erstellen Sie** Dashboards, um die Ansichten dieser kritischen Metriken und Variablen mit stündlicher Trendansicht anzuzeigen. Sie können außerdem intelligente Warnhinweise für jede Metrik einrichten und diese für ein bis zwei Tage überwachen, um sicherzustellen, dass die erwarteten Daten und die richtigen Daten vorliegen. Suchen Sie nach Wendepunkten. Seien Sie bereit, alle kritischen Probleme sofort zu beheben. Wenn Sie Abweichungen feststellen, sollten Sie sich Ihre Datenschicht, Tag-Manager-Regeln und Verarbeitungsregeln ansehen, um herauszufinden, warum dies der Fall ist.
* **Führen Sie das Analytics Health** Dashboard erneut aus, um breite Trends Ihrer KPI-Metriken und -Variablen zu überwachen.

Weitere Informationen dazu, wie Sie sicherstellen können, dass Ihre Metriken und Variablen ordnungsgemäß funktionieren, finden Sie unter [diese Tipps](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/my-five-best-tips-for-keeping-adobe-analytics-humming/td-p/388608) von Adobe Analytics Champion Sarah Owen.

## 3. Überprüfen Sie die Daten aus dem aktualisierten Abschnitt Ihrer Site sorgfältig.

Stellen Sie sicher, dass die letzte Site-Version die Datenerfassung für diesen Abschnitt der Site nicht negativ beeinflusste: Überprüfen Sie alle Code- und Variablen, die diesem Abschnitt entsprechen, um sicherzustellen, dass die neue Verfolgung wunschgemäß funktioniert.

## 4. Aktualisieren Sie Ihre Dokumentation.

Wenn Sie kürzlich Metriken oder Variablen hinzugefügt oder geändert haben, müssen Sie Ihr Business Requirement Dokument (BRD) und Ihre Lösungsdesignreferenz (SDR) aktualisieren.

Wenn Sie keine Dokumentation zu Ihrer Implementierung haben, exportieren Sie eine Liste von Variablen und erstellen Sie Ihre BRD oder SDR mit [dieser Vorlage](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=en#implementation).

## 5. Schließen Sie umgehend alle Lücken in Ihrer Datenqualität ab.

Beurteilung der Situation und Erstellung eines Plans zur Behebung der Daten. Nehmen Sie dann die erforderlichen Änderungen vor, aktualisieren Sie Ihre Dokumentation und informieren Sie Ihre Stakeholder über die vorgenommenen Änderungen.

*Sehen Sie sich dieses 2-minütige Video von Adobe Analytics Champion Sarah Owen über die natürlichen Zeiten an, in denen Sie Rezensionen Ihrer Implementierung in Ihren Zeitplan einpassen können:*

>[!VIDEO](https://video.tv.adobe.com/v/328340/?quality=12&learn=on)
