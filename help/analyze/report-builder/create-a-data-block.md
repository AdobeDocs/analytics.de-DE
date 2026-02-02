---
title: Erstellen eines Datenblocks in Report Builder
description: Erfahren Sie, wie Sie einen Datenblock erstellen.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: fd3ff12a-14de-46f6-ab89-a0152fb11b0d
source-git-commit: ff1722416fe5062d16c12185d17271ebc2d6b624
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 20%

---

# Erstellen eines Datenblocks

Ein *Datenblock* ist die Datentabelle, die von einer einzelnen Datenanforderung erstellt wird. Eine Report Builder-Arbeitsmappe kann mehrere Datenblöcke enthalten. Wenn Sie einen Datenblock erstellen, konfigurieren Sie ihn zunächst und erstellen Sie dann den Build.

## Datenblock konfigurieren

Konfigurieren Sie die anfänglichen Datenblockparameter für den Speicherort des Datenblocks, die Report Suite und einen Datumsbereich.

1. Wählen Sie ![Kreis hinzufügen](/help/assets/icons/AddCircle.svg) **[!UICONTROL Erstellen]**.

   ![Screenshot mit der Option „Datenblock erstellen“](./assets/create-data-block.png){zoomable="yes"}


1. Legen Sie den **[!UICONTROL Speicherort des Datenblocks]** fest.

   Die Option Datenblock-Speicherort definiert den Speicherort des Arbeitsblatts, an dem Report Builder die Daten zu Ihrem Arbeitsblatt hinzufügt.

   Um den Speicherort des Datenblocks anzugeben, wählen Sie eine einzelne Zelle im Arbeitsblatt aus oder geben Sie eine Zellenadresse ein, z. B. `a3`, `\\\$a3`, `a\\\$3` oder `sheet1!a2`. Die angegebene Zelle wird zur oberen linken Ecke des Datenblocks, wenn die Daten abgerufen werden.

   Verwenden ![DataBlockSelector](/help/assets/icons/DataBlockSelector.svg), um eine Datenblockposition aus der aktuell ausgewählten Zelle im Blatt auszuwählen.

1. Wählen Sie die **[!UICONTROL Report Suites]**.

   Mit der Option Report Suites können Sie eine Report Suite aus einem Dropdown-Menü auswählen oder eine Report Suite aus einer Zellenposition referenzieren.

   Wählen Sie ![DataViewSelector](/help/assets/icons/DataViewSelector.svg) aus, um eine Report Suite aus einer Zelle zu erstellen.

1. Legen Sie den **[!UICONTROL Datumsbereich]** fest.

   Mit **[!UICONTROL Option]** Datumsbereich) können Sie einen Datumsbereich auswählen. Datumsbereiche können fest oder rollierend sein.

   Wählen Sie **[!UICONTROL Kalender]** aus, um einen Datenbereich mithilfe von ![Kalender](/help/assets/icons/Calendar.svg) auszuwählen, oder geben Sie einen Datumsbereich manuell ein. Optional können Sie eine Vorgabe aus dem Dropdown **[!UICONTROL _Menü &quot;_]**&quot; auswählen.

   Wählen Sie **[!UICONTROL Aus Zelle]**, um Start- und Enddaten basierend auf einer Zelle im aktuellen Blatt zu definieren.

   Weitere Informationen zu Datumsbereichsoptionen finden Sie unter [Einen Datumsbereich auswählen](select-date-range.md).

1. Klicken Sie auf **[!UICONTROL Weiter]**.

   ![Screenshot mit der Option „Datumsbereich“ und der Schaltfläche „Aktiv Weiter“.](./assets/choose_date_data_view3.png)

   Nach der Konfiguration des Datenblocks können Sie Dimensionen, Metriken und Segmente auswählen, um Ihren Datenblock zu erstellen. Die **[!UICONTROL Dimensionen]**, **[!UICONTROL Metriken]** und **[!UICONTROL Segmente]** werden über dem Bereich **[!UICONTROL Tabelle]** angezeigt.

## Datenblock erstellen

Um den Datenblock zu erstellen, wählen Sie Berichtkomponenten aus und passen Sie dann das Layout an.

