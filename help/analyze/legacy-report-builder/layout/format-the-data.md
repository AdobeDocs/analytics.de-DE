---
description: Erfahren Sie, wie Sie Standardformatierungen und eingeschränkte Formatierungen auf Zellbereiche anwenden.
title: Formatieren des Datums in Report Builder
uuid: 5211db30-07b3-4413-97c3-e40e6ff223cd
feature: Report Builder
role: User, Admin
exl-id: 9b251b09-9156-40b5-8e1f-fb6594a25c26
TQID: https://experienceleague.adobe.com/8FuosvmSvi-bRNaG5QbwUExuDffOIXbrkuiQLh0NZXM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 22%

---

# Datum formatieren

{{legacy-arb}}

Zusätzlich zu den standardmäßigen Zellformatierungsoptionen, die über die Excel-Funktion Format > Zellen (Strg+1) verfügbar sind, können Sie mit Report Builder eingeschränkte Formatierungen auf Zellbereiche anwenden. Diese Formatierungsoptionen hängen von der gewählten Metrik ab.

Nachdem Sie [Dimensionen](/help/analyze/legacy-report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) zum Raster „Zeilenbezeichnungen“ hinzugefügt haben, klicken Sie auf **[!UICONTROL Format]**.

Klicken Sie im Menü **[!UICONTROL Format]** auf **[!UICONTROL Benutzerdefiniertes Format]**, um ähnlich wie beim Voranstellen oder Anhängen benutzerdefinierte Formate anzuwenden. Sie können beispielsweise Text eingeben, der immer nach dem Datum steht (z. B. A.D. B.C.E. A.H. usw.). Sie können Text vor dem Datum hinzufügen, z. B[!UICONTROL &#x200B; „Startdatum] und [!UICONTROL Start- und Enddatum]. Darüber hinaus können Sie einen benutzerdefinierten Datumsausdruck aus den Abkürzungen für Tag, Monat und Jahr erstellen und ein benutzerdefiniertes Trennzeichen zwischen Teilen des Datums verwenden. Alle Datumsformate dürfen aus drei Abkürzungen bestehen, die nur in Klammern stehen.

In der folgenden Tabelle wird beschrieben, wie Sie Datumsabkürzungen im Feld [!UICONTROL Benutzerdefiniertes Format] verwenden können:

| Abkürzung | Bedeutung | Beispiel mit Mittwoch, 14. März 2012 |
|--- |--- |--- |
| MM/TT/JJJ | Vollständiges numerisches Datum | 03/14/2012 |
| M | Anzahl der Monate | 3 |
| MM | Anzahl der Monate mit 0 Abstand für Monate &lt; 10 | 03 |
| MMM | Kurzname des Monats | Mär |
| MMMM | Langer Name des Monats | März |
| D | Langer Name des Datums | Donnerstag, 14. März 2012 |
| d | Anzahl der Tage | 14 |
| DD | Anzahl der Tage mit Auffüllung 0 für Tage &lt; 10 | 01 - 09 |
| TTT | Kurzname des Tages | Mi |
| TTTT | Langer Name des Tages | Mittwoch |
| JJ | 2-stelliges Jahr | 10 |
| JJJJ | Vollständige 4-stellige Jahreszahl | 2012 |
