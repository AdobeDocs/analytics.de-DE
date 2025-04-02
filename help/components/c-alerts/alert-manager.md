---
description: Verwalten Sie Warnhinweise.
title: Überblick über den Warnhinweis-Manager
feature: Alerts
exl-id: 3408c79f-3d85-44b9-8fca-ce956853dfa4
source-git-commit: 86580b3c149c0feb1d70d9ba197cf0810e472586
workflow-type: ht
source-wordcount: '638'
ht-degree: 100%

---

# Warnhinweis-Manager

Sie können vorhandene Warnhinweise im Warnhinweis-Manager verwalten. Sie können verschiedene Verwaltungsaufgaben für Warnhinweise ausführen, z. B. Tagging, Umbenennen, Löschen und mehr.

Der Warnhinweis-Manager ist ähnlich wie der [Segment-Manager](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=de) und der [Manager für berechnete Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=de) aufgebaut.

![](assets/alert-manager.png)

## Erstellen von Warnhinweisen

So erstellen Sie Warnhinweise über den Warnhinweis-Manager:

1. Wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]** aus, um auf den Warnhinweis-Manager in Adobe Analytics zuzugreifen.

   ![](assets/alert-manager.png)

1. Wählen Sie [!UICONTROL **Hinzufügen**] (oder [!UICONTROL **Neuen Warnhinweis erstellen**], wenn noch keine Warnhinweise vorhanden sind).

1. Wählen Sie den Warnhinweistyp aus, der dem zu erstellenden Warnhinweis entspricht:

   * [!UICONTROL **Warnhinweis zu Analytics-Daten**] Ein Warnhinweis, der Sie benachrichtigt, wenn anormale Ereignisse in Ihren Daten auftreten.

     Wenn Sie diese Option auswählen, fahren Sie mit dem Thema [Erstellen von Warnhinweisen](/help/components/c-alerts/alert-builder.md) fort, um weitere Informationen zum Erstellen von Warnhinweisen zu erhalten.

   * [!UICONTROL **Warnhinweis zur Nutzung von Server-Aufrufen**]: Ein Warnhinweis, der Sie über das Risiko oder das Auftreten einer Überschreitung bei Nutzung und Kontingent von Server-Aufrufen benachrichtigt.

     Wenn Sie diese Option auswählen, fahren Sie mit dem Thema [Warnhinweise zur Nutzung von Server-Aufrufen](/help/admin/admin/c-server-call-usage/scu-alerts.md) fort.

     >[!NOTE]
     >
     >Nur Analytics-Admins oder Benutzende mit der Berechtigung zur Nutzung von Server-Aufrufen haben Zugriff auf die Nutzung von Server-Aufrufen.

## Verwalten vorhandener Warnhinweise

Sie können verschiedene Aktionen für vorhandene Warnhinweise ausführen, z. B. Taggen, Umbenennen, Löschen usw.

So verwalten Sie vorhandene Warnhinweise im Warnhinweis-Manager:

1. Wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]** aus, um auf den Warnhinweis-Manager in Adobe Analytics zuzugreifen.

   ![](assets/alert-manager.png)

1. Wählen Sie einen oder mehrere Warnhinweise aus, die verwaltet werden sollen.

   ![](assets/alert-manager-tasks.png)

1. Wählen Sie in der Aktionsleiste eine der folgenden Optionen aus:

   | Aktion | Funktion |
   |---------|----------|
   | [!UICONTROL **Tag**] | Wendet ein Tag auf einen Warnhinweis an. Dadurch können Sie Warnhinweise zur einfachen Anwendung organisieren. |
   | [!UICONTROL **Löschen**] | Löscht den Warnhinweis. |
   | [!UICONTROL **Umbenennen**] | Benennt den Warnhinweis um. |
   | [!UICONTROL **Genehmigen**] | Markiert den Warnhinweis als genehmigt. |
   | [!UICONTROL **Kopieren**] | Erstellt eine Kopie (ein Duplikat) des Warnhinweises. |
   | [!UICONTROL **Deaktivieren**] | Deaktiviert einen derzeit aktivierten Warnhinweis. |
   | [!UICONTROL **Aktivieren**] | Aktiviert einen derzeit deaktivierten Warnhinweis. |
   | [!UICONTROL **Verlängern**] | Verlängert das Ablaufdatum für einen Warnhinweis. Dadurch wird das Ablaufdatum auf ein Jahr ab dem Tag, an dem diese Option ausgewählt wurde, verlängert, ungeachtet des ursprünglichen Ablaufdatums. |
   | [!UICONTROL **In CSV exportieren**] | Exportiert einen Warnhinweis als CSV-Datei. |

