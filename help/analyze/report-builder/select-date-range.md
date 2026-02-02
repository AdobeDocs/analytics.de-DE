---
title: Auswählen eines Datenbereichs in Report Builder
description: Erfahren Sie, wie Sie in Report Builder einen Datumsbereich auswählen.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 610ce2c8-8ff6-4434-912f-3015cc56a51e
source-git-commit: c3fe537967473754a3b5fe88c7b383647b2c742e
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 46%

---

# Auswählen eines Datumsbereichs

So ändern Sie den Datumsbereich eines vorhandenen Datenblocks:

- Wählen **[!UICONTROL Datenblock bearbeiten]** oder
- Wählen Sie den Link **[!UICONTROL Datumsbereich]** in **[!UICONTROL Schnellbearbeitung]**.

Verwenden Sie die folgenden Optionen, um einen Datumsbereich für einen Datenblock zu ändern.

## Kalender

Mit **[!UICONTROL Option]** Kalender“ können Sie statische oder rollierende Datumswerte mit den folgenden Optionen erstellen:

### Datumsbereich

Das Datumsbereichsfeld zeigt den aktuellen Datumsbereich für die Datenblockanfrage an. Sie können Datumsangaben direkt eingeben oder ![Kalender](/help/assets/icons/Calendar.svg) verwenden, um einen Datumsbereich anzugeben.

![Datumsbereichskalender](assets/date-range-calendar.png){zoomable="yes"}

### Voreinstellungen

Wählen Sie im Dropdown-Menü Vorgaben eine Vorgabe aus. Sie können auch Text eingeben, um nach Voreinstellungen zu suchen.

![Vorgaben für Datumsbereiche](assets/date-range-presets.png){zoomable="yes"}

Das Dropdown-Menü „Voreinstellung“ enthält einen Standardsatz vordefinierter Datumsbereiche und Datumsbereichskomponenten für eine von Ihnen gespeicherte Report Suite oder eine für Sie freigegebene Report Suite.

### Rollierende Datumswerte

So definieren Sie rollierende Datumswerte:

![Verwenden rollierender Datumswerte](assets/date-range-rolling-date.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Rollierende Datumswerte verwenden]**, um die Logik für eine Definition rollierender Datumswerte zu definieren. Sie können den Text in Klammern auswählen (z. B. **[!UICONTROL Fester Start - täglich rollierend]**), um das Bedienfeld zu erweitern und Details für **[!UICONTROL Start]** und **[!UICONTROL Ende]** anzugeben.

1. Wählen Sie **[!UICONTROL Anfang von]**, **[!UICONTROL Ende von]** oder **[!UICONTROL Festgelegter Tag]** aus.

   - Wenn Sie **[!UICONTROL Anfang von]** oder **[!UICONTROL Ende von]** ausgewählt haben, können Sie einen vollständigen Ausdruck erstellen. Beispiel: **[!UICONTROL Ende von]** **[!UICONTROL Aktuelles Jahr]** **[!UICONTROL plus]** `1` **[!UICONTROL Tag]**. Wählen Sie den entsprechenden Wert für jeden einzelnen Teil des Ausdrucks aus.

      - Wählen Sie einen Wert für den aktuellen Zeitraum aus, Beispiel: **[!UICONTROL aktuelles Jahr]**.
      - Wählen Sie einen Wert für eine optionale zusätzliche Berechnung. z. B. **[!UICONTROL plus]**.
      - Wenn Sie eine zusätzliche Berechnung angegeben haben, geben Sie einen Wert an. Zum Beispiel `1`.
      - Wenn Sie eine zusätzliche Berechnung angegeben haben, wählen Sie den Zeitraum aus, der für die Berechnung verwendet werden soll, Beispiel: **[!UICONTROL Tag]**.

   - Wenn Sie **[!UICONTROL Fester Tag]** ausgewählt haben, geben Sie einen festen Tag an oder wählen Sie mit der Auswahl einen Tag aus.

1. Wählen Sie **[!UICONTROL Ausblenden]**, um die Details für die Berechnung rollierender Datumswerte auszublenden.


