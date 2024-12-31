---
description: Konfigurieren Sie das Cloud-Importkonto und den Speicherort, an den Klassifizierungsdaten hochgeladen werden können
keywords: Analysis Workspace
title: Konfigurieren von Cloud-Import- und -Exportkonten
feature: Classifications
exl-id: 40d3d3f1-1047-4c37-8caf-6b0aabaa590a
source-git-commit: 8a9c51d46195737b5321cc617913261c059f651d
workflow-type: tm+mt
source-wordcount: '1470'
ht-degree: 56%

---

# Konfigurieren von Cloud-Import- und -Exportkonten

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

>[!NOTE]
>
>Beachten Sie beim Erstellen und Bearbeiten von Konten Folgendes: <ul><li>Systemadministratoren können das Erstellen von Konten durch Benutzer einschränken, wie unter [Konfigurieren, ob Benutzer Konten erstellen können](/help/components/locations/locations-manager.md#configure-whether-users-can-create-accounts) beschrieben. Wenn Sie keine Konten wie in diesem Abschnitt beschrieben erstellen können, wenden Sie sich an Ihren Systemadministrator.</li><li>Ein Konto kann nur von dem Benutzer, der es erstellt hat, oder von einem Systemadministrator bearbeitet werden.</li></ul>

Sie können ein Cloud-Konto konfigurieren, das für einen oder alle der folgenden Zwecke verwendet wird:

* Exportieren von Dateien mit [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md)
* Exportieren von Berichten mit [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
* Importieren von Schemas mithilfe [Klassifizierungssätze](/help/components/classifications/sets/overview.md)

Sie müssen Adobe Analytics mit den erforderlichen Informationen konfigurieren, um auf Ihr Cloud-Konto zugreifen zu können. Dieser Prozess besteht aus dem Hinzufügen und Konfigurieren des Kontos (z. B. Amazon S3 Role ARN, Google Cloud Platform usw.), wie in diesem Artikel beschrieben, und dem Hinzufügen und Konfigurieren des Speicherorts innerhalb dieses Kontos (z. B. eines Ordners innerhalb des Kontos), wie in [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md) beschrieben.

Informationen zum Anzeigen und Löschen vorhandener Konten finden Sie unter [Standort-Manager](/help/components/locations/locations-manager.md).

So konfigurieren Sie ein Cloud-Import- oder -Exportkonto:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] > [!UICONTROL **Standorte**] aus.
1. Wählen Sie auf [!UICONTROL  Seite ] die Registerkarte [!UICONTROL **Standortkonten**] aus.
1. (Bedingt) Wenn Sie Systemadministrator sind, können Sie die Option [!UICONTROL **Konten für alle Benutzer anzeigen**] aktivieren, um Konten anzuzeigen, die von allen Benutzern in Ihrer Organisation erstellt wurden.
   ![Konten für alle Benutzer anzeigen](assets/accounts-all-users.png)
1. Um ein neues Konto zu erstellen, wählen Sie [!UICONTROL **Konto hinzufügen**] aus.

   Das [!UICONTROL **Details des Standortkontos**] wird angezeigt.

   Oder

   Um ein vorhandenes Konto zu bearbeiten, suchen Sie das Konto, das Sie bearbeiten möchten, und klicken Sie dann auf die Schaltfläche [!UICONTROL **Details bearbeiten**].

   Das [!UICONTROL **Konto hinzufügen**] wird angezeigt.

1. Geben Sie die folgenden Informationen an:

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Speicherort-Kontoname**] | Der Name des Standortkontos. Dieser Name wird beim Erstellen eines Speicherorts angezeigt |
   | [!UICONTROL **Beschreibung des Standortkontos**] | Geben Sie eine kurze Beschreibung des Kontos ein, um es von anderen Konten desselben Kontotyps zu unterscheiden. |
   | [!UICONTROL **Konto für alle Benutzer in Ihrer Organisation verfügbar machen**] | Aktivieren Sie diese Option, damit andere Benutzer in Ihrem Unternehmen das Konto verwenden können.<p>Beachten Sie beim Freigeben von Konten Folgendes:</p><ul><li>Die Freigabe von Konten, die Sie freigeben, kann nicht aufgehoben werden.</li><li>Freigegebene Konten können nur vom Kontoinhaber bearbeitet werden.</li><li>Jeder kann einen Speicherort für das freigegebene Konto erstellen.</li></ul> |
   | [!UICONTROL **Kontotyp**] | Wählen Sie Ihren Cloud-Kontotyp aus. Es wird empfohlen, für jeden Kontotyp ein einziges Konto mit mehreren Speicherorten nach Bedarf innerhalb dieses Kontos zu führen.<p>Systemadministratoren können die Kontotypen, die Benutzer erstellen können, einschränken, wie unter [Konfigurieren, ob Benutzer Konten erstellen können](/help/components/locations/locations-manager.md#configure-whether-users-can-create-accounts) beschrieben. Wenn Sie keine Konten wie in diesem Abschnitt beschrieben erstellen können, wenden Sie sich an Ihren Systemadministrator.</p> |

1. Geben [!UICONTROL **im Abschnitt**] Kontoeigenschaften“ Informationen an, die für den von Ihnen ausgewählten Kontotyp spezifisch sind.

   Erweitern Sie für Konfigurationsanweisungen den folgenden Abschnitt, der dem ausgewählten [!UICONTROL **Kontotyp**] entspricht. (Zusätzliche Legacy-Kontotypen sind ebenfalls verfügbar, werden aber nicht empfohlen.)

   **Kontotypen**

   +++Amazon S3-Rollen-ARN

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
   | [!UICONTROL **Key Vault-URI**] | <p>Der Pfad zum SAS-Token im Azure Key Vault.  Um Azure SAS zu konfigurieren, müssen Sie ein SAS-Token als Geheimnis mit Azure Key Vault speichern. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zum Einrichten und Abrufen eines Geheimnisses aus Azure Key Vault](https://learn.microsoft.com/de-de/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nachdem der URI für den Schlüsseltresor erstellt wurde, fügen Sie eine Zugriffsrichtlinie für den Schlüsseltresor hinzu, um der von Ihnen erstellten Azure-Anwendung Berechtigungen zu gewähren. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation für die Zuweisung einer Key Vault-Zugriffsrichtlinie](https://learn.microsoft.com/de-de/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
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
   >E-Mail-Konten können nur mit [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) verwendet werden. (E-Mail-Konten werden nicht mit [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) oder [Klassifizierungssätzen](/help/components/classifications/sets/overview.md) unterstützt.

   Geben Sie die folgenden Informationen an, um ein Azure RBAC-Konto zu konfigurieren:

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Empfangende**] | Es können E-Mail-Benachrichtigungen an bestimmte Benutzende gesendet werden, wenn der Bericht gesendet wird. Geben Sie eine einzelne E-Mail-Adresse oder eine durch Kommata getrennte Liste von E-Mail-Adressen an. |

   {style="table-layout:auto"}

+++

   **Legacy-Kontotypen**

   Diese Legacy-Kontotypen sind nur beim Exportieren von Daten mit [Daten-Feeds](/help/export/analytics-data-feed/create-feed.md) und [Data Warehouse verfügbar](/help/export/data-warehouse/create-request/t-dw-create-request.md). Diese Optionen sind beim Importieren von Daten mit &quot;[&quot; nicht ](/help/components/classifications/sets/manage/schema.md).

   +++FTP

   Daten-Feed-Daten können an einen Adobe- oder vom Kunden gehosteten FTP-Speicherort bereitgestellt werden. Erfordert einen FTP-Host, einen Benutzernamen und ein Kennwort. Verwenden Sie das Pfadfeld, um Feed-Dateien in einem Ordner zu platzieren. Ordner müssen bereits vorhanden sein; Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist.

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Host**] | Geben Sie die gewünschte FTP-Ziel-URL ein. Zum Beispiel `ftp.adobe.com`. |
   | [!UICONTROL **Path**] | Kann leer gelassen werden. |
   | [!UICONTROL **Benutzername**] | Geben Sie den Benutzernamen für die Anmeldung bei der FTP-Site ein. |
   | [!UICONTROL **Passwort und Passwort bestätigen**] | Geben Sie das Passwort für die Anmeldung bei der FTP-Site ein. |

   {style="table-layout:auto"}

+++

   +++SFTP

   SFTP-Unterstützung für Daten-Feeds ist verfügbar. Erfordert einen SFTP-Host und Benutzernamen. Außerdem muss die Ziel-Site einen gültigen öffentlichen RSA- oder DSA-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Feeds herunterladen.

+++

   +++S3

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

1. Wählen Sie [!UICONTROL **Speichern**] aus.

1. Fahren Sie mit [Konfigurieren von Cloud-Import- und -](/help/components/locations/configure-import-locations.md)&quot; fort.
