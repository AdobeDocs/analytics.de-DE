---
description: Warnhinweise ermöglichen eine abgestufte Kontrolle über Benachrichtigungen und integrieren die Anomalieerkennung.
title: Warnhinweise – Überblick
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: e5f832bcedfa1c483fb31f5cff733bad4ed85be1
workflow-type: ht
source-wordcount: '305'
ht-degree: 100%

---

# Warnhinweise – Überblick

Warnhinweise in Adobe Analytics ermöglichen es Ihnen, sich über geänderte Prozentsätze oder bestimmte Datenpunkte benachrichtigen zu lassen.

Je nach Adobe Analytics-Paket können Sie auch Warnhinweise verwenden, die basierend auf Schwellenwerten für Anomalien ausgelöst werden. Diese Warnhinweise (auch als „intelligente Warnhinweise“ bezeichnet) bieten granulare Steuerelemente, die mit der [Anomalieerkennung](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) integriert sind und ausgelöst werden, wenn Sie sie am dringendsten benötigen.

Mithilfe von Warnhinweisen können Sie:

* In einer Vorschau anzeigen, wie oft ein Warnhinweis ausgelöst wird
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken
* „Gestapelte“ Warnhinweise erstellen, die mehrere Metriken in einem Warnhinweis vereinen.
* Warnhinweisen basierend auf Anomalien erstellen (Schwellenwerte von 90 %, 95 %, 99 %, 99,75 % und 99,9 %; prozentuale Veränderung; über/unter) (nur für Adobe Analytics-Kundschaft mit einem Select-, Prime- oder Ultimate-Paket verfügbar)

Das folgende Video-Tutorial bietet einen grundlegenden Überblick über Warnhinweise: [Warnhinweise](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html?lang=de) (5:34)

## Anomalie-Suche für Warnungen

>[!NOTE]
>
>Die Verwendung von Warnhinweisen mit der Anomalieerkennung (auch als _intelligente Warnhinweise_ bezeichnet) ist nur für Organisationen mit einem Adobe Analytics Prime- oder Ultimate-Paket verfügbar.

Wenn ein Warnhinweis eine Anomalieerkennung verwendet, hängt der Trainings-Zeitraum von der für den Warnhinweis ausgewählten Granularität ab.

* Monatliche Granularität: 15 Monate + derselbe Bereich im letzten Jahr
* Wöchentliche Granularität: 15 Wochen + derselbe Bereich im letzten Jahr
* Tägliche Granularität: 35 Tage + derselbe Bereich im letzten Jahr
* Stündliche Granularität: 336 Stunden

Weitere Informationen finden Sie unter [In der Anomalieerkennung verwendete statistische Verfahren](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md).

## Erstellen von Warnhinweisen

Informationen zum Erstellen von Warnhinweisen in Adobe Analytics finden Sie unter [Erstellen von Warnhinweisen](/help/components/c-alerts/alert-builder.md).

>[!IMPORTANT]
>
>Die Verwendung von Zeitstempeldaten zur Erstellung von Warnhinweisen kann dazu führen, dass Warnhinweise falsch ausgelöst werden. Adobe empfiehlt die Verwendung von Daten ohne Zeitstempel für Warnhinweise.

## Verwalten von Warnhinweisen

Sie können vorhandene Warnhinweise im Warnhinweis-Manager verwalten. Sie können verschiedene Verwaltungsaufgaben für Warnhinweise ausführen, z. B. Tagging, Umbenennen, Löschen und mehr.

Weitere Informationen zum Verwalten vorhandener Warnhinweise in Adobe Analytics finden Sie unter [Verwalten von Warnhinweisen](/help/components/c-alerts/alert-manager.md).
