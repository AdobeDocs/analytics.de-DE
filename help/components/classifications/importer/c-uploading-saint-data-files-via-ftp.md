---
description: Hochladen von Datendateien über FTP.
title: FTP-Import
feature: Classifications
exl-id: 3e93b35c-6f65-4a93-887d-d94e4d359bdc
source-git-commit: 95767d10f63e20d5943fa95be3f2fe8f88e67e97
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 73%

---

# FTP-Import

>[!IMPORTANT]
>
>Es wird nicht mehr empfohlen, FTP für den Import zu verwenden, wie auf dieser Seite beschrieben.
>
>FTP wird nicht empfohlen, da es sich um eine unverschlüsselte Methode der Dateifreigabe handelt. Dies bedeutet, dass jeder den Dateiinhalt sowie den Benutzernamen und das Kennwort für das Konto abfangen kann.
>
>Konfigurieren Sie stattdessen ein Cloud-Konto wie in [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) beschrieben.

In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.

## FTP-Import {#concept_2F965BE873254546A61FB755F25299FD}

So laden Sie Datendateien über FTP hoch:

1. **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.

Die folgenden empfohlenen Beschränkungen sind wichtig.

>[!IMPORTANT]
>
>Wenn Sie zu viele kleine Dateien oder einzelne große Dateien haben, kann dies zu einer unnötigen Verarbeitungslast auf den Verarbeitungsservern führen. Adobe empfiehlt, große Dateien in 50-MB-Blöcke aufzuteilen und kleine Dateien zu kombinieren.

Bei der anfänglichen Einrichtung wird die Classification-Datenbank mit einer großen Menge an Originaldaten gefüllt oder die Classifications werden neu strukturiert; es werden also nicht nur einige wenige Reihen neu klassifiziert oder hinzugefügt.

Adobe empfiehlt, nach einem ersten Upload in eine Report Suite (für eine gegebene Variable oder einen Bericht) in den darauffolgenden Importen nur neue und aktualisierte Zeilen zu importieren. Zeilen, die nicht geändert werden, sollten bei zukünftigen Uploads ausgeklammert werden.

Jeder neue Schlüsselwert, den Sie hochladen, zählt als eindeutige Classification der entsprechenden Variable für den Monat.

Wenn Sie die Zahl eindeutiger Classifications für den Monat überschritten haben, werden Ihnen für die über dem Grenzwert liegenden Classifications in den Berichten nicht die zugehörigen Classification-Daten angezeigt. Sie können diese Klassifizierungen in Data Warehouse sehen.

>[!NOTE]
>
>Die erforderliche Verarbeitungszeit für eine Klassifizierungsdatendatei hängt von der Dateigröße und der aktuellen Anzahl der Dateien ab, die zu dem Zeitpunkt auf den Adobe-Servern verarbeitet werden. Die Verarbeitung von Datendateien nimmt in der Regel nicht mehr als 72 Stunden in Anspruch.

## Erstellen Sie ein FTP-Konto

Erstellen Sie vor dem Hochladen von Daten via FTP ein FTP-Konto. >

Weitere Details zu Adobe FTP-Servern finden Sie unter [FTP und sFTP](/help/export/ftp-and-sftp/ftp-overview.md).

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]** und dann auf **[!UICONTROL FTP-Import]**.
1. Klicken Sie auf der Registerkarte **[!UICONTROL Datei importieren]** auf **[!UICONTROL Neu hinzufügen]**.
1. Geben Sie die Details zum FTP-Konto an:

   | Element | Beschreibung |
   |---|---|
   | **Name** | Der Name des FTP-Kontos. |
   | **Datensatz, der klassifiziert werden soll** | Wählen Sie in der Dropdown-Liste den zu klassifizierenden Datensatz (Marketing-Berichtsvariable) aus. |
   | **Report Suites auswählen** | Wählen Sie die Report Suites aus, in denen Sie den ausgewählten Datensatz klassifizieren möchten. Zur Auswahl mehrerer Report Suites müssen die Classifications für jede ausgewählte Report Suite identisch sein. |
   | **Daten bei Konflikten überschreiben** | Mit dieser Option werden doppelte Daten überschrieben. Diese Option ist hilfreich, wenn Sie bestehende Classifications aktualisieren. Wenn Sie die [neueste Klassifizierungsarchitektur](../sets/overview.md) verwenden, ist diese Einstellung immer aktiviert. |
   | **Nach Abschluss des Imports** | Wählen Sie diese Option, um den aktualisierten Datensatz automatisch in dasselbe FTP-Konto zu exportieren, sobald der Import abgeschlossen ist. Geben Sie die E-Mail-Adresse an, an die Benachrichtigungen über dieses FTP-Konto gesendet werden sollen. Wenn Sie die [neueste Klassifizierungsarchitektur](../sets/overview.md) verwenden, ist diese Option nicht verfügbar. |
   | **Benachrichtigungsempfänger** | Geben Sie die E-Mail-Adresse an, an die Benachrichtigungen zu diesem FTP-Konto gesendet werden sollen. |
   | **Authorize** | (Erforderlich) Berechtigt Adobe zum automatischen Importieren aller an das neue FTP-Konto gesendeten Datendateien. |

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Nach dem Erstellen können Sie FTP-Konten bearbeiten oder löschen, indem Sie auf den entsprechenden Link neben dem gewünschten FTP-Konto klicken.

>[!NOTE]
>
>Benachrichtigungen werden nicht gesendet, wenn bei einem Import keine Änderungen an einer Klassifizierung vorgenommen werden. Eine E-Mail wird nur gesendet, wenn sie erfolgreich ist und Änderungen an einer Klassifizierung zur Folge hat.

## Importieren von Classifications über FTP

Sie können ein FTP-Konto verwenden, um Klassifizierungen in Adobe Analytics zu importieren.

So importieren Sie Klassifizierungen über FTP:

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]** und dann auf **[!UICONTROL FTP-Import]**.
1. Klicken Sie neben dem FTP-Konto, das Sie verwenden möchten, auf **[!UICONTROL Ansicht]**.
1. Verwenden Sie die FTP-Zugriffsinformationen (Host, Benutzername, Kennwort), um mit einem FTP-Client Ihrer Wahl auf den FTP-Server zuzugreifen.
1. Laden Sie die Datendatei (`.tab` oder `.txt`) auf den FTP-Server hoch.
1. Laden Sie nach dem Hochladen der Datendatei eine FIN-Datei hoch, die anzeigt, dass die Datei zur Verarbeitung bereit ist.

   Die FIN-Datei ist eine leere Datei mit demselben Namen wie Ihre Datendatei, nur mit der Dateierweiterung `.fin`. Wenn Ihre Datendatei also `classdata1.tab` heißt, lautet der Name der FIN-Datei `classdata1.fin`.

Adobe ruft in regelmäßigen Abständen die hochgeladenen Datendateien mit zugewiesener FIN-Datei ab. Diese werden dann von Adobe in die Report Suites und Datensätze importiert, die bei der Konfiguration des FTP-Kontos angegeben wurden.

Sobald Adobe Analytics Dateien gelesen und verarbeitet hat, die in den FTP-Ordner hochgeladen wurden, werden sie automatisch von der FTP-Site entfernt.
