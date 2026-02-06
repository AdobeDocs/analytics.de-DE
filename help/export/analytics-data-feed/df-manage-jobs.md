---
title: Verwalten von Daten-Feed-Aufträgen
description: Erfahren Sie, wie Sie einzelne Aufträge in Daten-Feeds verwalten. Navigieren Sie in der -Benutzeroberfläche, verwenden Sie Filter und suchen Sie nach Spaltendefinitionen.
feature: Data Feeds
exl-id: b17e333e-290f-42e4-b304-1e34282237a7
source-git-commit: d042bdb680504fdbf0ba346e5829713e529bd543
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 11%

---

# Verwalten von Daten-Feed-Aufträgen

Aufträge sind einzelne Aufgaben, die eine komprimierte Datei ausgeben. Sie werden von Feeds erstellt und verwaltet.

Sie können den Vorgangsverlauf für jeden Daten-Feed anzeigen, Vorgänge erneut senden oder Vorgänge erneut verarbeiten.

## Anzeigen des Vorgangsverlaufs für einen Daten-Feed

Sie können eine Liste von Daten-Feed-Aufträgen für einen bestimmten Daten-Feed zusammen mit Informationen zu den einzelnen Aufträgen anzeigen.

So zeigen Sie den Vorgangsverlauf für einen Daten-Feed an:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.

1. Wählen Sie oben rechts das 9-Quadrat-Symbol und dann [!UICONTROL **Analytics**] aus.

1. Navigieren Sie in der oberen Navigationsleiste zu [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**].

   Es werden Daten-Feeds für alle Report Suites angezeigt, auf die Sie Zugriff haben. Wenn keine Feeds konfiguriert wurden, zeigt die Seite die Schaltfläche **[!UICONTROL Daten-Feed erstellen]**.

   ![Daten-Feed-Manager](assets/data-feed-manager.png)

1. Aktivieren Sie das Kontrollkästchen neben dem Daten-Feed, der die Aufträge enthält, die Sie anzeigen möchten, und wählen Sie dann [!UICONTROL **Auftragsverlauf**] aus.

   Der Verlauf der Daten-Feed-Aufträge wird mit Informationen zu jedem Auftrag in den verfügbaren Spalten angezeigt.

1. (Optional) Um die sichtbaren Spalten in der Tabelle anzupassen, klicken Sie oben rechts auf das Spaltensymbol ![Spaltensymbol](assets/customize-columns-icon.png) und wählen Sie dann im Dialogfeld Tabelle anpassen jede Spalte aus, die Sie anzeigen möchten, und heben Sie die Auswahl für jede Spalte auf, die Sie ausblenden möchten.

   Die folgenden Spalten sind verfügbar:

   * **[!UICONTROL Beginn des Anfragezeitraums]**

   * **[!UICONTROL Ende des Anforderungszeitraums]**

   * **[!UICONTROL Geplant]**

   * **[!UICONTROL Gestartet]**

   * **[!UICONTROL BEENDET]**

   * **[!UICONTROL Ausführen #]**

   * **[!UICONTROL Status]**

   * **[!UICONTROL Fehlercode]**

   * **[!UICONTROL Fehlermeldung]**

## Erneutes Senden von Daten-Feed-Aufträgen

Wenn Sie einen Daten-Feed-Auftrag erneut senden, sendet er die Daten-Feed-Datei erneut mit denselben Daten und derselben Verarbeitung wie beim ursprünglichen Versand der Datei. Alternativ können Sie [einen Daten-Feed-Auftrag erneut verarbeiten](#reprocess-data-feed-jobs).

So senden Sie einen oder mehrere Daten-Feed-Aufträge erneut:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**].

1. Aktivieren Sie das Kontrollkästchen neben dem Daten-Feed, der die Aufträge enthält, die Sie erneut senden möchten, und wählen Sie dann [!UICONTROL **Auftragsverlauf**] aus.

1. Aktivieren Sie das Kontrollkästchen neben einem oder mehreren Daten-Feed-Aufträgen und wählen Sie dann **[!UICONTROL Erneut senden]** aus<!-- What does the status need to be? Error, ... -->

   ![Daten-Feed-Auftrag erneut verarbeiten](assets/data-feed-job-resend.png)

## Neuverarbeitung von Daten-Feed-Aufträgen

Wenn Sie einen Daten-Feed-Auftrag erneut verarbeiten, verarbeitet er die Quelldaten eines Daten-Feed-Auftrags erneut und sendet sie erneut mit den erneut verarbeiteten Daten. Alternativ können Sie [einen Daten-Feed-Auftrag erneut senden](#resend-data-feed-jobs).

Neuverarbeitung eines oder mehrerer Daten-Feed-Aufträge:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**].

1. Aktivieren Sie das Kontrollkästchen neben dem Daten-Feed, der die Aufträge enthält, die Sie erneut verarbeiten möchten, und wählen Sie dann [!UICONTROL **Auftragsverlauf**] aus.

1. Aktivieren Sie das Kontrollkästchen neben einem oder mehreren Daten-Feed-Aufträgen und wählen Sie dann **[!UICONTROL Erneut verarbeiten]** aus<!-- What does the status need to be? Error, ... -->

   ![Daten-Feed-Auftrag erneut verarbeiten](assets/data-feed-job-reprocess.png)
