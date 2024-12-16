---
description: Warnhinweise verwalten.
title: Übersicht über den Warnhinweis-Manager
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 86580b3c149c0feb1d70d9ba197cf0810e472586
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 6%

---

# Warnhinweis-Manager

Sie können vorhandene Warnhinweise im Warnhinweis-Manager verwalten. Sie können verschiedene Verwaltungsaufgaben für Warnhinweise ausführen, z. B. Taggen, Umbenennen, Löschen und mehr.

Der Warnhinweis-Manager ist ähnlich wie der [Segment-Manager](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=de) und der [Manager für berechnete Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=de) strukturiert.

![](assets/alert-manager.png)

## Erstellen von Warnhinweisen

So erstellen Sie Warnhinweise über den Warnhinweis-Manager:

1. Wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]** aus, um auf die Warnhinweisverwaltung in Adobe Analytics zuzugreifen.

   ![](assets/alert-manager.png)

1. Wählen Sie [!UICONTROL **Hinzufügen**] (oder [!UICONTROL **Neuen Warnhinweis erstellen**], wenn noch keine Warnhinweise vorhanden sind).

1. Wählen Sie den Warnhinweistyp aus, der dem zu erstellenden Warnhinweis entspricht:

   * [!UICONTROL **Analytics-Datenwarnung**] Ein Warnhinweis, der Sie benachrichtigt, wenn abnormale Ereignisse in Ihren Daten auftreten.

     Wenn Sie diese Option wählen, fahren Sie mit [Warnhinweise erstellen](/help/components/c-alerts/alert-builder.md) fort, um weitere Informationen zum Erstellen von Warnhinweisen zu erhalten.

   * [!UICONTROL **Warnhinweis zur Nutzung von Server-Aufrufen**]: Ein Warnhinweis, der Sie über das Risiko oder das Auftreten eines Überschusses in Ihren Daten zur Nutzung und Zusage von Server-Aufrufen informiert.

     Wenn Sie diese Option wählen, fahren Sie mit [Warnhinweisen zur Nutzung von Server-Aufrufen](/help/admin/admin/c-server-call-usage/scu-alerts.md) fort.

     >[!NOTE]
     >
     >Sie müssen ein Analytics-Administrator oder ein Benutzer mit der Berechtigung zur Nutzung von Server-Aufrufen sein, um Zugriff auf die Nutzung von Server-Aufrufen zu erhalten.

## Verwalten vorhandener Warnhinweise

Sie können verschiedene Aktionen für vorhandene Warnhinweise ausführen, z. B. Taggen, Umbenennen, Löschen usw.

So verwalten Sie vorhandene Warnhinweise im Warnhinweis-Manager:

1. Wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]** aus, um auf die Warnhinweisverwaltung in Adobe Analytics zuzugreifen.

   ![](assets/alert-manager.png)

1. Wählen Sie einen oder mehrere Warnhinweise aus, die Sie verwalten möchten.

   ![](assets/alert-manager-tasks.png)

1. Wählen Sie in der Aktionsleiste eine der folgenden Optionen aus:

   | Aktion | Funktion |
   |---------|----------|
   | [!UICONTROL **Tag**] | Anwenden eines Tags auf einen Warnhinweis. Auf diese Weise können Sie Warnhinweise organisieren, um die Verwendung zu vereinfachen. |
   | [!UICONTROL **Löschen**] | Löscht den Warnhinweis |
   | [!UICONTROL **Umbenennen**] | Benennt den Warnhinweis um. |
   | [!UICONTROL **Genehmigen**] | Markieren Sie den Warnhinweis als genehmigt. |
   | [!UICONTROL **Kopieren**] | Erstellt eine Kopie (Duplikat) des Warnhinweises. |
   | [!UICONTROL **Deaktivieren**] | Deaktiviert einen derzeit aktivierten Warnhinweis. |
   | [!UICONTROL **Aktivieren**] | Aktiviert einen derzeit deaktivierten Warnhinweis. |
   | [!UICONTROL **Verlängern**] | Verlängert das Ablaufdatum des Warnhinweises. Dadurch wird das Ablaufdatum auf 1 Jahr ab dem Tag verlängert, den Sie diese Option ausgewählt haben, unabhängig vom ursprünglichen Ablaufdatum. |
   | [!UICONTROL **In CSV exportieren**] | Exportiert den Warnhinweis in eine CSV-Datei. |

