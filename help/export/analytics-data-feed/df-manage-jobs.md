---
title: Verwalten von Daten-Feed-Aufträgen
description: Erfahren Sie, wie Sie einzelne Aufträge in Daten-Feeds verwalten. Navigieren Sie in der -Benutzeroberfläche, verwenden Sie Filter und suchen Sie nach Spaltendefinitionen.
feature: Data Feeds
exl-id: b17e333e-290f-42e4-b304-1e34282237a7
TQID: 'https://experienceleague.adobe.com/4ACex-y-w3ppGhC1tRX8qH4WeU1NT9ubcJBlhSh9sY0'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
subfeature_v2: id: ede9f3ba-4ee4-4497-9d8e-e9da5848bda0
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 23%

---

# Verwalten von Daten-Feed-Aufträgen {#manage-data-feed-jobs}

Aufträge sind einzelne Aufgaben, die eine komprimierte Datei ausgeben. Sie werden von Feeds erstellt und verwaltet.

Sie können den Vorgangsverlauf für jeden Daten-Feed anzeigen, Vorgänge erneut senden oder Vorgänge erneut verarbeiten.

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_job_history"
>title="Verlauf der Daten-Feed-Aufträge"
>abstract="Auf dieser Seite können Sie eine Liste der Daten-Feed-Aufträge für einen bestimmten Daten-Feed anzeigen. Suchen Sie anhand der Anfrage-ID oder des Anfangsdatums des Anfragezeitraums nach Aufträgen. Informationen zu jedem Auftrag werden in den verfügbaren Spalten angezeigt. Sie können auch einen Auftrag mit denselben Daten erneut senden oder die Quelldaten eines Auftrags erneut verarbeiten, bevor Sie ihn erneut senden."

<!-- markdownlint-enable MD034 -->

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

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**] aus.

1. Aktivieren Sie das Kontrollkästchen neben dem Daten-Feed, der die Aufträge enthält, die Sie erneut senden möchten, und wählen Sie dann [!UICONTROL **Auftragsverlauf**] aus.

1. (Optional) Suchen Sie im Suchfeld nach der Anfrage-ID oder dem Startdatum der Anfrage-Periode, um die Liste der Daten-Feed-Aufträge zu durchsuchen.

1. Aktivieren Sie das Kontrollkästchen neben einem oder mehreren Daten-Feed-Aufträgen und wählen Sie dann **[!UICONTROL Erneut senden]** aus<!-- What does the status need to be? Error, ... -->

   ![Daten-Feed-Auftrag erneut verarbeiten](assets/data-feed-job-resend.png)

## Neuverarbeitung von Daten-Feed-Aufträgen

Wenn Sie einen Daten-Feed-Auftrag erneut verarbeiten, verarbeitet er die Quelldaten eines Daten-Feed-Auftrags erneut und sendet sie erneut mit den erneut verarbeiteten Daten. Alternativ können Sie [einen Daten-Feed-Auftrag erneut senden](#resend-data-feed-jobs).

Neuverarbeitung eines oder mehrerer Daten-Feed-Aufträge:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**] aus.

1. Aktivieren Sie das Kontrollkästchen neben dem Daten-Feed, der die Aufträge enthält, die Sie erneut verarbeiten möchten, und wählen Sie dann [!UICONTROL **Auftragsverlauf**] aus.

1. (Optional) Suchen Sie im Suchfeld nach der Anfrage-ID oder dem Startdatum der Anfrage-Periode, um die Liste der Daten-Feed-Aufträge zu durchsuchen.

1. Aktivieren Sie das Kontrollkästchen neben einem oder mehreren Daten-Feed-Aufträgen und wählen Sie dann **[!UICONTROL Erneut verarbeiten]** aus<!-- What does the status need to be? Error, ... -->

   ![Daten-Feed-Auftrag erneut verarbeiten](assets/data-feed-job-reprocess.png)
