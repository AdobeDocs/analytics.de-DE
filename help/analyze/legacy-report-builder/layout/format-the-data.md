---
description: Erfahren Sie, wie Sie Standardformatierungen und eingeschränkte Formatierungen auf Zellbereiche anwenden.
title: Formatieren des Datums im Report Builder
uuid: 5211db30-07b3-4413-97c3-e40e6ff223cd
feature: Report Builder
role: User, Admin
exl-id: 9b251b09-9156-40b5-8e1f-fb6594a25c26
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 81%

---

# Datum formatieren

{{legacy-arb}}

Zusätzlich zu den standardmäßigen Zellformatierungsoptionen, die über die Excel-Funktion Format > Zellen (Strg+1) verfügbar sind, können Sie für Zellbereiche mit Report Builder eine eingeschränkte Formatierung anwenden. Die möglichen Formatierungen hängen von der gewählten Metrik ab.

Nachdem Sie [Dimensionen](/help/analyze/legacy-report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) zum Raster „Zeilenbezeichnungen“ hinzugefügt haben, klicken Sie auf **[!UICONTROL Format]**.

Klicken Sie im Menü **[!UICONTROL Format]** auf **[!UICONTROL Benutzerdefiniertes Format]**, um ähnlich wie beim Voranstellen oder Anhängen benutzerdefinierte Formate anzuwenden. Beispielsweise können Sie Text eingeben, der immer nach dem Datum angezeigt werden soll (z. B. „A.D.“, „B.C.E.“, „A.H.“ usw.). Sie können Text vor dem Datum einfügen, z. B. [!UICONTROL Startdatum] und [!UICONTROL Start- und Enddatum]. Darüber hinaus können Sie einen eigenen Datumsausdruck mit Hilfe von Abkürzungen für Tag, Monat und Jahr erstellen und benutzerdefinierte Trennzeichen zwischen den Datumsbestandteilen verwenden. Alle Datumsformate müssen aus drei Abkürzungen bestehen, die nur in Klammern eingeschlossen werden dürfen.

In der folgenden Tabelle wird beschrieben, wie Datumsabkürzungen im Feld [!UICONTROL Benutzerdefiniertes Format] verwendet werden können:

| Abkürzung | Bedeutung | Beispiel   mit Mittwoch, 14. März 2012 |
|--- |--- |--- |
| MM/TT/JJJ | Volles numerisches Datum | 03/14/2012 |
| M | Monatsnummer | 3 |
| MM | Monatsnummer mit vorangestellter 0 für Monate &lt; 10 | 03 |
| MMM | Kurzname des Monats | Mär |
| MMMM | Langname des Monats | März |
| D | Langname des Datums | Donnerstag, 14. März 2012 |
| d | Tagesnummer | 14 |
| dd | Tagesnummer mit vorangestellter 0 für Tage &lt; 10 | 01 - 09 |
| TTT | Kurzname des Tages | Mit |
| TTTT | Langname des Tags | Mittwoch |
| yy | Jahr (zweistellig) | 10 |
| JJJJ | Jahr (vierstellig) | 2012 |
