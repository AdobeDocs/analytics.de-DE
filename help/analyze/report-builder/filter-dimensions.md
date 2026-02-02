---
title: Filtern von Dimensionen in Report Builder
description: Erfahren Sie, wie Sie Dimensionen in Report Builder filtern.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 43f48abf-951d-4fd1-afd4-58304ee5247b
source-git-commit: ba4fe682d717e8a90d87eaa5244a269f49a4a00a
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 34%

---

# Dimensionen filtern


Standardmäßig gibt jedes Dimensionselement in der Tabelle die 10 wichtigsten Elemente für diese Dimension zurück.

So ändern Sie die für jede Dimension zurückgegebenen Dimensionselemente:

1. Eine Zelle im Datenblock auswählen.

1. Wählen ![Bearbeiten](/help/assets/icons/Edit.svg) **[!UICONTROL Datenblock bearbeiten]** im Bedienfeld **[!UICONTROL Befehle]** aus.

1. Wählen Sie **[!UICONTROL Weiter]** aus, um die Registerkarte **[!UICONTROL Dimensionen]** anzuzeigen.

1. Wählen Sie ![MehrKlein](/help/assets/icons/MoreSmall.svg) neben einem Komponentennamen in der Tabelle aus.

   ![Optionen für das Symbol mit den Auslassungspunkten.](./assets/image27.png){zoomable="yes"}

1. Wählen **[!UICONTROL Filterdimension]** im Popup-Menü aus, um den Bereich **[!UICONTROL Filterdimension]** anzuzeigen.

1. Wählen Sie **Am beliebtesten** oder **Spezifisch** als **[!UICONTROL Typ]**.

   ![Die im Bereich „Filterdimension“ ausgewählte spezifische Option.](./assets/image28.png){zoomable="yes"}

