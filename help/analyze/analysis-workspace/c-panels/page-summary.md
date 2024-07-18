---
description: Das Bedienfeld "Seitenzusammenfassung"zeigt zusammenfassende Informationen für eine von Ihnen ausgewählte Seite an.
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

In diesem Bedienfeld können Sie einfach Schlüsselstatistiken zu bestimmten Seiten durchsuchen.

## Zugriff auf den Bereich

Sie können über [!UICONTROL Berichte] oder in [!UICONTROL Workspace] auf den Bereich zugreifen.

| Zugangspunkt | Beschreibung |
| --- | --- |
| [!UICONTROL Berichte] | <ul><li>Das Bedienfeld wurde bereits in einem Projekt abgelegt.</li><li>Die linke Leiste ist ausgeblendet.</li><li>Es wird nur die Dimension Seite unterstützt.</li><li>Eine Standardeinstellung wurde bereits angewendet, in diesem Fall die am häufigsten besuchte Seite für die Dimension[!UICONTROL Seite] . Sie können diese Einstellung ändern.</li></ul> |
| Workspace | Erstellen Sie ein neues Projekt und wählen Sie in der linken Leiste das Bedienfeldsymbol aus. Ziehen Sie den Bereich [!UICONTROL Seitenzusammenfassung] über die Freiformtabelle. Beachten Sie, dass das Feld &quot;Seitenelement [!UICONTROL Dimension ]&quot;leer gelassen wird. Wählen Sie ein Dimensionselement aus der Dropdownliste aus. |

## Bedienfeldeingaben {#Input}

Sie können den Bereich [!UICONTROL Seitenzusammenfassung] mit den folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
| --- | --- |
| Dropzone Segment (oder andere Komponente) | Sie können Segmente oder andere Komponenten per Drag-and-Drop verschieben, um die Ergebnisse Ihrer Bedienfelder weiter zu filtern. |
| Seitendimensionselement | Wählen Sie aus der Dropdownliste das Dimensionselement Seite aus, dessen Schlüsselstatistiken Sie untersuchen möchten. |

{style="table-layout:auto"}

Klicken Sie auf **[!UICONTROL Build]** , um das Bedienfeld zu erstellen.

## Bedienfeldausgabe {#output}

Das Bedienfeld [!UICONTROL Seitenzusammenfassung] gibt einen umfangreichen Satz an Metrikdaten und -visualisierungen zurück, damit Sie Statistiken über bestimmte Seiten besser verstehen können.

| Metrik/Visualisierung | Beschreibung |
| --- | --- |
| [!UICONTROL Seitenansichten] - Aktueller Monat bislang | Anzahl der Seitenansichten für diese Seite im aktuellen Monat. |
| [!UICONTROL Seitenansichten] - 4 Wochen zuvor | Anzahl der Seitenansichten für diese Seite im letzten Monat. |
| [!UICONTROL Seitenansichten] - 52 Wochen zuvor | Anzahl der Seitenansichten für diese Seite im letzten Jahr. |
| [!UICONTROL Trend] | Ein Trend-Seitenansichtsdiagramm für diesen Monat, 4 Wochen zuvor und 52 Wochen zuvor. |
| [!UICONTROL Prozentsatz aller Seitenansichten] | Eine Zusammenfassungsnummer für den Prozentsatz aller Seitenansichten, die auf diese Seite gelangt sind. |
| [!UICONTROL Besuchszeit pro Seite] | Ein horizontales Balkendiagramm mit der auf dieser Seite verbrachten Zeit. |
| [!UICONTROL Einzelseitenbesuche] | Eine Zusammenfassungsnummer mit der Anzahl der Seitenansichten, bei denen dies die einzige besuchte Seite war. |
| [!UICONTROL Neuladungen] | Die Metrik [!UICONTROL Neuladungen] gibt an, wie oft ein Dimensionselement während einer Neuladung vorhanden war. Ein Besucher, der seinen Browser aktualisiert, stellt die häufigste Methode dar, eine Neuladung auszulösen. |
| [!UICONTROL Einträge] | Die Metrik [!UICONTROL Einstiege] gibt an, wie oft ein bestimmtes Dimensionselement als erster Wert bei einem Besuch erfasst wird. |
| [!UICONTROL Ausstiege] | Die Metrik [!UICONTROL Ausstiege] gibt an, wie oft ein bestimmtes Dimensionselement als letzter Wert bei einem Besuch erfasst wird. |
| [!UICONTROL Fluss] | Ein Flussdiagramm mit der ausgewählten Seite als Fokuspunkt. Sie können die Daten wie in jedem [Flussdiagramm](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md) weiter aufschlüsseln. |

{style="table-layout:auto"}

![Bedienfeld „Seitenzusammenfassung“](assets/page-sum1.png)

![Metriken und Fluss](assets/page-sum2.png)
