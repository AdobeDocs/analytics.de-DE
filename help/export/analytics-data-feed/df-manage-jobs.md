---
title: Verwalten von Daten-Feed-Aufträgen
description: Erfahren Sie, wie Sie einzelne Aufträge in Daten-Feeds verwalten. Navigieren Sie in der -Benutzeroberfläche, verwenden Sie Filter und suchen Sie nach Spaltendefinitionen.
feature: Data Feeds
exl-id: b17e333e-290f-42e4-b304-1e34282237a7
source-git-commit: 728e807764901ad2bd6834339e5e75348dd5a988
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 30%

---

# Verwalten von Daten-Feed-Aufträgen

Aufträge sind einzelne Aufgaben, die eine komprimierte Datei ausgeben. Sie werden von Feeds erstellt und verwaltet.

So verwalten Sie Daten-Feed-Aufträge:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.

1. Wählen Sie oben rechts das 9-Quadrat-Symbol und dann [!UICONTROL **Analytics**] aus.

1. Navigieren Sie in der oberen Navigationsleiste zu [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**].

   Es werden Daten-Feeds für alle Report Suites angezeigt, auf die Sie Zugriff haben. Wenn keine Feeds konfiguriert wurden, zeigt die Seite die Schaltfläche [!UICONTROL Neuen Daten-Feed erstellen] an.

   ![Daten-Feed-Manager](assets/data-feed-manager.png)

