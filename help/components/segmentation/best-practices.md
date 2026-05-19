---
title: Best Practices
description: Lernen Sie einige Best Practices für die Segmentierung kennen.
feature: Segmentation
exl-id: 4115a804-5063-430a-b9d3-2b64b26ca4d8
TQID: https://experienceleague.adobe.com/PJi-kkv6HL3jHEKArltzxMGk9BVtZ-Mr1ivHMkhxt88
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 304
ht-degree: 60%

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
