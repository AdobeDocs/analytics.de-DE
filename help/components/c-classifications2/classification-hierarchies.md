---
description: Auf der Seite „Classification-Hierarchien“ können Sie Classification-Hierarchien definieren, auf deren Grundlage sie Hierarchieberichte mit dem gleichen Namen erstellen können.
seo-description: Auf der Seite „Classification-Hierarchien“ können Sie Classification-Hierarchien definieren, auf deren Grundlage sie Hierarchieberichte mit dem gleichen Namen erstellen können.
seo-title: Klassifizierungshierarchien
solution: Analytics
subtopic: Classifications
title: Klassifizierungshierarchien
topic: Admin Tools
uuid: 1b2b73af-84ea-4b90-b4a5-ba75235547fb
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Klassifizierungshierarchien

Auf der Seite „Classification-Hierarchien“ können Sie Classification-Hierarchien definieren, auf deren Grundlage sie Hierarchieberichte mit dem gleichen Namen erstellen können.

## Klassifizierungshierarchien {#concept_10A956342D7D4C3E9114CCFCE1364741}

Auf der Seite [!UICONTROL Classification-Hierarchien] können Sie Classification-Hierarchien definieren, auf deren Grundlage Sie [!UICONTROL Hierarchie]-Berichte mit dem gleichen Namen erstellen können.

In einem [!UICONTROL Hierarchie]-Bericht können Sie gestützt auf die Classification-Hierarchie ein Drilldown zu differenzierteren Datensätzen durchführen, um Datenbeziehungen leichter anzuzeigen.

Sie können Classification-Hierarchien für Webseiten, Kampagnen, Produkte oder beliebige andere Berichtsvariablen erstellen. Im Hierarchiebericht werden Einheiten, Bestellungen und Umsatz für jede Variablen-Classification in der Hierarchie angezeigt.

Angenommen, eine Produkthierarchie sieht wie folgt aus: Bekleidung &gt; Herrenbekleidung &gt; Hemden &gt; Polohemden &gt; XL-Polohemden. In diesem Fall werden im Hierarchiebericht Vertriebsdaten für die Classification „Bekleidung“ angezeigt. Anschließend können Sie per Drilldown weitere Informationen zu Herrenbekleidung, Hemden, Polohemden und XL-Polohemden abrufen. Durch die Classification-Hierarchie können Sie schnell feststellen, wie jede der Classifications in der Hierarchie zur Performance der Classification „Bekleidung“ beiträgt.

Erstellen Sie die Classifications, bevor Sie sie einer Hierarchie hinzufügen.

## Create a Classification Hierarchy {#task_3805EBCACC844261A7125D63D772CCDF}

<!-- 

t_classification_heirarchy.xml

 -->

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**.
1. Report Suite auswählen.
1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Conversion]** &gt; **[!UICONTROL Classification Hierarchies]**.
1. Wählen Sie in der Dropdownliste **Hierarchieaufbau für** die Variable aus, in der Sie eine Klassifizierungshierarchie erstellen möchten.

   In der Classification-List werden die verfügbaren Classifications für die ausgewählte Variable automatisch angezeigt.
1. Ziehen Sie eine Klassifizierung in das Feld **Neue Hierarchie-Root hierher ziehen**, um sie in die Klassifizierungshierarchie aufzunehmen.

   Ziehen Sie die Classifications in der Reihenfolge in die Hierarchie, in der sie angezeigt werden sollen. Die erste Classification bildet den Hierarchiestamm, die zweite Classification ist die erste Unter-Classification und so weiter.
1. Klicken Sie auf **[!UICONTROL Speichern]**.
