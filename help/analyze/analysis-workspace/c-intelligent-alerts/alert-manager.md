---
description: Warnhinweise erstellen, bearbeiten oder löschen.
title: Alert Manager (Analysis Workspace)
feature: Alerts
role: User, Admin
exl-id: c33a9a30-f53f-443c-96b7-6a87d03573c7
source-git-commit: 58e1d3025b455de7fa07037b3b0659330c8324c7
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 6%

---


# Verwalten von Warnhinweisen

Sie können vorhandene Warnhinweise im Warnhinweis-Manager verwalten. Sie können verschiedene Verwaltungsaufgaben für Warnhinweise ausführen, z. B. Tagging, Umbenennen, Löschen usw.

Der Warnhinweis-Manager ähnelt sehr dem [Segment-Manager](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-manage.html?lang=de) und dem [Manager für berechnete Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-manager.html?lang=de).

## Erstellen von Warnhinweisen

So erstellen Sie Warnhinweise vom Warnhinweis-Manager:

1. Wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]** aus, um auf den Warnhinweis-Manager in Adobe Analytics zuzugreifen.

   ![](assets/alert-manager.png)

1. Wählen Sie [!UICONTROL **Hinzufügen**] (oder [!UICONTROL **Neuen Warnhinweis erstellen**] , wenn keine Warnhinweise vorhanden sind).

1. Wählen Sie den Warnhinweistyp aus, der dem zu erstellenden Warnhinweis entspricht:

   * [!UICONTROL **Analytics-Datenwarnung**]: Ein Warnhinweis, der Sie benachrichtigt, wenn in Ihren Daten anormale Ereignisse auftreten.

     Wenn Sie diese Option auswählen, fahren Sie mit [Warnhinweise erstellen](/help/analyze/analysis-workspace/c-intelligent-alerts/alert-builder.md) fort, um weitere Informationen zum Erstellen von Warnhinweisen zu erhalten.

   * [!UICONTROL **Warnung zur Nutzung von Server-Aufrufen**]: Ein Warnhinweis, der Sie über das Risiko oder das Auftreten einer Überschreitung der Daten zur Nutzung und Zusage Ihrer Server-Aufrufe informiert.

     Wenn Sie diese Option auswählen, fahren Sie mit den [Warnhinweisen zur Nutzung von Server-Aufrufen](/help/admin/admin/c-server-call-usage/scu-alerts.md) fort.

     >[!NOTE]
     >
     >Sie müssen Analytics-Administrator oder Benutzer mit der Berechtigung zur Nutzung von Server-Aufrufen sein, um Zugriff auf die Nutzung von Server-Aufrufen zu erhalten.




## Vorhandene Warnungen verwalten

So verwalten Sie vorhandene Warnhinweise im Warnhinweis-Manager:

1. Wählen Sie **[!UICONTROL Komponenten]** > **[!UICONTROL Warnhinweise]** aus, um auf den Warnhinweis-Manager in Adobe Analytics zuzugreifen.

   ![](assets/alert-manager.png)

1. Wählen Sie einen oder mehrere Warnhinweise aus, die Sie verwalten möchten.

   ![](assets/alert-manager-tasks.png)

1. Wählen Sie in der Aktionsleiste eine der folgenden Optionen aus:

   | Aktion | Funktion |
   |---------|----------|
   | [!UICONTROL **Tag**] | Wenden Sie ein Tag auf einen Warnhinweis an. Auf diese Weise können Sie Warnhinweise zur einfachen Verwendung organisieren. |
   | [!UICONTROL **Löschen**] | Löscht den Warnhinweis. |
   | [!UICONTROL **Umbenennen**] | Benennt die Warnung um. |
   | [!UICONTROL **Genehmigen**] | Markieren Sie den Warnhinweis als Genehmigt. |
   | [!UICONTROL **Kopieren**] | Erstellt eine Kopie (Duplikat) des Warnhinweises. |
   | [!UICONTROL **Deaktivieren**] | Deaktiviert eine Warnung, die derzeit aktiviert ist. |
   | [!UICONTROL **Aktivieren**] | Aktiviert einen Warnhinweis, der derzeit deaktiviert ist. |
   | [!UICONTROL **Verlängern**] | Verlängern Sie das Ablaufdatum des Warnhinweises. Dadurch wird das Ablaufdatum ab dem Tag, an dem Sie diese Option ausgewählt haben, auf 1 Jahr verlängert, unabhängig vom ursprünglichen Ablaufdatum. |
   | [!UICONTROL **In CSV exportieren**] | Exportiert den Warnhinweis in eine .CSV-Datei. |
