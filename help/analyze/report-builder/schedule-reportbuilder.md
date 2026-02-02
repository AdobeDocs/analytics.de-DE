---
title: Erstellen von Zeitplänen für Arbeitsmappen mithilfe von Report Builder
description: Erfahren Sie, wie Sie die Zeitplanfunktion in Report Builder verwenden.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 40e1feb0-64bc-40e6-83cb-4a1ea7e2d0cc
source-git-commit: 8b6d8a4efec59b693a69984880d8f374ae0cfabc
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 26%

---

# Arbeitsmappen durch Freigabe per E-Mail planen

>[!NOTE]
>
>Zusätzlich zur Planung von Arbeitsmappen für die Freigabe per E-Mail, wie in diesem Abschnitt beschrieben, können Sie Arbeitsmappen für den Export in Cloud-Ziele planen, wie in [Arbeitsmappen für den Export in Cloud-Ziele planen](/help/analyze/report-builder/report-builder-export.md) beschrieben.

Nachdem Sie Ihre Arbeitsmappe gespeichert und Ihre Analyse abgeschlossen haben, können Sie die Arbeitsmappe mithilfe der Zeitplanfunktion für andere in Ihrem Team freigeben. Mit der Zeitplanfunktion können Sie einen Zeitplan erstellen, anhand dessen die Daten in der Arbeitsmappe automatisch aktualisiert werden und die Excel-Arbeitsmappe (.xlsx) als E-Mail-Anhang an Ihre ausgewählte Zielgruppe gesendet wird. Durch die Einrichtung eines Zeitplans erhalten die Empfänger und Empfängerinnen automatisch regelmäßige Aktualisierungen. Sie können die Zeitplanfunktion auch verwenden, um die Arbeitsmappe nur einmal zu senden, ohne automatische Aktualisierungen festzulegen.

Für eine Arbeitsmappe können mehrere Zeitpläne erstellt werden. So können Sie beispielsweise eine Arbeitsmappe täglich an Ihr Team und einmal wöchentlich an Ihren Vorgesetzten senden, indem Sie zwei verschiedene Zeitpläne erstellen.

Außerdem können Sie mit der Zeitplanfunktion einen Passwortschutz für eine Arbeitsmappe einrichten und zuvor geplante Arbeitsmappen bearbeiten.


