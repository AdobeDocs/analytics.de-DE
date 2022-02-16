---
description: Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.
title: Übersicht über intelligente Warnhinweise
feature: Alerts
role: User, Admin
exl-id: 49d47896-bf93-4960-b647-2765c935eb25
source-git-commit: 10ae8213b8745439ab5968853f655a1176b8c38a
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 84%

---

# Übersicht über intelligente Warnhinweise

Intelligente Warnhinweise ermöglichen eine feiner abgestufte Kontrolle über Warnhinweise und integrieren die Anomalieerkennung in das Warnhinweissystem.

Hier finden Sie ein Video-Tutorial zu [intelligenten Warnhinweisen](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html?lang=de) (5:34)

## Überblick

Die neuen Funktionen „Warnhinweiserstellung“ und „Warnhinweis-Manager“ in Analysis Workspace ersetzen die bisherigen Funktionen in Reports &amp; Analytics. Mithilfe intelligenter Warnhinweise können Sie:

* Warnhinweise erstellen, die auf Anomalien basieren (90-%-, 95-%-, 99-%-, 99,75-%- und 99,9-%-Schwellen, Änderungen in %, darüber/darunter)
* In einer Vorschau anzeigen, wie oft ein Warnhinweis ausgelöst wird
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken
* „Gestapelte“ Warnhinweise erstellen, die mehrere Metriken in einem Warnhinweis vereinen.

Es gibt vier Möglichkeiten, in die Warnhinweiserstellung zu gelangen:

| Methode | Details |
| --- | --- |
| Direkt zur Warnhinweiserstellung wechseln | **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]** |
| Verwenden des Tastaturbefehls in Workspace | `Ctrl + Shift + A` (Windows) oder `Cmd + Shift + A` (Mac) |
| Ein oder mehrere Freiform-Tabellenzeilenelemente auswählen | Klicken Sie mit der rechten Maustaste und wählen Sie **[!UICONTROL Warnhinweis aus Auswahl erstellen]**. Dadurch wird die [!UICONTROL Warnhinweiserstellung] und füllt die entsprechenden Metriken und angewendeten Filter aus. Falls erforderlich, können Sie den Warnhinweis dann bearbeiten. ![Warnhinweis aus Auswahl erstellen](assets/create-alert-from-selection.png) |
| Aus einem Reports &amp; Analytics-Bericht | Navigieren Sie zu  **[!UICONTROL Mehr]** > **[!UICONTROL Warnhinweis hinzufügen]** . Dadurch wird die Warnhinweiserstellung geöffnet und die entsprechenden Metriken und angewendeten Filter aus dem Bericht werden vorausgefüllt. Falls erforderlich, können Sie den Warnhinweis dann bearbeiten. ![Warnhinweis hinzufügen](assets/add-alert.png) |

Bei den prozentualen Schwellenwerten handelt es sich um Standardabweichungen. Beispiel: 95 % = 2 Standardabweichungen und 99 % = 3 Standardabweichungen. Je nach der von Ihnen ausgewählten Zeitgranularität  werden [verschiedene Modelle](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) verwendet, um zu berechnen, wie weit jeder Punkt von der Norm entfernt ist (Anzahl der Standardabweichungen). Wenn Sie einen niedrigeren Schwellenwert festlegen (z. B. 90 %), erhalten Sie mehr Anomalien als bei einem höheren Schwellenwert (99.75 %).

>[!IMPORTANT]
>
>Die Verwendung von Zeitstempeldaten zur Erstellung von Warnhinweisen kann dazu führen, dass Warnhinweise falsch ausgelöst werden. Adobe empfiehlt die Verwendung von Daten ohne Zeitstempel für intelligente Warnhinweise.

## Anomalie-Suche nach Warnungen

Wenn ein Warnhinweis eine Anomalieerkennung verwendet, hängt der Trainings-Zeitraum von der für den Warnhinweis ausgewählten Granularität ab.

* Monatliche Granularität: 15 Monate + derselbe Bereich im letzten Jahr
* Wöchentliche Granularität: 15 Wochen + derselbe Bereich im letzten Jahr
* Tägliche Granularität: 35 Tage + derselbe Bereich im letzten Jahr
* Stündliche Granularität: 336 Stunden

Weitere Informationen finden Sie unter [Statistische Verfahren zur Anomalieerkennung](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md).
