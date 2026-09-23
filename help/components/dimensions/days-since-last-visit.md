---
title: Tage seit dem letzten Besuch
description: Die Anzahl der Tage zwischen dem aktuellen Treffer und dem letzten Besuch.
feature: Dimensions
exl-id: 8063bdc6-516a-4dd0-a4ca-ded739e8d406
TQID: https://experienceleague.adobe.com/VOkdvehFSgp1xBEq49W5FIphzHi8ZCbrsoMnI7rgQMs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
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
source-wordcount: '206'
ht-degree: 57%
---
# Tage seit dem letzten Besuch

Die Dimension „Tage seit dem letzten Besuch[&#x200B; misst &#x200B;](overview.md) Zeitspanne zwischen dem aktuellen Treffer des Besuchers und seinem vorherigen Besuch (sofern vorhanden). Diese Dimension hilft Ihnen, das Verhalten der Besucher nach dem Besuch Ihrer Website zu verstehen. Beispiele hierfür sind:

* Wie häufig rufen Benutzer die Site erneut auf?
* Wie korreliert die Rückkehrhäufigkeit mit der Konversion? Besuchen Wiederholungskäufer häufig oder selten?
* Kehren Benutzer, die sich durch Kampagnen klicken, häufiger zurück?

Erstmalige Besucher sind in dieser Dimension nicht enthalten.

## Füllen dieser Dimension mit Daten

Adobe berechnet diese Dimension Server-seitig aus dem Besuchsverlauf des Besuchers. Es gibt keine Variable zum Festlegen. Dies ist bei allen Implementierungen vorkonfiguriert.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (berechnet von Adobe) |
| **Feld Web SDK/XDM** | Keine (berechnet von Adobe) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehört die Anzahl der Tage zwischen dem letzten Besuch eines Besuchers und dem aktuellen Treffer. Jede Anzahl von Tagen ist ein eigenes Dimensionselement, wobei `"Same day"` dort auftritt, wo der letzte Besuch eines Besuchers und der aktuelle Treffer am selben Tag stattgefunden haben.