>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Arbeitsmappen planen](https://video.tv.adobe.com/v/3413079?quality=12&learn=on){target="_blank"} für ein Demovideo.

>[!ENDSHADEBOX]


## Festlegen eines Zeitplans für eine Arbeitsmappe

So planen Sie eine Arbeitsmappe:

1. Wählen Sie **[!UICONTROL Zeitplan]** im Report Builder-Hub aus, um einen Zeitplan zu erstellen, damit Sie automatisch eine Excel-Arbeitsmappe (.xlsx) an eine Einzelperson oder eine Gruppe verteilen können.

   ![Wählen Sie die Schaltfläche „Zeitplan“, um einen Zeitplan zu erstellen.](./assets/schedule.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Arbeitsmappe planen]** oder ![Hinzufügen](/help/assets/icons/Add.svg), um eine neue geplante Arbeitsmappe zu erstellen.

   ![Das Fenster „Arbeitsmappen planen“.](./assets/schedule-workbook.png){zoomable="yes"}

   Im Zeitplanfenster werden einige vordefinierte Informationen zur Arbeitsmappe angezeigt, z. B. der Arbeitsmappenname und das Datum der letzten Änderung der Arbeitsmappe.

### Datei

Im Abschnitt **[!UICONTROL Datei]** geben Sie Details zum Dateityp, zum Dateinamen und zu einem Kennwort zum Schutz der Datei an.

![Der Zeitplanbereich.](./assets/schedule-pane.png){zoomable="yes"}

1. Verwenden ![TableSelect](/help/assets/icons/TableSelect.svg), um die aktuelle Arbeitsmappe auszuwählen, falls noch nicht ausgewählt.

1. (Optional) Geben Sie einen **[!UICONTROL Dateinamen]** ein.

   Der Dateiname der Arbeitsmappe entspricht standardmäßig dem Namen der Arbeitsmappe. Sie können den Dateinamen jedoch bei Bedarf ändern.

1. Wählen Sie einen **[!UICONTROL Dateityp]** aus.

   * **[!UICONTROL Excel]**
   * **[!UICONTROL PDF]**
   * **[!UICONTROL CSV]**

   Beachten Sie bei Auswahl **[!UICONTROL CSV]**, dass die geplante Arbeitsmappe als ZIP-Anlage gesendet wird. Einige E-Mail-Administratoren im Unternehmen blockieren möglicherweise E-Mails mit ZIP-Anhängen. Dementsprechend wird eine Warnung angezeigt.

1. (Optional) Wählen Sie **[!UICONTROL Zeitstempel an Dateinamen anhängen]**.

   Sie können einen Zeitstempel an den Dateinamen anhängen, um das Datum der Aktualisierung der Arbeitsmappe anzugeben. Ein Zeitstempel ist hilfreich, um zu sehen, welche Version einer Arbeitsmappe an einem bestimmten Datum gesendet wurde. Wenn diese Option aktiviert ist, können Sie zwischen folgenden Optionen wählen:

   * **[!UICONTROL ISO-Datumsformat]**, was dazu führt, dass `YYYY-MM-DD` an den Dateinamen angehängt wird.
   * **[!UICONTROL ISO-Datumsformat + Zeitstempel]** was dazu führt, dass `YYYY-MM-DD_HH-MM-SS` an den Dateinamen angehängt wird.

<!-- Does no longer seem to be an option? 
1. (Optional) Select **.zip compression** to compress the file and set up password protection on the file.

    When you make this selection, you're prompted to enter a password to open the file. This is helpful if you have concerns about data security and you want to password protect the workbook. Protecting the file with a password requires you to select **.zip compression**. The password must be at least 8 characters and contain a number and a special character.

    ![Enter a password in the Password protect the workbook field.](./assets/zip-compression.png){zoomable="yes"}{width="55%"}
-->

1. Geben Sie in „Kennwort **[!UICONTROL die Arbeitsmappe schützen“ ein]** ein. Ein gültiges Kennwort muss mindestens 8 Zeichen, eine Zahl und ein Sonderzeichen enthalten. Wählen Sie ![VisibilityOff](/help/assets/icons/VisibilityOff.svg) aus, um das Kennwort anzuzeigen, und ![Visibility](/help/assets/icons/Visibility.svg), um das Kennwort auszublenden (Standard).


### E-Mail

Im Abschnitt **[!UICONTROL E-Mail]** geben Sie die Empfänger, den Betreff und die Beschreibung der E-Mail an.

![E-Mail-Einstellungen planen](assets/schedule-email.png){zoomable="yes"}

1. Eingeben der **Empfänger und Empfängerinnen**. Sie können den Namen einer in Ihrem Unternehmen bekannten Person eingeben. Sie können auch eine E-Mail-Adresse einer Person eingeben, die nicht zu Ihrem Unternehmen gehört.

1. Geben Sie den **Betreff** Ihrer E-Mail und eine Beschreibung ein. Der Betreff verwendet standardmäßig den Namen der Arbeitsmappen-Datei. Sie können den Betreff jedoch bei Bedarf ändern. Im Beschreibungsabschnitt können Sie Informationen hinzufügen.

1. Sie können optional eine Beschreibung im Textbereich **[!UICONTROL Beschreibung]** eingeben.


### Zeitplan

Im Abschnitt **[!UICONTROL Zeitplan]** können Sie den Zeitplan definieren, nach dem die E-Mails mit der Arbeitsmappe an Ihre Empfänger gesendet werden sollen.

![Zeitplandefinition](assets/schedule-enable.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Planungsoptionen anzeigen]**, um einen Zeitplan zu definieren.

1. Geben Sie in &quot;**[!UICONTROL am“ ein]** ein. Wählen Sie alternativ ![Kalender](/help/assets/icons/Calendar.svg) aus, um ein Startdatum aus dem Kalender auszuwählen.

1. Geben Sie in „Endet am **[!UICONTROL ein Enddatum]**. Wählen Sie alternativ ![Kalender](/help/assets/icons/Calendar.svg) aus, um ein Enddatum aus dem Kalender auszuwählen.

1. Wählen Sie eine **[!UICONTROL Häufigkeit]** aus. Je nach ausgewählter Häufigkeit stehen Ihnen zusätzliche Optionen zur Verfügung. Siehe Tabelle unten.

   | Häufigkeit | Optionen |
   |---|---|
   | **[!UICONTROL Stündlich senden]** | Geben Sie einen Wert für **[!UICONTROL Alle Stunden senden]** ein. |
   | **[!UICONTROL Täglich senden]** | Wählen Sie eine **[!UICONTROL Tägliche Häufigkeit]** aus: **[!UICONTROL Täglich senden]**, **[!UICONTROL Täglich senden]** oder **[!UICONTROL Benutzerdefinierte Häufigkeit]**.<br/>Wenn Sie **[!UICONTROL Benutzerdefinierte Häufigkeit]** auswählen, geben Sie einen Wert für **[!UICONTROL Alle Tage senden]** ein. |
   | **[!UICONTROL Wöchentlich senden]** | Geben Sie einen Wert für **[!UICONTROL Nach jeder Anzahl von Wochen senden]** ein. und wählen Sie einen **[!UICONTROL Wochentag]**. |
   | **[!UICONTROL Monatlich nach Wochentag senden]** | Wählen Sie einen **[!UICONTROL Wochentag]** und eine **[!UICONTROL Woche des Monats]** aus. |
   | **[!UICONTROL Monatlich nach Tag des Monats senden]** | Wählen Sie einen Wert unter **[!UICONTROL An diesem Tag des Monats senden]** aus. |
   | **[!UICONTROL Jährlich nach Tag des Monats senden]** | Wählen Sie einen **[!UICONTROL Wochentag]**, eine **[!UICONTROL Woche des Monats]** und einen **[!UICONTROL Monatstag des Jahres]** aus. |
   | **[!UICONTROL Jährlich nach bestimmtem Datum senden]** | Wählen Sie einen **[!UICONTROL Monat des Jahres]** und wählen Sie einen Wert aus **[!UICONTROL An diesem Tag des Monats senden]**. |

### Senden

So senden Sie die Arbeitsmappe:

* Wenn Sie keinen Zeitplan mit **[!UICONTROL Planungsoptionen anzeigen]** definiert haben, wählen Sie **[!UICONTROL Jetzt senden]** aus, um die Arbeitsmappe sofort per E-Mail zu senden.
* Wenn Sie einen Zeitplan mit **[!UICONTROL Planungsoptionen anzeigen]** definiert haben, wählen Sie **[!UICONTROL Planmäßig senden]** aus, um die Arbeitsmappe mithilfe des von Ihnen definierten Zeitplans per E-Mail zu senden.

In beiden Fällen wird unten im Report Builder-Hub ein Bestätigungsfoast angezeigt.

Um den Versand der Arbeitsmappe abzubrechen, wählen Sie **[!UICONTROL Abbrechen]** aus.

## Verwalten von geplanten Arbeitsmappen

Informationen zum Verwalten von bereits geplanten Arbeitsmappen finden Sie unter [Verwalten geplanter Arbeitsmappen](/help/analyze/report-builder/manage-reportbuilder.md).




<!--

## Schedule a workbook

Use the Schedule button in the Report Builder hub to quickly create a schedule so that you can automatically distribute a workbook Excel file (.xlsx) to an individual or a group.

1. Click the Schedule button in the Report Builder hub.

    ![Click the Schedule button to create a schedule.](./assets/schedule-button.png){width="55%"}

1. Click Schedule Workbook or the plus button in the upper-left to create a new scheduled workbook.

    ![The Schedule workbooks window.](./assets/schedule-workbook.png){width="55%"}

    The scheduling pane displays some pre-defined information about the workbook such as the workbook name and the last date that the workbook was modified.

    ![The scheduling pane.](./assets/schedule-pane.png){width="55%"}

1. (Optional) Enter a file name.

    The workbook file name defaults to the name of the workbook but you can change this if you want. If you\'re sending the same workbook to multiple audiences and you want to name it something a little bit more friendly for a certain audience, you can change the name.

1. (Optional) Select **Append time-stamp to file name**.

    You can append a timestamp to the file name to identify the date the workbook was updated. This is helpful to quickly see which version of a workbook was sent on a specific date. The **Filename preview** shows how the workbook file name will appear in the email when the workbook is distributed. The time-stamp format is YYYY-MM-DD.

1. (Optional) Select **.zip compression** to compress the file and set up password protection on the file.

    When you make this selection, you're prompted to enter a password to open the file. This is helpful if you have concerns about data security and you want to password protect the workbook. Protecting the file with a password requires you to select **.zip compression**. The password must be at least 8 characters and contain a number and a special character.

    ![Enter a password in the Password protect the workbook field.](./assets/zip-compression.png){width="55%"}

1. Enter **Recipients**. You can enter the name of a person that is recognized in your organization, or you can enter an email address of a person inside or outside of your organization.

1. Enter the **Subject** of the email and a description for your recipients. The subject defaults to the workbook file name but you can modify the subject if needed. You can add details in the description section.

    ![Enter a subject in the Subject field.](./assets/recipients-subject.png){width="55%"}

1. Set up the scheduling options to set the date and time that you want the workbook emailed to your recipients.

    Choose the start and end date and time frames. This can be today's date or a date in the future.

    Choose the **Frequency** from the drop-down menu. You can set the frequency to be hourly, daily, weekly, monthly, or yearly on a specific day. For example, you can set up a schedule to send the workbook on the first Sunday night of the month so that your recipients will have the email in their inbox first thing on Monday morning.

    ![Select the frequency to schedule your report.](./assets/frequency.png){width="55%"}

1. After you set the schedule, click **Send on schedule**.

    ![Click Send on schedule.](./assets/send-on-schedule.png){width="55%"}

    You see a confirmation toast at the bottom of the Report Builder hub and the scheduled workbook is listed under the Workbooks tab.

    ![Confirmation toast](./assets/confirmation-toast.png){width="55%"}

## Schedule a converted workbook {#converted}

1. Schedule a [converted](/help/analyze/report-builder/convert-workbooks.md) legacy workbook.

   A pop up appears, asking if you want to use the scheduling metada from the legacy workbook to create a new scheduled task. 

1. If you select **[!UICONTROL Use]**, Report Builder automatically fills in the legacy scheduling information. 

1. Ensure that this information is correct and schedule. 

1. If you want to send the workbook on a different schedule, schedule a completely fresh scheduled task. 


## Send the workbook one-time only

You can also send out the workbook only once.

1. Un-check **Show scheduling options** 

    ![Click Un-check Show scheduling options to send out a workbook one time.](./assets/send-now.png){width="40%"}

1. Click **Send Now**.

## Manage scheduled workbooks

For information about managing workbooks that are already scheduled, see [Manage scheduled workbooks](/help/analyze/report-builder/manage-schedules-reportbuilder.md).

-->