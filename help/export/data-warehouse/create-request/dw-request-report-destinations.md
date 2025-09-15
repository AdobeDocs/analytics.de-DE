---
description: In diesen Schritten wird beschrieben, wie Sie eine Data Warehouse-Anfrage erstellen.
title: Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage
feature: Data Warehouse
exl-id: 3c7faea3-4d90-4274-88f3-e9337c94155f
source-git-commit: f0a5f72667fd6fc7847ede82d5196d9159fc558c
workflow-type: tm+mt
source-wordcount: '1980'
ht-degree: 82%

---

# Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage

Beim Erstellen einer Data Warehouse-Anfrage stehen verschiedene Konfigurationsoptionen zur Verfügung. Im Folgenden wird beschrieben, wie Sie ein Berichtsziel für die Anfrage konfigurieren.

Informationen zum Erstellen einer Anfrage sowie Links zu anderen wichtigen Konfigurationsoptionen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

>[!NOTE]
>
>Beachten Sie bei der Konfiguration eines Berichtsziels Folgendes:
>
>* Es wird empfohlen, ein Cloud-Konto oder eine E-Mail-Adresse für Ihr Berichtsziel zu verwenden. [Alte FTP- und SFTP-Konten](#legacy-destinations) sind verfügbar, werden jedoch nicht empfohlen.
>
>* Alle von Ihnen zuvor konfigurierten Cloud-Konten stehen zur Data Warehouse-Verwendung zur Verfügung. Sie können Cloud-Konten wie folgt konfigurieren:
>
>   * beim Konfigurieren von [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md)
>   
>   * beim [Importieren von Adobe Analytics-Klassifizierungsdaten](/help/components/locations/locations-manager.md) (Konten verwendbar, alle für diese Konten konfigurierten Speicherorte allerdings nicht)
>   
>   * über den Speicherort-Manager unter [Komponenten > Speicherorte](/help/components/locations/configure-import-accounts.md)
>
>* Cloud-Konten sind mit Ihrem Adobe Analytics-Benutzerkonto verknüpft. Andere Benutzende können die von Ihnen konfigurierten Cloud-Konten nicht verwenden oder anzeigen.
>
>* Sie können alle über den Speicherort-Manager erstellten Speicherorte unter [Komponenten > Speicherorte](/help/components/locations/configure-import-accounts.md) bearbeiten.

Konfigurieren des Ziels, an das die Data Warehouse-Berichte gesendet werden:

1. Falls Sie noch keine Anfrage in Adobe Analytics erstellt haben, tun Sie dies nun durch Auswahl von **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **Hinzufügen**].

   Weitere Informationen finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. Wählen Sie auf der Seite „Neue Data Warehouse-Anfrage“ die Registerkarte [!UICONTROL **Berichtsziel**] aus.

   ![Registerkarte „Berichtsziel“](assets/dw-report-destination.png)

1. (Bedingt) Wenn ein Cloud-Konto (und ein Ziel in diesem Konto) bereits in Adobe Analytics konfiguriert wurde, können Sie es als Berichtsziel verwenden:

   >[!NOTE]
   >
   >Konten stehen nur zur Verfügung, wenn Sie sie konfiguriert haben oder wenn sie für eine Organisation freigegeben wurden, zu der Sie gehören.
   >
   >(Optional) Als Systemadmin steht Ihnen die Option [!UICONTROL **Alle Ziele anzeigen**] zur Verfügung. Aktivieren Sie diese Option, um Zugriff auf alle Konten und Speicherorte zu erhalten, die von Benutzenden in der Organisation erstellt wurden.

   1. Wählen Sie das Konto aus dem Dropdown [!UICONTROL **Menü**] Konto“.

      Alle Cloud-Konten, die Sie in einem der folgenden Bereiche von Adobe Analytics konfiguriert haben, stehen zur Verwendung zur Verfügung:

      * Wenn Sie Adobe Analytics-Klassifizierungsdaten importieren, wie unter [Schema](/help/components/classifications/sets/manage/schema.md) beschrieben.

        Es können jedoch keine Speicherorte verwendet werden, die für den Import von Klassifizierungsdaten konfiguriert sind. Fügen Sie stattdessen ein neues Ziel wie unten beschrieben hinzu.

      * Wenn Sie Konten und Speicherorte im Bereich „Speicherorte“ konfigurieren, wie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) und [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md) beschrieben.

   1. Wählen Sie das mit dem Konto verknüpfte Ziel aus dem Dropdown-Menü [!UICONTROL **Ziel auswählen**] aus. <!-- Is this correct? -->

