---
title: Treffertyp
description: Bestimmt, ob es sich bei dem Treffer um einen Vordergrund- oder Hintergrundtreffer handelt.
feature: Dimensions
exl-id: b922adbb-fe36-46c7-aab2-b9471de07d2f
TQID: https://experienceleague.adobe.com/6G-XpOMMZGum9LAQzKn0zGdeNRmHFPpmYizqRrbKuUE
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
subfeature_v2:
  - id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2
    internal-label: VRS
  - id: c77ba355-6681-41fe-b719-563d3f507fdb
    internal-label: Mobile SDK
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 31%
---
# Treffertyp

Der „Treffertyp“ [Dimension](overview.md) bestimmt, ob sich eine Mobile App im Vorder- oder Hintergrund befand, als der Treffer an die Datenerfassungs-Server von Adobe gesendet wurde. Diese Dimension ist nur für Report Suites relevant, die Daten für mobile Apps enthalten. Über AppMeasurement erfasste Browser-Daten melden den Treffer immer als `"Foreground"`.

## Füllen dieser Dimension mit Daten

Mobile SDK legt die [`customerPerspective`](/help/implement/vars/page-vars/customerperspective.md) fest, um anzugeben, ob jeder Treffer im Vorder- oder Hintergrund stattgefunden hat. Diese Dimension funktioniert bei allen Mobile SDK-Implementierungen ab Version 4.13.6 standardmäßig. Wenn Sie die mobile SDK nicht verwenden, werden alle Treffer unter `"Foreground"` aufgelistet. Wenn **[!UICONTROL Starten neuer Besuche durch Hintergrundtreffer verhindern]** bei der Konfiguration einer [Virtual Report Suite](../vrs/vrs-mobile-visit-processing.md) ausgewählt wird, werden durch Hintergrundtreffer [[!UICONTROL Besuche]](../metrics/visits.md) und [[!UICONTROL Unique Visitors]](../metrics/unique-visitors.md).

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | [`customerPerspective`](/help/implement/vars/page-vars/customerperspective.md) |
| **Feld Web SDK/XDM** | Keine |
| **Abfrageparameter** | [`cp`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML-Tag** | [`<customerPerspective>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehören `"Foreground"` und `"Background"`. Hintergrundtreffer treten nur auf Mobilgeräten auf, auf denen sich die verfolgte Anwendung im Hintergrund befindet.
