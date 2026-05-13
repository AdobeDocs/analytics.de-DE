---
description: Erfahren Sie, wie Sie mit Warnhinweisen eine granulare Steuerung der Benachrichtigungen und die Integration mit der Anomalieerkennung ermöglichen.
title: Warnhinweise – Überblick
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
TQID: https://experienceleague.adobe.com/FDzJzBjxMc-EkhW0k0NiENt-g53sRnzXQDs1XQWFseI
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b0ca67c6-0a35-482c-ad91-baac1bcb26d6id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 435
ht-degree: 53%

---

# Überblick über Warnhinweise

Warnhinweise in Adobe Analytics ermöglichen es Ihnen, sich über geänderte Prozentsätze oder bestimmte Datenpunkte benachrichtigen zu lassen.

Je nach Adobe Analytics-Paket können Sie auch Warnhinweise verwenden, die basierend auf Schwellenwerten für Anomalien ausgelöst werden. Diese Warnhinweise (auch *intelligente Warnhinweise* genannt) bieten granulare Steuerelemente, die in die [Anomalieerkennung“ integriert sind ](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) ausgelöst werden, wenn Sie sie am dringendsten benötigen.

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
