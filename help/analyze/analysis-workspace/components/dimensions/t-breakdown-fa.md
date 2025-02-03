---
description: Schlüsseln Sie Dimensionen und Dimensionselemente in Analysis Workspace auf.
keywords: Analysis Workspace
title: Dimensionen aufschlüsseln
feature: Dimensions
role: User, Admin
exl-id: 0d26c920-d0d9-4650-9cf0-b67dbc4629e1
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 89%

---

# Dimensionen aufschlüsseln

Schlüsseln Sie Dimensionen und Dimensionselemente in Analysis Workspace auf.

Sie können Ihre Daten für Ihre spezifischen Anforderungen unbegrenzt aufschlüsseln. Erstellen Sie Abfragen mithilfe relevanter Metriken, Dimensionen, Segmente, Zeitachsen und anderer Aufschlüsselungswerte für die Analyse.

1. [Erstellen Sie ein Projekt](/help/analyze/analysis-workspace/home.md) mit einer Datentabelle.
1. Klicken Sie in der Datentabelle mit der rechten Maustaste auf einen Zeileneintrag und wählen Sie **[!UICONTROL Aufschlüsselung]** > *`<item>`* aus.

   ![Ergebnis des Schritts](assets/fa_data_table_actions.png)

   Sie können Metriken nach Dimensionselementen oder Zielgruppensegmenten über ausgewählte Zeiträume aufschlüsseln. Sie können auch noch granularer aufschlüsseln.

   >[!NOTE]
   >
   >Die Anzahl der in der Tabelle angezeigten Aufschlüsselungen ist auf 200 beschränkt. Für das Exportieren von Aufschlüsselungen ist diese Einschränkung höher.

## Attributionsmodelle auf Aufschlüsselungen anwenden

Auf jede Aufschlüsselung innerhalb einer Tabelle kann auch ein beliebiges Attributionsmodell angewandt werden. Dieses Attributionsmodell kann mit der übergeordneten Spalte identisch sein oder sich von ihr unterscheiden. Sie können beispielsweise lineare Bestellungen in Ihrer Dimension „Marketing-Kanäle“ analysieren, jedoch U-förmige Bestellungen auf spezifische Trackingcodes in einem Kanal anwenden. Bewegen Sie zum Bearbeiten des auf eine Aufschlüsselung angewendeten Attributionsmodells einfach den Mauszeiger auf das Aufschlüsselungsmodell und klicken Sie auf **[!UICONTROL Bearbeiten]**:

![Aufschlüsselungseinstellungen](assets/breakdown_settings.png)

Dies ist das erwartete Verhalten, wenn Attributionsmodelle auf Aufschlüsselungen angewendet oder bearbeitet werden:

* Wenn Sie eine Zuordnung anwenden, wenn keine anderen Zuordnungen vorhanden sind, gilt die Zuordnung für die gesamte Spaltenstruktur.

* Wenn Sie eine Aufschlüsselung hinzufügen, nachdem eine Attribution angewendet wurde, wird der Standardwert für die angegebene Aufschlüsselung verwendet, die hinzugefügt wurde, wenn diese Dimension einen Standardwert hat. Andernfalls wird die Aufschlüsselung aus der übergeordneten Spalte verwendet. Einige Dimensionen haben eine Standardzuweisung.  Zum Beispiel verwenden [!UICONTROL Time] Dimensionen und [!UICONTROL Referrer] [!UICONTROL Same Touch]. Die Dimension [!UICONTROL Produkt] verwendet [!UICONTROL Letzte Berührung]. Andere Dimensionen haben keinen Standardwert und verwenden die Zuordnung der übergeordneten Spalte.

* Wenn im Spaltenbaum bereits Zuordnungen vorhanden sind, wirkt sich eine Änderung der Zuordnung nur auf diejenige aus, die Sie gerade bearbeiten.

## Videos


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Hinzufügen von Dimensionen und Metriken zu Ihrem Projekt in Analysis Workspace](https://video.tv.adobe.com/v/30606?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]



>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Arbeiten mit Dimensionen in einer Freiformtabelle](https://video.tv.adobe.com/v/40179?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Dimensionsaufschlüsselungen nach Position](https://video.tv.adobe.com/v/24033?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]

