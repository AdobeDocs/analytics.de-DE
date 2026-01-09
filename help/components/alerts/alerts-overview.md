---
description: Erfahren Sie, wie Sie mit Warnhinweisen eine granulare Steuerung der Benachrichtigungen und die Integration mit der Anomalieerkennung ermöglichen.
title: Warnhinweise – Überblick
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: f02b660b551f5291443b8f7c5c51179a06b22eb9
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 54%

---

# Warnhinweise – Überblick

Warnhinweise in Adobe Analytics ermöglichen es Ihnen, sich über geänderte Prozentsätze oder bestimmte Datenpunkte benachrichtigen zu lassen.

Je nach Adobe Analytics-Paket können Sie auch Warnhinweise verwenden, die basierend auf Schwellenwerten für Anomalien ausgelöst werden. Diese Warnhinweise (auch *intelligente Warnhinweise* genannt) bieten granulare Steuerelemente, die in die [Anomalieerkennung“ integriert sind &#x200B;](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) ausgelöst werden, wenn Sie sie am dringendsten benötigen.

Mithilfe von Warnhinweisen können Sie:

* Vorschau der Trigger eines Warnhinweises.
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken.
* Erstellen *gestapelten* Warnhinweisen, die mehrere Metriken in einem Warnhinweis erfassen.
* Erstellen von Warnhinweisen basierend auf:
   * Anomalien in Metriken, die vorhanden sind, über oder unter den erwarteten Schwellenwerten liegen.

     [Anomalieerkennung](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) erstellt anhand historischer Daten einen erwarteten Wert plus eine obere und untere Grenze. Wenn der tatsächliche Metrikwert über die Obergrenze oder unter die Untergrenze, die als Schwellenwert definiert ist, fällt, wird dieses Ereignis als Anomalie auf der Konfidenzschwelle des Schwellenwerts betrachtet und führt zum Trigger des Warnhinweises. Ein höherer Schwellenwert (z. B.: 99 % oder 99,9 %) bedeutet eine breitere Bandbreite, was zu weniger Warnungen führt, die durch extremere Anomalien verursacht werden. Ein niedrigerer Schwellenwert (z. B.: 90 %) bedeutet eine engere Bandbreite, was zu mehr Warnungen führt, die durch weniger extreme Anomalien verursacht werden.
   * Änderungen an Metriken um einen bestimmten Prozentsatz.
   * Metriken, die über, unter oder gleich einem bestimmten Wert sind. (nur für Adobe Analytics-Kunden mit einem Select-, Prime- oder Ultimate-Paket verfügbar)

Dieses [Video-Tutorial](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/data-science/intelligent-alerts) bietet einen grundlegenden Überblick über Warnhinweise.


## Anomalie-Suche nach Warnungen

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

Informationen zum Erstellen von Warnhinweisen in Adobe Analytics finden Sie unter [Erstellen von Warnhinweisen](/help/components/alerts/alert-builder.md).

>[!IMPORTANT]
>
>Die Verwendung von Zeitstempeldaten zur Erstellung von Warnhinweisen kann dazu führen, dass Warnhinweise falsch ausgelöst werden. Adobe empfiehlt die Verwendung von Daten ohne Zeitstempel für Warnhinweise.

## Verwalten von Warnhinweisen

Sie können vorhandene Warnhinweise im Warnhinweis-Manager verwalten. Sie können verschiedene Verwaltungsaufgaben für Warnhinweise ausführen, z. B. Tagging, Umbenennen, Löschen und mehr.

Weitere Informationen zum Verwalten vorhandener Warnhinweise in Adobe Analytics finden Sie unter [Verwalten von Warnhinweisen](/help/components/alerts/alert-manager.md).
