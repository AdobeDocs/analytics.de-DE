---
description: Erläutert, wie Sie eine Metrik erstellen, die zeigt, welche Marketing-Kanäle zur Erhöhung der Bestellungen beitragen. Dies kann an beliebige relevante Dimensionen oder Erfolgsereignisse angepasst werden.
title: Order Assist-Metrik
feature: Calculated Metrics
exl-id: 33cb441d-d003-408d-ba67-1bcdd0e821ff
source-git-commit: 7722a2f01ff77dfec8ce110fd04fe977f6c627c6
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 59%

---

# Erstellen einer Metrik vom Typ „Bestellhilfen“

In den folgenden Informationen wird erläutert, wie Sie eine Metrik erstellen, die anzeigt, welche Marketing-Kanäle bei Bestellungen helfen. Dies kann an beliebige relevante Dimensionen oder Erfolgsereignisse angepasst werden.

1. Beginnen Sie mit der Erstellung einer berechneten Metrik, wie in [Metriken erstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) beschrieben.

1. Benennen Sie im Generator für berechnete Metriken die Metrik „Unterstützte Bestellungen“ oder etwas Ähnliches.

1. Ziehen Sie eine Bestellungsmetrik in die Arbeitsfläche „Definition“. Passen Sie das Attributionsmodell anschließend über das Zahnradsymbol für Einstellungen an, indem Sie das Kontrollkästchen **[!UICONTROL Nicht standardmäßige Attributionsmodelle verwenden]** aktivieren.

   ![](assets/attr-model.png)

1. Wählen Sie als Attributionsmodell **[!UICONTROL Benutzerdefiniert]** aus. Ändern Sie die Attributstärke zu 0 (Starter), 100 (Player) und 0 (Closer).

   ![](assets/custom-attr-model.png)

1. Wählen [!UICONTROL **Anwenden**] > [!UICONTROL **Speichern**].

1. Erstellen Sie in Analysis Workspace eine Freiformtabelle mit der Dimension Marketing-Kanal, Bestellungen und Ihrer neuen Metrik für unterstützte Bestellungen .

   ![](assets/mktg-channel-assists.png)

   Dies ist eine einfache Möglichkeit, um festzustellen, welche Marketing-Kanäle zur Erhöhung der Bestellungen beigetragen haben. Alternativ können Sie in einer Freiformtabelle mit der rechten Maustaste auf eine Metrik klicken und das Attributionsmodell direkt über die Tabelle anpassen.

1. (Optional) Geben Sie die Metrik für andere Benutzer in Ihrer Organisation frei, wie unter [Freigeben berechneter Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md) beschrieben.
