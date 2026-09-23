---
title: Ursprüngliche Referrer-Domain
description: Die erste Referrer-Domain, auf der sich eine Besucherin bzw. ein Besucher befand, bevor sie bzw. er zu Ihrer Site klickte.
feature: Dimensions
exl-id: 6b9ac662-a79a-477b-8612-7980da7cfadd
TQID: https://experienceleague.adobe.com/G-se6LH33gMTt8ttrP5RBzL85m335ujtbiSm6EjLGuU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 72%
---
# Ursprüngliche Referrer-Domain

Die Dimension „Ursprüngliche Referrer[&#x200B; gibt die erste Referrer](overview.md)Domain an, auf die sich ein Besucher geklickt hat, um zu Ihrer Site zu gelangen. Sobald sie festgelegt wurde, enthält sie denselben Wert für die gesamte Lebensdauer dieser Besucher-ID. Diese Dimension ist nützlich, um zu verstehen, welche Drittanbieter-Websites ursprünglich Traffic auf Ihre Site bringen.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension vom ersten Referrer des Besuchers [, indem &#x200B;](referrer.md) Domain-Teil dieser Referrer-URL verwendet wird. Es gibt keine Variable zum Festlegen. Sie müssen die „Internen URL[Filter“ Ihrer Report Suite konfigurieren](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) Andernfalls können interne Domains einbezogen oder das Auftreten externer Domains verhindert werden.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom ersten Referrer des Besuchers) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom ersten Referrer des Besuchers) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | Besucher |

Wenn ein Besucher zu irgendeinem Zeitpunkt einen Link auf einer anderen Domain durchklickt, wird der neue Wert nicht erfasst. Informationen zu neuen Werten finden Sie unter [Verweisende Domain](referring-domain.md).

## Dimensionselemente

Zu den Dimensionselementen gehören die Domänen, durch die Besucher zu Ihrer Site klicken. Wenn ein Treffer keine Referrer-Daten (entweder gesetzt oder beibehalten) enthält, wird er unter dem Dimensionselement `"None"` gruppiert. Dieses Dimensionselement bedeutet, dass kein Referrer-Wert vorhanden ist, z. B. wenn der Besucher die Browser-Adresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat.

## Referrer-Domäne im Vergleich zur ursprünglichen Referrer-Domäne

Die Referrer-Domäne kann sich zwischen Besuchen ändern. So gelangt beispielsweise ein Besucher über `google.com` zu Ihrer Site und dann eine Woche später über `twitter.com`. Schließlich tätigen sie einen Kauf auf Ihrer Site. Wenn Sie Referrer-Domäne als Dimension mit Letztkontakt-Attribution verwenden, wird der Kauf `twitter.com` gutgeschrieben. Wenn Sie die ursprüngliche Referrer-Domäne als Dimension verwenden, wird der Kauf unabhängig vom Attributionsmodell `google.com` gutgeschrieben.

Die ursprüngliche Referrer-Domain ändert sich während der gesamten Lebensdauer einer bestimmten Besucher-ID nie.
