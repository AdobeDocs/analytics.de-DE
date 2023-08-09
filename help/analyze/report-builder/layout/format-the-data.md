---
description: Erfahren Sie, wie Sie eine standardmäßige und eingeschränkte Formatierung auf Zellbereiche anwenden.
title: Formatieren des Datums in Report Builder
uuid: 5211db30-07b3-4413-97c3-e40e6ff223cd
feature: Report Builder
role: User, Admin
exl-id: 9b251b09-9156-40b5-8e1f-fb6594a25c26
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 80%

---

# Datum formatieren

Zusätzlich zu den in Excel über Format > Zellen formatieren (Strg+1) verfügbaren Standard-Zellformatierungsoptionen können Sie bestimmte Formatierungen auf Zellbereiche mit Report Builder anwenden. Die möglichen Formatierungen hängen von der gewählten Metrik ab.

Nachdem Sie [Dimensionen](/help/analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) zum Raster „Zeilenbezeichnungen“ hinzugefügt haben, klicken Sie auf **[!UICONTROL Format]**.

Klicken Sie im Menü **[!UICONTROL Format]** auf **[!UICONTROL Benutzerdefiniertes Format]**, um ähnlich wie beim Voranstellen oder Anhängen benutzerdefinierte Formate anzuwenden. Beispielsweise können Sie Text eingeben, der immer nach dem Datum angezeigt werden soll (z. B. „A.D.“, „B.C.E.“, „A.H.“ usw.). Sie können Text vor dem Datum einfügen, z. B. [!UICONTROL Startdatum] und [!UICONTROL Start- und Enddatum]. Darüber hinaus können Sie einen eigenen Datumsausdruck mit Hilfe von Abkürzungen für Tag, Monat und Jahr erstellen und benutzerdefinierte Trennzeichen zwischen den Datumsbestandteilen verwenden. Alle Datumsformate müssen aus drei Abkürzungen bestehen, die nur in Klammern eingeschlossen werden dürfen.

In der folgenden Tabelle wird beschrieben, wie Datumsabkürzungen im Feld [!UICONTROL Benutzerdefiniertes Format] verwendet werden können:

| Abkürzung | Bedeutung | Beispiel mit Mittwoch, 14. März 2012 |
|--- |--- |--- |
| MM/TT/JJJ | Volles numerisches Datum | 03/14/2012 |
| M | Monatsnummer | 3 |
| MM | Monatsnummer mit vorangestellter 0 für Monate &lt; 10 | 03 |
| MMM | Kurzname des Monats | Mär |
| MMMM | Langname des Monats | März |
| D | Langname des Datums | Mittwoch, 14. März 2012 |
| d | Tagesnummer | 14 |
| dd | Tagesnummer mit vorangestellter 0 für Tage &lt; 10 | 01 - 09 |
| TTT | Kurzname des Tages | Mit |
| TTTT | Langname des Tags | Mittwoch |
| yy | Jahr (zweistellig) | 10 |
| JJJJ | Jahr (vierstellig) | 2012 |
