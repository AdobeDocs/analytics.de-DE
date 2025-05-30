---
title: Konfigurieren der Einstellungen für den Report Builder in Adobe Analytics
description: Beschreibt, wie Einstellungen für Offline-Modus, Sprache, Datum und Fehlerbehebung festgelegt werden.
role: Admin
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: d158ad45-d467-4355-b091-f015bde7a243
source-git-commit: ec14dde5b0e91a9fcfb217a811d36af2eea5f772
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 83%

---

# Report Builder-Einstellungen

Verwenden Sie den Bereich **Einstellungen**, um Einstellungen auf Anwendungsebene zu konfigurieren, z. B. die von der UI angezeigte Sprache oder ob das Arbeiten im Offline-Modus möglich sein soll oder nicht. Die Einstellungen gelten sofort und sind für alle zukünftigen Sitzungen festgelegt, bis sie geändert werden.

So ändern Sie die Report Builder-Einstellungen

1. Klicken Sie auf das Symbol **Einstellungen**.

1. Nehmen Sie Änderungen vor, sodass der Offline-Modus aktiviert ist, wählen Sie eine Sprache aus oder aktivieren Sie die Fehlerbehebungs-Protokolleinstellungen.

1. Klicken Sie auf **Anwenden**.

   ![Report Builder-Einstellungen.](./assets/image38.png)

## Offline-Modus

Beim Erstellen und Bearbeiten eines Datenblocks im Offline-Modus werden keine Daten abgerufen. Stattdessen werden Simulationsdaten verwendet, damit Sie schnell einen Datenblock erstellen und bearbeiten können, ohne auf die Ausführung der Anfrage warten zu müssen. Wenn Sie wieder online sind, aktualisiert der Befehl *Datenblock aktualisieren* oder *Alle Datenblöcke aktualisieren* die von Ihnen erstellten Datenblöcke mit den tatsächlichen Daten.

So aktivieren Sie den Offline-Modus

1. Klicken Sie auf das Symbol **[!UICONTROL Einstellungen]**.

1. Wählen Sie **[!UICONTROL Offline-Modus aktivieren]e** aus.

1. Geben Sie eine positive Ganzzahl in das Feld **[!UICONTROL Metrikdaten anzeigen als]** ein.

1. Klicken Sie auf **[!UICONTROL Anwenden]**.

## Sprache

Sie können die Sprache für die UI von Report Builder auswählen. Alle unterstützten Adobe Analytics-Sprachen sind verfügbar.

So wählen Sie die in der UI von Report Builder verwendete Sprache aus

1. Klicken Sie auf Einstellungen.

1. Wählen Sie eine Sprache aus dem Dropdown-Menü **[!UICONTROL Sprache]** aus.

   Datumsbereich des Report Builders ![mit Sprachliste und ausgewähltem Englisch.](./assets/image39.png)

1. Klicken Sie **[!UICONTROL Apply].**

## Fehlerbehebung

Verwenden Sie die Einstellung „Fehlerbehebung“, um alle Client-/Server-Daten in einer lokalen Datei zu protokollieren. Verwenden Sie diese Option, um Support-Tickets zu klären.

Um die Option „Fehlerbehebung“ zu aktivieren, wählen Sie **[!UICONTROL Report Builder-Datenblock in Web-Konsole protokollieren]**.
