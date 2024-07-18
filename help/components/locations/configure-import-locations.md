---
description: Konfigurieren Sie das Cloud-Importkonto und den Speicherort, an den Classification-Daten hochgeladen werden können.
keywords: Analysis Workspace
title: Konfigurieren von Cloud-Import- und -Exportspeicherorten
feature: Classifications
exl-id: 55179868-6228-44ff-835c-f4a7b38e929b
source-git-commit: df9470f1870879ac91f00a021ed890bc6fb10cda
workflow-type: tm+mt
source-wordcount: '1687'
ht-degree: 30%

---

# Konfigurieren von Cloud-Import- und -Exportspeicherorten

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

>[!NOTE]
>
>Beachten Sie beim Erstellen und Bearbeiten von Standorten Folgendes:<ul><li>Systemadministratoren können Benutzer daran hindern, Standorte zu erstellen, wie unter [Konfigurieren, ob Benutzer Orte erstellen können](/help/components/locations/locations-manager.md#configure-whether-users-can-create-locations) beschrieben. Wenn Sie keine Standorte wie in diesem Abschnitt beschrieben erstellen können, wenden Sie sich an Ihren Systemadministrator.</li><li>Ein Speicherort kann nur von dem Benutzer, der ihn erstellt hat, oder von einem Systemadministrator bearbeitet werden.</li></ul>

Nachdem Sie [ ein Cloud-Konto konfiguriert haben, können Sie einen Speicherort für dieses Konto konfigurieren. ](/help/components/locations/configure-import-accounts.md) Ein einzelner Ort kann für einen der folgenden Zwecke verwendet werden (ein einzelner Ort kann nicht mehreren Zwecken zugeordnet werden):

* Exportieren von Dateien mit [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md)
* Exportieren von Berichten mit [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Importieren von Schemata mit [Klassifizierungssätzen](/help/components/classifications/sets/overview.md)

Sie müssen Adobe Analytics mit den für den Zugriff auf Ihr Cloud-Konto erforderlichen Informationen konfigurieren. Dieser Prozess besteht darin, das Konto hinzuzufügen und zu konfigurieren (z. B. Amazon S3 Role ARN, Google Cloud Platform usw.), wie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) beschrieben, und dann den Speicherort innerhalb dieses Kontos hinzuzufügen und zu konfigurieren (wie in diesem Artikel beschrieben).

Informationen zum Anzeigen und Löschen vorhandener Speicherorte finden Sie unter [Standorte-Manager](/help/components/locations/locations-manager.md).

## Erstellen oder Bearbeiten eines Standorts beginnen

1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] > [!UICONTROL **Standorte**] aus.

1. Wählen Sie auf der Seite [!UICONTROL Standorte] die Registerkarte [!UICONTROL **Standorte**] aus.

1. (Bedingt) Wenn Sie Systemadministrator sind, können Sie die Option [!UICONTROL **Standorte für alle Benutzer anzeigen**] aktivieren, um von allen Benutzern in Ihrer Organisation erstellte Standorte anzuzeigen.
   ![Anzeigen von Speicherorten für alle Benutzer](assets/locations-all-users.png)

1. Um einen neuen Speicherort hinzuzufügen, wählen Sie [!UICONTROL **Position hinzufügen**] aus. (Wenn Sie noch kein Konto hinzugefügt haben, fügen Sie eines wie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) beschrieben hinzu.)

   Das Dialogfeld [!UICONTROL **Ort hinzufügen**] wird angezeigt

   Oder

   Um einen vorhandenen Speicherort zu bearbeiten, wählen Sie das 3-Punkt-Menü neben dem Ortsnamen und dann [!UICONTROL **Bearbeiten**] aus.

   Das Dialogfeld [!UICONTROL **Standortdetails**] wird angezeigt.