## Bearbeiten eines Warnhinweises

So bearbeiten Sie einen Warnhinweis:

1. Wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]** aus, um auf den Warnhinweis-Manager in Adobe Analytics zuzugreifen.

   ![](assets/alert-manager.png)

1. Wählen Sie den Namen des Warnhinweises in der Spalte [!UICONTROL **Titel und Beschreibung**] aus.

1. Bearbeiten Sie den Warnhinweis nach Bedarf.

   Im Folgenden finden Sie einige Möglichkeiten zur Bearbeitung eines Warnhinweises:

   * Warnhinweise zu anderen Report Suites hinzufügen
   * Beschreibung hinzufügen oder ändern
   * Zeitgranularität ändern
   * Empfängerinnen und Empfänger ändern
   * Ablaufdatum ändern
   * Metriken und Filter ändern

1. Wählen Sie [!UICONTROL **Speichern**] aus.

## Konfigurieren von Spalten

Sie können die für jeden Warnhinweis im Warnhinweis-Manager angezeigten Informationen konfigurieren, indem Sie die angezeigten Spalten konfigurieren.

So konfigurieren Sie die sichtbaren Spalten im Warnhinweis-Manager:

1. Wählen Sie in Adobe Analytics die Registerkarte **[!UICONTROL Komponenten]** und dann **[!UICONTROL Warnhinweise]** aus.

1. Wählen Sie im Warnhinweis-Manager das Symbol **Spalten anpassen** ![Symbol „Spalten anpassen“](assets/customize-columns-icon.png) und dann die Spalten aus, die im Warnhinweis-Manager angezeigt werden sollen.

   Die folgenden Spalten sind verfügbar:

   | Spaltentitel | Beschreibung |
   |---|---|
   | Titel und Beschreibung | Diese Werte werden im Warnhinweis-Generator bereitgestellt. Um den Titel und die Beschreibung zu bearbeiten, wählen Sie den Titel-Link aus. Dadurch wird der Warnhinweis-Generator geöffnet. |
   | Favoriten | Zeigt Sternsymbole neben jedem Warnhinweis an, sodass Sie Warnhinweise als Favoriten markieren können. <!-- For more information, see [Mark calculated metrics as favorites](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-favorite.md). --> |
   | Typ | Zeigt an, ob es sich bei dem Warnhinweis um einen Warnhinweis zu Analytics-Daten oder zur Nutzung von Server-Aufrufen handelt. |
   | Aktiviert | Zeigt an, ob der Warnhinweis derzeit aktiviert oder deaktiviert ist. |
   | Report Suite | Gibt an, in welcher Report Suite der Warnhinweis zuletzt gespeichert wurde. |
   | Inhaberin oder Inhaber | Gibt an, wer für den Warnhinweis verantwortlich ist. Wenn Sie keine Administratorberechtigungen haben, können Sie nur Metriken sehen, die Ihnen gehören, sowie Metriken, die für Sie freigegeben wurden. |
   | Tags | Zeigt Tags an, die entweder durch Sie oder durch Personen, die den Warnhinweis für Sie freigegeben haben, auf den Warnhinweis angewendet wurden. |
   | Ablaufdatum | Zeigt das Datum und die Uhrzeit an, zu denen der Warnhinweis ablaufen soll. |
   | Änderungsdatum | Gibt das Datum an, an dem der Warnhinweis zuletzt geändert wurde. |

   {style="table-layout:auto"}

   <!-- When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul> -->


