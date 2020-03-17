---
description: Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.
title: PDF- oder CSV-Dateien herunterladen
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
translation-type: tm+mt
source-git-commit: 08d564f7fb06b94c2010515ea4a1dcbb2e6e2815

---


# PDF- oder CSV-Dateien herunterladen

Sie können gespeicherte und ungespeicherte Projekte im PDF- oder CSV-Format herunterladen.

Der Name der PDF- oder CSV-Datei entspricht dem aktuellen Projektnamen. Bei ungespeicherten Projekten sind die nicht gespeicherten Änderungen am Projekt in der heruntergeladenen Datei enthalten. Beachten Sie, dass Sie ungespeicherte Projekte im PDF- oder CSV-Format nicht planen können.

Beachten Sie:

* Wir unterstützen auch die Fallout-Visualisierung im CSV-Format.
* Wenn ein Projekt in eine PDF gerendert wird, dann wird nur der Seiteninhalt gerendert. Wenn ein Projekt Visualisierungen und Bedienfelder in benutzerdefinierter Größe enthält, müssen Sie diese so ändern, dass die Größe automatisch bestimmt wird (Schaltfläche in der oberen rechten Ecke), damit der Inhalt nicht abgeschnitten wird.
* Der Export von im Browser heruntergeladenen PDFs kann einige Minuten dauern. Das liegt daran, dass wir das gesamte Projekt auf unseren Servern erneut ausführen müssen, bevor wir es im PDF-Format wiedergeben können. Es wird empfohlen, das Projekt erst dann zu verlassen, wenn die PDF-Datei in Ihrem Browser heruntergeladen wurde. Sie können jedoch weiterhin Änderungen am Projekt vornehmen, während Sie warten.
* Wenn Sie sehr lange Workspace-Projekte haben, werden PDFs derzeit als eine Riesenseite und nicht als paginiertes Dokument exportiert. Wir arbeiten an einer Verbesserung des PDF-Exports von Workspace, die Paginierung ermöglicht.

1. Erstellen oder öffnen Sie ein Projekt.
1. Klicken Sie auf **[!UICONTROL Project]** > **[!UICONTROL Download CSV (or Download PDF).]**

Am 11. April 2019 wurden mehrere Änderungen an **[!CSV Downloads]** (und **[!CIn Zwischenablage kopieren]**) in Analysis Workspace vorgenommen, um die Formatierung aus den exportierten Daten zu entfernen.
* Das Tausendertrennzeichen ist nicht mehr enthalten. (The decimal separator will continue to be included, and will adhere to the format defined under **[!UICONTROL Components > Report Settings > Thousands Separator]**).
* Es werden keine Währungssymbole angezeigt.
* Es werden keine Prozentzeichen angezeigt.
* Prozentsätze sind dezimal; 75 % wird beispielsweise als 0,75 angezeigt.
* Die Zeit wird in Sekunden angezeigt.
* Kohortentabellen zeigen nur Rohwerte an. Prozentwerte wurden entfernt.
* Wenn eine Zahl ungültig ist, wird eine leere Zelle angezeigt.

>[!NHinweis:]
>
> Numerische Werte, die ein Komma als Dezimaltrennzeichen verwenden, werden weiterhin in der exportierten CSV angegeben.
