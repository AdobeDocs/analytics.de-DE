---
description: Erfahren Sie, wie die Sortierung nach Metrik die Interpretation und den Vergleich von Data Warehouse-Berichten mit anderen Analytics-Aufschlüsselungsansichten erleichtert.
title: Nach Metrik sortieren
feature: Data Warehouse
exl-id: 6bd82951-c3b4-4ba2-8e4d-b7c9b351911b
TQID: https://experienceleague.adobe.com/YPqL6i9RWACubLdf2ywm8xuPyeQkZ30L6rO6FAbhpJI
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 21%

---

# Nach Metrik sortieren

Bietet nach Rang geordnet Detailberichte in Data Warehouse, die nach absteigendem Metrikwert sortiert sind.

Die Sortierung nach Metrik erleichtert die Interpretation von Data Warehouse-Berichten und die Vergleichbarkeit dieser Berichte mit anderen Analytics-Aufschlüsselungs-Reporting-Ansichten.

Im Folgenden wird gezeigt, wie bei Aktivierung der Option „Metriken sortieren“ die Zeilen in einem Data Warehouse-Bericht neu angeordnet werden.

Es gibt vier mögliche Methoden, Data Warehouse-Berichte mit „Metriken sortieren“ zu organisieren, je nachdem, wie Datumsgranularität, Berichtsdimensionen oder Metriken konfiguriert sind und ob „Maximale Zeilen“ festgelegt ist:

* **Layout 1**: Zeileneinträge werden in der Reihenfolge des Wörterbuchs sortiert (Standard). Wenn „Max. Zeilen“ festgelegt ist, werden nur die ersten N Zeilen im Bericht bereitgestellt.
* **Layout 2**: Data Warehouse wendet eine Metriksortierung auf alle Zeilen im Bericht an. Die Verbindungen im ersten Metrikwert werden durch die zweite Metrik unterbrochen, dann durch die dritte und so weiter. Wenn alle Metriken verknüpft sind, wird die standardmäßige Wörterbuchreihenfolge der Aufschlüsselungszeilenelemente angewendet.
* **Layout 3**: Wie Layout 2, wobei nur die obersten N Zeilen (d. h. die in „Max. Zeilen“ festgelegte Zahl) im Bericht ausgegeben werden.
* **Layout 4**: Als Layout 2, mit der Ausnahme, dass Zeilenelemente für jeden Datumsgranularitätzeitraum gruppiert und innerhalb dieses entsprechenden Zeitbereichs sortiert werden.

Die Spalte „Berichtslayout“ in dieser Tabelle sollte herangezogen werden, um zu bestimmen, wie „Metriksortierung“ mit anderen Data Warehouse-Berichtsoptionen interagiert.

| Nach Metrik sortieren? | Hat Metriken? | Hat Pannen? | Datumsgranularität? | Max. Zeilen festgelegt? | Bericht-Layout |
|---|---|---|---|---|---|
| Nein | Ja oder Nein | Ja oder Nein | Ja oder Nein | Ja oder Nein | 1 |
| Ja | Nein | Ja oder Nein | Ja oder Nein | Ja oder Nein | 1 |
| Ja | Ja | Nein | Nein | nicht angegeben | 1 |
| Ja | Ja | Nein | Ja oder Nein | Nein | 1 |
| Ja | Ja | Ja | Nein | Nein | 2 |
| Ja | Ja | Nein | Ja | Ja | 3 |
| Ja | Ja | Ja | Ja oder Nein | Ja | 3 |
| Ja | Ja | Ja | Ja | Nein | 4 |