## Warnhinweis bearbeiten

So bearbeiten Sie einen vorhandenen Warnhinweis:

1. Wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]** aus, um auf die Warnhinweisverwaltung in Adobe Analytics zuzugreifen.

   ![](assets/alert-manager.png)

1. Wählen Sie den Namen des Warnhinweises in der Spalte [!UICONTROL **Titel und Beschreibung**] aus.

1. Bearbeiten Sie den Warnhinweis nach Bedarf.

   Im Folgenden finden Sie einige Möglichkeiten zur Bearbeitung eines Warnhinweises:

   * Hinzufügen von Warnhinweisen zu anderen Report Suites
   * Beschreibung hinzufügen oder ändern
   * Ändern der Zeitgranularität
   * Ändern der Empfänger
   * Ablaufdatum ändern
   * Metriken und Filter ändern

1. Wählen Sie [!UICONTROL **Speichern**] aus.

## Spalten konfigurieren

Sie können die für jeden Warnhinweis im Warnhinweis-Manager angezeigten Informationen konfigurieren, indem Sie die angezeigten Spalten konfigurieren.

So konfigurieren Sie die sichtbaren Spalten im Warnhinweis-Manager:

1. Wählen Sie in Adobe Analytics die Registerkarte **[!UICONTROL Komponenten]** und dann **[!UICONTROL Warnhinweise]** aus.

1. Klicken Sie in der Warnhinweisverwaltung auf das **Spalten anpassen**-Symbol ![Symbol Spalten anpassen](assets/customize-columns-icon.png) und wählen Sie dann die Spalten aus, die Sie in der Warnhinweisverwaltung anzeigen möchten.

   Die folgenden Spalten sind verfügbar:

   | Spaltentitel | Beschreibung |
   |---|---|
   | Titel und Beschreibung | Diese Werte werden im Warnhinweis-Builder bereitgestellt. Um den Titel und die Beschreibung zu bearbeiten, klicken Sie auf den Titel-Link, um die Warnhinweiserstellung zu öffnen. |
   | Favoriten | Zeigt Sternsymbole neben jedem Warnhinweis an, sodass Sie Warnhinweise als Favoriten markieren können. <!-- For more information, see [Mark calculated metrics as favorites](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md). --> |
   | Typ | Zeigt an, ob es sich bei dem Warnhinweis um einen Warnhinweis zu Analytics-Daten oder zur Nutzung von Server-Aufrufen handelt. |
   | Aktiviert | Zeigt an, ob der Warnhinweis derzeit aktiviert oder deaktiviert ist. |
   | Report Suite | Gibt an, in welcher Report Suite der Warnhinweis zuletzt gespeichert wurde. |
   | Besitzer | Gibt an, wem der Warnhinweis gehört. Wenn Sie kein Administrator sind, können Sie nur Warnhinweise sehen, deren Inhaber Sie sind oder die für Sie freigegeben wurden. |
   | Tags | Zeigt Tags an, die auf den Warnhinweis angewendet wurden, entweder von Ihnen oder von Personen, die den Warnhinweis für Sie freigegeben haben. |
   | Ablaufdatum | Zeigt das Datum und die Uhrzeit an, zu der der Warnhinweis ablaufen soll. |
   | Änderungsdatum | Gibt das Datum an, an dem der Warnhinweis zuletzt geändert wurde. |

   {style="table-layout:auto"}

   <!-- When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul> -->


