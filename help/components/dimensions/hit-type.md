---
title: Treffertyp
description: Bestimmt, ob es sich bei dem Treffer um einen Vordergrund- oder Hintergrundtreffer handelt.
feature: Dimensions
exl-id: b922adbb-fe36-46c7-aab2-b9471de07d2f
TQID: https://experienceleague.adobe.com/6G-XpOMMZGum9LAQzKn0zGdeNRmHFPpmYizqRrbKuUE
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2id: c77ba355-6681-41fe-b719-563d3f507fdbid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 34%

---

# Treffertyp

Der „Treffertyp“ [Dimension](overview.md) bestimmt, ob sich eine Mobile App im Vorder- oder Hintergrund befand, als der Treffer an die Datenerfassungs-Server von Adobe gesendet wurde. Diese Dimension ist nur für Report Suites relevant, die Daten für mobile Apps enthalten. Über AppMeasurement erfasste Browser-Daten melden den Treffer immer als `"Foreground"`.

## Füllen dieser Dimension mit Daten

Diese Dimension funktioniert bei allen Mobile SDK-Implementierungen ab Version 4.13.6 standardmäßig. Mobile SDK legt die [`customerPerspective`](/help/implement/vars/page-vars/customerperspective.md)-Variable (den `cp` Abfrageparameter) fest, um anzugeben, ob jeder Treffer im Vordergrund oder im Hintergrund aufgetreten ist. Wenn Sie die mobile SDK nicht verwenden, werden alle Treffer unter `"Foreground"` aufgelistet. Wenn **[!UICONTROL Starten neuer Besuche durch Hintergrundtreffer verhindern]** bei der Konfiguration einer [Virtual Report Suite](../vrs/vrs-mobile-visit-processing.md) ausgewählt wird, werden durch Hintergrundtreffer [[!UICONTROL Besuche]](../metrics/visits.md) und [[!UICONTROL Unique Visitors]](../metrics/unique-visitors.md).

## Dimensionselemente

Zu den Dimensionselementen gehören `"Foreground"` und `"Background"`. Hintergrundtreffer treten nur auf Mobilgeräten auf, auf denen sich die verfolgte Anwendung im Hintergrund befindet.