1. Geben Sie die folgenden Informationen an:
|Feld | Funktion |
|—|—|
| [!UICONTROL **Name**] | Der Name des Standorts.  |
| [!UICONTROL **Beschreibung**] | Geben Sie eine kurze Beschreibung des Kontos ein, um es von anderen Konten desselben Kontotyps zu unterscheiden. |
| [!UICONTROL **Verwenden mit**] | Wählen Sie aus, ob Sie diesen Speicherort mit [!UICONTROL **Daten-Feeds**], [!UICONTROL **Data Warehouse**] oder [!UICONTROL **Klassifizierungssätzen**] verwenden möchten. <p>Beachten Sie bei der Auswahl Folgendes:</p><ul><li>Ein einzelner Ort kann nicht für mehrere Zwecke verwendet werden. Beispielsweise kann ein Speicherort, der für Daten-Feeds verwendet wird, nicht auch für Data Warehouse- oder Classification-Sets verwendet werden.</li><li>Um Dateikonflikte innerhalb eines Standorts zu vermeiden, ändern Sie den Wert des Felds [!UICONTROL **Use with**] nicht, nachdem der Speicherort verwendet wurde.</li><li>Wenn Sie einen Speicherort für ein E-Mail-Konto erstellen, wählen Sie in diesem Feld [!UICONTROL **Data Warehouse**] aus. E-Mail-Standorte werden von Daten-Feeds und Classification-Sets nicht unterstützt.</li></ul> |
| [!UICONTROL **Stellen Sie den Standort allen Benutzern in Ihrer Organisation zur Verfügung**] | Aktivieren Sie diese Option, damit andere Benutzer in Ihrer Organisation den Standort verwenden können.<p>Beachten Sie beim Freigeben von Orten Folgendes:</p><ul><li>Die Freigabe von freigegebenen Speicherorten kann nicht aufgehoben werden.</li><li>Freigegebene Standorte können nur vom Eigentümer des Standorts bearbeitet werden.</li><li>Standorte können nur freigegeben werden, wenn auch das Konto, mit dem der Ort verknüpft ist, freigegeben wurde.</li></ul> |
| [!UICONTROL **Standortkonto**] | Wählen Sie das Standortkonto aus, in dem Sie diesen Ort erstellen möchten. Informationen zum Erstellen eines Kontos finden Sie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md). |

1. Um das Formular für die Konfiguration des Standorts auszufüllen, fahren Sie mit dem folgenden Abschnitt fort, der dem Kontotyp entspricht, den Sie im Feld [!UICONTROL **Standortkonten**] ausgewählt haben. (Es sind auch zusätzliche veraltete Kontotypen verfügbar, jedoch nicht empfohlen.)

### Amazon S3 Role ARN

Geben Sie die folgenden Informationen an, um einen Amazon S3 Role ARN-Speicherort zu konfigurieren:

