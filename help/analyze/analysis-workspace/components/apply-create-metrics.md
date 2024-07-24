---
description: In Analysis Workspace gibt es zwei Möglichkeiten zur Verwendung von Metriken.
title: Metriken in Analysis Workspace
feature: Metrics
role: User, Admin
exl-id: 0a5dc709-c4e8-412a-a6cf-37b85d811f65
source-git-commit: f8541ac8f82e63f1664b06ed788d307c5d224ca9
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 51%

---

# Metriken

Mit Metriken können Sie Datenpunkte in Analysis Workspace quantifizieren. Sie werden meist als Spalten in einer Visualisierung verwendet und sind an Dimensionen gebunden.

## Arten von Metriken

Adobe bietet verschiedene Arten von Metriken zur Verwendung in Analysis Workspace:

* **Standardmetriken**: Die meisten Metriken, die Sie in Projekten verwenden, sind Standardmetriken. Beispiele sind [Seitenansichten](/help/components/metrics/page-views.md), [Umsatz](/help/components/metrics/revenue.md) oder [Benutzerspezifische Ereignisse](/help/components/metrics/custom-events.md). Weitere Informationen finden Sie in der [Übersicht zu Metriken](/help/components/metrics/overview.md) im Komponenten-Benutzerhandbuch.

  ![Standardmetrik](assets/standard-metric.png)

* **Berechnete Metriken**: Benutzerdefinierte Metriken, die auf Standardmetriken, statischen Zahlen oder algorithmischen Funktionen basieren. Bei benutzerdefinierten berechneten Metriken wird in der Liste der verfügbaren Komponenten ein Taschenrechnersymbol angezeigt. Weitere Informationen finden Sie in der [Übersicht zu berechneten Metriken](/help/components/c-calcmetrics/cm-overview.md) im Komponenten-Benutzerhandbuch.

  ![Berechnete Kennzahl](assets/calculated-metric.png)

* **Vorlagen für berechnete Metriken**: Von Adobe definierte Metriken, die sich ähnlich wie berechnete Metriken verhalten. Sie können sie unverändert in Workspace-Projekten verwenden oder eine Kopie speichern, um ihre Logik anzupassen. Bei Vorlagen für berechnete Metriken wird in der Liste der verfügbaren Komponenten ein Adobe-Symbol angezeigt.

  ![Vorlage für berechnete Metriken](assets/calculated-metric-template.png)

## Verwenden von Metriken in Analysis Workspace

Metriken können in Analysis Workspace auf verschiedene Arten verwendet werden. Informationen zum Hinzufügen von Metriken und anderen Komponententypen zu Analysis Workspace finden Sie unter [Verwenden von Komponenten in Analysis Workspace](/help/analyze/analysis-workspace/components/use-components-in-workspace.md).

>[!VIDEO](https://video.tv.adobe.com/v/40817/?quality=12)

## Berechnete Metriken erstellen

Berechnete Metriken ermöglichen es Ihnen, mithilfe einfacher Operatoren oder statistischer Funktionen einfach zu erkennen, wie sich Metriken zueinander verhalten.

Es gibt mehrere Möglichkeiten, berechnete Metriken zu erstellen. Die gewählte Methode bestimmt, ob die berechnete Metrik in der Komponentenliste für alle Projekte oder nur in dem Projekt verfügbar ist, in dem sie erstellt wurde.

### Berechnete Metriken für alle Projekte erstellen

Mit dem Generator für berechnete Metriken können Sie berechnete Metriken erstellen. Auf diese Weise werden berechnete Metriken in der Komponentenliste verfügbar und können dann in Projekten in Ihrer gesamten Organisation verwendet werden.

Informationen zum Zugriff auf den Generator für berechnete Metriken finden Sie unter [Metriken erstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md).

### Berechnete Metriken für ein einzelnes Projekt erstellen

Sie können schnell berechnete Metriken erstellen, die nur für das Projekt verfügbar sind, in dem sie erstellt wurden.

So erstellen Sie eine berechnete Metrik für ein einzelnes Projekt:

1. Öffnen Sie in Analysis Workspace das Projekt, in dem Sie die berechnete Metrik erstellen möchten.

1. Klicken Sie in einer Freiformtabelle mit der rechten Maustaste auf eine oder mehrere Spaltenüberschriftszellen und wählen Sie dann **[!UICONTROL Metrik aus Auswahl erstellen]**

   ![Workspace-Bedienfeld, das die Option Aus Auswahl erstellen hervorhebt](assets/create-metric-from-selection.png)

1. Um nur eine berechnete Metrik für dieses Projekt zu erstellen, wählen Sie eine der folgenden Optionen aus:

   * [!UICONTROL **divide**]

   * [!UICONTROL **Subtract**]

   * [!UICONTROL **Hinzufügen**]

   * [!UICONTROL **Multiply**]

   Alternativ können Sie den Generator für berechnete Metriken öffnen und die berechnete Metrik für alle Projekte erstellen, indem Sie [!UICONTROL **Im Generator für berechnete Metriken öffnen**] und dann mit [Metriken erstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) fortfahren.

[Berechnete Metriken: implementierungslose Metriken](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/calculated-metrics/calculated-metrics-implementationless-metrics.html?lang=de) (3:42)

## Vergleichen von Metriken mit verschiedenen Attributionsmodellen

Wenn Sie Attributionsmodelle schnell und einfach miteinander vergleichen möchten, können Sie mit der rechten Maustaste auf eine Metrik klicken und **[!UICONTROL Attributionsmodelle vergleichen]** auswählen:

![Vergleichsattribution](assets/compare-attribution.png)

Dadurch können Sie Attributionsmodelle schnell und einfach miteinander vergleichen, ohne eine Metrik hereinzuziehen und sie zweifach zu konfigurieren.

## Verwenden der Funktion [!UICONTROL Kumulativer Durchschnitt] zum Anwenden der Metrikausgleichung

Im Folgenden finden Sie ein Video zum Thema:

>[!VIDEO](https://video.tv.adobe.com/v/27068/?quality=12)
