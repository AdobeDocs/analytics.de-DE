---
title: Konsolidierungsprozess für Klassifizierungssätze
description: Der vollständige Prozess der Konsolidierung von Klassifizierungssätzen.
exl-id: f36bcbcb-0ed0-44a7-a6a9-b28fd244fb27
feature: Classifications
source-git-commit: 9f70dbeb9dfe54897915213480f05cbdfaf920ef
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Konsolidierungsprozess für Klassifizierungssätze

Verwenden Sie diese Schnittstelle, um von Anfang bis Ende eine Konsolidierung des Klassifizierungssatzes zu erstellen.

## Erstellung

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Konsolidierung]** > **[!UICONTROL Hinzufügen]**

Beim Erstellen einer Konsolidierung stehen die folgenden Felder zur Verfügung:

* **[!UICONTROL Name]**: Der Name der Konsolidierung.
* **[!UICONTROL Über Probleme benachrichtigen]**: Eine kommagetrennte Liste von E-Mail-Adressen, die über Probleme bei dieser Konsolidierung benachrichtigt werden.
* **[!UICONTROL Datensatz, der mit]** übereinstimmt: Eine Dropdown-Liste aller Classification-Sets.

Nachdem Sie einen Classification-Satz ausgewählt haben, wird eine Tabelle mit zwei Spalten angezeigt:

* Die rechte Spalte enthält alle Classification-Sets, die Sie konsolidieren möchten. Er beginnt mit dem Classification-Satz, der mithilfe der obigen Dropdownliste ausgewählt wurde.
* Die linke Spalte enthält alle Classification-Sets, die für die Zusammenführung mit dem ursprünglich ausgewählten Datensatz infrage kommen. **Schemas müssen genau übereinstimmen, damit sie für die Konsolidierung infrage kommen**. Wenn Schemata nicht mit dem ausgewählten Classification-Satz übereinstimmen, werden sie nicht in dieser linken Spalte angezeigt.

Ziehen Sie die gewünschten Classification-Sets aus der verfügbaren Spalte auf der linken Seite in die Konsolidierungsspalte auf der rechten Seite. Nachdem die Konsolidierung einen Namen erhalten hat und sich zwei oder mehr Classification-Sets in der rechten Spalte befinden, klicken Sie auf **[!UICONTROL Speichern und fortfahren]**.

## Validierung

Nachdem Sie eine Konsolidierung erstellt haben, wird rechts eine Liste der Quelldatensätze angezeigt. Die Schaltfläche **[!UICONTROL Validieren]** stellt sicher, dass jeder einzelne Classification-Satz für diese Konsolidierung gültig ist. Sie können die Classification-Schritte hier neu anordnen, um die Priorität bei nicht übereinstimmenden Classification-Werten zu bestimmen. **Der höchste Classification-Satz in der Liste überschreibt alle nicht übereinstimmenden Werte in anderen Classification-Sets.**

## Ausführen

Nachdem eine Konsolidierung validiert wurde, können Sie sie ausführen. Das Ausführen einer Konsolidierung bietet einen Ähnlichkeitsbericht mit den folgenden Tabellenspalten:

* **[!UICONTROL Datensatzname]**: Der Name des Classification-Sets.
* **[!UICONTROL Abweichung]**: Der Prozentsatz der Zeilen, in denen Schlüsselwerte nicht mit dem Quell-Classification-Satz übereinstimmten. Wenn der Prozentsatz der Abweichungen hoch ist, können die Classification-Daten zu unterschiedlich sein. Überprüfen Sie, ob die ausgewählten Classification-Sets ähnliche Classification-Daten aufweisen.
* **[!UICONTROL Abwesend]**: Der Prozentsatz der Zeilen, in denen Schlüsselwerte in diesem Classification-Satz waren, aber nicht im Quell-Classification-Satz. Alle fehlenden Zeilen werden zum konsolidierten Classification-Satz hinzugefügt.

## Genehmigen

fungiert als letzter Aufruf, bevor die einzelnen Classification-Sets entfernt und ein konsolidierter Classification-Satz erstellt wird. Vergewissern Sie sich, dass alles korrekt ist, und klicken Sie dann auf **[!UICONTROL Genehmigen]**.

Nach der Genehmigung wird der konsolidierte Classification-Satz erstellt. Der Status ist auf [!UICONTROL Abgeschlossen] festgelegt, und für die Konsolidierung ist keine weitere Aktion erforderlich.
