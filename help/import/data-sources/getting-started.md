---
title: Erste Schritte mit Datenquellen
description: Laden Sie Beispieldaten in eine Entwicklungs-Report Suite hoch.
exl-id: d9f74f55-abbb-4ceb-b4db-8d3c32aacd4a
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Erste Schritte mit Datenquellen

Sie können diese Schritte ausführen, um Beispieldaten einfach in eine Entwicklungs-Report Suite hochzuladen und den Workflow in Aktion zu sehen. Sobald Sie den Prozess verstanden haben, können Sie ihn speziell auf die Implementierung Ihres Unternehmens ausdehnen und anpassen.

>[!IMPORTANT]
>
>Führen Sie diese Schritte mithilfe einer Entwicklungs- oder Test-Report-Suite aus. Daten, die über Datenquellen hochgeladen wurden, sind **dauerhaft**. Das Hochladen in die Produktions-Report-Suite wirkt sich auf die dort hochgeladenen Daten aus.

1. Melden Sie sich über [https://experience.adobe.com bei Adobe Analytics &#x200B;](https://experience.adobe.com).
1. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Datenquellen]**.
1. Wählen Sie mithilfe der Dropdown-Liste oben rechts eine Entwicklungs-Report Suite aus.
1. Klicken Sie oben links **[!UICONTROL die Schaltfläche]** Erstellen“.
1. Wählen [!UICONTROL &#x200B; unter &quot;] auswählen“ die Option &quot;[!UICONTROL Generisch]&quot; und wählen Sie unter [!UICONTROL Typ auswählen] die Option &quot;[!UICONTROL Generische Daten-Source (nur Zusammenfassungsdaten)]&quot;.
1. Klicken Sie **[!UICONTROL Aktivieren]**. Ein Popup-Fenster mit dem [!UICONTROL Aktivierungsassistenten für Data Source] wird geöffnet.
   1. Schritt 1: Benennen Sie die Datenquelle und aktivieren Sie das Kontrollkästchen „Haftungsausschluss“.
   1. Schritt 2: Dieser Schritt wurde in früheren Versionen von Adobe Analytics häufiger verwendet. Aktivieren Sie ein Kontrollkästchen, und geben Sie dann einen beliebigen Wert in das Textfeld daneben ein.
   1. Schritt 3: Wählen Sie die Metrik aus, die in Ihre Datenquellenvorlagendatei aufgenommen werden soll. Wählen Sie Ereignis 1 aus der Dropdown-Liste aus.
   1. Schritt 4: Dieser Schritt wurde in früheren Versionen von Adobe Analytics häufiger verwendet. Aktivieren Sie ein Kontrollkästchen, und geben Sie dann einen beliebigen Wert in das Textfeld daneben ein.
   1. Schritt 5: Wählen Sie die Dimension aus, die in Ihre Datenquellenvorlagendatei aufgenommen werden soll. Wählen Sie &quot;eVar1“ aus der Dropdown-Liste aus.
   1. Schritt 6: Überprüfen Sie die Zusammenfassung und zeigen Sie die Dimensionen und Metriken an, die in der Vorlagendatei enthalten sind.
   1. Schritt 7: Klicken Sie auf **[!UICONTROL Herunterladen]**, um die Datenquellen-Vorlagendatei herunterzuladen. Beachten Sie auch die Anmeldedaten für die FTP-Site, da sie in Kürze verwendet werden.
1. Die Datenquelle wird jetzt erstellt. Der nächste Schritt besteht darin, ihr Daten zur Verarbeitung bereitzustellen. Öffnen Sie die heruntergeladene Datei in Ihrem gewünschten Texteditor.
1. Die Vorlagendatei enthält drei Zeilen: zwei Kommentarzeilen (beginnend mit &quot;`#`„) und eine Kopfzeile:

   ```text
   # Generic Data Source (Summary Data Only) template file (user: 123456789 ds_id: 2)
   #    eVar1    event1
   Date    Evar 1    Event 1
   ```

1. Geben Sie in mehrere Datenzeilen ein, indem Sie jeden Eintrag durch eine Registerkarte trennen. Verwenden Sie keine Leerzeichen oder Kommas, um Werte zu trennen.
   * Die erste Spalte ist das Datum im folgenden Format: `MM/DD/YYYY/HH/mm/SS`.
   * Die zweite Spalte ist der Textwert, den Sie in eVar1 einschließen möchten.
   * Die dritte Spalte ist der Betrag, den Sie für Ereignis 1 erhöhen möchten.

   ```text
   # Generic Data Source (Summary Data Only) template file (user: 123456789 ds_id: 5)
   #    eVar1    event1
   Date    Evar 1    Event 1
   09/07/YYYY/11/23/00    Data source example value    3
   09/07/YYYY/15/59/00    Another data source value    18
   ```

1. Speichern Sie die Datei. Sie können ihr optional einen anderen Dateinamen geben. Nach dem Speichern der Datei können Sie den Texteditor schließen.
1. Navigieren Sie in Windows Explorer, Finder oder einem beliebigen FTP-Client zu [ftp://ftp.omniture.com](ftp://ftp.omniture.com).
1. Wenn Sie nach Anmeldeinformationen gefragt werden, verwenden Sie den Benutzernamen und das Kennwort, die im letzten Schritt des Assistenten zur Erstellung von Datenquellen bereitgestellt wurden. Sie können erneut darauf verweisen, indem Sie zu [!UICONTROL Datenquellen] navigieren und auf **[!UICONTROL FTP-]**) neben der von Ihnen erstellten Datenquelle klicken.
1. Ziehen Sie die von Ihnen bearbeitete Datei nach der Authentifizierung in das Fenster „Authentifizierte FTP“.
1. Erstellen Sie eine leere Textdatei an einem beliebigen Ort außerhalb des FTP-Fensters. Verwenden Sie denselben Dateinamen wie die Datenquellendatei, die Sie auf die FTP-Site hochgeladen haben, mit einer Ausnahme. Geben Sie anstelle eines `.txt` Dateityps einen `.fin` Dateityp an. Stellen Sie sicher, dass Sie mit Ihren Betriebssystemeinstellungen Dateitypen anzeigen und ändern können.
1. Ziehen Sie die leere `.fin` an denselben FTP-Speicherort wie die Datenquellendatei. Das Vorhandensein der `.fin` teilt Adobe mit, dass die Datenquellendatei vollständig hochgeladen wurde und aufgenommen werden kann.
1. Nach einigen Minuten verschwindet die Datei vom FTP-Speicherort und ist im Reporting sichtbar.
1. Aktualisieren Sie die Seite „Datenquellen“ und überprüfen Sie, ob die Datei erfolgreich aufgenommen wurde.
1. Navigieren Sie zu Analysis Workspace und erstellen Sie ein Projekt.
1. Ziehen Sie eVar1 als Dimension auf die Arbeitsfläche des Arbeitsbereichs und Ereignis 1 als Metrik. Stellen Sie sicher, dass der Workspace-Datumsbereich die Daten enthält, die Sie in der Datenquelle angegeben haben.

   ![Beispielbericht](assets/success-report.png)

## Nächste Schritte

[Dateiformat](file-format.md): Erfahren Sie mehr über die Erstellung einer Datenquellendatei, die auf Ihr Unternehmen zugeschnitten ist.
