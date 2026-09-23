---
title: Tage seit letztem Kauf
description: Die Anzahl der Tage zwischen dem aktuellen Treffer und dem letzten Kauf, den er getätigt hat.
feature: Dimensions
exl-id: 6f0d9d79-cf40-4de3-9d9f-9b1bc57f97b6
TQID: https://experienceleague.adobe.com/q86bc1bMRctUBe7dFEJaALsq0GjALFQQtKU9cRpRkoU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
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
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 64%
---
# Tage seit letztem Kauf

Die Dimension „Tage seit dem letzten Kauf[&#x200B; misst &#x200B;](overview.md) Zeitspanne zwischen dem aktuellen Treffer der Besucherin oder des Besuchers und ihrem bzw. seinem letzten Kauf zu diesem Zeitpunkt. Diese Dimension hilft Ihnen, das Verhalten der Besucher nach einem Kauf auf Ihrer Website zu verstehen.

Besucher, die noch nie etwas gekauft haben, werden in dieser Dimension nicht berücksichtigt. Auch Treffer, die vor dem ersten Kauf eines Besuchers erzielt wurden, sind nicht enthalten. Es werden nur Treffer nach dem ersten Kauf des Besuchers berücksichtigt.

## Füllen dieser Dimension mit Daten

Adobe berechnet diese Dimension Server-seitig aus dem Kaufverlauf des Besuchers. Es gibt keine Variable zum Festlegen. Dies hängt vom [`purchase`](/help/implement/vars/page-vars/events/event-purchase.md) ab, das auf Ihrer Site implementiert wird.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (berechnet von Adobe) |
| **Feld Web SDK/XDM** | Keine (berechnet von Adobe) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehört die Anzahl der Tage zwischen dem letzten Kauf eines Besuchers und dem aktuellen Treffer. Jede Anzahl von Tagen ist ein eigenes Dimensionselement, wobei „Gleicher Tag“ dann auftritt, wenn der letzte Kauf eines Besuchers und der aktuelle Treffer am selben Tag stattgefunden haben.