1. [Beginnen Sie mit der Erstellung oder Bearbeitung eines Standorts](#begin-creating-or-editing-a-location), wie oben beschrieben.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Behälter**] | Der Bucket in Ihrem Amazon S3-Konto, an den Adobe Analytics-Daten gesendet werden sollen. <p>Stellen Sie sicher, dass die von Adobe bereitgestellte Benutzer-ARN über die Berechtigung `S3:PutObject` verfügt, um Dateien in diesen Behälter hochzuladen. </p><p>Bucket-Namen müssen bestimmten Benennungsregeln entsprechen. Bucket-Namen müssen etwa zwischen 3 und 63 Zeichen lang sein, dürfen nur aus Kleinbuchstaben, Zahlen, Punkten (.) und Bindestrichen (-) bestehen und müssen mit einem Buchstaben oder einer Zahl beginnen und enden. [Eine vollständige Liste der Benennungsregeln finden Sie in der AWS-Dokumentation.](https://docs.aws.amazon.com/de_de/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
   | [!UICONTROL **Präfix**] | Der Ordner im Bucket, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. (Beispiel: Ordnername/) |

   {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Speichern**] aus.

   Sie können jetzt Daten in das oder aus dem von Ihnen konfigurierten Konto und Speicherort importieren oder exportieren. Verwenden Sie zum Exportieren von Daten [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Verwenden Sie zum Importieren von Daten [Klassifizierungssätze](/help/components/classifications/sets/overview.md).

   Importierte Daten werden nach dem Import nicht mehr aus dem Cloud-Ziel gelöscht.

   >[!NOTE]
   >
   >   Wenn Sie zuvor [FTP zum Importieren von Classifications](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) in Adobe Analytics verwendet haben, müssen Sie eine FIN-Datei hochladen. Diese FIN-Datei ist beim Import aus Cloud-Konten nicht erforderlich.


### Google Cloud Platform

Geben Sie die folgenden Informationen an, um einen Google Cloud Platform-Speicherort zu konfigurieren:

1. [Beginnen Sie mit der Erstellung oder Bearbeitung eines Standorts](#begin-creating-or-editing-a-location), wie oben beschrieben.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Behälter**] | Der Behälter in Ihrem GCP-Konto, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass Sie dem von Adobe bereitgestellten Prinzipal die Berechtigung zum Hochladen von Dateien in diesen Bucket erteilt haben. |
   | [!UICONTROL **Präfix**] | Der Ordner im Bucket, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. (Beispiel: Ordnername/) |

   {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Speichern**] aus.

   Sie können jetzt Daten in das oder aus dem von Ihnen konfigurierten Konto und Speicherort importieren oder exportieren. Verwenden Sie zum Exportieren von Daten [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Verwenden Sie zum Importieren von Daten [Klassifizierungssätze](/help/components/classifications/sets/overview.md).

   Importierte Daten werden nach dem Import nicht mehr aus dem Cloud-Ziel gelöscht.

   >[!NOTE]
   >
   >   Wenn Sie zuvor [FTP zum Importieren von Classifications](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) in Adobe Analytics verwendet haben, müssen Sie eine FIN-Datei hochladen. Diese FIN-Datei ist beim Import aus Cloud-Konten nicht erforderlich.


### Azure SAS

Geben Sie die folgenden Informationen an, um einen Azure SAS-Speicherort zu konfigurieren:

1. [Beginnen Sie mit der Erstellung oder Bearbeitung eines Standorts](#begin-creating-or-editing-a-location), wie oben beschrieben.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Container**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. |
   | [!UICONTROL **Präfix**] | Der Ordner im Container, in dem Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/` |

   {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Speichern**] aus.

   Sie können jetzt Daten in das oder aus dem von Ihnen konfigurierten Konto und Speicherort importieren oder exportieren. Verwenden Sie zum Exportieren von Daten [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Verwenden Sie zum Importieren von Daten [Klassifizierungssätze](/help/components/classifications/sets/overview.md).

   Importierte Daten werden nach dem Import nicht mehr aus dem Cloud-Ziel gelöscht.

   >[!NOTE]
   >
   >   Wenn Sie zuvor [FTP zum Importieren von Classifications](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) in Adobe Analytics verwendet haben, müssen Sie eine FIN-Datei hochladen. Diese FIN-Datei ist beim Import aus Cloud-Konten nicht erforderlich.


### Azure RBAC

Geben Sie die folgenden Informationen an, um einen Azure RBAC-Speicherort zu konfigurieren:

1. [Beginnen Sie mit der Erstellung oder Bearbeitung eines Standorts](#begin-creating-or-editing-a-location), wie oben beschrieben.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Konto**] | Das Azure-Speicherkonto. |
   | [!UICONTROL **Container**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass Sie Berechtigungen zum Hochladen von Dateien in die Azure-Anwendung erteilen, die Sie zuvor erstellt haben. |
   | [!UICONTROL **Präfix**] | Der Ordner im Container, in dem Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/` |

   {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Speichern**] aus.

   Sie können jetzt Daten in das oder aus dem von Ihnen konfigurierten Konto und Speicherort importieren oder exportieren. Verwenden Sie zum Exportieren von Daten [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). Verwenden Sie zum Importieren von Daten [Klassifizierungssätze](/help/components/classifications/sets/overview.md).

   Importierte Daten werden nach dem Import nicht mehr aus dem Cloud-Ziel gelöscht.

   >[!NOTE]
   >
   >   Wenn Sie zuvor [FTP zum Importieren von Classifications](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) in Adobe Analytics verwendet haben, müssen Sie eine FIN-Datei hochladen. Diese FIN-Datei ist beim Import aus Cloud-Konten nicht erforderlich.

### E-Mail

Geben Sie die folgenden Informationen an, um einen E-Mail-Speicherort zu konfigurieren:

1. [Beginnen Sie mit der Erstellung oder Bearbeitung eines Standorts](#begin-creating-or-editing-a-location), wie oben beschrieben.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Betreff**] | Betreff der E-Mail-Nachricht. |
   | [!UICONTROL **Hinweise**] | Der Inhalt der E-Mail-Nachricht. |

   {style="table-layout:auto"}

1. Wählen Sie [!UICONTROL **Speichern**] aus.

   Sie können jetzt Daten in das Konto und den Speicherort exportieren, die Sie bei Verwendung von [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) konfiguriert haben. (E-Mail-Speicherorte werden von [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) oder [Klassifizierungssätzen](/help/components/classifications/sets/overview.md) nicht unterstützt.)

### Alte Kontotypen

Diese veralteten Kontotypen sind nur beim Exportieren von Daten mit [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) und [Data Warehouse](/help/export/data-warehouse/create-request/t-dw-create-request.md) verfügbar. Diese Optionen sind beim Import von Daten mit [Klassifizierungssätzen](/help/components/classifications/sets/manage/schema.md) nicht verfügbar.

+++FTP

Daten-Feed-Daten können an einen Adobe- oder kundengehosteten FTP-Speicherort bereitgestellt werden. Ordner angeben Verwenden Sie das Pfadfeld, um Feed-Dateien in einem Ordner zu platzieren.

| Feld | Funktion |
|---------|----------|
| [!UICONTROL **Ordnerpfad**] | Geben Sie den Pfad zum Verzeichnis auf dem FTP-Server ein. Ordner müssen bereits vorhanden sein. Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist. </br>Beispiel: `/folder_name/folder_name`. |

{style="table-layout:auto"}

+++

+++SFTP

Daten-Feed-Daten können an einen Adobe- oder kundengehosteten SFTP-Speicherort bereitgestellt werden. Die Ziel-Site muss einen gültigen öffentlichen RSA- oder DSA-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Feeds herunterladen.

| Feld | Funktion |
|---------|----------|
| [!UICONTROL **Ordnerpfad**] | Geben Sie den Pfad zum Verzeichnis auf dem FTP-Server ein. Ordner müssen bereits vorhanden sein. Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist. </br>Beispiel: `/folder_name/folder_name`. |

{style="table-layout:auto"}

+++

++ + S3

Sie können Warehouse-Daten direkt an Amazon S3-Buckets senden. Dieser Zieltyp erfordert einen Behälternamen, eine Zugriffsschlüssel-ID und einen geheimen Schlüssel. Weitere Informationen finden Sie unter [Benennungsanforderungen für Amazon S3-Behälter](https://docs.aws.amazon.com/de_de/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in der Amazon S3-Dokumentation.

Die Benutzerin oder der Benutzer, die bzw. den Sie zum Hochladen von Data Warehouse-Daten angeben, muss über die folgenden [Berechtigungen](https://docs.aws.amazon.com/de_de/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html) verfügen:

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

Die folgenden 16 standardmäßigen AWS-Regionen werden unterstützt (gegebenenfalls unter Verwendung des entsprechenden Signaturalgorithmus):

* us-east-2
* us-east-1
* us-west-1
* us-west-2
* ap-south-1
* ap-northeast-2
* ap-southeast-1
* ap-southeast-2
* ap-northeast-1
* ca-central-1
* eu-central-1
* eu-west-1
* eu-west-2
* eu-west-3
* eu-north-1
* sa-east-1

>[!NOTE]
>
>Die Region „cn-north-1“ wird nicht unterstützt.

+++

+++Azure Blob

Data Warehouse unterstützt Azure Blob-Ziele. Erfordert einen Container, ein Konto und einen Schlüssel. Amazon verschlüsselt die Daten automatisch während der Ruhezeit. Wenn Sie die Daten herunterladen, werden sie automatisch entschlüsselt. Weitere Informationen finden Sie unter [Erstellen eines Speicherkontos](https://docs.microsoft.com/de-de/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in der Dokumentation zu Microsoft Azure.

>[!NOTE]
>
>Sie müssen Ihren eigenen Prozess implementieren, um Speicherplatz auf dem Data Warehouse-Ziel zu verwalten. Adobe löscht keine Daten vom Server.

+++


