---
title: Einstellungen für Report Builder konfigurieren
description: Erfahren Sie, wie Sie Einstellungen für Report Builder konfigurieren.
role: Admin
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: d158ad45-d467-4355-b091-f015bde7a243
TQID: https://experienceleague.adobe.com/aHEmYs37KDXtaoAbFiI6WBCvmdhN0RrMWDl-CeEotKw
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 257
ht-degree: 29%

---

# Report Builder-Einstellungen


Verwenden Sie den Bereich **Einstellungen**, um Einstellungen auf Anwendungsebene zu konfigurieren, z. B. die von der UI angezeigte Sprache oder ob das Arbeiten im Offline-Modus möglich sein soll oder nicht. Die Einstellungen gelten sofort und sind für alle zukünftigen Sitzungen festgelegt, bis sie geändert werden.

So ändern Sie die Report Builder-Einstellungen

1. Wählen Sie das Symbol **Einstellungen** aus.

1. Nehmen Sie Änderungen an [Aktivieren oder Deaktivieren des Offline-](#off-line-mode), [Sprache auswählen](#language) oder [Fehlerbehebung aktivieren](#troubleshooting) vor.

1. Wählen Sie **[!UICONTROL Anwenden]** aus.

   ![Datumsbereich von Report Builder mit den Schaltflächen „Abbrechen“ und „Anwenden“.](./assets/report-builder-settings.png){zoomable="yes"}

## Offline-Modus

Wenn Sie einen Datenblock im Offline-Modus erstellen und bearbeiten, werden keine Daten abgerufen. Stattdessen werden Simulationsdaten verwendet, damit Sie schnell arbeiten können, ohne auf die Ausführung der Anfrage zu warten. Wenn Sie wieder online sind, wählen Sie ![Aktualisieren](/help/assets/icons/Refresh.svg) **[!UICONTROL Datenblock aktualisieren]** oder ![DocumentRefresh](/help/assets/icons/DocumentRefresh.svg) **[!UICONTROL Alle Datenblöcke aktualisieren]**, um die Datenblöcke mit den tatsächlichen Daten zu aktualisieren.

So aktivieren Sie den Offline-Modus

1. Wählen Sie ![Einstellung](/help/assets/icons/Setting.svg) aus.

1. Schalten Sie **[!UICONTROL Offline-Modus aktivieren]** ein.

1. Geben Sie eine positive Ganzzahl in das Feld **[!UICONTROL Metrikdaten anzeigen]** als ein.

1. Wählen Sie **[!UICONTROL Anwenden]** aus.


## Sprache

Sie können die Sprache für die Benutzeroberfläche von Report Builder auswählen. Alle unterstützten Customer Journey Analytics-Sprachen sind verfügbar.

So wählen Sie die in der Benutzeroberfläche von Report Builder verwendete Sprache aus:

1. Wählen Sie eine Sprache aus **[!UICONTROL Dropdown-Menü]** Sprache“ aus.

1. Wählen Sie **Apply.**

## Fehlerbehebung

Die Einstellung **[!UICONTROL Fehlerbehebungsprotokolle]** protokolliert alle Client/Server-Daten in einer lokalen Datei. Verwenden Sie diese Option, um Support-Tickets zu klären.

Um die Fehlerbehebungsprotokolle zu aktivieren, aktivieren Sie **[!UICONTROL Report Builder-Anfrage in lokaler Datei protokollieren]**.

<!--
Use the **Settings** pane to configure application-level settings such as the language displayed by the UI or whether or not to work in off-line mode. The settings are applied immediately and they are set for all future sessions until they're changed.

To change Report Builder settings

1. Click the **Settings** icon.

1. Make changes to Enable off-line mode, select a Language, or enable Troubleshooting log settings.

1. Click **Apply**.

    ![Report Builder settings.](./assets/image38.png)

## Off-line mode

When creating and editing a data block in off-line mode, data is not retrieved. Instead, simulation data is used so that you can quickly create and edit a data block without waiting for the request to run. When you are back online, the *Refresh data block* command or *Refresh all data blocks* command refreshes the data blocks that you created with actual data.

To enable off-line mode

1. Click the **[!UICONTROL Settings]** icon.

1. Select **[!UICONTROL Enable off-line mod]e**.

1. Enter a positive integer in the **[!UICONTROL Display metric data as]** field.

1. Click **[!UICONTROL Apply]**.

## Language

You can choose the language for the Report Builder UI. All supported Adobe Analytics languages are available.

To select the language used in the Report Builder UI

 1. Click Settings.

 1. Select a language from the **[!UICONTROL Language]** drop down menu.

     ![Report Builder date range pane showing the Language list with English selected.](./assets/image39.png)

 1. Click **[!UICONTROL Apply].**

## Troubleshooting

Use the Troubleshooting setting to log all client/server data to a local file. Use this option to help resolve support tickets.

To enable the Troubleshooting option, select **[!UICONTROL Log report builder data block to web console]**.
-->