1. Wählen Sie je nach ausgewähltem [Filtertyp](#filter-type) die entsprechenden Optionen aus.

1. Wählen Sie **[!UICONTROL Anwenden]** aus, um den Filter hinzuzufügen.

1. Report Builder zeigt eine Benachrichtigung zur Bestätigung des hinzugefügten Filters an.

Um angewendete Filter anzuzeigen, bewegen Sie den Mauszeiger über eine Dimension. Dimensionen mit angewendeten Filtern zeigen ![&#x200B; Filtersymbol &#x200B;](/help/assets/icons/Filter.svg)Filter) neben dem Dimensionsnamen an.

## Filter und Sortierreihenfolge ändern

Neben ![&#x200B; Metrik, die zum Filtern &#x200B;](/help/assets/icons/ArrowUp.svg) Sortieren des Datenblocks verwendet ![, wird ein „ArrowUp“ oder &#x200B;](/help/assets/icons/ArrowDown.svg)ArrowDown“ angezeigt. Die Pfeilrichtung gibt an, ob die Metrik in auf- oder absteigender Reihenfolge sortiert wird.

Sortierreihenfolge ändern:

- Wählen Sie ![ArrowUp](/help/assets/icons/ArrowUp.svg) oder ![ArrowDown](/help/assets/icons/ArrowDown.svg) neben der Metrik aus, um die Sortierreihenfolge umzuschalten.

So ändern Sie die zum Filtern und Sortieren des Datenblocks verwendete Metrik:

1. Bewegen Sie den Mauszeiger über die gewünschte Metrikkomponente im Tabellen-Builder, um zusätzliche Optionen anzuzeigen.

2. Wählen Sie ![&#x200B; bevorzugte Metrik &#x200B;](/help/assets/icons/ArrowDown.svg)ArrowDown) aus.

   ![Der Tabellen-Builder und die Metriken.](./assets/image30.png){zoomable="yes"}



## Filtertyp

Es gibt zwei Möglichkeiten, Dimensionselemente zu filtern: [Am beliebtesten](#most-popular) und [Spezifisch](#specific-filtering)

### **[!UICONTROL Am beliebtesten]**

Mit **[!UICONTROL Option]** Am beliebtesten“ können Sie Dimensionselemente basierend auf Metrikwerten dynamisch filtern. „Am beliebtesten“ gibt die am höchsten bewerteten Dimensionselemente basierend auf Metrikwerten zurück. Standardmäßig werden die ersten 10 Dimensionselemente aufgelistet, sortiert nach der ersten Metrik, die zum Datenblock hinzugefügt wurde.

![Die beliebteste Option.](./assets/image29.png){zoomable="yes"}


#### Seiten- und Zeilenoptionen

Verwenden Sie die Felder **[!UICONTROL Seite]** und **[!UICONTROL Zeilen]**, um Daten in sequenzielle Gruppen oder Seiten zu unterteilen. Mit dieser Funktion können Sie andere Rangzeilenwerte als die höchsten Werte in Ihren Bericht ziehen. Und ist besonders nützlich, um Daten über die Zeilenbegrenzung von 50.000 hinaus abzurufen.

Der Standardwert für Seite ist `1` und für Zeilen ist `10`. Diese Standardwerte implizieren, dass jede Seite 10 Datenzeilen enthält. Seite 1 gibt die 10 wichtigsten Elemente zurück, Seite 2 die nächsten 10 Elemente usw.

In der folgenden Tabelle finden Sie Beispiele für Seiten- und Zeilenwerte sowie die resultierende Ausgabe.

| Seite | Zeile  | Ausgabe |
|------|--------|----------------------|
| 1 | 10 | Die 10 beliebtesten Elemente |
| 2 | 10 | Elemente 11-20 |
| 1 | 100 | Die 100 beliebtesten Elemente |
| 2 | 100 | Elemente 101-200 |
| 2 | 50.000 | Elemente 50.001-100.000 |

In der folgenden Tabelle sind die Mindest- und Höchstwerte für Seiten und Zeilen aufgeführt.

|       | Mindestwerte | Maximale Werte |
|-------|---------------:|---------------:|
| Start Seite | 1 | 50 Million |
| Anzahl Zeilen | 1 | 50.000 |


#### „Kein Wert“ einschließen

In Customer Journey Analytics erfassen einige Dimensionen den Eintrag *Kein Wert*. Mit **[!UICONTROL Einstellung „Kein Wert]**&quot; können Sie diese Werte aus Berichten ausschließen. Sie können beispielsweise eine Klassifizierung wie die Klassifizierung „Produktname“ basierend auf dem Produkt-SKU-Schlüssel erstellen. Wenn eine bestimmte Produkt-SKU nicht mit ihrer spezifischen Produktnamenklassifizierung eingerichtet wurde, wird ihr Produktnamenwert auf &quot;*Wert“*.

**[!UICONTROL Einschließen von „Kein Wert]** ist standardmäßig ausgewählt. Deaktivieren Sie diese Option, um Einträge ohne Wert auszuschließen.

#### Nach Kriterien filtern

Sie können Dimensionselemente danach filtern, ob alle Kriterien erfüllt sind oder ob überhaupt Kriterium erfüllt ist.

So legen Sie Filterkriterien fest:

1. Wählen Sie im Dropdown-Menü Operator einen Operator aus. Standardmäßig ist **[!UICONTROL Enthält den]**) ausgewählt

   ![Die Benutzerliste.](./assets/image31.png){zoomable="yes"}

1. Geben Sie einen Suchbegriff ein.

1. Wählen Sie ![Hinzufügen](/help/assets/icons/Add.svg) **[!UICONTROL Zeile hinzufügen]** aus, um die Auswahl zu bestätigen und ein weiteres Kriterienelement hinzuzufügen.

1. Wählen Sie ![CrossSize75](/help/assets/icons/CrossSize75.svg) aus, um ein Kriterienelement zu entfernen.

Sie können bis zu 10 Kriterienelemente einbeziehen.

### **[!UICONTROL spezifisch]**

Mit **[!UICONTROL Option]** können Sie für jede Dimension eine feste Liste von Dimensionselementen erstellen. Verwenden Sie den Filtertyp **[!UICONTROL Spezifisch]**, um die genauen Dimensionselemente anzugeben, die in Ihren Filter aufgenommen werden sollen. Sie können Elemente aus einer Liste oder aus einem Zellenbereich auswählen.

![Die spezifischen Optionen und ausgewählten Elemente.](./assets/image32.png){zoomable="yes"}

#### Aus Liste

1. Wählen Sie die Option **[!UICONTROL Aus Liste]** aus, um nach Dimensionselementen zu suchen und diese auszuwählen.

   Wenn Sie die Option **Aus Liste** auswählen, wird die Liste **[!UICONTROL Dimension-]** Elemente&#39; mit Dimensionselementen gefüllt, sortiert nach der Anzahl der Ereignisse.

   ![Die Option „Von Liste“ und die verfügbaren Elemente.](./assets/image33.png){zoomable="yes"}

1. Geben Sie einen Suchbegriff in das Feld ![Suche](/help/assets/icons/Search.svg) **[!UICONTROL _Element hinzufügen_]** ein, um die Liste zu durchsuchen.

1. Um nach einem Element zu suchen, das in den letzten 90 Tagen nicht enthalten war, wählen Sie **[!UICONTROL Elemente für die letzten 6 Monate anzeigen]** aus, um die Suche zu erweitern. Nachdem die Daten der letzten 6 Monate geladen wurden, aktualisiert Report Builder den Link zu **[!UICONTROL Elemente für die letzten 18 Monate anzeigen]**.

1. Um ein Element aus der Liste **[!UICONTROL Ausgewählte Elemente]** zu löschen, wählen Sie ![CrossSize75](/help/assets/icons/CrossSize75.svg) aus.

1. Um ein Element in der Liste **[!UICONTROL Ausgewählte Elemente]** zu verschieben, ziehen Sie das Element per Drag-and-Drop oder wählen Sie ![MehrKlein](/help/assets/icons/MoreSmall.svg) aus, um das Kontextmenü anzuzeigen und aus den Optionen zum Verschieben auszuwählen.

1. Wählen Sie **[!UICONTROL Anwenden]** aus.

Report Builder aktualisiert die Liste, um die angewendeten spezifischen Filter anzuzeigen.

#### Aus Zellenbereich

Wählen Sie die Option **Aus Zellenbereich** aus, um einen Zellenbereich auszuwählen, der die Liste der abzugleichenden Dimensionselemente enthält.

![Die Option Aus Zellenbereich und das Feld zur Auswahl eines Zellenbereichs.](./assets/image37.png){zoomable="yes"}

Beachten Sie bei der Auswahl eines Zellenbereichs die folgenden Einschränkungen:

- Der Bereich muss über mindestens eine Zelle verfügen.
- Der Bereich kann nicht mehr als 50.000 Zellen umfassen.
- Der Bereich muss sich in einer einzigen unterbrechungsfreien Zeile oder Spalte befinden.

Ihre Auswahl kann leere Zellen oder Zellen mit Werten enthalten, die nicht mit einem bestimmten Dimensionselement übereinstimmen.


### Schnelles Filtern einer Dimension

So filtern Sie eine Dimension, für die derzeit kein Filter angewendet wird:

1. Wählen Sie ![ChevronRight](/help/assets/icons/ChevronRight.svg) für eine Dimension aus. Beispiel: **[!UICONTROL Interaktionskanal]**.

1. Doppelklicken Sie auf Dimensionselemente, die zum Filter hinzugefügt werden sollen. Alternativ können Sie ein oder mehrere Dimensionselemente auswählen und die Auswahl per Drag-and-Drop auf den Abschnitt ![TableSelectRow](/help/assets/icons/TableSelectRow.svg) **[!UICONTROL Row]** ziehen.

   ![Die Registerkarte „Dimensionen“ und die Liste der Dimensionen.](./assets/quickly-filter.png){zoomable="yes"}


<!--

By default, each dimension item in the table returns the top 10 items for that dimension.

To change the dimension items returned for each dimension

1. Click **[!UICONTROL Manage]** and select a data block from the list.

   ![Manage > Edit data block](./assets/manage-edit.png)

1. Click **[!UICONTROL Edit data block]** in the COMMANDS panel.

1. Click **[!UICONTROL Next]** to display the Dimensions tab.

1. Click the **...** icon next to a component name in the table.

    ![The ellipsis icon options.](./assets/image27.png)

1. Select **[!UICONTROL Filter dimension]** in the pop-up menu to display the **[!UICONTROL Filter dimension]** pane.

1. Select **[!UICONTROL Most popular]** or **[!UICONTROL Specific]**.

    ![The specific option selected in the Filter dimension pane.](./assets/image28.png)

1. Select appropriate options based on the filter type chosen.

1. Click **[!UICONTROL Apply]** to add the filter.

    Report Builder displays a notification to confirm the added filter.

To display applied filters, hover over a dimension. Dimensions with applied filters display a filter icon to the right of the Dimension name.

## Filter Type

There are two ways to filter dimension items: Most popular and Specific.

## Most popular

The [!UICONTROL Most popular] option allows you to dynamically filter dimension items based on metric values. [!UICONTROL Most popular] filtering returns the highest ranked dimension items based on metric values. By default, the first 10 dimensions items are listed, sorted by the first metric added to the data block.

 ![The Most popular option.](./assets/image29.png)


### Page and Rows options

Use the **Page** and **Rows** fields to divide data into sequential groups or pages. This allows you to pull ranked row values other than the top-most values into your report. This feature is especially useful for pulling data beyond the 50,000 row limit.

#### Page and Rows defaults

- Page = 1
- Rows = 10

The Page and Rows default settings identify that each page has 10 rows of data. Page 1 returns the top 10 items, page 2 returns the next 10 items, and so on.

The table below lists examples of page and row values and the resulting output.

| Page | Row    | Output               |
|------|--------|----------------------|
| 1    | 10     | Top 10 items         |
| 2    | 10     | Items 11-20          |
| 1    | 100    | Top 100 items        |
| 2    | 100    | Items 101-200        |
| 2    | 50,000 | Items 50,001-100,000 |

#### Minimum and maximum values

- Starting page: Min = 1, Max: 50 million
- Number of rows: Min = 1, Max: 50,000

### Include "No value"

In Adobe Analytics, some dimensions collect a "no value" entry. This filter allows you to exclude these values from reports. For example, you can create a classification such as the Product Name classification based on the Product SKU key. If a specific product SKU has not been set up with its specific Product Name classification, its Product Name value is set to "no value".

Include "**No value**" is selected by default. Deselect this option to exclude entries with no value.

### Filter by Criteria

You can filter dimension items based on whether all criteria are met or if any criteria are met.

To set filtering criteria

1. Select an operator from the drop-down list.

    ![The operator list.](./assets/image31.png)

1. Enter a value into the search field.

1. Click **[!UICONTROL Add row]** to confirm the selection and add another criteria item.

1. Click the delete icon to remove a criteria item.

    You can include up to 10 criteria items.

### Change the filter and sort order

An arrow appears next to the metric used to filter and sort the data block. The direction of the arrow indicates whether the metric is sorted greatest to least or least to greatest.

To change the sort direction, click the arrow next to the metric.

To change the metric used to filter and sort the data block,

1. Hover over the desired metric component in the Table builder to display additional options.

2. Click the arrow on the preferred metric.

   ![The Table builder and metrics.](./assets/image30.png)


## Specific filtering

The Specific option allows you to create a fixed list of dimension items for each dimension. Use the **[!UICONTROL Specific]** filtering type to specify the exact dimension items to include in your filter. You can select items from a list or from a range of cells.

![The Specific options and selected items.](./assets/image32.png)

### From list

1. Select the **[!UICONTROL From list]** option to search for and select dimension items.

    When you select the **[!UICONTROL From list]** option, the list is populated with dimension items with the most events first.

    ![The From list option and available items.](./assets/image33.png)

    The **[!UICONTROL Available items]** list is ordered from dimension items with the most events to those with the least.

1. Enter a search term in the **[!UICONTROL Add item]** field to search the list.

1. To search for an item not included in the last 90 days of data, click **[!UICONTROL Show items for the last 6 months]** to extend the search.

    ![The Show items from the last 6 months list.](./assets/image34.png)

    After data from the past 6 months loads, Report Builder updates the link to **[!UICONTROL Show items for last 18 months]**.

1. Select a dimension item.

    Selected dimension items are automatically added to the **[!UICONTROL Selected items]** list.

    ![](./assets/image35.png)

    To delete an item from the list, click the delete icon to remove the item from the list.

    To move an item in the list, drag and drop the item or click ... to display the move menu.

    ![The dimension items list.](./assets/image36.png)

1. Click **[!UICONTROL Apply]**

    Report Builder updates the list to show the specific filtering you applied.

### From range of cells

Select the **[!UICONTROL From range of cells]** option to choose a range of cell that contain the list of dimensions items to match.

 ![The From range of cells option and field to select one range of cells.](./assets/image37.png)

When you select a range of cells, consider the following restrictions:

- The range must have at least one cell.
- The range can't have more than 50,000 cells.
- The range must be in a single uninterrupted row, or column.

Your selection can contain empty cells or cells with values that don't match with a specific dimension item.

### From the Dimensions tab in the Table builder

From the **[!UICONTROL Dimensions]** tab, click the chevron icon next to a dimension name to view the list of dimension items.

 ![The Dimensions tab and the list of dimensions.](./assets/dimensions_chevron.png)

You can drag and drop items onto the **[!UICONTROL Table]** or double-click an item name to add it to the **[!UICONTROL Table]** builder.

-->