1. (Optional) Aktivieren Sie das Kontrollkästchen neben dem Daten-Feed, der die Aufträge enthält, die Sie anzeigen möchten, und wählen Sie dann [!UICONTROL **Auftragsverlauf**] aus.

   Weitere Informationen finden Sie unter [Anzeigen des Auftragsverlaufs für einen Daten-Feed](#view-job-history-for-a-data-feed).

## Filtern und Suchen

Sie können nach dem gewünschten Auftrag filtern und suchen.

Klicken Sie ganz links auf das Filtersymbol, um die Filteroptionen ein- oder auszublenden. Filter sind nach Kategorie geordnet. Klicken Sie auf das Chevron, um die Filterkategorien ein- oder auszublenden. Aktivieren Sie das Kontrollkästchen, um einen Filter anzuwenden.

![Filter](assets/jobs-filter.png)

Suchen Sie nach einem Auftrag anhand des Namens.

![Durchsuchen](assets/search.png)

## Sortieren und Anpassen von Spalten

Jeder Auftrag enthält mehrere Spalten mit Informationen zum Auftrag. Sie können die Informationen in den einzelnen Spalten sortieren und die angezeigten Spalten anpassen.

### Sortierungsspalten

Spaltenüberschrift auswählen, um sie in aufsteigender Reihenfolge zu sortieren. Wählen Sie eine Spaltenüberschrift erneut aus, um sie in absteigender Reihenfolge zu sortieren.

### Spalten anpassen

So passen Sie die sichtbaren Spalten in der Tabelle an:

1. Wählen Sie oben ![&#x200B; das Spaltensymbol &#x200B;](assets/customize-columns-icon.png)Spaltensymbol) aus.

1. Wählen Sie im Dialogfeld Tabelle anpassen jede Spalte aus, die Sie anzeigen möchten, und heben Sie die Auswahl für jede Spalte auf, die Sie ausblenden möchten.

   Die folgenden Spalten sind verfügbar:

* **Feed-**: Erforderliche Spalte. Zeigt den Feed-Namen an. Von demselben Feed erstellte Vorgänge haben denselben Feed-Namen.
* **Feed-ID**: Zeigt die Feed-ID an, eine eindeutige Kennung. Aufträge, die von demselben Feed erstellt werden, haben dieselbe Feed-ID.
* **Report Suite**: Die Report Suite, aus der der Vorgang auf Daten verweist.
* **Report Suite-**: Die eindeutige Kennung der Report Suite.
* **Intervall**: Das Intervall des Feeds.
* **Zieltyp**: Der Zieltyp des Feeds.
* **Ziel**: Das Ziel des Feeds.
* **Inhaber**: Der Besitzer des Feeds.
* **Status:** Der Status des Feeds.
   * Warten auf Daten: Der Auftrag ist betriebsfähig, und Daten für das Berichtsfenster werden erfasst.
   * In Verarbeitung: Der Auftrag erstellt die Datendateien und bereitet das Senden dieser Dateien vor.
   * Abgeschlossen: Der Auftrag wurde ohne Probleme abgeschlossen.
   * Fehlgeschlagen: Der Auftrag wurde nicht abgeschlossen. Informationen zur Ermittlung der Fehlerursache finden Sie unter [Fehlerbehebung bei Daten-Feeds](troubleshooting.md).
   * Warten auf Export: Die Daten für das Berichtsfenster wurden noch nicht vollständig verarbeitet.
   * Keine Daten: Die Report Suite enthält für das angeforderte Berichtsfenster keine Daten.
* **Zuletzt geändert**: Die Zeit, zu der der Feed zuletzt geändert wurde.
* **Startdatum**: Die Zeit, zu der der Auftrag gestartet wurde. Datum und Uhrzeit werden in der Zeitzone der Report Suite mit GMT-Verschiebung angezeigt. Tägliche Feeds beginnen üblicherweise gegen Mitternacht in der Zeitzone der Report Suite.
* **Enddatum**: Die Zeit, zu der der Auftrag beendet wurde. Datum und Uhrzeit werden in der Zeitzone der Report Suite mit GMT-Verschiebung angezeigt.

## Anzeigen des Vorgangsverlaufs für einen Daten-Feed

Sie können eine Liste vergangener Daten-Feed-Aufträge für einen bestimmten Daten-Feed zusammen mit Informationen zu jedem Auftrag anzeigen.

So zeigen Sie den Vorgangsverlauf für einen Daten-Feed an:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**].

   ![Daten-Feed-Manager](assets/data-feed-manager.png)

1. Aktivieren Sie das Kontrollkästchen neben dem Daten-Feed, dessen Vorgangsverlauf Sie anzeigen möchten, und wählen Sie dann [!UICONTROL **Vorgangsverlauf**] aus.

   Der Verlauf des Daten-Feed-Auftrags wird mit den folgenden Informationen zu jedem Auftrag angezeigt (wählen Sie das Spaltensymbol aus, um Spalten hinzuzufügen, die standardmäßig nicht sichtbar sind):

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

Sie können einen Daten-Feed-Auftrag erneut senden, wenn Sie die Daten-Feed-Datei erneut mit denselben Daten und derselben Verarbeitung senden möchten wie ursprünglich. Alternativ können Sie [einen Daten-Feed-Auftrag erneut verarbeiten](#reprocess-data-feed-jobs).

So senden Sie einen oder mehrere Daten-Feed-Aufträge erneut:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**].

1. Aktivieren Sie das Kontrollkästchen neben dem Daten-Feed, der die Aufträge enthält, die Sie erneut senden möchten, und wählen Sie dann [!UICONTROL **Auftragsverlauf**] aus.

1. Aktivieren Sie das Kontrollkästchen neben einem oder mehreren Daten-Feed-Aufträgen und wählen Sie dann **[!UICONTROL Erneut senden]** aus<!-- What does the status need to be? Error, ... -->

   ![Daten-Feed-Auftrag erneut verarbeiten](assets/data-feed-job-resend.png)

## Neuverarbeitung von Daten-Feed-Aufträgen

Sie können die Quelldaten eines Daten-Feed-Auftrags erneut verarbeiten und mit den erneut verarbeiteten Daten senden. Alternativ können Sie [einen Daten-Feed-Auftrag erneut senden](#resend-data-feed-jobs).

Neuverarbeitung eines oder mehrerer Daten-Feed-Aufträge:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**].

1. Aktivieren Sie das Kontrollkästchen neben dem Daten-Feed, der die Aufträge enthält, die Sie erneut verarbeiten möchten, und wählen Sie dann [!UICONTROL **Auftragsverlauf**] aus.

1. Aktivieren Sie das Kontrollkästchen neben einem oder mehreren Daten-Feed-Aufträgen und wählen Sie dann **[!UICONTROL Erneut verarbeiten]** aus<!-- What does the status need to be? Error, ... -->

   ![Daten-Feed-Auftrag erneut verarbeiten](assets/data-feed-job-reprocess.png)
