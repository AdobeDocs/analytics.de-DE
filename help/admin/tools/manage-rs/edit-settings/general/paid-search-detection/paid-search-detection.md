---
description: Die Paid-Search-Erkennung unterscheidet in den Berichten zu Suchmaschinen und Suchbegriffen zwischen Paid Searches und organischen Suchvorgängen.
title: Paid-Search-Erkennung
feature: Admin Tools
exl-id: 6b513ad2-f955-4a34-92f8-57a141e44801
TQID: https://experienceleague.adobe.com/g26-86nQZ-k3kaID-Dq6qbwYkdqLpHDdUEswP-p361Y
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 187
ht-degree: 91%

---

# Paid-Search-Erkennung

Die [!UICONTROL Paid-Search-Erkennung] unterscheidet in den Berichten zu [!UICONTROL Suchmaschinen] und [!UICONTROL Suchbegriffen] zwischen Paid Searches und organischen Suchvorgängen. Sie können die Suchmaschinen angeben, in denen Sie kostenpflichtige Werbung verwenden, und eine Zeichenfolge in der URL eines Besuchs bei einer kostenpflichtigen Werbung spezifizieren.

## Konfigurationsoptionen {#configuration}

In der folgenden Tabelle werden die Felder und Optionen beschrieben, die Sie zur [Konfiguration der PaidSearch-Erkennung](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/t-paid-search-detection.md) verwenden.

| Option | Beschreibung |
| --- | --- |
| [!UICONTROL Suchmaschine] | Wählen Sie eine Suchmaschine aus der Dropdown-Liste. Sie geben die Engine an, wenn Sie für verschiedene Suchmaschinen unterschiedliche Abfragezeichenfolgen-Parameter verwenden. Normalerweise reicht der Wert `Any`. |
| [!UICONTROL Abfragezeichenfolge] | Gibt eine Zeichenfolge für eine Übereinstimmung (unter Berücksichtigung der Groß- und Kleinschreibung) mit einem beliebigen Teil des Abfragezeichenfolgenparameters an, d. h. dem Teil der URL nach dem „?“. <br>**Hinweis**: Bei der [!UICONTROL Paid-Search-Erkennung] wird zwischen Groß- und Kleinschreibung unterschieden. Beispielsweise zeigt eine Regel, die „PID“ als Abfragezeichenfolgenparameter angibt, „pid“ nicht in Berichten an. Wenn Ihre Organisation gemischte Groß- und Kleinschreibung verwendet, geben Sie die exakten Werte als separate Regeln ein, damit alle gewünschten Abfragezeichenfolgenparameter erfasst werden. |
