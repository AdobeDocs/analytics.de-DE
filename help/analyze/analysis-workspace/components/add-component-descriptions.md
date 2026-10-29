---
description: Erfahren Sie, wie Administratoren mithilfe einer Report Suite oder des Datenwörterbuchs Beschreibungen zu Komponenten hinzufügen können.
title: Komponentenbeschreibungen hinzufügen
feature: Components
role: Admin
exl-id: db36ee4a-66e2-45d1-8b7a-49570b5fce93
TQID: https://experienceleague.adobe.com/8z9vnSfrxEb1nkOlTTlHrp3BdElFJmTjbsSLBGbE7Gs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
    internal-label: Dashboards
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
    internal-label: Components
  - id: c45e2849-b5ab-4ac6-8df1-bbe34c2dd79e
    internal-label: Data Dictionary
  - id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2
    internal-label: VRS
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
    internal-label: Report suites
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: b3d9fb81837398b349496ec261dc1d0ba3df3645
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 20%
---
# Komponentenbeschreibungen hinzufügen

Beschreibungen helfen Benutzenden, die verschiedenen Komponenten optimal zu nutzen – beim Erstellen von Projekten in Analysis Workspace oder beim Anzeigen von Berichten.

Analytics-Admins können Komponentenbeschreibungen (Dimensionen, Metriken, Segmente und Datumsbereiche) entweder innerhalb einer Report Suite oder mithilfe des Datenwörterbuchs direkt in Analysis Workspace hinzufügen.

## Report Suite

Sie können Komponenten in einer Report Suite Beschreibungen hinzufügen.

1. Wählen Sie **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Report Suites]**.
1. Wählen Sie die Report Suite im Report Suite Manager aus, für die Sie Komponentenbeschreibungen angeben möchten.
1. Wählen Sie **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Konversionsvariablen]** aus.
1. Wählen ![Hinzufügen](/help/assets/icons/Add.svg), um Details für eine Konversionsvariable anzuzeigen.
1. Aktivieren Sie das Kontrollkästchen für **[!UICONTROL Beschreibung]** und fügen Sie eine Beschreibung hinzu.
1. Wiederholen Sie die Schritte 4 und 5 für jede andere Variable, der Sie eine Beschreibung hinzufügen möchten.
1. Wählen Sie **[!UICONTROL Speichern]** aus.

>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Komponentenbeschreibungen hinzufügen](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/intro-to-analytics/customizing-the-ui/adding-dimension-and-metric-descriptions){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


## Datenwörterbuch {#add-descriptions}

Das Datenwörterbuch in Analysis Workspace hilft Benutzenden und Administrierenden, die Komponenten in ihrer Analytics-Umgebung zu verfolgen und besser zu verstehen. Mit dem Datenwörterbuch können Analytics-Admins Komponentenbeschreibungen direkt in Analysis Workspace hinzufügen.

Informationen zum Bearbeiten einer Komponentenbeschreibung im Datenwörterbuch finden Sie unter [Bearbeiten von Komponenteneinträgen im Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md).

Allgemeine Informationen zum Datenwörterbuch finden Sie unter [Datenwörterbuch – Übersicht](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md).

>[!MORELIKETHIS]
>
>[Einstellungen der Berichtskomponente](/help/components/vrs/vrs-components.md)
>[Komponenteneinträge für Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md)
>

## Beschreibungen automatisch generieren

{{release-limited-testing-section}}

Anstatt jede Beschreibung manuell zu schreiben, kann Adobe Analytics generative KI verwenden, um Beschreibungen für Sie zu schreiben. Sie können für eine einzelne Komponente eine Beschreibung oder für viele Komponenten gleichzeitig Beschreibungen erstellen.

Erzeugte Beschreibungen:

* Es sind nicht mehr als drei Sätze lang.
* Beenden Sie mit dem Text **[!UICONTROL Von Adobe mithilfe von KI generiert]**, damit die Benutzer wissen, dass die Beschreibung generiert wurde.
* Kann nach ihrer Erstellung bearbeitet werden.

### Voraussetzungen

Bevor Sie Beschreibungen generieren können, muss Ihr Unternehmen bestimmten rechtlichen Bedingungen für Generative AI zustimmen. Wenn Ihr Unternehmen diesen Bedingungen nicht zugestimmt hat, ist die Option zum Generieren von Beschreibungen abgeblendet. Wählen Sie das Informationssymbol ![Info](/help/assets/icons/InfoOutline.svg) neben der Option aus, um zu erfahren, wie Sie die Funktion aktivieren, oder wenden Sie sich an den Administrator Ihres Unternehmens oder das Adobe-Accountteam.

### Wie Beschreibungen generiert werden

Die generierten Beschreibungen basieren auf der Definition der Komponente und auf zusätzlichem Kontext darüber, wie die Komponente in Ihrer Report Suite verwendet wird, z. B.:

* Die obersten Elemente einer Dimension
* Komponenten, die häufig mit der Komponente verwendet werden

Wenn eine berechnete Metrik oder ein Segment auf ein anderes Segment verweist, wird in der generierten Beschreibung die Definition des referenzierten Segments erläutert.

### Beschreibungen von verschiedenen Speicherorten generieren

Sie können Beschreibungen in den folgenden Bereichen von Adobe Analytics erstellen. Einige Speicherorte ermöglichen es Ihnen, Beschreibungen für mehrere Komponenten zu generieren, andere jedoch nicht.

Wählen Sie einen Speicherort aus, um zu erfahren, wie Sie dort Beschreibungen generieren können.

| Standort | Unterstützte Komponenten | Einzelne Komponente | Mehrere Komponenten |
| --- | --- | --- | --- |
| [Datenwörterbuch](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md) | <ul><li>Dimensionen</li><li>Metriken</li><li>Berechnete Metriken</li><li>Segmente</li><li>Datumsbereiche</li></ul> | Ja | Ja |
| [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-build.md) | Segmente | Ja | Nein |
| [Segment-Manager](/help/components/segmentation/segmentation-workflow/seg-manage.md#action-bar) | Segmente | Nein | Ja |
| [Generator für berechnete Metriken](/help/components/calculated-metrics/workflow/c-build-metrics/cm-build-metrics.md) | Berechnete Metriken | Ja | Nein |
| [Manager für berechnete Metriken](/help/components/calculated-metrics/workflow/cm-manager.md#action-bar) | Berechnete Metriken | Nein | Ja |
| [Generator für Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/create.md#date-range-builder) | Datumsbereiche | Ja | Nein |
| [Datumsbereichs-Manager](/help/analyze/analysis-workspace/components/calendar-date-ranges/manage.md#action-bar) | Datumsbereiche | Nein | Ja |

{style="table-layout:auto"}