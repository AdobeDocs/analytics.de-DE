---
title: Konsolidierungsprozess für Klassifizierungssatz
description: Der vollständige Prozess der Konsolidierung von Klassifizierungssätzen.
exl-id: f36bcbcb-0ed0-44a7-a6a9-b28fd244fb27
feature: Classifications
source-git-commit: 828f41bf45c1954c3b68ad71a7746e24626b9eed
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# Konsolidierungsprozess für Klassifizierungssatz

Klassifizierungskonsolidierungen ermöglichen es Ihnen, Klassifizierungen aus mehreren Datensätzen zu nehmen und zu einem zusammenzufassen. Verwenden Sie diese Schnittstelle, um eine Klassifizierungssatz-Konsolidierung von Anfang bis Ende zu erstellen. Diese Benutzeroberfläche ist besonders nützlich für Unternehmen, die von einer veralteten Klassifizierungsarchitektur zu einer Klassifizierungssatz-Architektur wechseln. Die meisten Unternehmen, die bereits eine Klassifizierungssatz-Architektur verwenden, müssen diesen Konsolidierungs-Workflow normalerweise nicht verwenden.

## Erstellung

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Konsolidierungen]** > **[!UICONTROL Hinzufügen]**

Beim Erstellen einer Konsolidierung stehen die folgenden Felder zur Verfügung:

* **[!UICONTROL Name]**: Der Name der Konsolidierung.
* **[!UICONTROL Über Probleme informieren]**: Eine kommagetrennte Liste von E-Mail-Adressen, die bei Problemen mit dieser Konsolidierung benachrichtigt werden.
* **[!UICONTROL Abzugleichender Datensatz]**: Eine Dropdown-Liste aller Klassifizierungssätze.

Nachdem Sie einen Klassifizierungssatz ausgewählt haben, wird eine Tabelle mit zwei Spalten angezeigt:

* Die rechte Spalte enthält alle Klassifizierungssätze, die Sie konsolidieren möchten. Sie beginnt mit dem Klassifizierungssatz, der mithilfe der obigen Dropdown-Liste ausgewählt wurde.
* Die linke Spalte enthält alle Klassifizierungssätze, die mit dem ursprünglich ausgewählten Datensatz zusammengeführt werden können. **Schemata müssen genau übereinstimmen, damit sie konsolidiert werden können**. Wenn Schemata nicht mit dem ausgewählten Klassifizierungssatz übereinstimmen, werden sie nicht in dieser linken Spalte angezeigt.

Ziehen Sie die gewünschten Klassifizierungssätze aus der verfügbaren Spalte links in die Konsolidierungsspalte auf der rechten Seite. Sobald der Konsolidierung ein Name zugewiesen wurde und sich zwei oder mehr Klassifizierungssätze in der rechten Spalte befinden, klicken Sie auf **[!UICONTROL Speichern und fortfahren]**.

## Validierung

Nachdem Sie eine Konsolidierung erstellt haben, wird rechts eine Liste der Quelldatensätze angezeigt. Mit **[!UICONTROL Schaltfläche &quot;]**&quot; wird sichergestellt, dass jeder einzelne Klassifizierungssatz für diese Konsolidierung gültig ist. Sie können die Classification-Schritte hier neu anordnen, um die Priorität im Fall von nicht übereinstimmenden Classification-Werten zu bestimmen. **Der höchste Klassifizierungssatz in der Liste überschreibt alle nicht übereinstimmenden Werte in anderen Klassifizierungssätzen.**

## Ausführen

Nachdem eine Konsolidierung validiert wurde, können Sie sie ausführen. Die Ausführung einer Konsolidierung liefert einen Ähnlichkeitsbericht mit den folgenden Tabellenspalten:

* **[!UICONTROL Datensatzname]**: Der Name des Klassifizierungssatzes.
* **[!UICONTROL Nicht]**: Der Prozentsatz der Zeilen, bei denen die Schlüsselwerte nicht mit dem Quellklassifizierungssatz übereinstimmten. Wenn der Prozentsatz der nicht übereinstimmenden Elemente hoch ist, können die Klassifizierungsdaten zu unterschiedlich sein. Überprüfen Sie, ob die ausgewählten Klassifizierungssätze ähnliche Klassifizierungsdaten aufweisen.
* **[!UICONTROL Absent]**: Der Prozentsatz der Zeilen, in denen sich Schlüsselwerte in diesem Klassifizierungssatz, aber nicht im Quellklassifizierungssatz befanden. Alle fehlenden Zeilen werden dem konsolidierten Klassifizierungssatz hinzugefügt.

## Genehmigen

Der letzte Aufruf, bevor einzelne Klassifizierungssätze entfernt und durch einen konsolidierten Klassifizierungssatz ersetzt werden. Überprüfen Sie, ob alles korrekt ist, und wählen Sie dann **[!UICONTROL Genehmigen]** aus.

Nach der Genehmigung wird der konsolidierte Klassifizierungssatz erstellt. Der Status ist auf [!UICONTROL Abgeschlossen] festgelegt, und es sind keine weiteren Maßnahmen für die Konsolidierung erforderlich.
