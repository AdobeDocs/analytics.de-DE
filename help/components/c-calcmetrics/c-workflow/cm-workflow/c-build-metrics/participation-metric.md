---
description: Mit dem Generator für berechnete Metriken kann jeder Benutzer eine Beitragsmetrik erstellen.
title: Partizipationsmetrik
feature: Calculated Metrics
exl-id: bef185d6-72c0-4068-80f8-57261369573f
source-git-commit: 4bf8397ee979614539baf21b36363eb03357567a
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 37%

---

# Erstellen einer Metrik vom Typ „Teilnahme“

In den folgenden Informationen wird erläutert, wie Sie eine Metrik erstellen, die anzeigt, welche Seiten zu Besuchen beigetragen haben (oder an ihnen teilgenommen haben), die eine Bestellung enthielten.

Diese Art von Informationen kann für jeden Inhaltsverantwortlichen nützlich sein.

>[!NOTE]
>
>Sie können Teilnahmemetriken in den Admin Tools aktivieren, jedoch nur für benutzerdefinierte Ereignisse 1 - 100.

1. Beginnen Sie mit der Erstellung einer berechneten Metrik, wie in [Metriken erstellen](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) beschrieben.

1. Benennen Sie die Metrik im Generator für berechnete Metriken mit „Teilnahme“.

1. Ziehen Sie das Erfolgsereignis „Bestellungen“ in die Arbeitsfläche „Definition“.

1. Ändern Sie das [Attributionsmodell](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) dieses Ereignisses in **[!UICONTROL Beteiligung]** unter dem Zahnradsymbol für **[!UICONTROL Einstellungen]**. Wählen Sie das Lookback **[!UICONTROL Besuch]**. Die Definition sollte etwa so aussehen:

   ![](assets/participation.png)

1. Wählen [!UICONTROL **Speichern**], um die Metrik zu speichern.

1. Verwenden Sie die berechnete Metrik im Bericht **[!UICONTROL Seiten]**.

   ![](assets/participation-pages.png)

1. (Optional) Geben Sie die Metrik für andere Benutzer in Ihrer Organisation frei, wie unter [Freigeben berechneter Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-sharing.md) beschrieben.