1. Fügen Sie **[!UICONTROL Dimensionen]**, **[!UICONTROL Metriken]** und **[!UICONTROL Segmente]** hinzu.

   Scrollen Sie in den Komponentenlisten oder verwenden Sie das Feld ![Suchen](/help/assets/icons/Search.svg) **[!UICONTROL _Komponenten suchen_]**, um Komponenten zu finden. Ziehen Sie Komponenten per Drag-and[!UICONTROL Drop in den Bereich ]Tabelle“ oder doppelwählen Sie einen Komponentennamen in der Liste aus, um die Komponente dem Bereich [!UICONTROL Tabelle] hinzuzufügen.

   Doppelklicken Sie auf eine Komponente, um sie einem Standardabschnitt der Tabelle hinzuzufügen.

   - Dimension-Komponenten werden dem Abschnitt ![TableSelectRow](/help/assets/icons/TableSelectRow.svg) **[!UICONTROL Row]** oder dem Abschnitt ![TableSelectColumn](/help/assets/icons/TableSelectColumn.svg) **[!UICONTROL Column]** hinzugefügt, wenn die Dimension bereits in den Spalten vorhanden ist.
   - Datumskomponenten werden dem Abschnitt ![TableSelectColumn](/help/assets/icons/TableSelectColumn.svg) **[!UICONTROL Column]** hinzugefügt.
   - Segmentkomponenten werden zum Abschnitt ![Segmentierung](/help/assets/icons/Segmentation.svg)**[!UICONTROL Segmente]** hinzugefügt.
   - Metrikkomponenten werden zum Abschnitt ![Ereignis](/help/assets/icons/Event.svg)**[!UICONTROL Werte]** hinzugefügt.

1. Ordnen Sie die Elemente im Tabellenbereich an, um das Layout Ihres Datenblocks anzupassen.

   Ziehen Sie Komponenten per Drag-and-Drop in jede Liste im Tabellenbereich, um die Komponenten neu anzuordnen, oder wählen Sie ![MehrKlein](/help/assets/icons/MoreSmall.svg) und wählen Sie ![Pfeil](/help/assets/icons/ArrowUp.svg) Nach oben, ![PfeilNach unten](/help/assets/icons/ArrowDown.svg) Nach unten und mehr aus, um Komponenten innerhalb einer Liste zu verschieben.

   Wenn Sie Komponenten zur Tabelle hinzufügen, wird eine Vorschau des Datenblocks an der Stelle des Datenblocks im Arbeitsblatt angezeigt. Das Layout der Datenblock-Vorschau wird automatisch aktualisiert, wenn Sie in der Tabelle Elemente hinzufügen, verschieben oder entfernen.

   ![Screenshot mit den hinzugefügten Komponenten und dem aktualisierten Arbeitsblatt.](./assets/image10.png)


1. Legen Sie optional das **[!UICONTROL Startdatum]** als Dimension fest, um das Startdatum Ihres Datenblocks zu identifizieren. Das Hinzufügen der Startdaten als Dimension ist hilfreich, wenn Sie einen regelmäßig terminierten Bericht mit einem rollierenden Datumsbereich haben. Oder wenn Sie einen unkonventionellen Datumsbereich haben und Sie das Startdatum explizit angeben müssen.

   ![Screenshot mit dem Startdatum in der Liste der Dimensionen.](./assets/start-date-dimension.png)

1. Optional können Sie Zeilen- und Spaltenüberschriften ein- oder ausblenden. Gehen Sie dazu wie folgt vor:

   1. Wählen Sie das Symbol **[!UICONTROL Tabelle]** ![Einstellung](/help/assets/icons/Setting.svg)Einstellungen aus.

      ![Screenshot mit der Option „Tabelleneinstellungen“](./assets/table-settings.png)

   1. Aktivieren oder deaktivieren Sie die Option **[!UICONTROL Zeilen- und Spaltenüberschriften anzeigen]**. Die Kopfzeilen werden standardmäßig angezeigt.

1. Optional können Sie auch Dimensionsbeschriftungen und Metrikkopfzeilen ein- oder ausblenden. Gehen Sie dazu wie folgt vor:

   1. Wählen Sie ![MehrKlein](/help/assets/icons/MoreSmall.svg) auf der Dimensionsbeschriftung oder in der Spaltenüberschrift aus, um das Kontextmenü anzuzeigen.

      ![Das Symbol mit den Auslassungspunkten im Zeilenabschnitt.](./assets/row-heading.png)

   1. Wählen Sie ![VisibilityOff](/help/assets/icons/VisibilityOff.svg) **[!UICONTROL Hide]** oder ![Visibility](/help/assets/icons/Visibility.svg) **[!UICONTROL Show]** aus, um die Dimensionsbeschriftung oder Spaltenüberschrift umzuschalten. Alle Beschriftungen werden standardmäßig angezeigt.

