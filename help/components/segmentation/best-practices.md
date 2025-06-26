---
title: Best Practices für die Segmentierung
description: Erstellen Sie optimale Segmente, die Daten effizient zurückgeben.
feature: Segmentation
exl-id: 4115a804-5063-430a-b9d3-2b64b26ca4d8
source-git-commit: 80e4a3ba4a5985563fcf02acf06997b4592261e4
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 62%

---

# Best Practices für die Segmentierung

Oft sind komplexe Segmente erforderlich, um die gewünschten Daten zu erhalten. Wenn komplexe Segmente ineffizient sind und in einer großen Report Suite verwendet werden, dauert die Ausführung von Berichten erheblich länger. Berücksichtigen Sie beim Erstellen oder Bearbeiten eines Segments die folgenden Ressourcen, um die Komplexität zu minimieren.

## Verwenden Sie den `Contains` Operator nur als letztes Mittel

Der [**[!UICONTROL Enthält &#x200B;]**-Operator](/help/components/segmentation/seg-reference/seg-operators.md) ist eines der verarbeitungsintensivsten Funktionen in der Segmentierung, da der Operator den gesamten Inhalt jedes Werts analysieren muss. Erwägen Sie die Verwendung anderer Operatoren&#x200B;**[!UICONTROL &#x200B; Beginnt mit &#x200B;]**&#x200B;oder&#x200B;**[!UICONTROL &#x200B; Endet mit &#x200B;]**&#x200B;wenn die gewünschten Werte am Anfang oder Ende einer Zeichenfolge sind.

Wenn ein **[!UICONTROL Enthält]**-Operator in einem Segment eine große Anzahl von Ergebnissen zurückgibt, tritt in der Regel eine Zeitüberschreitung des Berichts auf. Wenn Sie beispielsweise ein Segment erstellt haben, in dem **[!UICONTROL Referrer]** **[!UICONTROL gleich]** `"."`, durchsucht das Segment den Inhalt jedes Werts. Verwenden Sie stattdessen den Operator **[!UICONTROL Vorhanden]**.

## Verwenden Sie Klassifizierungen zum Gruppieren von Dimensionselementen.

Wenn Sie viele Segmentbedingungen haben, können diese die Segmentleistung schnell beeinträchtigen. Beispiel: **[!UICONTROL Seite]** **[!UICONTROL gleich]** `X` **[!UICONTROL ODER**&#x200B;[!UICONTROL &#x200B; Seite **&#x200B;**&#x200B;gleich &#x200B;]&#x200B;**&#x200B;**&#x200B;**ODER**&#x200B;**]** Seite **&#x200B;**&#x200B;`Y`gleich`Z` mit Hunderten von verschiedenen Werten wiederholt. Anstatt diese Hunderte von Bedingungen aufzuschreiben, klassifizieren Sie alle gewünschten Werte in ein Segment und verwenden Sie dann den klassifizierten Wert in einem Segment.

1. Erstellen Sie eine Classification für die Variable, mit der Sie arbeiten.
2. Laden Sie die Classification-Vorlage herunter und öffnen Sie sie in der gewünschten Tabelle oder im Texteditor.
3. Weisen Sie jedem Dimensionselement, das Sie in Ihr Segment einbeziehen möchten, denselben Wert zu.
4. Verwenden Sie den Classification Importer, um die Tabelle wieder in Adobe Analytics zu importieren.
5. Nachdem die Classification verarbeitet wurde, erstellen Sie ein Segment mit dem klassifizierten Wert.

Diese Methode erhöht die Leistung drastisch und bietet eine einfache Möglichkeit, Segmentbedingungen zu ändern. Anstatt das Segment mit unterschiedlichen Werten zu bearbeiten, können Sie Dimensionselemente zur Klassifizierung hinzufügen oder daraus entfernen.
