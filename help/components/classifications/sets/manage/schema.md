---
title: Schema des Klassifizierungssatzes
description: Erfahren Sie, wie Sie das Schema für einen einzelnen Klassifizierungssatz anzeigen und bearbeiten.
exl-id: 4a7c5bfe-ff2b-4380-af46-435801d73c1e
feature: Classifications
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '1431'
ht-degree: 4%

---

# Klassifizierungssatz-Schema

Das Schema ist die Liste von Klassifizierungen, die Sie auf die Schlüsseldimensionen anwenden möchten, die Sie für den Klassifizierungssatz definiert haben. Wenn Sie beispielsweise Produkt als Schlüsseldimension definiert haben und dieses Feld eine Produkt-SKU enthält, verwenden Sie das Schema, um Klassifizierungen wie Produktname, Produktfarbe, Produktgröße und mehr hinzuzufügen.

So bearbeiten Sie das Schema für einen Klassifizierungssatz:


1. Wählen Sie **[!UICONTROL Komponenten]** in der oberen Menüleiste von Adobe Analytics aus und wählen Sie dann **[!UICONTROL Klassifizierungssätze]**.
1. Wählen **[!UICONTROL unter]** die Registerkarte **[!UICONTROL Klassifizierungssätze]** aus.
1. Wählen **[!UICONTROL Manager Klassifizierungssätze]** Klassifizierungssatz aus, für den Sie das Schema bearbeiten möchten.
1. Wählen Sie **[!UICONTROL Dialogfeld „Klassifizierungssatz _(Klassifizierungssatzname_]**&#x200B;die Registerkarte **[!UICONTROL Schema]**&#x200B;aus. Diese Registerkarte besteht aus den folgenden Elementen der Benutzeroberfläche:

   ![Klassifizierungssätze - Schema](assets/classification-sets-schema.png)

   * [Klassifizierungsliste](#classification-list)
   * [Suche](#search)
   * [Aktionen](#actions)
   * [Aktionsleiste](#action-bar)

## Klassifizierungsliste

Die Liste der Klassifizierungen enthält die folgenden Spalten:

| Spalte | Beschreibung |
|---|---|
| **[!UICONTROL Klassifizierungsname]** | Der von Ihnen für die Klassifizierung angegebene Name. |
| **[!UICONTROL Identitätsname]** | Der abgeleitete Name durch das System für die Klassifizierung. Dies ist ein schreibgeschützter Wert, und Sie können den Identitätsnamen verwenden |
| **[!UICONTROL Klassifiziert nach]** | Falls verwendet, einen Link zum Such-Klassifizierungssatz, der zur Klassifizierung dieser Klassifizierung verwendet wird. |


## Suche

Sie können schnell ![Suchen](/help/assets/icons/Search.svg) nach einer oder mehreren Klassifizierungen suchen. Verwenden Sie ![CrossSize100](/help/assets/icons/CrossSize100.svg), um die Suche zu löschen.

## Aktionen

Die folgenden Aktionen sind als Schaltflächen oben in der Klassifizierungsliste verfügbar:

| Symbol | Aktion | Beschreibung |
|---|---|---|
| ![Hinzufügen](/help/assets/icons/Add.svg) | **[!UICONTROL Hinzufügen]** | [Klassifizierung hinzufügen](#add) zur Liste hinzufügen. |
| ![UploadToCloud](/help/assets/icons/UploadToCloud.svg) | **[!UICONTROL Hochladen]** | [Hochladen einer JSON-, CSV-, TSV- oder TAB-Datei](#upload). |
| ![Herunterladen](/help/assets/icons/Download.svg) | **[!UICONTROL Herunterladen]** | [Herunterladen von Klassifizierungsdaten](#download). |
| ![DocumentFragment](/help/assets/icons/DocumentFragment.svg) | **[!UICONTROL Vorlage]** | [Vorlage herunterladen](#template) für Klassifizierungsdaten. |
| ![Verlauf](/help/assets/icons/History.svg) | **[!UICONTROL Vorgangsverlauf]** | Den [Auftrags-Manager für Klassifizierungssätze](/help/components/classifications/sets/job-manager.md) anzeigen, der nach dem ausgewählten Klassifizierungssatz gefiltert wurde. |
| ![Zahnrad](/help/assets/icons/Gear.svg) | **[!UICONTROL Automate]** | [Automatisieren Sie die Aufnahme von Klassifizierungsdaten](#automate) durch die Verwendung eines Cloud-Speicherorts. |


### Hinzufügen

Um eine neue Klassifizierung hinzuzufügen, wählen Sie ![Hinzufügen](/help/assets/icons/Add.svg) **[!UICONTROL Hinzufügen]** aus.

![Klassifizierungssätze - Hinzufügen einer Klassifizierung zu einem Schema](assets/classification-sets-schema-add-classification.png)

Geben **[!UICONTROL im Dialogfeld Neue Klassifizierung für _Klassifizierungssatzname_]**&#x200B;den **[!UICONTROL Klassifizierungsnamen]**&#x200B;ein und wählen Sie **[!UICONTROL Hinzufügen]**. Die Klassifizierung wird der Liste hinzugefügt.



### Hochladen

Um Klassifizierungsdaten in das Schema für eine Klassifizierung zu importieren, wählen Sie ![UploadToCloud](/help/assets/icons/UploadToCloud.svg) **[!UICONTROL Upload]** aus.


![Klassifizierungssätze - Schema zum Hochladen einer Datei](assets/classification-sets-schema-upload-file.png)

1. Im Dialogfeld **[!UICONTROL Neue Klassifizierungen hinzufügen]**:

   * Ziehen Sie eine Datei, die Klassifizierungsdaten enthält, und legen Sie die Datei auf **[!UICONTROL hier per Drag-and-Drop]**.
   * Wählen Sie **[!UICONTROL Durchsuchen]** und wählen Sie eine Datei von Ihrem Computer oder Netzwerk aus.

   Es wird eine **[!UICONTROL Schemavorschau]** des Inhalts der Datei angezeigt. Die Vorschau zeigt die Datenspalten aus der Datei an. Um die Größe einer Spalte zu ändern, wählen Sie ![ChevronDownSize300](/help/assets/icons2/ChevronDownSize300.svg) und anschließend **[!UICONTROL Spaltengröße ändern]** aus. Es wird ein Ziehgriff angezeigt, mit dem Sie die Größe der Spalte ändern können.

   Wenn im Klassifizierungssatz für eine Spalte keine Klassifizierung definiert ist, wird ein Warnhinweis ![Warnhinweis](/help/assets/icons/Alert.svg) angezeigt. Der Warnhinweis erklärt, dass im vorhandenen Klassifizierungsschemasatz keine Klassifizierung vorhanden ist und beim Import erstellt wird.

1. Wählen Sie **[!UICONTROL Bei Konflikt Daten überschreiben?]**, wenn Sie die aktuellen Klassifizierungsdaten mit den neuen importierten überschreiben möchten. Zum Beispiel:

   | | Schlüssel | Aktuelle Produktfarbe | Datei importieren | Neue Produktfarbe |
   |---|---|---|---|---|
   | ![SelectBox](/help/assets/icons/SelectBox.svg) **[!UICONTROL Daten bei Konflikt überschreiben?]** | 1234 | Grün | Blau | Blau |
   | ![Quadrat](/help/assets/icons2/Square.svg) **[!UICONTROL Daten bei Konflikt überschreiben?]** | 1234 | Grün | Blau | Grün |

1. Wählen Sie **[!UICONTROL Anwenden]** aus. Ein Warnhinweis wird angezeigt, wenn Spalten im vorhandenen Schemasatz nicht als Klassifizierungen vorhanden sind. Diese Spalten werden als neue Klassifizierungen hinzugefügt, wenn Sie den Upload bestätigen.

   ![Klassifizierungssatz - Warnhinweis zum Hochladen von Klassifizierungen](assets/classification-sets-schema-upload-file-preview-alert.png)

   Wählen Sie **[!UICONTROL Upload bestätigen]** aus, um den Upload zu bestätigen. Wählen Sie **[!UICONTROL Upload abbrechen]**, um den Upload abzubrechen.


### Herunterladen

Um Klassifizierungsdaten herunterzuladen, wählen Sie ![Herunterladen](/help/assets/icons/Download.svg) **[!UICONTROL Herunterladen]** aus.

![Klassifizierungssätze - Herunterladen von Klassifizierungsdaten durch Schemas](assets/classification-sets-schema-download-file.png)

Im Dialogfeld **[!UICONTROL Daten für Klassifizierungssatz _Name des Klassifizierungssatzes_]**&#x200B;herunterladen:

1. Geben Sie die Anzahl **[!UICONTROL Zeilen]** ein, die Sie herunterladen möchten. Beispiel: `10000`.
1. Um den Zeitraum auszuwählen, für den Sie Classification-Datenzeilen herunterladen möchten, geben Sie Start- und Enddaten für &quot;**[!UICONTROL Zeilen herunterladen, die zwischen empfangen wurden]** ein. Oder verwenden Sie ![Kalender](/help/assets/icons/Calendar.svg), um ein Kalender-Popup zur Auswahl des Zeitraums zu verwenden.
1. Um auszuwählen, welche Daten zurückgegeben werden sollen, wählen Sie eine Option unter **[!UICONTROL Daten zurückgegeben]** aus.

   * **[!UICONTROL Alle Werte]** gibt alle Werte für die aktuellen Klassifizierungsdaten zurück.
   * **[!UICONTROL Alle Spalten leer]** Gibt eine Spalte mit Schlüsselwerten für die vorhandenen Klassifizierungsdaten zurück. und Spalten ohne Wert für Klassifizierungsdaten, für die keine Werte vorhanden sind.
   * **[!UICONTROL Alle Spalten leer]** gibt eine Schlüsselspalte mit Werten für die vorhandenen Klassifizierungsdaten zurück. und Spalten ohne Wert für Klassifizierungsdaten.
1. Um das [Dateiformat](/help/components/classifications/sets/data-files.md#general-file-requirements) der heruntergeladenen Klassifizierungsdaten auszuwählen, wählen Sie eine Option aus dem Dropdown-Menü **[!UICONTROL Dateiformat]** aus. Die Optionen sind:

   * **[!UICONTROL JSON]**.
   * **[!UICONTROL Kommagetrennte Werte]** (CSV)
   * **[!UICONTROL Tabulatorgetrennte Werte für Excel]** (TSV oder TAB).

1. Um die [Dateicodierung](/help/components/classifications/sets/data-files.md#general-file-requirements) zu wählen, wenn die Datei heruntergeladen wird, wählen Sie eine Option aus dem Dropdown-Menü Dateicodierung aus. Die Optionen sind:

   * **[!UICONTROL UTF-8]**
   * **[!UICONTROL Latin-1]**.


1. Wählen Sie **[!UICONTROL Herunterladen]** aus, um die Klassifizierungsdaten herunterzuladen. Sie finden die heruntergeladene Datei im Standard-Download-Verzeichnis Ihres Browsers und die Datei heißt <code><i>Klassifizierungssatz</i>.<i>json</i>|<i>csv</i>|<i>tsv</i></code>  Wenn die Datei bereits vorhanden ist, eine Sequenznummer <code>(<i>x</i>)</code> wird dem Dateinamen hinzugefügt.<br/>Wenn Sie Optionen angegeben haben, die keine Daten zurückgeben, wird ein Dialogfeld **[!UICONTROL Hinweis]** angezeigt, in dem Sie darüber informiert werden, die Optionen für den Datumsbereich und die zurückgegebenen Daten zu ändern.


### Vorlage

Um eine Vorlage für Klassifizierungsdaten herunterzuladen, wählen Sie ![DocumentFragment](/help/assets/icons/DocumentFragment.svg) **[!UICONTROL Template]** aus.

![Schema für Klassifizierungssätze - Vorlage herunterladen](assets/classification-sets-schema-download-template.png)

Im Dialogfeld **[!UICONTROL Vorlage für Klassifizierungssatz _herunterladen_]**:

1. Um das [Dateiformat](/help/components/classifications/sets/data-files.md#general-file-requirements) der heruntergeladenen Klassifizierungsdaten auszuwählen, wählen Sie eine Option aus dem Dropdown-Menü **[!UICONTROL Dateiformat]** aus. Die Optionen sind:

   * **[!UICONTROL Kommagetrennte Werte]**.
   * **[!UICONTROL Tabulatorgetrennte Werte für Excel]**.

1. Um die [Dateicodierung](/help/components/classifications/sets/data-files.md#general-file-requirements) zu wählen, wenn die Datei heruntergeladen wird, wählen Sie eine Option aus dem Dropdown-Menü Dateicodierung aus. Die Optionen sind:

   * **[!UICONTROL UTF-8]**
   * **[!UICONTROL Latin-1]**.

1. Wählen Sie **[!UICONTROL Herunterladen]** aus, um die Klassifizierungsdatenvorlage herunterzuladen. Sie finden die heruntergeladene Datei im Standard-Download-Verzeichnis Ihres Browsers mit dem Titel <code><i>Klassifizierungssatz</i>.<i>CSV</i>|<i>TSV</i></code>  Wenn die Datei bereits vorhanden ist, eine Sequenznummer <code>(<i>x</i>)</code> wird dem Dateinamen hinzugefügt.


### Automate

Um die Aufnahme der Klassifizierung zu automatisieren, wählen Sie ![Zahnrad](/help/assets/icons/Gear.svg) **[!UICONTROL Automatisieren]**.

![Schema für Klassifizierungssätze - Automatisieren](assets/classification-sets-schema-automate.png)

Im Dialogfeld **[!UICONTROL Aufnahme-Speicherort zuordnen/aktualisieren _Klassifizierungssatzname_]**:

1. Um einen Cloud-Speicherort auszuwählen, wählen Sie eine Option aus **[!UICONTROL Speicherort-Konto]**. Es [&#x200B; nur (Speicherort-Konten unterstützter Kontotypen angezeigt, die den Import von Klassifizierungsdaten &#x200B;](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-accounts). Um ein neues Konto zu erstellen, wählen Sie **[!UICONTROL Neues Konto]** aus.
1. Um einen Speicherort auszuwählen, wählen Sie eine Option aus **[!UICONTROL Speicherort]**. Es werden nur die Standorte der ausgewählten Kontotypen für den Import von Klassifizierungsdaten angezeigt. Um einen neuen Speicherort zu erstellen, wählen Sie **[!UICONTROL Neuer Speicherort]**.

   >[!IMPORTANT]
   >
   >Der Speicherort, den Sie erstellen oder auswählen, sollte ein **[!UICONTROL Präfix]** (Ordner) innerhalb des **[!UICONTROL Buckets]** enthalten, um die Klassifizierungsdatendateien zu hosten. Beispiel: ein Ordner mit dem Namen `files`. Das Hosten von Dateien am Stamm eines Buckets funktioniert nicht mit den meisten Cloud-Speicherorten.
   >

1. Um ein Trennzeichen auszuwählen, wählen Sie eine Option aus dem Dropdown-Menü **[!UICONTROL Listentrennzeichen]** aus. Die Optionen sind:
   * **[!UICONTROL Komma ,]**
   * **[!UICONTROL Semikolon ;]**
   * **[!UICONTROL Doppelpunkt :]**
   * **[!UICONTROL Vertikaler Balken |]**
   * **[!UICONTROL Leerzeichen]**
   * **[!UICONTROL tab]**
1. Um die [Dateicodierung](/help/components/classifications/sets/data-files.md#general-file-requirements) beim Herunterladen der Datei auszuwählen, wählen Sie eine Option aus dem Dropdown-Menü **[!UICONTROL Dateicodierung]** aus. Die Optionen sind:

   * **[!UICONTROL UTF-8]**
   * **[!UICONTROL Latin-1]**.

1. Um Benutzer über den Abschluss von Aufnahmevorgängen zu benachrichtigen, geben Sie E-Mail-Adressen ein, durch Kommata getrennt, **[!UICONTROL E-Mail(s), die benachrichtigt werden sollen, wenn Aufnahmevorgänge abgeschlossen sind (durch Kommata getrennt)]**.
1. Wählen Sie **[!UICONTROL Validieren]** aus. Die Verbindung zum Cloud-Speicherort wird validiert.
1. Wenn die Validierung erfolgreich war, wird eine Popup-Meldung angezeigt, in der die ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg)Location **[!UICONTROL Validierung erfolgreich angezeigt wird. Verbindung mit Cloud-Speicher verifiziert.]**<br/>Wählen Sie&#x200B;**[!UICONTROL &#x200B; Speichern &#x200B;]**, wenn Sie die Verbindung zur Cloud-Verbindung erstellt haben. Wählen Sie andernfalls&#x200B;**[!UICONTROL &#x200B; Aktualisieren &#x200B;]**&#x200B;aus. Oder wählen Sie&#x200B;**[!UICONTROL &#x200B; Abbrechen &#x200B;]**, um die Konfiguration des Cloud-Speicherorts abzubrechen.

Wenn Sie Dateien in den Cloud-Speicherort hochladen, wird die Datei innerhalb von 15 Minuten erkannt und als Importvorgang übermittelt. Das Ergebnis dieses Importvorgangs wird im [Classifications Job Manager“ &#x200B;](/help/components/classifications/sets/job-manager.md). Wenn Sie der Liste der Benutzer hinzugefügt werden, um über den Abschluss von Aufnahmevorgängen zu informieren, erhalten Sie auch E-Mail-Nachrichten.

Zum Beispiel:

![Klassifizierungssätze - E-Mail zur Auftragsvalidierung](assets/job-failed-validation.png){width="400"}


## Aktionsleiste

In der Aktionsleiste werden die für die ausgewählte Klassifizierung verfügbaren Aktionen angezeigt. Verfügbare Optionen sind:

| Symbol | Aktion | Beschreibung |
|---|---|---|
| ![Durchsuchen](/help/assets/icons/Browse.svg) | **[!UICONTROL Suche hinzufügen]** | Fügen Sie einen Klassifizierungssatz als Suche hinzu (Unterklassifizierung).<br/>In der **[!UICONTROL Lookup anhängen]**-Tabelle: <ol><li>Wählen Sie im Dropdown-Menü **[!UICONTROL Klassifizierungsname]** eine Suchklassifizierung aus.</li><li>Wählen Sie **[!UICONTROL Hinzufügen]** aus.</li></ol>Die Lookup-Klassifizierung wird zur Klassifizierung hinzugefügt und in der Spalte **[!UICONTROL Klassifiziert nach]** mit der internen ID aufgeführt. |
| ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) | **[!UICONTROL Suche entfernen]** | Entfernen Sie einen Klassifizierungssatz als Suche. Um die Suche dauerhaft aus der Klassifizierung zu löschen, klicken Sie im Bestätigungsdialogfeld **[!UICONTROL _Klassifizierungssatz entfernen_ aus _Klassifizierung_]**&#x200B;auf **[!UICONTROL Löschen]**. |
| ![Umbenennen](/help/assets/icons/Rename.svg) | **[!UICONTROL Umbenennen]** | Benennen Sie **[!UICONTROL Klassifizierungsname]** einer Klassifizierung um. Geben **[!UICONTROL im Dialogfeld &quot;_: (Klassifizierungsname_]**&#x200B;einen neuen Namen ein und wählen Sie **[!UICONTROL Umbenennen]**. |
| ![Löschen](/help/assets/icons/Delete.svg) | **[!UICONTROL Löschen]** | Löschen einer Klassifizierung. Das **[!UICONTROL Löschen _Klassifizierungsname_]**&#x200B;wird angezeigt. Wählen Sie **[!UICONTROL Löschen]**&#x200B;aus, um die Klassifizierung zu löschen. |


<!--

View currently configured classification dimensions for this classification set.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Sets]** > Click the desired classification set name > **[!UICONTROL Schema]**

![classification set schema UI](../../assets/classification-set-schema.png)

The following buttons are available:


* **[!UICONTROL Upload]**: Manually upload classification data for a classification dimensions. `JSON`, `CSV`, `TSV`, and `TAB` files are supported. Uploading a valid file shows a table preview of data to classify.
  * **[!UICONTROL File encoding]**: Select the correct file encoding using this drop-down. Valid options include [!UICONTROL UTF-8] and [!UICONTROL Latin1].
  * **[!UICONTROL List delimiter]**: Select the correct list delimiter. If using a downloaded file or template file, make sure that the [!UICONTROL List delimiter] here matches the [!UICONTROL List delimiter] when the file was downloaded.
  * **[!UICONTROL Apply]**: Save the uploaded classification data to the classification set.

  ![Classification set upload](../../assets/classification-set-upload.png)

* **[!UICONTROL Download]**: Download key values and their classification columns.
  * **[!UICONTROL Rows]**: The maximum number of rows to include in the download file.
  * **[!UICONTROL Download rows received between]**: A calendar date picker that allows you to filter key values by when they appear in reporting. If a key value was not collected in this date range, it does not appear in the downloaded file.
  * **[!UICONTROL Data returned]**: A drop-down list that lets you filter key values included in the downloaded file based on their associated classification data.
    * **[!UICONTROL All classified values]**: Includes rows where classification data is included in at least one column.
    * **[!UICONTROL All unclassified values]**: Includes rows where classification data is missing in at least one column.
  * **[!UICONTROL File format]**: A drop-down list that determines the file format that the download file is in. Options include [!UICONTROL JSON], [!UICONTROL Comma separated values], and [!UICONTROL Excel tab separated values].
  * **[!UICONTROL File encoding]**: A drop-down list that determines the file encoding. Options include [!UICONTROL UTF-8] and [!UICONTROL Latin1]. UTF-8 is recommended.

  ![Classification set download](../../assets/classification-set-download.png)

* **[!UICONTROL Template]**: Download a template file. This file is similar to the [!UICONTROL Download] button, except it does not contain any classification data or key values.
  * **[!UICONTROL File format]**: A drop-down list that determines the file format that the template file is in. Options include [!UICONTROL Comma separated values], and [!UICONTROL Excel tab separated values].
  * **[!UICONTROL File encoding]**: A drop-down list that determines the file encoding. Options include [!UICONTROL UTF-8] and [!UICONTROL Latin1]. UTF-8 is recommended.
  * **[!UICONTROL List delimiters]**: A drop-down list that determines the list delimiter separating classification columns on each row.

  ![Classification set template](../../assets/classification-set-template.png)

* **[!UICONTROL Job history]**: A shortcut link that takes you to the [Job manager](../job-manager.md), showing jobs only for this classification set.
* **[!UICONTROL Automate]**: Automatically ingest data from external storage locations.
  * **[!UICONTROL Location account]**: A drop-down list showing existing location accounts that your organization has configured. If your organization hasn't already configured a location account, you can configure one by selecting [!UICONTROL **Create a new account**].
    
    For information about configuring the location account, see [Configure cloud import and export accounts](/help/components/locations/configure-import-accounts.md).

  * **[!UICONTROL Location]**: A drop-down list showing existing locations that your organization has configured. If your organization hasn't already configured a location, you can configure one by selecting [!UICONTROL **Create a new location**]. 

    For information about configuring a location, see [Configure cloud import and export locations](/help/components/locations/configure-import-locations.md). 

  * **[!UICONTROL Delimiter]**: The column delimiter for uploaded files. Options include [!UICONTROL Comma], [!UICONTROL Semicolon], [!UICONTROL Colon], [!UICONTROL Vertical bar], [!UICONTROL Space], [!UICONTROL Forward slash], [!UICONTROL Backward slash], [!UICONTROL Dash], or [!UICONTROL Underscore].

  * **[!UICONTROL Encoding]**: A drop-down list that determines the file encoding. Options include [!UICONTROL UTF-8] and [!UICONTROL Latin1]. UTF-8 is recommended.

The following actions are available only after selecting a classification.

* **Add lookup**: A lookup table is a classification of a classification. It is metadata about a classification value, rather than the variable itself. For example, the Product variable might have a classification of "color code". A lookup table of "color name" might be attached to "color code" to explain what the colors are.

  ![Attach lookup table](../../assets/lookup.png)

* **Rename**: Lets you rename the classification.

* **Delete**: Lets you delete the classification.
-->