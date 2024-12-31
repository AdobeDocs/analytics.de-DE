---
description: Warnhinweise ermöglichen eine granulare Steuerung der Benachrichtigungen und die Integration in die Anomalieerkennung.
title: Warnhinweise – Übersicht
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: e5f832bcedfa1c483fb31f5cff733bad4ed85be1
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 33%

---

# Warnhinweise – Übersicht

Warnhinweise in Adobe Analytics ermöglichen die Benachrichtigung anhand geänderter Prozentsätze oder bestimmter Datenpunkte.

Je nach Adobe Analytics-Paket können Sie auch Warnhinweise verwenden, die auf der Grundlage von Anomalieschwellen ausgelöst werden. Diese Warnhinweise (auch als „intelligente Warnhinweise“ bezeichnet) bieten granulare Steuerelemente, die in die [Anomalieerkennung“ integriert ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) und bei Bedarf ausgelöst werden.

Warnhinweise ermöglichen Folgendes:

* In einer Vorschau anzeigen, wie oft ein Warnhinweis ausgelöst wird
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken
* „Gestapelte“ Warnhinweise erstellen, die mehrere Metriken in einem Warnhinweis vereinen.
* Erstellen von Warnhinweisen basierend auf Anomalien (Schwellenwerte von 90 %, 95 %, 99 %, 99,75 % und 99,9 %; prozentuale Veränderung; über/unter) (nur für Adobe Analytics-Kunden mit einem Select-, Prime- oder Ultimate-Paket verfügbar)

Das folgende Video-Tutorial bietet einen grundlegenden Überblick über Warnhinweise: [Warnhinweise](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html?lang=de) (5:34)

## Anomalie-Suche nach Warnungen

>[!NOTE]
>
>Die Verwendung von Warnhinweisen mit Anomalieerkennung (auch _intelligente Warnhinweise_ genannt) ist nur für Unternehmen mit einem Adobe Analytics Prime- oder Ultimate-Paket verfügbar.

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

Sie können vorhandene Warnhinweise im Warnhinweis-Manager verwalten. Sie können verschiedene Verwaltungsaufgaben für Warnhinweise ausführen, z. B. Taggen, Umbenennen, Löschen und mehr.

Weitere Informationen zum Verwalten vorhandener Warnhinweise in Adobe Analytics finden Sie unter [Verwalten von Warnhinweisen](/help/components/c-alerts/alert-manager.md).
