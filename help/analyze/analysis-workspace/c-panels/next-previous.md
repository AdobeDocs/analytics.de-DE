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

Dieses Bedienfeld enthält eine Reihe von Tabellen und Visualisierungen, mit denen Sie das nächste oder vorherige Dimensionselement für eine bestimmte Dimension leicht identifizieren können. Vielleicht möchten Sie herausfinden, welche Seiten Kundinnen und Kunden am häufigsten besucht haben, nachdem sie die Startseite besucht haben.

## Zugriff auf das Bedienfeld

Sie können auf das Bedienfeld in [!UICONTROL Berichte] oder in [!UICONTROL Workspace ].

| Zugangspunkt | Beschreibung |
| --- | --- |
| [!UICONTROL Berichte] | <ul><li>Das Bedienfeld ist bereits in einem Projekt abgelegt.</li><li>Die linke Leiste ist reduziert.</li><li>Wenn Sie [!UICONTROL Nächste Seite] ausgewählt haben, wurden bereits Standardeinstellungen angewendet, z. B. [!UICONTROL Seite] für [!UICONTROL Dimension ] und die obere Dimension als [!UICONTROL Seitenelement], [!UICONTROL Weiter] für [!UICONTROL Direction] und [!UICONTROL Visit] für [!UICONTROL Container]. Sie können alle diese Einstellungen ändern.</li></ul>![Bedienfeld „Weiter/Zurück“](assets/next-previous.png) |
| Workspace | Erstellen Sie ein neues Projekt und wählen Sie das Bedienfeldsymbol in der linken Leiste aus. Ziehen Sie dann das Bedienfeld [!UICONTROL Nächstes oder vorheriges Element] über die Freiformtabelle. Beachten Sie, dass die Felder {0]Dimension) und [!UICONTROL Dimension ]Element leer bleiben. [!UICONTROL  Wählen Sie eine Dimension aus der Dropdown-Liste. [!UICONTROL Dimensionen-Elemente] werden basierend auf der ausgewählten [!UICONTROL Dimension] befüllt. Das obere Dimensionselement wird hinzugefügt, Sie können jedoch ein anderes Element auswählen. Die Standardwerte sind „Weiter“ und „Besucher“. Auch diese können geändert werden.<p>![Bedienfeld „Weiter/Zurück“](assets/next-previous2.png) |

{style="table-layout:auto"}

## Panel-Eingaben {#Input}

Sie können das Bedienfeld [!UICONTROL Nächstes oder vorheriges Element] mit den folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
| --- | --- |
| Ablegebereich für Segmente (oder andere Komponenten) | Sie können Segmente oder andere Komponenten per Drag-and-Drop verschieben, um Ihre Bedienfeldergebnisse weiter zu filtern. |
| Dimension | Die Dimension, für die Sie die nächsten oder vorherigen Elemente untersuchen möchten. |
| Dimensionselement | Der spezifische Artikel im Mittelpunkt Ihrer nächsten/vorherigen Anfrage. |
| Richtung | Geben Sie an, ob Sie nach dem Dimensionselement [!UICONTROL Weiter] oder [!UICONTROL Zurück] suchen. |
| Container | [!UICONTROL Besuch] oder [!UICONTROL Besucher] (Standard) bestimmen den Umfang Ihrer Anfrage. |

{style="table-layout:auto"}

Klicken Sie **[!UICONTROL Erstellen]**, um das Bedienfeld zu erstellen.

## Bedienfeldausgabe {#output}

Das Bedienfeld [!UICONTROL Nächstes oder vorheriges Element] gibt einen umfangreichen Satz von Daten und Visualisierungen zurück, damit Sie besser verstehen können, welche Ereignisse bestimmten Dimensionselementen folgen oder vorausgehen.

![Nächste/Vorherige Bedienfeldausgabe](assets/next-previous-output.png)

![Nächste/Vorherige Bedienfeldausgabe](assets/next-previous-output2.png)

| Visualisierung | Beschreibung |
| --- | --- |
| Horizontalbalken | Listet die nächsten (oder vorherigen) Elemente basierend auf dem ausgewählten Dimensionselement auf. Wenn Sie den Mauszeiger über eine einzelne Leiste bewegen, wird das entsprechende Element in der Freiformtabelle hervorgehoben. |
| Zusammenfassungszahl | Allgemeine Zusammenfassung der Anzahl aller nächsten oder vorherigen Dimensionselement-Vorkommen für den aktuellen Monat (bis jetzt). |
| Freiformtabelle | Listet die nächsten (oder vorherigen) Elemente basierend auf dem ausgewählten Dimensionselement in einem Tabellenformat auf. Dies waren beispielsweise die beliebtesten Seiten (nach Vorkommen), zu denen Personen nach (oder vor) der Startseite oder Workspace-Seite gegangen sind. |

{style="table-layout:auto"}
