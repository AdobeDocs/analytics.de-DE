---
title: Einstellungen für Report Builder konfigurieren
description: Erfahren Sie, wie Sie Einstellungen für Report Builder konfigurieren.
role: Admin
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: d158ad45-d467-4355-b091-f015bde7a243
TQID: https://experienceleague.adobe.com/aHEmYs37KDXtaoAbFiI6WBCvmdhN0RrMWDl-CeEotKw
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f571897740322c1f10255c54fbf745091752a507
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 24%

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

Mithilfe der Fehlerbehebung und der Behebung von Support-Tickets können Sie Report Builder-Anfragen protokollieren. Im Bedienfeld **[!UICONTROL Report Builder]**:

1. Wählen Sie ![Einstellung](/help/assets/icons/Setting.svg) aus.
1. Wählen Sie **[!UICONTROL Datenblock/Datenblöcke der Report Builder-Anfrage in Web-Konsole protokollieren]**. <br/>Anfragen werden an Ihre Webbrowser-Konsole gesendet. Weitere Informationen finden Sie in der Dokumentation Ihres Webbrowsers zum Öffnen des Konsolenprotokolls als Teil der Entwickler-Tools für Webbrowser.
