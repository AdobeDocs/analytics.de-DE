---
title: Erstellen eines Daten-Feeds
description: Erfahren Sie, wie Sie einen Daten-Feed erstellen und welche Dateiinformationen Adobe zur Verfügung gestellt werden müssen.
feature: Data Feeds
exl-id: 36c8a40e-6137-4836-9d4b-bebf17b932bc
source-git-commit: f0a5f72667fd6fc7847ede82d5196d9159fc558c
workflow-type: tm+mt
source-wordcount: '4140'
ht-degree: 53%

---

# Erstellen eines Daten-Feeds

Beim Erstellen eines Daten-Feeds stellen Sie Adobe Folgendes zur Verfügung:

* Die Informationen über das Ziel, an das Rohdatendateien gesendet werden sollen
* Die Daten, die in die einzelnen Dateien aufgenommen werden sollen

Bevor Sie einen Daten-Feed erstellen, müssen Sie über grundlegende Kenntnisse zu Daten-Feeds verfügen und sicherstellen, dass Sie alle Voraussetzungen erfüllen. Weitere Informationen finden Sie unter [Übersicht über Daten-Feeds](data-feed-overview.md).

## Erstellen und Konfigurieren eines Daten-Feeds

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
1. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf [!UICONTROL **Analytics**].
1. Navigieren Sie in der oberen Navigationsleiste zu [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**].
1. Wählen Sie [!UICONTROL **Hinzufügen**] aus.

   ![Daten-Feed hinzufügen](assets/datafeed-add.png)

   Eine Seite wird mit drei Hauptkategorien angezeigt: [!UICONTROL **Feed-Informationen**], [!UICONTROL **Ziel**] und [!UICONTROL **Datenspaltendefinitionen**].