### Benutzerdefinierte Ausdrücke

Mit der Option für benutzerdefinierte Ausdrücke können Sie den Datumsbereich ändern, indem Sie einen benutzerdefinierten Ausdruck erstellen oder eine arithmetische Formel eingeben.

![Benutzerdefinierter Ausdruck für Datumsbereich](assets/date-range-custom-expression.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Rollierende Datumswerte verwenden]** aus.

1. Wählen Sie **[!UICONTROL Benutzerdefinierte Ausdrücke verwenden]** aus.

   Wenn Sie **[!UICONTROL Benutzerdefinierte Ausdrücke verwenden]** auswählen, sind die standardmäßigen Steuerelemente für rollierende Datumsbereiche deaktiviert.

1. Geben Sie einen [benutzerdefinierten Ausdruck](#create-a-custom-expression) ein.

1. Verwenden Sie die **[!UICONTROL Datumsvorschau]**, um den resultierenden Datumsbereich zu überprüfen.

#### Erstellen eines benutzerdefinierten Ausdrucks

1. Geben Sie [Datumsreferenz“ &#x200B;](#date-references).

1. Fügen Sie einen optionalen [Datumsoperator](#date-operators) hinzu, um das Datum in die Vergangenheit oder in die Zukunft zu verschieben.

Sie können einen benutzerdefinierten Ausdruck eingeben, der mehrere Operatoren enthält, z. B. `tm-11m-1d`.

#### Datumsreferenzen

In der folgenden Tabelle sind Beispiele für Datumsreferenzen aufgeführt.

| Datumsreferenz | Typ | Beschreibung |
|----------------|--------------|----------------------------|
| `1/1/10` | Statisches Datum | Im ISO-Datumsformat eingegeben |
| `td` | Rollierendes Datum | Beginn des aktuellen Tages |
| `tw` | Rollierendes Datum | Beginn der aktuellen Woche |
| `tm` | Rollierendes Datum | Beginn des aktuellen Monats |
| `tq` | Rollierendes Datum | Beginn des aktuellen Quartals |
| `ty` | Rollierendes Datum | Beginn des laufenden Jahres |

#### Datumsoperatoren

In der folgenden Tabelle sind Beispiele für Datumsoperatoren aufgeführt.

| Datumsoperator | Einheit | Beschreibung |
|----------------|---------|--------------------|
| `+6d` | Tag | Hinzufügen von 6 Tagen zur Datumsreferenz |
| `+1w` | Woche | Hinzufügen einer ganzen Woche zur Datumsreferenz |
| `-2m` | Monat | Abziehen von 2 vollständigen Monaten von der Datumsreferenz |
| `-4q` | Quartal | Abziehen von 4 Quartalen von der Datumsreferenz |
| -`1y` | Jahr | Abziehen von 1 Jahr von der Datumsreferenz |

#### Datumsausdrücke

In der folgenden Tabelle sind Beispiele für Datumsausdrücke aufgeführt.

| Datumsausdruck | Bedeutung |
|-----------------|--------------------------------------|
| `td` | Am aktuellen Tag |
| `td-1w` | Erster Tag der letzten Woche |
| `tm-1d` | Letzter Tag des vorherigen Monats |
| `td-52w` | Derselbe Tag vor 52 Wochen |
| `tm-11m-1d` | Letzter Tag des gleichen Monats im letzten Jahr |
| `"2020-09-06"` | Spezifisches Datum, 9. September 2020 |



## Datumsbereich aus Zelle

Der Datumsbereich kann in Zellen eines Arbeitsblatts angegeben werden. Verwenden Sie die Option **[!UICONTROL Datumsbereich aus Zelle]**, um das Start- und Enddatum des Datenblocks aus ausgewählten Zellen auszuwählen. Wenn Sie die Option **[!UICONTROL Aus Zelle]** auswählen, zeigt das Bedienfeld die Felder **[!UICONTROL Von]** und **[!UICONTROL Bis]** an, in die Sie eine Zellenposition eingeben oder ![DataBlockSelector](/help/assets/icons/DataBlockSelector.svg) verwenden können, um die aktuell ausgewählte Zelle auszuwählen.

![Aus Zelle auswählen Sheet1!H4 zu Sheet1!I4](./assets/date-range-from-cell.png){zoomable="yes"}


## Heute ausschließen

Wählen Sie **[!UICONTROL Heute ausschließen]**, um den aktuellen Tag aus einem ausgewählten Datumsbereich auszuschließen. Der aktuelle Tag wird aus allen Modi ausgeschlossen, die zum Definieren eines Datumsbereichs verwendet werden: Kalender, rollierende Datumswerte oder benutzerdefinierte Ausdrücke.


## Gültige Datumsbereiche

In der folgenden Liste werden gültige Datumsbereichsformate beschrieben.

- Das Start- und das Enddatum müssen im folgenden Format angegeben werden: YYYY-MM-DD

- Das Startdatum muss vor dem Enddatum liegen oder damit übereinstimmen. Bei beiden Daten kann es sich um Daten in der Zukunft handeln.

- Bei Verwendung rollierender Datumswerte muss das Startdatum heute oder in der Vergangenheit liegen. Der Starttag muss in der Vergangenheit liegen, wenn **[!UICONTROL Heute ausschließen]** ausgewählt ist.

- Sie können einen statischen Datumsbereich für die Zukunft erstellen. Beispielsweise müssen Sie möglicherweise ein künftiges Datum für den Start einer Marketing-Kampagne in der nächsten Woche festlegen. Mit dieser Option wird ein Arbeitsmappen-Monitoring für eine Kampagne im Voraus erstellt.

## Datumsbereich ändern

Sie können den Datumsbereich eines vorhandenen Datenblocks bearbeiten.

1. Wählen Sie eine Zelle in Ihrem Datenblock aus.

- Wählen **[!UICONTROL Datenblock bearbeiten]** im Bedienfeld **[!UICONTROL Befehle]** oder
- Wählen Sie den **[!UICONTROL Datumsbereich]** im Bedienfeld **[!UICONTROL Schnellbearbeitung]** aus.

1. Ändern Sie den Datumsbereich mit einer der verfügbaren Datumsauswahloptionen.

1. Wählen Sie **[!UICONTROL Anwenden]** aus.

Report Builder wendet den neuen Datumsbereich auf alle Datenblöcke in der Auswahl an.

<!--
To change the date range of an existing data block, select Edit a data block or use the QUICK EDIT panel.

Use the following options to change a date range for a data block.

**Calendar**

 The Calendar allows you to create static or rolling dates using the following options:

- Date range field
- Calendar
- Preset drop-down menu
- Rolling date mode
- Customize expressions


**From cell**

The **[!UICONTROL From cell]** option allows you to reference dates entered in worksheet cells.

You have the option to exclude today on any selected date range.

 ![Report Builder Quick edit pane with calendar selected and Exclude today selected.](./assets/image17.png)

## Use the Calendar

When you use the **Calendar**, the date range field displays the current date range for the data block request. You can enter dates directly into the date range field or use a data range selection option.

### Date range field

To enter dates directly into the date range field

1. Click the date range field next to the calendar icon.

1. Enter start and end dates for your date range.

### Calendar

To select dates using the calendar

1. Click the calendar icon to display a monthly calendar.

1. Click a start date.

1. Click an end date.

To set a date range in reverse, click the end date first and then click the start date.

![Report Builder date range pane showing the calendar and the end date and the start date selected.](./assets/image18.png)

### Preset drop down menu

The preset drop-down menu includes a standard set of preset date ranges and date range components for a report suite that you saved or a report suite that was shared with you.

### Rolling dates

The rolling dates option allows you to select a date range using rolling dates.

1. Select **Use rolling dates**.

1. Select a rolling expression for your start and or end date.

    ![Report Builder date range pane showing Use rolling dates selected and the rolling expression.](./assets/image19.png)

    **Start of** — Allows you to select the beginning of a day, week, month, quarter, or year.

    **End of** — Allows you to select the end of a day, week, month, quarter, or year.

    **Fixed day** — Allows you to fix a start or end date while the other date is rolling.

1. Choose day, week, month, quarter, or year as the rolling period.

    ![Report Builder date range pane showing the current day selected.](./assets/image20.png)

1. Add or subtract days, weeks, months, quarters, or years from your rolling date.

    ![Report Builder date range pane showing the current day plus 14 days selected.](./assets/image21.png)

1. Click Next to define the data range.

    Use the date preview to confirm the resulting date range is the desired range.

### Custom expressions

The custom expression option allows you to change the date range by building a custom expression or you can enter an arithmetic formula.

1. Select **Use rolling dates**.

1. Select **Use custom expression**.

    When you select the **Use custom expression** option, the standard rolling date range controls are disabled.

    ![Select Use custom expression showing tm-1m to td-1d.](./assets/custom_expression.png)

1. Enter a custom expression.

    For a sample list of custom expressions, see **Date expressions**.

1. Use the date preview to verify the resulting date range is the desired range.

#### Create a custom expression

1. Enter a **Date reference**.

1. Add **Date operators** to move the date to the past or future.

You can enter a custom date expression that includes multiple operators, such as ```tm-11m-1d```.

#### Date references

The following table lists date reference examples.

| Date Reference | Type         | Description                |
|----------------|--------------|----------------------------|
| 1/1/10         | Static Date  | Entered in ISO Date format |
| td             | Rolling Date | Start of current day       |
| tw             | Rolling Date | Start of current week      |
| tm             | Rolling Date | Start of current month     |
| tq             | Rolling Date | Start of current quarter   |
| ty             | Rolling Date | Start of current year      |

#### Date operators

The following table lists date operator examples.

| Date Operators | Unit    | Description   |
|----------------|---------|--------------------|
| +6d            | Day     | Add 6 days to the Date Reference |
| +1w            | Week    | Add one full week to the Date Reference |
| -2m            | Month   | Subtract 2 full months to the Date Reference |
| -4q            | Quarter | Subtract 4 quarters to the Date Reference |
| -1y            | Year    | Subtract one year to the Date Reference |

#### Date expressions

The following table lists date expression examples.

| Date Expression | Meaning                              |
|-----------------|--------------------------------------|
| td-1w           | First day of last week               |
| tm-1d           | Last day of previous month           |
| td-52w          | Same day, 52 weeks ago               |
| tm-11m-1d       | Last day of the same month last year |
| "2020-09-06"    | Sept 9th, 2020                       |

## Date range from cell

The date range can be specified in worksheet cells. Use the **Date range from cell** option to choose the data block start and end date from selected cells. When you select the **From cell** option, the panel displays **From** and **To** fields where you can enter a cell location.

![Select From cell Sheet1!H4 to Sheet1!I4](./assets/image23.png)

## Exclude today

Choose the **Exclude today** option to exclude today from a selected date range. Choosing to include today may pull incomplete data for today.

When selected, the **Exclude today** option excludes the current day from all date range modes including calendar, rolling dates, or custom expressions.

## Valid date ranges

The following list describe valid date range formats.

- The start and end dates must be in the following format: YYYY-MM-DD

- The start date must be earlier to or equal to the end date. Both dates can be set to the future.

- When using rolling dates, the start date must be today or in the past. It must be in the past if **Exclude today** is checked.

- You can create a static date range set for the future. For example, you may need to set a future date for a marketing campaign launch next week. This option creates a workbook monitoring for a campaign ahead of time.

## Change the date range

You can edit the date range of an existing data block by selecting Edit data block in the COMMANDS panel or by selecting the date range link in the QUICK EDIT panel.

**Edit data block** — Allows you to edit multiple data block parameters, including date range, for a single data block.

**Quick Edit: Date range** — Allows you to edit the date range of one or more data blocks.

To edit the date range from the QUICK EDIT panel

1. Select cells within one or more data blocks in a worksheet.

1. Click the **Date range** link in the QUICK EDIT panel.

1. Select the date range using any of the date selection options.

1. Click **Apply**.


Report Builder applies the new date range to all data blocks in the selection.
-->