---
description: Die Paid-Search-Erkennung unterscheidet in den Berichten zu Suchmaschinen und Suchbegriffen zwischen Paid Searches und organischen Suchvorgängen.
title: Paid-Search-Erkennung
feature: Admin Tools
exl-id: 6b513ad2-f955-4a34-92f8-57a141e44801
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---

# Paid-Search-Erkennung

Die [!UICONTROL Paid-Search-Erkennung] unterscheidet in den Berichten zu [!UICONTROL Suchmaschinen] und [!UICONTROL Suchbegriffen] zwischen Paid Searches und organischen Suchvorgängen. Sie können die Suchmaschinen angeben, in denen Sie kostenpflichtige Werbung verwenden, und eine Zeichenfolge in der URL eines Besuchs bei einer kostenpflichtigen Werbung spezifizieren.

## Konfigurationsoptionen {#configuration}

In der folgenden Tabelle werden die Felder und Optionen beschrieben, die Sie zur [Konfiguration der PaidSearch-Erkennung](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/t-paid-search-detection.md) verwenden.

| Option | Beschreibung |
| --- | --- |
| [!UICONTROL Suchmaschine] | Wählen Sie eine Suchmaschine aus der Dropdown-Liste. Sie geben die Suchmaschine an, wenn Sie unterschiedliche Parameter für die Abfragezeichenfolge in unterschiedlichen Suchmaschinen verwenden. Normalerweise reicht der Wert `Any`. |
| [!UICONTROL Abfragezeichenfolge] | Gibt eine Zeichenfolge für eine Übereinstimmung (unter Berücksichtigung der Groß- und Kleinschreibung) mit einem beliebigen Teil des Abfragezeichenfolgenparameters an, d. h. dem Teil der URL nach dem „?“. <br>**Hinweis**: Bei der [!UICONTROL Paid-Search-Erkennung] wird zwischen Groß- und Kleinschreibung unterschieden. Beispielsweise zeigt eine Regel, die „PID“ als Abfragezeichenfolgenparameter angibt, „pid“ nicht in Berichten an. Wenn Ihre Organisation gemischte Groß- und Kleinschreibung verwendet, geben Sie die exakten Werte als separate Regeln ein, damit alle gewünschten Abfragezeichenfolgenparameter erfasst werden. |
