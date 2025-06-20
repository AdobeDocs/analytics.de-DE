---
description: Erläutert, wie Sie eine Metrik erstellen, die zeigt, welche Marketing-Kanäle zur Erhöhung der Bestellungen beitragen. Dies kann an beliebige relevante Dimensionen oder Erfolgsereignisse angepasst werden.
title: Order Assist-Metrik
feature: Calculated Metrics
exl-id: 33cb441d-d003-408d-ba67-1bcdd0e821ff
source-git-commit: bf58da2a39e8b9fd298356f23a9bf8f6c394d3de
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 25%

---

# Erstellen einer komplexeren berechneten Metrik

In diesem Artikel wird ein komplexeres Beispiel für eine berechnete Metrik erläutert. Diese berechnete Metrik zeigt an, welche Marketing-Kanäle bei Bestellungen helfen. Dieser Typ der berechneten Metrik kann an jede Dimension oder jedes Erfolgsereignis angepasst werden.

1. Beginnen Sie mit dem Erstellen einer berechneten Metrik, wie in [Metriken erstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) beschrieben.

1. Benennen Sie im Generator für berechnete Metriken die Metrik `Assisted Orders` oder etwas Ähnliches.

1. Wählen Sie die Metrik **[!UICONTROL Online-Bestellungen]** aus den Komponenten **[!UICONTROL Metriken]** und ziehen Sie die Metrik in den Bereich **[!UICONTROL Definition]**.

   1. Wählen Sie ![ Metrik ](/help/assets/icons/Setting.svg)Einstellung“ aus.
   1. Wählen **[!UICONTROL Nicht-standardmäßiges Attributionsmodell verwenden]**.
   1. Passen Sie das Attributionsmodell im **[!UICONTROL Spalten-Attributionsmodell]** an.
      1. Wählen Sie **[!UICONTROL Benutzerdefiniert]** für **[!UICONTROL Modell]** aus. Legen Sie **[!UICONTROL Starter]** auf `0`, **[!UICONTROL Player]** auf `100` und **[!UICONTROL Closer]** auf `0` fest.
      1. Wählen Sie **[!UICONTROL Besucher]** für **[!UICONTROL Container]** aus.
      1. Wählen Sie **[!UICONTROL 30 Tage]** für **[!UICONTROL Lookback-Fenster]**.

      1. Wählen Sie **[!UICONTROL Anwenden]** aus.

      ![Spalten-Attributionsmodell](assets/complex-calculated-metric.png)

1. Wählen **[!UICONTROL Speichern]**, um die berechnete Metrik zu speichern.

So verwenden Sie die berechnete Metrik:

1. Erstellen Sie in Analysis Workspace eine Freiformtabelle mit der Dimension **[!UICONTROL Marketing]** Kanal“, **[!UICONTROL Online-Bestellungen]** und Ihrer neuen Metrik **[!UICONTROL Unterstützte Online-Bestellungen]**.

   ![Bestellungen über den Marketing-Kanal](assets/marketing-channel-assists.png)

1. (Optional) Geben Sie die Metrik für andere Benutzer in Ihrer Organisation frei, wie unter [Freigeben berechneter Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md) beschrieben.

Dies ist eine einfache Möglichkeit, um festzustellen, welche Marketing-Kanäle zur Erhöhung der Bestellungen beigetragen haben. Alternativ können Sie in einer Freiformtabelle mit der rechten Maustaste auf eine Metrik klicken und das Attributionsmodell direkt über die Tabelle anpassen.