1. Füllen [!UICONTROL **im Abschnitt „Feed**] Informationen die folgenden Felder aus:

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Name**] | Der Name des Daten-Feeds. Muss innerhalb der ausgewählten Report Suite eindeutig sein und kann bis zu 255 Zeichen lang sein. [Weitere Informationen](/help/export/analytics-data-feed/df-faq.md#must-feed-names-be-unique) |
   | [!UICONTROL **Report Suite**] | Die Report Suite, auf der der Daten-Feed basiert. Wenn mehrere Daten-Feeds für dieselbe Report Suite erstellt werden, müssen sie unterschiedliche Spaltendefinitionen haben. Nur Quell-Report Suites unterstützen Daten-Feeds. Virtual Report Suites werden nicht unterstützt. |
   | [!UICONTROL **E-Mail nach Abschluss**] | Die E-Mail-Adresse, die benachrichtigt werden soll, wenn ein Feed die Verarbeitung abgeschlossen hat. Die E-Mail-Adresse muss korrekt formatiert sein. |
   | [!UICONTROL **Vorschub-Intervall**] | Wählen Sie **Täglich** für Aufstockung oder historische Daten aus. Tägliche Feeds enthalten Daten eines ganzen Tages von Mitternacht bis Mitternacht in der Zeitzone der Report Suite. Wählen Sie **Stündlich** für weitere Daten aus (Täglich ist auch für weitere Feeds verfügbar, wenn Sie es vorziehen). Stündliche Feeds enthalten Daten für eine einzige Stunde. |
   | [!UICONTROL **Verarbeitung verzögern**] | Warten Sie eine bestimmte Zeit, bevor Sie eine Daten-Feed-Datei verarbeiten. Eine Verzögerung kann nützlich sein, um mobilen Implementierungen die Möglichkeit zu geben, dass Offlinegeräte online gehen und Daten senden können. Sie kann auch verwendet werden, um die serverseitigen Prozesse Ihrer Organisation bei der Verwaltung zuvor verarbeiteter Dateien zu berücksichtigen. In den meisten Fällen ist keine Verzögerung erforderlich. Ein Feed kann um bis zu 120 Minuten verzögert werden. |
   | [!UICONTROL **Start- und Enddatum**] | Das Startdatum gibt das Datum an, an dem der Daten-Feed beginnen soll. Um sofort mit der Verarbeitung von Daten-Feeds für historische Daten zu beginnen, setzen Sie dieses Datum auf ein beliebiges Datum in der Vergangenheit, an dem Daten erfasst werden. Start- und Enddatum basieren auf der Zeitzone der Report Suite. |
   | [!UICONTROL **Fortlaufender**] | Dieses Kontrollkästchen entfernt das Enddatum, sodass ein Feed unbegrenzt ausgeführt werden kann. Wenn ein Feed die Verarbeitung historischer Daten abschließt, wartet er, bis die Datenerfassung für die jeweilige Stunde bzw. dem jeweiligen Tag abgeschlossen ist. Sobald die aktuelle Stunde oder der aktuelle Tag abgeschlossen ist, beginnt die Verarbeitung nach der angegebenen Verzögerung. |

1. Wählen Sie im [!UICONTROL **Ziel**] im Dropdown-Menü [!UICONTROL **Typ**] das Ziel aus, an das die Daten gesendet werden sollen.

   >[!NOTE]
   >
   >Beachten Sie bei der Konfiguration eines Berichtsziels Folgendes:
   >
   >* Es wird empfohlen, ein Cloud-Konto für Ihr Berichtsziel zu verwenden. [Ältere FTP- und SFTP](#legacy-destinations)Konten sind verfügbar, werden jedoch nicht empfohlen.
   >* Alle Cloud-Konten, die Sie zuvor konfiguriert haben, können für Daten-Feeds verwendet werden. Sie können Cloud-Konten wie folgt konfigurieren:
   >
   >   * Beim Konfigurieren von Cloud-Konten für [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
   >   
   >   * Beim [Importieren von Adobe Analytics-Klassifizierungsdaten](/help/components/locations/locations-manager.md) (Alle Speicherorte, die für den Import von Klassifizierungsdaten konfiguriert sind, können nicht verwendet werden.)
   >   
   >   * Über den Standort-Manager unter [Komponenten > Standorte](/help/components/locations/configure-import-accounts.md)
   >
   >* Cloud-Konten sind mit Ihrem Adobe Analytics-Benutzerkonto verknüpft. Andere Benutzende können die von Ihnen konfigurierten Cloud-Konten nicht verwenden oder anzeigen.
   >
   >* Sie können alle über den Speicherort-Manager erstellten Speicherorte unter [Komponenten > Speicherorte](/help/components/locations/configure-import-accounts.md) bearbeiten.

   ![Dropdown-Menü „Daten-Feed-Ziel“](assets/datafeed-destinations-dropdown.png)

   Verwenden Sie beim Erstellen eines Daten-Feeds einen der folgenden Zieltypen. Erweitern Sie für Konfigurationsanweisungen den Zieltyp . (Zusätzliche [alte Ziele](#legacy-destinations) sind ebenfalls verfügbar, werden jedoch nicht empfohlen.)

   +++Amazon S3

   Sie können Feeds direkt an Amazon S3-Behälter senden. Dieser Zieltyp erfordert nur Ihr Amazon S3-Konto und den Speicherort (Bucket).

   Adobe Analytics verwendet die kontenübergreifende Authentifizierung, um Dateien von Adobe Analytics an den angegebenen Speicherort in Ihrer Amazon S3-Instanz hochzuladen.

   Bei Verwendung von Amazon S3 mit Daten-Feeds wird nur die SSE-S3-Verschlüsselung unterstützt.

   So konfigurieren Sie einen Amazon S3-Bucket als Ziel für einen Daten-Feed:

   1. Erstellen Sie einen Daten-Feed wie in [Erstellen und Konfigurieren eines Daten-Feeds](#create-and-configure-a-data-feed) beschrieben.

   1. Wählen Sie [!UICONTROL **Abschnitt**] Ziel“ im Dropdown-Menü [!UICONTROL **Typ**] die Option [!UICONTROL **Amazon S3**] aus.

      ![Amazon S3-Ziel](assets/datafeed-destination-amazons3.png)

   1. Wählen Sie [!UICONTROL **Speicherort auswählen**] aus.

      Die Seite Amazon S3-Exportspeicherorte wird angezeigt.

   1. (Bedingt) Wenn in Adobe Analytics bereits ein Amazon S3-Konto (und ein Speicherort in diesem Konto) konfiguriert wurde, können Sie es als Daten-Feed-Ziel verwenden:

      >[!NOTE]
      >
      >Konten stehen nur zur Verfügung, wenn Sie sie konfiguriert haben oder wenn sie für eine Organisation freigegeben wurden, zu der Sie gehören.

      1. Wählen Sie das Konto aus dem Dropdown-Menü [!UICONTROL **Konto auswählen**] aus.

         Alle Cloud-Konten, die in einem der folgenden Bereiche von Adobe Analytics konfiguriert wurden, können verwendet werden:

         * Wenn Sie Adobe Analytics-Klassifizierungsdaten importieren, wie unter [Schema](/help/components/classifications/sets/manage/schema.md) beschrieben.

           Es können jedoch keine Speicherorte verwendet werden, die für den Import von Klassifizierungsdaten konfiguriert sind. Fügen Sie stattdessen ein neues Ziel wie unten beschrieben hinzu.

         * Wenn Sie Konten und Speicherorte im Bereich „Speicherorte“ konfigurieren, wie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) und [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md) beschrieben.

      1. Wählen Sie den Speicherort aus dem Dropdown [!UICONTROL **Menü**] Speicherort auswählen“ aus.

      1. Wählen [!UICONTROL **Speichern**] > [!UICONTROL **Speichern**].

      Das Ziel ist jetzt so konfiguriert, dass Daten an den von Ihnen angegebenen Amazon S3-Speicherort gesendet werden.

   1. (Bedingt) Wenn Sie zuvor noch kein Amazon S3-Konto hinzugefügt haben:

      1. Wählen Sie [!UICONTROL **Konto hinzufügen**] aus und geben Sie dann die folgenden Informationen an:

         | Feld | Funktion |
         |---------|----------|
         | [!UICONTROL **Kontoname**] | Ein Name für das Konto. Dabei kann es sich um einen beliebigen Namen handeln. |
         | [!UICONTROL **Kontobeschreibung**] | Eine Beschreibung für das Konto. |
         | [!UICONTROL **Rollen-ARN**] | Sie müssen einen Rollen-ARN (Amazon Resource Name) bereitstellen, den Adobe verwenden kann, um Zugriff auf das Amazon S3-Konto zu erhalten. Erstellen Sie hierfür eine IAM-Berechtigungsrichtlinie für das Quellkonto, hängen Sie die Richtlinie an eine Benutzerin oder einen Benutzer an und erstellen Sie dann eine Rolle für das Zielkonto. Spezifische Informationen finden Sie in [dieser AWS-Dokumentation](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |
         | [!UICONTROL **Benutzer-ARN**] | Der Benutzer-ARN (Amazon Resource Name) wird von Adobe bereitgestellt. Sie müssen diese Benutzerin oder diesen Benutzer an die von Ihnen erstellte Richtlinie anhängen. |

         {style="table-layout:auto"}

      1. Wählen Sie [!UICONTROL **Speicherort hinzufügen**] aus und geben Sie dann die folgenden Informationen an:

         | Feld | Funktion |
         |---------|----------|
         | [!UICONTROL **Name**] | Ein Name für das Konto. |
         | [!UICONTROL **Beschreibung**] | Eine Beschreibung für das Konto. |
         | [!UICONTROL **Bucket**] | Der Bucket in Ihrem Amazon S3-Konto, an den Adobe Analytics-Daten gesendet werden sollen. <p>Stellen Sie sicher, dass der von Adobe bereitgestellte Benutzer-ARN über die `S3:PutObject`-Berechtigung verfügt, um Dateien in diesen Bucket hochzuladen. Diese Berechtigung ermöglicht es dem Benutzer-ARN, ursprüngliche Dateien hochzuladen und Dateien für nachfolgende Uploads zu überschreiben.</p><p>Bucket-Namen müssen bestimmten Benennungsregeln entsprechen. Bucket-Namen müssen etwa zwischen 3 und 63 Zeichen lang sein, dürfen nur aus Kleinbuchstaben, Zahlen, Punkten (.) und Bindestrichen (-) bestehen und müssen mit einem Buchstaben oder einer Zahl beginnen und enden. [Eine vollständige Liste der Benennungsregeln finden Sie in der AWS-Dokumentation.](https://docs.aws.amazon.com/de_de/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
         | [!UICONTROL **Präfix**] | Der Ordner im Bucket, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/` |

         {style="table-layout:auto"}

      1. Wählen [!UICONTROL **Erstellen**] > [!UICONTROL **Speichern**].

         Das Ziel ist jetzt so konfiguriert, dass Daten an den von Ihnen angegebenen Amazon S3-Speicherort gesendet werden.

      1. (Bedingt) Wenn Sie das soeben erstellte Ziel (Konto und Speicherort) verwalten müssen, ist es in der [Standort-Manager“ ](/help/components/locations/locations-manager.md).

   +++

   +++Azure RBAC

   Mithilfe der RBAC-Authentifizierung können Sie Feeds direkt an einen Azure-Container senden. Dieser Zieltyp erfordert eine Anwendungs-ID, eine Mandanten-ID und ein Geheimnis.

   So konfigurieren Sie ein Azure RBAC-Konto als Ziel für einen Daten-Feed:

   1. Erstellen Sie, falls noch nicht geschehen, eine Azure-Anwendung, die Adobe Analytics für die Authentifizierung verwenden kann, und gewähren Sie dann Zugriffsberechtigungen in der Zugriffssteuerung (IAM).

      Weitere Informationen zum Erstellen einer Azure Active Directory-Anwendung finden Sie in der [Microsoft Azure-Dokumentation](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal).

   1. Wählen Sie in der Adobe Analytics Admin Console im Abschnitt [!UICONTROL **Ziel**] im Dropdown-Menü [!UICONTROL **Typ**] die Option [!UICONTROL **Azure RBAC**].

      ![Azure RBAC-Ziel](assets/datafeed-destination-azurerbac.png)

   1. Wählen Sie [!UICONTROL **Speicherort auswählen**] aus.

      Die Seite Azure RBAC-Exportspeicherorte wird angezeigt.

   1. (Bedingt) Wenn in Adobe Analytics bereits ein Azure RBAC-Konto (und ein Speicherort in diesem Konto) konfiguriert wurde, können Sie es als Daten-Feed-Ziel verwenden:

      >[!NOTE]
      >
      >Konten stehen nur zur Verfügung, wenn Sie sie konfiguriert haben oder wenn sie für eine Organisation freigegeben wurden, zu der Sie gehören.

      1. Wählen Sie das Konto aus dem Dropdown-Menü [!UICONTROL **Konto auswählen**] aus.

      Alle Cloud-Konten, die Sie in einem der folgenden Bereiche von Adobe Analytics konfiguriert haben, stehen zur Verwendung zur Verfügung:

      * Wenn Sie Adobe Analytics-Klassifizierungsdaten importieren, wie unter [Schema](/help/components/classifications/sets/manage/schema.md) beschrieben.

        Es können jedoch keine Speicherorte verwendet werden, die für den Import von Klassifizierungsdaten konfiguriert sind. Fügen Sie stattdessen ein neues Ziel wie unten beschrieben hinzu.

      * Wenn Sie Konten und Speicherorte im Bereich „Speicherorte“ konfigurieren, wie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) und [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md) beschrieben.

      1. Wählen Sie den Speicherort aus dem Dropdown [!UICONTROL **Menü**] Speicherort auswählen“ aus.

      1. Wählen [!UICONTROL **Speichern**] > [!UICONTROL **Speichern**].

         Das Ziel ist jetzt so konfiguriert, dass Daten an den von Ihnen angegebenen Azure RBAC-Speicherort gesendet werden.

   1. (Bedingt) Wenn Sie zuvor noch kein Azure RBAC-Konto hinzugefügt haben:

      1. Wählen Sie [!UICONTROL **Konto hinzufügen**] aus und geben Sie dann die folgenden Informationen an:

         | Feld | Funktion |
         |---------|----------|
         | [!UICONTROL **Kontoname**] | Ein Name für das Azure RBAC-Konto. Dieser Name wird im Dropdown-Feld [!UICONTROL **Konto auswählen**] angezeigt und kann ein beliebiger Name sein. |
         | [!UICONTROL **Kontobeschreibung**] | Eine Beschreibung für das Azure RBAC-Konto. Diese Beschreibung wird im Dropdown-Feld [!UICONTROL **Konto auswählen**] angezeigt und kann ein beliebiger Name sein. |
         | [!UICONTROL **Anwendungs-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Mandanten-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Geheimnis**] | Kopieren Sie das Geheimnis aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Zertifikate und Geheimnisse** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |

         {style="table-layout:auto"}

      1. Wählen Sie [!UICONTROL **Speicherort hinzufügen**] aus und geben Sie dann die folgenden Informationen an:

         | Feld | Funktion |
         |---------|----------|
         | [!UICONTROL **Name**] | Ein Name für den Speicherort. Dieser Name wird im Dropdown-Feld [!UICONTROL **Speicherort auswählen**] angezeigt und kann ein beliebiger Name sein. |
         | [!UICONTROL **Beschreibung**] | Eine Beschreibung für den Speicherort. Diese Beschreibung wird im Dropdown-Feld [!UICONTROL **Speicherort auswählen**] angezeigt und kann ein beliebiger Name sein. |
         | [!UICONTROL **Konto**] | Das Azure-Speicherkonto. |
         | [!UICONTROL **Container**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. Stellen Sie sicher, dass Sie Berechtigungen zum Hochladen von Dateien in die Azure-Anwendung erteilen, die Sie zuvor erstellt haben. |
         | [!UICONTROL **Präfix**] | Der Ordner im Container, in dem Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/`<p>Stellen Sie sicher, dass die Anwendungs-ID, die Sie beim Konfigurieren des Azure RBAC-Kontos angegeben haben, der Rolle `Storage Blob Data Contributor` zugeteilt wurde, damit der Zugriff auf den Container (Ordner) möglich ist.</p> <p>Weitere Informationen finden Sie unter [Integrierte Azure-Rollen](https://learn.microsoft.com/de-de/azure/role-based-access-control/built-in-roles).</p> |

         {style="table-layout:auto"}

      1. Wählen [!UICONTROL **Erstellen**] > [!UICONTROL **Speichern**].

         Das Ziel ist jetzt so konfiguriert, dass Daten an den von Ihnen angegebenen Azure RBAC-Speicherort gesendet werden.

      1. (Bedingt) Wenn Sie das soeben erstellte Ziel (Konto und Speicherort) verwalten müssen, ist es in der [Standort-Manager“ ](/help/components/locations/locations-manager.md).

   +++

   +++Azure SAS

   Mithilfe der SAS-Authentifizierung können Sie Feeds direkt an einen Azure-Container senden. Dieser Zieltyp erfordert eine Anwendungs-ID, eine Mandanten-ID, einen Schlüsseltresor-URI, einen Schlüsseltresor-Geheimnisnamen und ein Geheimnis.

   So konfigurieren Sie Azure SAS als Ziel für einen Daten-Feed:

   1. Wenn Sie dies noch nicht getan haben, erstellen Sie ein Azure-Programm, das Adobe Analytics für die Authentifizierung verwenden kann.

      Weitere Informationen zum Erstellen einer Azure Active Directory-Anwendung finden Sie in der [Microsoft Azure-Dokumentation](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal).

   1. Wählen Sie in der Adobe Analytics Admin Console im Abschnitt [!UICONTROL **Ziel**] die Option [!UICONTROL **Azure SAS**] aus.

      ![Azure SAS-Ziel](assets/datafeed-destination-azuresas.png)

   1. Wählen Sie [!UICONTROL **Speicherort auswählen**] aus.

      Die Seite Azure SAS-Exportspeicherorte wird angezeigt.

   1. (Bedingt) Wenn in Adobe Analytics bereits ein Azure SAS-Konto (und ein Speicherort in diesem Konto) konfiguriert wurde, können Sie es als Daten-Feed-Ziel verwenden:

      >[!NOTE]
      >
      >Konten stehen nur zur Verfügung, wenn Sie sie konfiguriert haben oder wenn sie für eine Organisation freigegeben wurden, zu der Sie gehören.

      1. Wählen Sie das Konto aus dem Dropdown-Menü [!UICONTROL **Konto auswählen**] aus.

         Alle Cloud-Konten, die Sie in einem der folgenden Bereiche von Adobe Analytics konfiguriert haben, stehen zur Verwendung zur Verfügung:

         * Wenn Sie Adobe Analytics-Klassifizierungsdaten importieren, wie unter [Schema](/help/components/classifications/sets/manage/schema.md) beschrieben.

           Es können jedoch keine Speicherorte verwendet werden, die für den Import von Klassifizierungsdaten konfiguriert sind. Fügen Sie stattdessen ein neues Ziel wie unten beschrieben hinzu.

         * Wenn Sie Konten und Speicherorte im Bereich „Speicherorte“ konfigurieren, wie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) und [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md) beschrieben.

      1. Wählen Sie den Speicherort aus dem Dropdown [!UICONTROL **Menü**] Speicherort auswählen“ aus.

      1. Wählen [!UICONTROL **Speichern**] > [!UICONTROL **Speichern**].

         Das Ziel ist jetzt so konfiguriert, dass Daten an den von Ihnen angegebenen Azure SAS-Speicherort gesendet werden.

   1. (Bedingt) Wenn Sie zuvor noch kein Azure SAS-Konto hinzugefügt haben:

      1. Wählen Sie [!UICONTROL **Konto hinzufügen**] aus und geben Sie dann die folgenden Informationen an:

         | Feld | Funktion |
         |---------|----------|
         | [!UICONTROL **Kontoname**] | Ein Name für das Azure SAS-Konto. Dieser Name wird im Dropdown-Feld [!UICONTROL **Konto auswählen**] angezeigt und kann ein beliebiger Name sein. |
         | [!UICONTROL **Kontobeschreibung**] | Eine Beschreibung für das Azure SAS-Konto. Diese Beschreibung wird im Dropdown-Feld [!UICONTROL **Konto auswählen**] angezeigt und kann ein beliebiger Name sein. |
         | [!UICONTROL **Anwendungs-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Mandanten-ID**] | Kopieren Sie diese ID aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Übersicht** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **Key Vault-URI**] | <p>Der Pfad zum SAS-URI in Azure Key Vault. Um Azure SAS zu konfigurieren, müssen Sie einen SAS-URI mithilfe des Azure Key Vault als Geheimnis speichern. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zum Einrichten und Abrufen eines Geheimnisses aus Azure Key Vault](https://learn.microsoft.com/de-de/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Nachdem die Key Vault-URI erstellt wurde:<ul><li>Fügen Sie im Key Vault eine Zugriffsrichtlinie hinzu, um der von Ihnen erstellten Azure-Anwendung Berechtigungen zu erteilen.<p>Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation für die Zuweisung einer Key Vault-Zugriffsrichtlinie](https://learn.microsoft.com/de-de/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p><p>Oder</p><p>Wenn Sie eine Zugriffsrolle direkt gewähren möchten, ohne eine Zugriffsrichtlinie zu erstellen, finden Sie weitere Informationen zum Zuweisen von Azure-Rollen mithilfe des Azure-Portals in der [Microsoft Azure-Dokumentation](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal). Dadurch wird die Rollenzuweisung für die Anwendungs-ID hinzugefügt, um auf den Schlüsseltresor-URI zuzugreifen. </p></li><li>Stellen Sie sicher, dass der Anwendungs-ID die `Key Vault Certificate User` integrierte Rolle für den Zugriff auf den URI des Key Vault zugewiesen wurde.</br><p>Weitere Informationen finden Sie unter [Integrierte Azure-Rollen](https://learn.microsoft.com/de-de/azure/role-based-access-control/built-in-roles).</p></li></ul> |
         | [!UICONTROL **Key Vault-Geheimnisname**] | Der Geheimnisname, den Sie beim Hinzufügen des Geheimnisses zum Azure Key Vault erstellt haben. In Microsoft Azure befinden sich diese Informationen im von Ihnen erstellten Key Vault auf den **Key Vault**-Einstellungsseiten. Weitere Informationen finden Sie unter [Microsoft Azure-Dokumentation zum Einrichten und Abrufen eines Geheimnisses aus Azure Key Vault](https://learn.microsoft.com/de-de/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
         | [!UICONTROL **Geheimnis**] | Kopieren Sie das Geheimnis aus der von Ihnen erstellten Azure-Anwendung. In Microsoft Azure befinden sich diese Informationen auf der Registerkarte **Zertifikate und Geheimnisse** in Ihrer Anwendung. Weitere Informationen finden Sie in der [Microsoft Azure-Dokumentation zur Registrierung einer Anwendung bei der Microsoft Identity Platform](https://learn.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app). |

         {style="table-layout:auto"}

      1. Wählen Sie [!UICONTROL **Speicherort hinzufügen**] aus und geben Sie dann die folgenden Informationen an:

         | Feld | Funktion |
         |---------|----------|
         | [!UICONTROL **Name**] | Ein Name für den Speicherort. Dieser Name wird im Dropdown-Feld [!UICONTROL **Speicherort auswählen**] angezeigt und kann ein beliebiger Name sein. |
         | [!UICONTROL **Beschreibung**] | Eine Beschreibung für den Speicherort. Diese Beschreibung wird im Dropdown-Feld [!UICONTROL **Speicherort auswählen**] angezeigt und kann ein beliebiger Name sein. |
         | [!UICONTROL **Container**] | Der Container innerhalb des von Ihnen angegebenen Kontos, an den Adobe Analytics-Daten gesendet werden sollen. |
         | [!UICONTROL **Präfix**] | Der Ordner im Container, in dem Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/`<p>Stellen Sie sicher, dass der SAS-URI-Speicher, den Sie bei der Konfiguration des Azure SAS-Kontos im Feld „Key Vault-Geheimnisname“ angegeben haben, über die `Write`-Berechtigung verfügt. Dadurch kann der SAS-URI Dateien in Ihrem Azure-Container erstellen. <p>Wenn Sie möchten, dass der SAS-URI auch Dateien überschreibt, stellen Sie sicher, dass der SAS-URI-Speicher die `Delete`-Berechtigung besitzt.</p><p>Weitere Informationen finden Sie in der Azure Blob Storage-Dokumentation unter [Blob Storage-Ressourcen](https://learn.microsoft.com/de-de/azure/storage/blobs/storage-blobs-introduction#blob-storage-resources).</p> |

         {style="table-layout:auto"}

      1. Wählen [!UICONTROL **Erstellen**] > [!UICONTROL **Speichern**].

         Das Ziel ist jetzt so konfiguriert, dass Daten an den von Ihnen angegebenen Azure SAS-Speicherort gesendet werden.

      1. (Bedingt) Wenn Sie das soeben erstellte Ziel (Konto und Speicherort) verwalten müssen, ist es in der [Standort-Manager“ ](/help/components/locations/locations-manager.md).

   +++

   +++Google Cloud Platform

   Sie können Feeds direkt an Google Cloud Platform (GCP)-Buckets senden. Dieser Zieltyp erfordert nur Ihren GCP-Kontonamen und den Speicherort (Bucket)-Namen.

   Adobe Analytics verwendet die kontenübergreifende Authentifizierung, um Dateien von Adobe Analytics an den angegebenen Speicherort in Ihrer GCP-Instanz hochzuladen.

   So konfigurieren Sie einen GCP-Bucket als Ziel für einen Daten-Feed:

   1. Wählen Sie in der Adobe Analytics Admin Console im Abschnitt [!UICONTROL **Ziel**] die Option [!UICONTROL **Google Cloud Platform**] aus.

      ![Google Cloud Platform-Ziel](assets/datafeed-destination-gcp.png)

   1. Wählen Sie [!UICONTROL **Speicherort auswählen**] aus.

      Die Seite GCP-Exportverzeichnisse wird angezeigt.

   1. (Bedingt) Wenn in Adobe Analytics bereits ein Google Cloud Platform-Konto (und ein Speicherort in diesem Konto) konfiguriert wurde, können Sie es als Daten-Feed-Ziel verwenden:

      >[!NOTE]
      >
      >Konten stehen nur zur Verfügung, wenn Sie sie konfiguriert haben oder wenn sie für eine Organisation freigegeben wurden, zu der Sie gehören.

      1. Wählen Sie das Konto aus dem Dropdown-Menü [!UICONTROL **Konto auswählen**] aus.

         Alle Cloud-Konten, die Sie in einem der folgenden Bereiche von Adobe Analytics konfiguriert haben, stehen zur Verwendung zur Verfügung:

         * Wenn Sie Adobe Analytics-Klassifizierungsdaten importieren, wie unter [Schema](/help/components/classifications/sets/manage/schema.md) beschrieben.

           Es können jedoch keine Speicherorte verwendet werden, die für den Import von Klassifizierungsdaten konfiguriert sind. Fügen Sie stattdessen ein neues Ziel wie unten beschrieben hinzu.

         * Wenn Sie Konten und Speicherorte im Bereich „Speicherorte“ konfigurieren, wie unter [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) und [Konfigurieren von Cloud-Import- und -Exportspeicherorten](/help/components/locations/configure-import-locations.md) beschrieben.

      1. Wählen Sie den Speicherort aus dem Dropdown [!UICONTROL **Menü**] Speicherort auswählen“ aus.

      1. Wählen [!UICONTROL **Speichern**] > [!UICONTROL **Speichern**].

         Das Ziel ist jetzt so konfiguriert, dass Daten an den von Ihnen angegebenen Google Cloud Platform-Speicherort gesendet werden.

   1. (Bedingt) Wenn Sie zuvor noch kein GCP-Konto hinzugefügt haben:

      1. Wählen Sie [!UICONTROL **Konto hinzufügen**] aus und geben Sie dann die folgenden Informationen an:

         | Feld | Funktion |
         |---------|----------|
         | [!UICONTROL **Kontoname**] | Ein Name für das Konto. Dabei kann es sich um einen beliebigen Namen handeln. |
         | [!UICONTROL **Kontobeschreibung**] | Eine Beschreibung für das Konto. |
         | [!UICONTROL **Projekt-ID**] | Ihre Google Cloud-Projekt-ID. Siehe [Dokumentation zu Google Cloud zum Abrufen einer Projekt-ID](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

         {style="table-layout:auto"}

      1. Wählen Sie [!UICONTROL **Speicherort hinzufügen**] aus und geben Sie dann die folgenden Informationen an:

         | Feld | Funktion |
         |---------|----------|
         | [!UICONTROL **Prinzipal**] | Der Prinzipal wird von Adobe bereitgestellt. Sie müssen die Berechtigung zum Empfang von Feeds an diesen Prinzipal erteilen. |
         | [!UICONTROL **Name**] | Ein Name für das Konto. |
         | [!UICONTROL **Beschreibung**] | Eine Beschreibung für das Konto. |
         | [!UICONTROL **Bucket**] | Der Bucket in Ihrem GCP-Konto, an den Adobe Analytics-Daten gesendet werden sollen. <p>Vergewissern Sie sich, dass Sie dem durch Adobe bereitgestellten Prinzipal eine der folgenden Berechtigungen erteilt haben: (Informationen zum Gewähren von Berechtigungen finden Sie unter [Prinzipal zu einer Richtlinie auf Bucket-Ebene hinzufügen](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) in der Dokumentation zu Google Cloud.)<ul><li>`roles/storage.objectCreator`: Verwenden Sie diese Berechtigung, wenn Sie den Prinzipal so einschränken möchten, dass nur Dateien in Ihrem GCP-Konto erstellt werden. </br>**Wichtig:** Wenn Sie diese Berechtigung mit geplanten Berichten einsetzen, müssen Sie für jeden neuen geplanten Export einen eindeutigen Dateinamen verwenden. Andernfalls schlägt die Berichterstellung fehl, da der Prinzipal nicht berechtigt ist, vorhandene Dateien zu überschreiben.</li><li>(Empfohlen) `roles/storage.objectUser`: Verwenden Sie diese Berechtigung, wenn Sie möchten, dass der Prinzipal Zugriff auf das Anzeigen, Auflisten, Aktualisieren und Löschen von Dateien in Ihrem GCP-Konto hat.</br>Mit dieser Berechtigung kann der Prinzipal vorhandene Dateien bei nachfolgenden Uploads überschreiben, ohne dass für jeden neuen geplanten Export automatisch eindeutige Dateinamen generiert werden müssen.</li></ul><p>Wenn Ihre Organisation [Organisationsrichtlinieneinschränkungen](https://cloud.google.com/storage/docs/org-policy-constraints) verwendet, um nur das Google Cloud Platform-Konto in Ihrer Zulassungsliste zuzulassen, benötigen Sie die folgende Adobe-eigene Organisations-ID für Google Cloud Platform: <ul><li>`DISPLAY_NAME`: `adobe.com`</li><li>`ID`: `178012854243`</li><li>`DIRECTORY_CUSTOMER_ID`: `C02jo8puj`</li></ul> </p> |
         | [!UICONTROL **Präfix**] | Der Ordner im Bucket, in den Sie die Daten ablegen möchten. Geben Sie einen Ordnernamen an und fügen Sie dann einen umgekehrten Schrägstrich nach dem Namen hinzu, um den Ordner zu erstellen. Beispiel: `folder_name/` |

         {style="table-layout:auto"}

      1. Wählen [!UICONTROL **Erstellen**] > [!UICONTROL **Speichern**].

         Das Ziel ist jetzt so konfiguriert, dass Daten an den von Ihnen angegebenen GCP-Speicherort gesendet werden.

      1. (Bedingt) Wenn Sie das soeben erstellte Ziel (Konto und Speicherort) verwalten müssen, ist es in der [Standort-Manager“ ](/help/components/locations/locations-manager.md).

   +++

1. Wählen [!UICONTROL **Abschnitt „Datenspaltendefinitionen**] die neueste Vorlage [!UICONTROL **Alle Adobe-Spalten**] im Dropdown-Menü aus und füllen Sie dann die folgenden Felder aus:

   | Feld | Funktion |
   |---------|----------|
   | [!UICONTROL **Entfernen von Escape-Zeichen**] | Beim Erfassen von Daten können einige Zeichen (z. B. Zeilenumbrüche) Probleme verursachen. Aktivieren Sie dieses Kontrollkästchen, wenn diese Zeichen aus Feed-Dateien entfernt werden sollen. |
   | [!UICONTROL **Komprimierungsformat**] | Der Typ der verwendeten Komprimierung. **Gzip** gibt Dateien im `.tar.gz` Format aus. **Zip** gibt Dateien im `.zip` aus. |
   | [!UICONTROL **Verpackungsart**] | Wählen Sie [!UICONTROL **Mehrere Dateien**] für die meisten Daten-Feeds aus. Mit dieser Option werden Ihre Daten in unkomprimierte 2-GB-Blöcke unterteilt. (Wenn die Option [!UICONTROL **Mehrere Dateien**] ausgewählt ist und die unkomprimierten Daten für das Berichtsfenster weniger als 2 GB betragen, wird eine Datei gesendet.) Wenn Sie **Einzeldatei** auswählen, wird die `hit_data.tsv` in einer einzelnen, potenziell umfangreichen Datei ausgegeben. |
   | [!UICONTROL **Manifest**] | Bestimmt, ob Adobe eine [Manifestdatei) an ](c-df-contents/datafeeds-contents.md#feed-manifest) Ziel senden soll, wenn für ein Feed-Intervall keine Daten erfasst wurden. Wenn Sie **Manifestdatei** auswählen, erhalten Sie eine Manifestdatei ähnlich der folgenden, wenn keine Daten erfasst werden:<p>`text`</p><p>`Datafeed-Manifest-Version: 1.0`</p><p>`Lookup-Files: 0`</p><p>`Data-Files: 0`</p><p> `Total-Records: 0`</p> |
   | [!UICONTROL **Spaltenvorlagen**] | Bei der Erstellung vieler Daten-Feeds empfiehlt Adobe die Erstellung einer Spaltenvorlage. Bei Auswahl einer Spaltenvorlage werden automatisch die angegebenen Spalten in der Vorlage eingefügt. Adobe stellt standardmäßig auch mehrere Vorlagen bereit. |
   | [!UICONTROL **Verfügbare Spalten**] | Alle verfügbaren Datenspalten in Adobe Analytics. Klicken Sie auf [!UICONTROL Alle hinzufügen], um alle Spalten in einen Daten-Feed einzubeziehen. |
   | [!UICONTROL **Enthaltene Spalten**] | Die in einen Daten-Feed einzuschließenden Spalten. Klicken Sie auf [!UICONTROL Alle entfernen], um alle Spalten aus einem Daten-Feed zu entfernen. |
   | [!UICONTROL **CSV herunterladen**] | Lädt eine CSV-Datei herunter, die alle eingeschlossenen Spalten enthält. |

1. Klicken [!UICONTROL **oben**] auf „Speichern“.

   Die Verarbeitung historischer Daten beginnt sofort. Wenn die Datenverarbeitung für einen Tag abgeschlossen ist, wird die Datei an das von Ihnen konfigurierte Ziel gesendet.

   Informationen zum Zugriff auf den Daten-Feed und zu einem besseren Verständnis seiner Inhalte finden Sie unter [Daten-Feed-Inhalte - Übersicht](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md).

## Veraltete Ziele

>[!IMPORTANT]
>
>Die in diesem Abschnitt beschriebenen Ziele sind veraltet und werden nicht empfohlen. Verwenden Sie stattdessen beim Erstellen eines Daten-Feeds eines der folgenden Ziele: Amazon S3, Google Cloud Platform, Azure RBAC oder Azure SAS. Detaillierte [ zu den einzelnen empfohlenen Zielen finden Sie unter](#create-and-configure-a-data-feed) Erstellen und Konfigurieren eines Daten-Feeds .


Die folgenden Informationen enthalten Konfigurationsinformationen für die einzelnen veralteten Ziele:

### FTP

Daten-Feed-Daten können an einen Adobe- oder vom Kunden gehosteten FTP-Speicherort bereitgestellt werden. Erfordert einen FTP-Host, einen Benutzernamen und ein Kennwort. Verwenden Sie das Pfadfeld, um Feed-Dateien in einem Ordner zu platzieren. Ordner müssen bereits vorhanden sein; Feeds geben einen Fehler aus, wenn der angegebene Pfad nicht vorhanden ist.

Verwenden Sie beim Ausfüllen der verfügbaren Felder die folgenden Informationen:

* [!UICONTROL **Host**]: Geben Sie die gewünschte FTP-Ziel-URL ein. Zum Beispiel `ftp://ftp.omniture.com`.
* [!UICONTROL **Pfad**]: Kann leer gelassen werden
* [!UICONTROL **Benutzername**]: Geben Sie den Benutzernamen ein, um sich bei der FTP-Site anzumelden.
* [!UICONTROL **Kennwort und Kennwort bestätigen**]: Geben Sie das Kennwort ein, um sich bei der FTP-Site anzumelden.

### SFTP

SFTP-Unterstützung für Daten-Feeds ist verfügbar. Erfordert einen SFTP-Host und Benutzernamen. Außerdem muss die Ziel-Site einen gültigen öffentlichen RSA- oder DSA-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Feeds herunterladen.

### S3

Sie können Feeds direkt an Amazon S3-Behälter senden. Dieser Zieltyp erfordert einen Behälternamen, eine Zugriffsschlüssel-ID und einen geheimen Schlüssel. Weitere Informationen finden Sie unter [Benennungsanforderungen für Amazon S3-Behälter](https://docs.aws.amazon.com/de_de/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html) in der Amazon S3-Dokumentation.

Der Benutzer, den Sie zum Hochladen von Daten-Feeds angeben, muss über die folgenden [Berechtigungen](https://docs.aws.amazon.com/de_de/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html) verfügen:

* S3:GetObject
* S3:PutObject
* S3:PutObjectAcl

  >[!NOTE]
  >
  >Bei jedem Upload in einen Amazon S3-Bucket fügt [!DNL Analytics] den Bucket-Inhaber zur BucketOwnerFullControl-ACL hinzu, unabhängig davon, ob der Bucket eine Richtlinie enthält, die dies erfordert. Weitere Informationen finden Sie unter [Was ist die BucketOwnerFullControl-Einstellung für Amazon S3-Daten-Feeds?](df-faq.md#BucketOwnerFullControl)&quot;

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

Daten-Feeds unterstützen Azure Blob-Ziele. Erfordert einen Container, ein Konto und einen Schlüssel. Amazon verschlüsselt die Daten automatisch während der Ruhezeit. Wenn Sie die Daten herunterladen, werden sie automatisch entschlüsselt. Weitere Informationen finden Sie unter [Erstellen eines Speicherkontos](https://docs.microsoft.com/de-de/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys) in der Dokumentation zu Microsoft Azure.

>[!NOTE]
>
>Sie müssen Ihren eigenen Prozess implementieren, um Speicherplatz auf dem Feed-Ziel zu verwalten. Adobe löscht keine Daten vom Server.
