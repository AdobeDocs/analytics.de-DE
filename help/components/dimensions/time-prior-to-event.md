---
title: Zeit vor Ereignis
description: Die Zeit zwischen der Metrik und dem ersten Treffer des Besuchs.
feature: Dimensions
exl-id: 2586673f-d908-4b69-901a-5fafe635d0d5
TQID: https://experienceleague.adobe.com/vO3S-yZwV7KSLmIzRfwNDrVaB3NzpsIocmHsAaamfj0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 84%

---

# Zeit vor Ereignis

Die „Zeit vor Ereignis“ [Dimension](overview.md) gibt die Zeit an, die zwischen dem ersten Treffer des Besuchs und der gewünschten Metrik vergangen ist. Diese Dimension ist nützlich, um die Zeitdauer zu bestimmen, die zum Erzielen eines Erfolgsereignisses (z. B. einer Formularübermittlung oder eines Kaufs) benötigt wird.

## Füllen dieser Dimension mit Daten

Obwohl diese Dimension technisch bei allen Implementierungen vorkonfiguriert ist, funktioniert sie am besten mit benutzerspezifischen und Kaufereignissen. Adobe empfiehlt die Implementierung benutzerspezifischer Ereignisse auf Ihrer Site. Wenn Sie benutzerspezifische Ereignisse implementieren, ist für diese Dimension keine zusätzliche Implementierung erforderlich.

## Dimensionselemente

Zu den Dimensionselementen zählen zeitbasierte Behälter von `"Less than 1 minute"` bis `"More than 15 hours"`. Wenn ein Besucher beispielsweise 23 Minuten von seinem ersten Treffer bis zu einem Kauf benötigte, würde er unter das Dimensionselement `"10 to 30 minutes"` fallen. Die Buckets können für diese Metrik nicht angepasst werden.
