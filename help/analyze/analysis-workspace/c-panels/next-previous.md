---
description: Ein Bedienfeld, das die nächsten oder vorherigen Dimensionselemente für eine bestimmte Dimension anzeigt.
title: Bedienfeld „Nächstes oder vorheriges Element“
feature: Panels
role: User, Admin
exl-id: 9f2f8134-2a38-42bb-b195-5e5601d33c4e
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 6%

---

# Bedienfeld „Nächstes oder vorheriges Element“

Dieses Bedienfeld enthält eine Reihe von Tabellen und Visualisierungen, um das nächste oder vorherige Dimensionselement für eine bestimmte Dimension einfach zu identifizieren. Sie können beispielsweise untersuchen, welche Seiten Kunden nach dem Besuch der Startseite am häufigsten besucht haben.

## Zugriff auf den Bereich

Sie können über [!UICONTROL Berichte] oder in [!UICONTROL Workspace] auf den Bereich zugreifen.

| Zugangspunkt | Beschreibung |
| --- | --- |
| [!UICONTROL Berichte] | <ul><li>Das Bedienfeld wurde bereits in einem Projekt abgelegt.</li><li>Die linke Leiste ist ausgeblendet.</li><li>Wenn Sie &quot;[!UICONTROL Nächste Seite]&quot;ausgewählt haben, wurden bereits Standardeinstellungen angewendet, wie z. B. [!UICONTROL Dimension] für [!UICONTROL Dimension] und die oberste Seite als [!UICONTROL Seitenelement], [!UICONTROL Weiter] für [!UICONTROL Richtung] und [!UICONTROL Besuch] für [!UICONTROL Container]. Sie können alle diese Einstellungen ändern.</li></ul>![Nächstes/Vorheriges Bedienfeld](assets/next-previous.png) |
| Workspace | Erstellen Sie ein neues Projekt und wählen Sie in der linken Leiste das Bedienfeldsymbol aus. Ziehen Sie dann das Bedienfeld &quot;[!UICONTROL Nächstes oder vorheriges Element]&quot;über die Freiformtabelle. Beachten Sie, dass die Felder [!UICONTROL Dimension] und [!UICONTROL Dimension Element] leer bleiben. Wählen Sie eine Dimension aus der Dropdownliste aus. [!UICONTROL Dimension-Elemente] werden basierend auf der ausgewählten [!UICONTROL Dimension] gefüllt. Das oberste Dimensionselement wird hinzugefügt, Sie können jedoch ein anderes Element auswählen. Die Standardeinstellung ist &quot;Weiter&quot;und &quot;Besucher&quot;. Auch hier können Sie diese ändern.<p>![Nächstes/Vorheriges Bedienfeld](assets/next-previous2.png) |

{style="table-layout:auto"}

## Panel-Eingaben {#Input}

Sie können das Bedienfeld &quot;[!UICONTROL Nächstes oder vorheriges Element]&quot;mithilfe der folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
| --- | --- |
| Dropzone Segment (oder andere Komponente) | Sie können Segmente oder andere Komponenten per Drag-and-Drop verschieben, um die Ergebnisse Ihrer Bedienfelder weiter zu filtern. |
| Dimension | Die Dimension, für die Sie die nächsten oder vorherigen Elemente untersuchen möchten. |
| Dimensionselement | Der spezifische Artikel im Mittelpunkt Ihrer nächsten/vorherigen Anfrage. |
| Richtung | Geben Sie an, ob Sie nach dem Dimensionselement [!UICONTROL Weiter] oder dem Dimensionselement [!UICONTROL Zurück] suchen. |
| Container | [!UICONTROL Besuch] oder [!UICONTROL Besucher] (Standard) bestimmen den Umfang Ihrer Anfrage. |

{style="table-layout:auto"}

Klicken Sie auf **[!UICONTROL Build]** , um das Bedienfeld zu erstellen.

## Bedienfeldausgabe {#output}

Das Bedienfeld [!UICONTROL Nächstes oder vorheriges Element] gibt einen umfangreichen Satz an Daten und Visualisierungen zurück, damit Sie besser verstehen können, welche Vorkommen bestimmten Dimensionselementen folgen oder vorausgehen.

![Nächste/Vorherige Bereichsausgabe](assets/next-previous-output.png)

![Nächste/Vorherige Bereichsausgabe](assets/next-previous-output2.png)

| Visualisierung | Beschreibung |
| --- | --- |
| Horizontalbalken | Führt die nächsten (oder vorherigen) Elemente basierend auf dem ausgewählten Dimensionselement auf. Wenn Sie den Mauszeiger über eine einzelne Leiste bewegen, wird das entsprechende Element in der Freiformtabelle markiert. |
| Zusammenfassungszahl | Allgemeine Zusammenfassungsnummer aller nächsten oder vorherigen Dimensionselementvorkommen für den aktuellen Monat (bisher) |
| Freiformtabelle | Führt die nächsten (oder vorherigen) Elemente basierend auf dem ausgewählten Dimensionselement im Tabellenformat auf. Hierbei handelte es sich beispielsweise um die beliebtesten Seiten (nach Vorfällen), die Besucher nach (oder vor) der Startseite oder Workspace-Seite aufriefen. |

{style="table-layout:auto"}
