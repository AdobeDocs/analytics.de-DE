---
description: Das Bedienfeld Seitenzusammenfassung zeigt Zusammenfassungsinformationen für eine von Ihnen ausgewählte Seite an.
title: Bedienfeld „Seitenzusammenfassung“
feature: Panels
role: User, Admin
exl-id: f0b7cd92-17b2-452d-9aab-f78629360ab8
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 9%

---

# Bedienfeld „Seitenzusammenfassung“

In diesem Bedienfeld können Sie wichtige Statistiken zu bestimmten Seiten einfach untersuchen.

## Zugriff auf das Bedienfeld

Sie können auf das Bedienfeld in [!UICONTROL Berichte] oder in [!UICONTROL Workspace ].

| Zugangspunkt | Beschreibung |
| --- | --- |
| [!UICONTROL Berichte] | <ul><li>Das Bedienfeld ist bereits in einem Projekt abgelegt.</li><li>Die linke Leiste ist reduziert.</li><li>Es wird nur die Dimension Seite unterstützt.</li><li>Eine Standardeinstellung wurde bereits angewendet, in diesem Fall die am häufigsten besuchte Seite für die Dimension [!UICONTROL Seite]. Sie können diese Einstellung ändern.</li></ul> |
| Workspace | Erstellen Sie ein neues Projekt und wählen Sie das Bedienfeldsymbol in der linken Leiste aus. Ziehen Sie das Bedienfeld [!UICONTROL Seitenzusammenfassung] über die Freiformtabelle. Beachten Sie, dass das Feld Dimension [!UICONTROL Element] leer gelassen wird. Wählen Sie ein Dimensionselement aus der Dropdownliste aus. |

## Panel-Eingaben {#Input}

Sie können das Bedienfeld [!UICONTROL Seitenzusammenfassung] mit den folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
| --- | --- |
| Ablegebereich für Segmente (oder andere Komponenten) | Sie können Segmente oder andere Komponenten per Drag-and-Drop verschieben, um Ihre Bedienfeldergebnisse weiter zu filtern. |
| Dimensionselement der Seite | Wählen Sie aus der Dropdown-Liste das Dimensionselement Seite aus, dessen Schlüsselstatistiken Sie untersuchen möchten. |

{style="table-layout:auto"}

Klicken Sie **[!UICONTROL Erstellen]**, um das Bedienfeld zu erstellen.

## Bedienfeldausgabe {#output}

Das Bedienfeld [!UICONTROL Seitenzusammenfassung] gibt eine Vielzahl von Metrikdaten und Visualisierungen zurück, die Ihnen helfen, Statistiken zu bestimmten Seiten besser zu verstehen.

| Metrik/Visualisierung | Beschreibung |
| --- | --- |
| [!UICONTROL Seitenansichten] - Aktueller Monat, bis jetzt | Anzahl der Seitenansichten für diese Seite im aktuellen Monat. |
| [!UICONTROL Seitenansichten] - 4 Wochen vorher | Anzahl der Seitenansichten für diese Seite im letzten Monat. |
| [!UICONTROL Seitenansichten] - 52 Wochen vorher | Anzahl der Seitenansichten für diese Seite im letzten Jahr. |
| [!UICONTROL Trend] | Ein Diagramm mit einer Trend-Seitenansicht für diesen Monat, vor 4 Wochen und vor 52 Wochen. |
| [!UICONTROL Prozentsatz aller Seitenansichten] | Eine Zusammenfassungszahl für den Prozentsatz aller Seitenansichten, die zu dieser Seite gewechselt sind. |
| [!UICONTROL Besuchszeit pro Seite] | Ein horizontales Balkendiagramm mit der auf dieser Seite verbrachten Zeit. |
| [!UICONTROL Einzelseitenbesuche] | Eine Zusammenfassungszahl, die die Anzahl der Seitenansichten auflistet, bei denen dies die einzige besuchte Seite war. |
| [!UICONTROL Neuladungen] | Die Metrik [!UICONTROL Neuladungen] gibt an, wie oft ein Dimensionselement während eines Neuladens vorhanden war. Ein Besucher, der seinen Browser aktualisiert, stellt die häufigste Methode dar, eine Neuladung auszulösen. |
| [!UICONTROL Einträge] | Die Metrik [!UICONTROL Einträge] gibt an, wie oft ein bestimmtes Dimensionselement als erster Wert bei einem Besuch erfasst wird. |
| [!UICONTROL Ausstiege] | Die [!UICONTROL Exits]-Metrik zeigt an, wie oft ein bestimmtes Dimensionselement als letzter Wert bei einem Besuch erfasst wird. |
| [!UICONTROL Fluss] | Ein Flussdiagramm mit der ausgewählten Seite als Fokus. Sie können die Daten wie in jedem [-Diagramm weiter ](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md). |

{style="table-layout:auto"}

![Bedienfeld „Seitenzusammenfassung“](assets/page-sum1.png)

![Metriken und Fluss](assets/page-sum2.png)
