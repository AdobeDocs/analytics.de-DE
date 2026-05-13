---
title: Dynamische und statische Dimension-Elemente
description: Erfahren Sie, wie Sie dynamische und statische Dimensionselemente in Freiformtabellen in Analysis Workspace verwenden.
feature: Freeform Tables
role: User, Admin
exl-id: 4cdc93b5-67ed-46a4-ba9f-a96e640da9d9
TQID: https://experienceleague.adobe.com/hP5X4gRBiRB1wmGziYT25iGS-Enpuu0C--3qeGxrvb4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: dcae653e-62c6-4cc8-84e6-ee110b848296
  - id: e318d41c-1d01-4c1e-9b18-1f61d435ceee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 80%

---

# Dynamische und statische Dimensionselemente

In Freiformtabellen können die Zeilen und Spalten verschiedene Komponentenwerte enthalten. Diese Werte können abhängig von der Analyse, die Sie erstellen möchten, dynamisch (zeitabhängig) oder statisch (nicht zeitabhängig) sein.

## Dynamische Dimensionselemente

Dynamische Dimensionselemente ändern sich mit der Zeit und hängen von der Metrik ab, nach der in der Freiformtabelle sortiert wird. Dynamische Dimensionselemente werden bevorzugt, wenn Sie die obersten Elemente für einen bestimmten Zeitraum analysieren möchten.

Wenn Sie eine Dimension in eine Freiform-Tabelle ablegen, werden dynamische Zeilen zurückgegeben. Dynamische Zeilen stellen die obersten Elemente dar, die der Dimension für eine bestimmte Metrik und einen bestimmten Zeitraum entsprechen. Sie können eine Dimension auch in Freiform-Tabellenspalten ablegen, und die Dimension wird automatisch in die fünf obersten Dimensionselemente erweitert.

Wenn Sie beispielsweise die Dimension „Browsertyp“ in die Tabelle ziehen, werden die Dimensionselemente für den oberen Browser-Typ (z. B. Microsoft, Apple, Google usw.) Dynamische Rückkehr zu den Tabellenzeilen. Wenn sie in eine Spalte abgelegt wurde, werden die obersten 5 Dimensionselemente des Browser-Typs dynamisch zurückgegeben.

Dynamische Dimensionselemente verfügen über die Zeilenfilteroption ![Filter](/help/assets/icons/Filter.svg) und ein ![Schließen](/help/assets/icons/Close.svg) und **nicht** eine Sperre ![LockClosed](/help/assets/icons/LockClosed.svg). <!--do they have the lock icon? --> Wenn Sie ![Schließen](/help/assets/icons/Close.svg) neben einem dynamischen Dimensionselement klicken, wird automatisch ein Filter angewendet. Weitere Informationen zum Anwenden von Filtern auf Tabellen finden Sie unter [Filtern und Sortieren von Tabellen](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).


![Eine Freiformtabelle mit hervorgehobenem Filtersymbol.](assets/dynamic-items.png)

## Statische Dimensionselemente

Statische Dimensionselemente ändern sich nicht mit der Zeit. Es handelt sich dabei um feste Komponenten, die immer in einer Freiform-Tabelle zurückgegeben werden. Statische Dimensionselemente werden bevorzugt, wenn Sie immer dasselbe Element analysieren möchten, unabhängig davon, ob es sich um bestimmte Kampagnen oder bestimmte Wochentage handelt.

Jedes Mal, wenn Sie bestimmte Komponentenwerte (Dimension, Metrik, Filter, Datumsbereich) manuell in eine Tabelle eingeben, ist das Ergebnis eine statische Liste von Zeilen oder Spalten.

Wenn Sie beispielsweise über bestimmte Browser-Typ-Elemente wie „Microsoft“ und „Apple“ ziehen, werden diese beiden Elemente immer in die Tabelle gezogen.

Statische Dimensionselemente können auch erstellt werden, wenn Sie **[!UICONTROL Nur ausgewählte Zeilen anzeigen]** aus dem Kontextmenü für ausgewählte Zeilen auswählen.

Statische Dimensionselemente verfügen **nicht** über die Zeilenfilteroption. Stattdessen sind für jedes Element ![LockClosed](/help/assets/icons/LockClosed.svg) und ![Close](/help/assets/icons/Close.svg) vorhanden. Wählen Sie ![Close](/help/assets/icons/Close.svg) aus, um dieses Dimensionselement aus der Tabelle zu entfernen.

![Eine Freiformtabelle mit dem Browser-Typ und der Microsoft-Zeile mit einem Sperrsymbol. Hinweis: Dieses Dimensionselement ist statisch und ändert sich nicht mit der Zeit.](assets/static-items.png)

## Gemischte Dimensionselemente

Dimensionselemente aus verschiedenen Dimensionen können derselben Tabelle hinzugefügt werden. In diesen Fällen steht in der Kopfzeile der Zeile **[!UICONTROL Gemischte Dimensionen]**. Diese Dimensionselemente sind statisch. Fügen Sie beispielsweise bestimmte Dimensionselemente aus der Dimension „Browser-Gruppe“ und andere Dimensionselemente aus der Dimension „Browser-Name“ hinzu.

![Eine Freiformtabelle mit hervorgehobener Spalte mit den gemischten Dimensionen.](assets/mixed-dimensions.png)

## Freiform-Gesamtzeilen

Dynamische und statische Zeilen verhalten sich in der Freiform-Gesamtzeile unterschiedlich. Standardmäßig:

* Dynamische Zeilen werden Server-seitig summiert und deduplizieren Metriken wie „Sitzungen“ oder „Personen“.
* Statische Zeilen werden Client-seitig summiert und deduplizieren **keine** Metriken. Um die Gesamtzeile Server-seitig zu berechnen, ändern Sie die Zeileneinstellung auf **Gesamtsumme anzeigen**. [Weitere Informationen](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md)


>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Neuanordnen von statischen Zeilen](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/reordering-static-rows-in-analysis-workspace){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]


