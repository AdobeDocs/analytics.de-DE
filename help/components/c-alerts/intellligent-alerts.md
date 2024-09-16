---
description: Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.
title: Intelligente Warnhinweise
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: 2b8688da1400857b7f5093197d06c04681cd87ff
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 59%

---

# Übersicht über intelligente Warnhinweise

Intelligente Warnhinweise (oder nur &quot;Warnhinweise&quot;) in Adobe Analytics ermöglichen es Ihnen, sofort benachrichtigt zu werden, wenn in Ihren Daten abnorme Ereignisse auftreten.

Sie können festlegen, dass Warnhinweise auf der Grundlage von Schwellenwerten für Anomalien, geänderten Prozentsätzen oder spezifischen Datenpunkten ausgelöst werden. Warnhinweise bieten granulare Steuerelemente, die mit der [Anomalieerkennung](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) integriert werden und ausgelöst werden, wenn Sie sie am dringendsten benötigen.

Mithilfe intelligenter Warnhinweise können Sie:

* Warnhinweise erstellen, die auf Anomalien basieren (90-%-, 95-%-, 99-%-, 99,75-%- und 99,9-%-Schwellen, Änderungen in %, darüber/darunter)
* In einer Vorschau anzeigen, wie oft ein Warnhinweis ausgelöst wird
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken
* „Gestapelte“ Warnhinweise erstellen, die mehrere Metriken in einem Warnhinweis vereinen.

Das folgende Video-Tutorial bietet einen grundlegenden Überblick über Warnhinweise: [Intelligente Warnhinweise](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html?lang=de) (5:34)

## Anomalie-Suche nach Warnungen

Wenn ein Warnhinweis eine Anomalieerkennung verwendet, hängt der Trainings-Zeitraum von der für den Warnhinweis ausgewählten Granularität ab.

* Monatliche Granularität: 15 Monate + derselbe Bereich im letzten Jahr
* Wöchentliche Granularität: 15 Wochen + derselbe Bereich im letzten Jahr
* Tägliche Granularität: 35 Tage + derselbe Bereich im letzten Jahr
* Stündliche Granularität: 336 Stunden

Weitere Informationen finden Sie unter [Statistische Verfahren zur Anomalieerkennung](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md).

## Erstellen von Warnhinweisen

Informationen zum Erstellen von Warnhinweisen in Adobe Analytics finden Sie unter [Warnhinweise erstellen](/help/components/c-alerts/alert-builder.md).

>[!IMPORTANT]
>
>Die Verwendung von Zeitstempeldaten zur Erstellung von Warnhinweisen kann dazu führen, dass Warnhinweise falsch ausgelöst werden. Adobe empfiehlt die Verwendung von Daten ohne Zeitstempel für intelligente Warnhinweise.

## Verwalten von Warnhinweisen

Sie können vorhandene Warnhinweise im Warnhinweis-Manager verwalten. Sie können verschiedene Verwaltungsaufgaben für Warnhinweise ausführen, z. B. Tagging, Umbenennen, Löschen usw.

Weitere Informationen zum Verwalten vorhandener Warnhinweise in Adobe Analytics finden Sie unter [Warnhinweise verwalten](/help/components/c-alerts/alert-manager.md).
