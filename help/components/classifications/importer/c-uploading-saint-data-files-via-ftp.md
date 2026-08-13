---
description: Hochladen von Datendateien über FTP.
title: FTP-Import
feature: Classifications
exl-id: 3e93b35c-6f65-4a93-887d-d94e4d359bdc
TQID: https://experienceleague.adobe.com/CMHQpWtGl14Z7kHaZ7ufp6-tDIfQ-pCEzSI47XMi-pA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 727
ht-degree: 39%

---

# FTP-Import (veraltet)

{{classification-importer-deprecation}}

>[!IMPORTANT]
>
>Adobe empfiehlt nicht mehr, FTP zum Importieren zu verwenden, wie auf dieser Seite beschrieben.
>
>FTP wird nicht empfohlen, da es sich um eine unverschlüsselte Methode zur Freigabe von Dateien handelt, was bedeutet, dass jeder den Dateiinhalt sowie den Benutzernamen und das Passwort für das Konto abfangen kann.
>
>Konfigurieren Sie stattdessen ein Cloud-Konto wie in [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) beschrieben.

In diesen Schritten wird beschrieben, wie Sie Datendateien über FTP hochladen.

## FTP-Import {#concept_2F965BE873254546A61FB755F25299FD}

So laden Sie Datendateien über FTP hoch:

1. **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.

Die folgenden empfohlenen Grenzwerte sind wichtig.

>[!IMPORTANT]
>
>Zu viele kleine Dateien oder einzelne große Dateien können zu unnötiger Verarbeitungslast auf den Verarbeitungs-Servern führen. Adobe empfiehlt, große Dateien in Blöcke von 50 MB aufzuteilen und kleine Dateien miteinander zu kombinieren.

Bei der Ersteinrichtung wird die Klassifizierungsdatenbank mit einem großen Satz Originaldaten ausgefüllt oder die Klassifizierungen werden neu strukturiert, anstatt einige Zeilen neu zu klassifizieren oder Zeilen hinzuzufügen.

Nach einem ersten Upload in eine Report Suite (für eine bestimmte Variable oder einen bestimmten Bericht) empfiehlt Adobe, in nachfolgenden Importen nur neue und aktualisierte Zeilen hochzuladen. Zeilen, die nicht geändert werden, sollten in zukünftigen Uploads weggelassen werden.

Jeder neue Schlüsselwert, den Sie hochladen, wird anhand Ihrer eindeutigen Werte für diese Variable für den Monat gezählt.

Wenn Sie Ihre eindeutigen Werte für den Monat überschritten haben, werden die entsprechenden Klassifizierungsdaten für die eindeutigen Werte überschritten im Bericht nicht angezeigt. Sie können diese Klassifizierungen in Data Warehouse sehen.

>[!NOTE]
>
>Die erforderliche Verarbeitungszeit für eine Klassifizierungsdatendatei hängt von der Dateigröße und der aktuellen Anzahl der Dateien ab, die zu dem Zeitpunkt auf den Adobe-Servern verarbeitet werden. Die Verarbeitung von Datendateien dauert in der Regel nicht länger als 72 Stunden.

## Erstellen Sie ein FTP-Konto

Erstellen Sie vor dem Hochladen von Daten via FTP ein FTP-Konto. >

Weitere Details zu Adobe FTP-Servern finden Sie unter [FTP und sFTP](/help/export/ftp-and-sftp/ftp-overview.md).

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]** und dann auf **[!UICONTROL FTP-Import]**.
1. Klicken Sie auf der Registerkarte **[!UICONTROL Datei importieren]** auf **[!UICONTROL Neu hinzufügen]**.
1. Geben Sie die Details zum FTP-Konto an:

   | Element | Beschreibung |
   |---|---|
   | **Name** | Der FTP-Kontoname. |
   | **Datensatz, der klassifiziert werden soll** | Wählen Sie aus der Dropdown-Liste den Datensatz (Marketing-Berichtsvariable) aus, den Sie klassifizieren möchten. |
   | **Report Suites auswählen** | Wählen Sie die Report Suites aus, in denen Sie den ausgewählten Datensatz klassifizieren möchten. Um mehrere Report Suites auszuwählen, müssen die Klassifizierungen für jede der ausgewählten Report Suites identisch sein. |
   | **Daten bei Konflikten überschreiben** | Wählen Sie diese Option, um doppelte Daten zu überschreiben. Diese Option ist nützlich, wenn Sie vorhandene Klassifizierungen aktualisieren. Wenn Sie die [neueste Klassifizierungsarchitektur](../sets/overview.md) verwenden, ist diese Einstellung immer aktiviert. |
   | **Nach Abschluss des Imports** | Wählen Sie diese Option aus, um den aktualisierten Datensatz automatisch in dasselbe FTP-Konto zu exportieren, sobald Sie die E-Mail-Adresse angeben, an die nach Abschluss des Imports Benachrichtigungen über dieses FTP-Konto gesendet werden sollen. Wenn Sie die [neueste Klassifizierungsarchitektur](../sets/overview.md) verwenden, ist diese Option nicht verfügbar. |
   | **Benachrichtigungsempfänger** | Geben Sie die E-Mail-Adresse an, an die Benachrichtigungen zu diesem FTP-Konto gesendet werden sollen. |
   | **Autorisieren** | (Erforderlich) Autorisiert Adobe, alle Datendateien, die an das neue FTP-Konto gesendet werden, automatisch zu importieren. |

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

In regelmäßigen Abständen ruft Adobe hochgeladene Datendateien mit einer zugehörigen FIN-Datei ab. Adobe importiert sie in die Report Suites und Datensätze, die in der FTP-Kontokonfiguration angegeben sind.

Nachdem Adobe Analytics in den FTP-Ordner hochgeladene Dateien gelesen und verarbeitet hat, werden die Dateien automatisch von der FTP-Site entfernt.