1. Wählen **[!UICONTROL Beenden]**, um die Konfiguration Ihres Datenblocks abzuschließen.

1. Eine Verarbeitungsmeldung **[!UICONTROL #BUSY]** wird angezeigt, während die Analysedaten abgerufen werden.

   ![Die Verarbeitungsmeldung.](./assets/image11.png)

1. Report Builder ruft die Daten ab und zeigt den abgeschlossenen Datenblock im Arbeitsblatt an.

   ![Der abgeschlossene Datenblock.](./assets/image12.png)


>[!MORELIKETHIS]
>
>[Report Suite auswählen](select-report-suite.md)
>[Datumsbereich auswählen](select-date-range.md)
>[Filterdimensionen](filter-dimensions.md)
>[Arbeiten mit Segmenten](work-with-segments.md)
>


<!--

A *data block* is the table of data created by a single data request. A Report Builder workbook can contain multiple data blocks. When you create a data block, first configure the data block and then build the data block.

## Configure the data block

Configure the initial data block parameters for the data block location, report suite, and a date range.

1. Click **[!UICONTROL Create]**.

    ![Screenshot showing the Create data block option.](./assets/create_db.png)

1. Set the **[!UICONTROL Data block location]**.

    The data block location option defines the worksheet location where report builder adds the data to your worksheet.

    To specify the data block location, select a single cell in the worksheet and click the icon next to **[!UICONTROL Data block location]**: 
    
    You can also enter a cell address such as a3, \\\$a3, a\\\$3 or sheet1!a2. The cell specified marks the upper-left corner of the data block when the data is retrieved.

1. Choose a **Report Suite**.

    The report suites option allows you to choose a report suite from a drop-down menu or to reference a report suite from a cell location.

1. Set the **[!UICONTROL Date range]**.

    The Date range option allows you to choose a date range. Date ranges may be fixed or rolling. For information about data range options, see [Select a Date Range](select-date-range.md).

1. Click **[!UICONTROL Next]**.

    ![Screenshot showing the date range option and the active Next button.](./assets/choose_date_report_suite.png)

    After you configure the data block, you can select dimensions, metrics, and segments to build your data block. The Dimensions, Metrics, and Filters tabs are displayed above the Table builder pane.

## Build the data block

To build the data block, select report components, and then customize the layout.

1. Add Dimensions, Metrics, and Segments.

    Scroll the component lists or use the **[!UICONTROL Search]** field to locate components. Drag and drop components to the Table pane or double-click a component name in the list to automatically add the component to the Table pane.

    Double-click a component to add it to a default section of the table.

    - Dimension components are added to the Row section or to the Column section if you have a dimension already in the columns.
    - Date components are added to the Column section.
    - Segment components are added to the Segments section.

    **Start date as a Dimension**

    Set the **[!UICONTROL Start date]** as a dimension to clearly identify the start date of your data block. This is helpful if you have a regularly scheduled report that has a rolling date range or if you have an unconventional date range and you need to be clear on the start date.

    ![Screenshot showing the Start date in the list of dimensions.](./assets/start-date-dimension.png){width="30%"}

1. Arrange the items in the Table pane to customize the layout of your data block.

    Drag and drop components in the Table pane to reorder components or right-click a component name and select from the options menu.

    When you add components to the table, a preview of the data block is displayed at the Data block location in the worksheet. The layout of the data block preview automatically updates as you add, move, or remove items in the table.

    ![Screenshot showing the added components and updated worksheet.](./assets/image10.png)

    **Display or hide row and column headers**

1. Click the **[!UICONTROL Table settings]** icon.

    ![Screenshot showing the Table settings option.](./assets/table-settings.png){width="35%"}

1. Check or uncheck the option to Display row and column headers. The headers are displayed by default.

    **Hide or show dimension labels and metric headers**

1. Click the ellipsis icon on either the dimensions or the column headers to display the settings.

    ![The ellipsis icon in the Row section.](./assets/row-heading.png){width="35%"}

1. Click Hide or Show to toggle the dimension labels or column headers. All labels are displayed by default.

1. Click **[!UICONTROL Finish]**.

    A processing message is displayed while the analytics data is retrieved.

    Report Builder retrieves the data and displays the completed data block in the worksheet.

    ![The completed data block.](./assets/image12.png)

-->