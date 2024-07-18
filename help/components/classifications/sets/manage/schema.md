---
title: Klassifizierungssatz-Schema
description: Anzeigen und Bearbeiten des Schemas für einen einzelnen Classification-Satz.
exl-id: 4a7c5bfe-ff2b-4380-af46-435801d73c1e
feature: Classifications
source-git-commit: 95767d10f63e20d5943fa95be3f2fe8f88e67e97
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 43%

---

# Schema

Zeigen Sie die derzeit konfigurierten Classification-Dimensionen für diesen Classification-Satz an.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > Klicken Sie auf den Namen des gewünschten Klassifizierungssatzes > **[!UICONTROL Schema]**

Folgende Schaltflächen sind verfügbar:

<!--* **[!UICONTROL Add]**: Adds an empty row so that you can add a classification dimension to the schema.-->
* **[!UICONTROL Hochladen]**: Manuelles Hochladen von Klassifizierungsdaten für eine oder mehrere Klassifizierungsdimensionen. Die Dateien `JSON`, `CSV`, `TSV` und `TAB` werden unterstützt. Beim Hochladen einer gültigen Datei wird eine Tabellenvorschau der zu klassifizierenden Daten angezeigt.
   * **[!UICONTROL Dateikodierung]**: Wählen Sie mithilfe dieser Dropdown-Liste die korrekte Dateikodierung aus. Zu den gültigen Optionen gehören [!UICONTROL UTF-8] und [!UICONTROL Latin1].
   * **[!UICONTROL Listentrennzeichen]**: Wählen Sie das richtige Listentrennzeichen aus. Wenn Sie eine heruntergeladene Datei oder eine Vorlagendatei verwenden, stellen Sie sicher, dass das [!UICONTROL Listentrennzeichen] hier mit dem [!UICONTROL Listentrennzeichen] übereinstimmt, das beim Herunterladen der Datei verwendet wurde.
   * **[!UICONTROL Anwenden]**: Speichern Sie die hochgeladenen Classification-Daten in den Classification-Satz.

  ![Hochladen eines Klassifizierungssatzes](../../assets/classification-set-upload.png)

* **[!UICONTROL Herunterladen]**: Laden Sie Schlüsselwerte und ihre Classification-Spalten herunter.
   * **[!UICONTROL Zeilen]**: Die maximale Anzahl von Zeilen, die in die herunterzuladene Datei aufgenommen werden sollen.
   * **[!UICONTROL Zeilen herunterladen, die eingingen zwischen]**: Eine Datumsauswahl im Kalender, mit der Sie Schlüsselwerte nach dem Zeitpunkt filtern können, zu dem sie in Berichten angezeigt werden. Wenn in diesem Datumsbereich kein Schlüsselwert erfasst wurde, erscheint er nicht in der heruntergeladenen Datei.
   * **[!UICONTROL Zurückgegebene Daten]**: Eine Dropdown-Liste, mit der Sie in der heruntergeladenen Datei enthaltene Schlüsselwerte anhand der zugehörigen Classification-Daten filtern können.
      * **[!UICONTROL Alle klassifizierten Werte]**: Umfasst Zeilen, in denen in mindestens einer Spalte Klassifizierungsdaten enthalten sind.
      * **[!UICONTROL Alle nicht klassifizierten Werte]**: Umfasst Zeilen, in denen in mindestens einer Spalte Klassifizierungsdaten fehlen.
   * **[!UICONTROL Dateiformat]**: Eine Dropdown-Liste, die das Dateiformat der Download-Datei bestimmt. Die Optionen umfassen [!UICONTROL JSON], [!UICONTROL Kommagetrennte Werte] und [!UICONTROL Tabulatorgetrennte Werte für Excel].
   * **[!UICONTROL Dateikodierung]**: Eine Dropdown-Liste, die die Dateikodierung bestimmt. Die Optionen umfassen [!UICONTROL UTF-8] und [!UICONTROL Latin1]. UTF-8 wird empfohlen.

  ![Herunterladen des Klassifizierungssatzes](../../assets/classification-set-download.png)

* **[!UICONTROL Vorlage]**: Herunterladen einer Vorlagendatei. Diese Datei ähnelt der Datei, die mit der Schaltfläche [!UICONTROL Herunterladen] erhalten wird, mit der Ausnahme, dass sie keine Klassifizierungsdaten oder Schlüsselwerte enthält.
   * **[!UICONTROL Dateiformat]**: Eine Dropdown-Liste, die das Dateiformat der Vorlagendatei bestimmt. Die Optionen umfassen [!UICONTROL Kommagetrennte Werte] und [!UICONTROL Tabulatorgetrennte Werte für Excel].
   * **[!UICONTROL Dateikodierung]**: Eine Dropdown-Liste, die die Dateikodierung bestimmt. Die Optionen umfassen [!UICONTROL UTF-8] und [!UICONTROL Latin1]. UTF-8 wird empfohlen.
   * **[!UICONTROL Listentrennzeichen]**: Eine Dropdownliste, die das Listentrennzeichen zur Trennung von Classification-Spalten für jede Zeile festlegt.

  ![Klassifizierungsset-Vorlage](../../assets/classification-set-template.png)

* **[!UICONTROL Auftragsverlauf]**: Ein Verknüpfungslink, über den Sie zum [Job Manager](../job-manager.md) gelangen und Aufträge nur für diesen Classification-Satz anzeigen.
* **[!UICONTROL Automatisieren]**: Erfassen Sie automatisch Daten von externen Speicherorten.
   * **[!UICONTROL Standortkonto]**: Eine Dropdownliste mit vorhandenen Standortkonten, die von Ihrem Unternehmen konfiguriert wurden. Wenn Ihr Unternehmen noch kein Standortkonto konfiguriert hat, können Sie eines konfigurieren, indem Sie [!UICONTROL **Neues Konto erstellen**] auswählen.

     Informationen zum Konfigurieren des Standortkontos finden Sie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md).

   * **[!UICONTROL Position]**: Eine Dropdownliste mit vorhandenen Speicherorten, die Ihre Organisation konfiguriert hat. Wenn Ihr Unternehmen noch keinen Speicherort konfiguriert hat, können Sie einen konfigurieren, indem Sie [!UICONTROL **Neuen Speicherort erstellen**] auswählen.

     Weitere Informationen zum Konfigurieren eines Standorts finden Sie unter [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md).

   * **[!UICONTROL Trennzeichen]**: Das Spaltentrennzeichen für hochgeladene Dateien. Zu den Optionen gehören [!UICONTROL Komma], [!UICONTROL Semikolon], [!UICONTROL Doppelpunkt], [!UICONTROL Vertikalbalken], [!UICONTROL Leerraum], [!UICONTROL Schrägstrich], [!UICONTROL Abwärtsschrägstrich], [!UICONTROL Bindestrich] oder [!UICONTROL Unterstrich].

   * **[!UICONTROL Kodierung]**: Eine Dropdown-Liste, die die Dateikodierung bestimmt. Die Optionen umfassen [!UICONTROL UTF-8] und [!UICONTROL Latin1]. UTF-8 wird empfohlen.