1. (Bedingt) Wenn Sie keinen Zugriff auf ein Cloud-Konto haben, das bereits in Adobe Analytics konfiguriert ist, können Sie eines wie folgt konfigurieren:

   1. Wählen Sie das [!UICONTROL **Konto**] Dropdown-Menü und dann [!UICONTROL **Konto hinzufügen**] aus.

   1. Geben Sie im Dialogfeld Konto hinzufügen die folgenden Informationen an:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Speicherort-Kontoname**] | Der Name des Standortkontos. Dieser Name wird beim Erstellen eines Speicherorts angezeigt. |
      | [!UICONTROL **Beschreibung des Standortkontos**] | Geben Sie eine kurze Beschreibung des Kontos ein, um es von anderen Konten desselben Kontotyps zu unterscheiden. |
      | [!UICONTROL **Konto für alle Benutzer in Ihrer Organisation verfügbar machen**] | Aktivieren Sie diese Option, damit andere Benutzer in Ihrem Unternehmen das Konto verwenden können.<p>Beachten Sie beim Freigeben von Konten Folgendes:</p><ul><li>Die Freigabe von Konten, die Sie freigeben, kann nicht aufgehoben werden.</li><li>Freigegebene Konten können nur vom Kontoinhaber bearbeitet werden.</li><li>Jeder kann einen Speicherort für das freigegebene Konto erstellen.</li></ul> |
      | [!UICONTROL **Kontotyp**] | Wählen Sie Ihren Cloud-Kontotyp aus. Es wird empfohlen, für jeden Kontotyp ein einziges Konto mit mehreren Speicherorten nach Bedarf innerhalb dieses Kontos zu führen.<p>Systemadministratoren können die Kontotypen, die Benutzer erstellen können, einschränken, wie unter [Konfigurieren, ob Benutzer Konten erstellen können](/help/components/locations/locations-manager.md#configure-whether-users-can-create-accounts) beschrieben. Wenn Sie keine Konten wie in diesem Abschnitt beschrieben erstellen können, wenden Sie sich an Ihren Systemadministrator.</p> |

   1. Geben [!UICONTROL **im Abschnitt**] Kontoeigenschaften“ Informationen an, die für den von Ihnen ausgewählten Kontotyp spezifisch sind.

      Erweitern Sie für Konfigurationsanweisungen den folgenden Abschnitt, der dem ausgewählten [!UICONTROL **Kontotyp**] entspricht. (Zusätzliche Legacy-Kontotypen sind ebenfalls verfügbar, werden aber nicht empfohlen.)

      **Kontotypen**

      +++Amazon S3 Role ARN

      **HINWEIS:** Bei Verwendung von Amazon S3 mit Data Warehouse wird nur die SSE-S3-Verschlüsselung unterstützt.

      Geben Sie die folgenden Informationen an, um ein Amazon S3-Rollen-ARN-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Rollen-ARN**] | Sie müssen einen Rollen-ARN (Amazon Resource Name) bereitstellen, den Adobe verwenden kann, um Zugriff auf das Amazon S3-Konto zu erhalten. Erstellen Sie hierfür eine IAM-Berechtigungsrichtlinie für das Quellkonto, hängen Sie die Richtlinie an eine Benutzerin oder einen Benutzer an und erstellen Sie dann eine Rolle für das Zielkonto. Spezifische Informationen finden Sie in [dieser AWS-Dokumentation](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |

      {style="table-layout:auto"}

      +++

      +++Google Cloud Platform

      Geben Sie die folgenden Informationen an, um ein Google Cloud Platform-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Projekt-ID**] | Ihre Google Cloud-Projekt-ID. Siehe [Dokumentation zu Google Cloud zum Abrufen einer Projekt-ID](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

      {style="table-layout:auto"}

      +++

      +++Azure SAS

      Geben Sie die folgenden Informationen an, um ein Azure SAS-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Anwendungs-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Mandanten-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Key Vault-URI**] | <p>Der Pfad zum SAS-Token im Azure Key Vault.  Um Azure SAS zu konfigurieren, müssen Sie ein SAS-Token als Geheimnis mit Azure Key Vault speichern. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zum Einrichten und Abrufen eines Geheimnisses aus Azure Key Vault](https://learn.microsoft.com/de-de/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nachdem der URI für den Schlüsseltresor erstellt wurde, fügen Sie eine Zugriffsrichtlinie für den Schlüsseltresor hinzu, um der von Ihnen erstellten Azure-Anwendung Berechtigungen zu gewähren. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation für die Zuweisung einer Key Vault-Zugriffsrichtlinie](https://learn.microsoft.com/de-de/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p><p>Oder</p><p>Wenn Sie eine Zugriffsrolle direkt gewähren möchten, ohne eine Zugriffsrichtlinie zu erstellen, finden Sie weitere Informationen zum Zuweisen von Azure-Rollen mithilfe des Azure-Portals in der [Microsoft Azure-Dokumentation](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal). Dadurch wird die Rollenzuweisung für die Anwendungs-ID hinzugefügt, um auf den Schlüsseltresor-URI zuzugreifen. </p> |
      | [!UICONTROL **Key Vault-Geheimnisname**] | Der geheime Name, den Sie beim Hinzufügen der geheimen Daten zum Azure-Schlüsseltresor erstellt haben. In Microsoft Azure befinden sich diese Informationen in dem von Ihnen erstellten Schlüsseltresor auf der Seite mit den **Schlüsseltresor** Einstellungen. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zum Einrichten und Abrufen eines Geheimnisses aus Azure Key Vault](https://learn.microsoft.com/de-de/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
      | [!UICONTROL **Geheimnis des Standortkontos**] | Kopieren Sie das Geheimnis aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Zertifikate und Geheimnisse** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

      +++   

      +++Azure RBAC

      Geben Sie die folgenden Informationen an, um ein Azure RBAC-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Anwendungs-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Mandanten-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Geheimnis des Standortkontos**] | Kopieren Sie das Geheimnis aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Zertifikate und Geheimnisse** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

      +++

      +++E-Mail

      >[!NOTE]
      >
      >E-Mail-Konten können nur mit [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) verwendet werden. (E-Mail-Konten werden nicht mit [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) oder [Klassifizierungssätzen](/help/components/classifications/sets/overview.md) unterstützt.

      Geben Sie die folgenden Informationen an, um ein Azure RBAC-Konto zu konfigurieren:

      | Feld | Funktion |
      |---------|----------|
      | [!UICONTROL **Empfangende**] | Es können E-Mail-Benachrichtigungen an bestimmte Benutzende gesendet werden, wenn der Bericht gesendet wird. Geben Sie eine einzelne E-Mail-Adresse oder eine durch Kommata getrennte Liste von E-Mail-Adressen an. |

      {style="table-layout:auto"}

      +++

1. Fahren Sie mit der Konfiguration Ihrer Data Warehouse-Anfrage auf der Registerkarte [!UICONTROL **Berichtsoptionen**] fort. Weitere Informationen finden Sie unter [Konfigurieren von Berichtsoptionen für eine Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/dw-request-report-options.md).

## Legacy-Kontotypen

>[!IMPORTANT]
>
>Die in diesem Abschnitt beschriebenen Ziele sind veraltet und werden nicht empfohlen. Verwenden Sie stattdessen eines der folgenden Ziele beim Erstellen eines Data Warehouse-Ziels: Amazon S3, Google Cloud Platform, Azure RBAC, Azure SAS oder E-Mail. Weitere Informationen zu den einzelnen empfohlenen Zielen finden Sie in den Informationen oben.

Die folgenden Informationen enthalten Konfigurationsinformationen für die einzelnen veralteten Ziele:

### FTP

Data Warehouse-Daten können für einen von Adobe oder auf Kundenseite gehosteten FTP-Speicherort bereitgestellt werden. Erfordert einen FTP-Host, einen Benutzernamen und ein Kennwort. Verwenden Sie das Pfadfeld, um Feed-Dateien in einem Ordner zu platzieren. Ordner müssen bereits vorhanden sein; Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist.

Verwenden Sie beim Ausfüllen der verfügbaren Felder die folgenden Informationen:

#### Kontofelder

* [!UICONTROL **Kontoname**]: Der Name des FTP-Kontos.

* [!UICONTROL **Kontobeschreibung**]: Eine Beschreibung des FTP-Kontos.

* [!UICONTROL **Host-Name**]: Geben Sie die gewünschte FTP-Ziel-URL ein. Zum Beispiel `ftp.company.com`.

  >[!NOTE]
  >
  >  Schließen Sie `ftp://` am Anfang der URL nicht mit ein.

* [!UICONTROL **Benutzername**]: Geben Sie den Benutzernamen ein, um sich bei der FTP-Site anzumelden.

* [!UICONTROL **Kennwort und Kennwort bestätigen**]: Geben Sie das Kennwort ein, um sich bei der FTP-Site anzumelden.

#### Speicherortfelder

* [!UICONTROL **Speicherortname**]: Der Name des Speicherorts im FTP-Konto, an den Dateien gesendet werden sollen.

* [!UICONTROL **Speicherortbeschreibung**]: Eine Beschreibung des Speicherorts im FTP-Konto.

* [!UICONTROL **Verzeichnispfad**]: Der Pfad zum Speicherort im FTP-Konto.

### SFTP

SFTP-Unterstützung für Data Warehouse ist verfügbar. Erfordert einen SFTP-Host und Benutzernamen. Außerdem muss die Ziel-Site einen gültigen öffentlichen RSA- oder DSA-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Data Warehouse-Ziels herunterladen.

Verwenden Sie beim Ausfüllen der verfügbaren Felder die folgenden Informationen:

#### Kontofelder

* [!UICONTROL **Kontoname**]: Der Name des FTP-Kontos.

* [!UICONTROL **Kontobeschreibung**]: Eine Beschreibung des FTP-Kontos.

* [!UICONTROL **Host-Name**]: Geben Sie die gewünschte SFTP-Ziel-URL ein. Zum Beispiel `sftp.company.com`.

  >[!NOTE]
  >
  >  Schließen Sie `sftp://` am Anfang der URL nicht mit ein.

* [!UICONTROL **Benutzername**]: Geben Sie den Benutzernamen ein, um sich bei der SFTP-Site anzumelden.

* [!UICONTROL **Beim Hochladen temporäre Dateierweiterung verwenden**]: Wenn diese Option aktiviert ist, wird die Dateierweiterung `.part` während des Upload-Prozesses verwendet. Lassen Sie diese Option aktiviert, sofern der SFTP-Server die Änderung von Dateinamen nach Abschluss des Uploads zulässt.

* [!UICONTROL **Öffentliche Schlüssel**]: Laden Sie den entsprechenden öffentlichen Schlüssel herunter, wenn Sie das Data Warehouse-Ziel erstellen.

#### Speicherortfelder

* [!UICONTROL **Speicherortname**]: Der Name des Speicherorts im SFTP-Konto, an den Dateien gesendet werden sollen.

* [!UICONTROL **Speicherortbeschreibung**]: Eine Beschreibung des Speicherorts im SFTP-Konto.

* [!UICONTROL **Verzeichnispfad**]: Der Pfad zum Speicherort im SFTP-Konto.

Weitere Informationen zur SFTP-Konfiguration finden Sie unter [Senden von Data Warehouse-Anfragen an SFTP-Server](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md).

### S3

Sie können Warehouse-Daten direkt an Amazon S3-Buckets senden. Dieser Zieltyp erfordert einen Behälternamen, eine Zugriffsschlüssel-ID und einen geheimen Schlüssel. Weitere Informationen finden Sie unter [Benennungsanforderungen für Amazon S3-Behälter](https://docs.aws.amazon.com/de_de/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in der Amazon S3-Dokumentation.

Die Benutzerin oder der Benutzer, die bzw. den Sie zum Hochladen von Data Warehouse-Daten angeben, muss über die folgenden [Berechtigungen](https://docs.aws.amazon.com/de_de/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html) verfügen:

* S3:GetObject
* S3:PutObject
* S3:PutObjectAcl

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

### Azure Blob

Data Warehouse unterstützt Azure Blob-Ziele. Erfordert einen Container, ein Konto und einen Schlüssel. Amazon verschlüsselt die Daten automatisch während der Ruhezeit. Wenn Sie die Daten herunterladen, werden sie automatisch entschlüsselt. Weitere Informationen finden Sie unter [Erstellen eines Speicherkontos](https://docs.microsoft.com/de-de/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in der Dokumentation zu Microsoft Azure.

>[!NOTE]
>
>Sie müssen Ihren eigenen Prozess implementieren, um Speicherplatz auf dem Data Warehouse-Ziel zu verwalten. Adobe löscht keine Daten vom Server.
