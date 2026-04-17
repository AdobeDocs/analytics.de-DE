---
title: Sicherheitsanforderungen für FTP- und SFTP-Server
description: Erfahren Sie mehr über die Sicherheitsanforderungen für FTP- und SFTP-Server.
feature: Data Configuration and Collection
role: Admin
source-git-commit: 26ae4edacbc3591d4d3358afe009bf7831d45efb
workflow-type: tm+mt
source-wordcount: '1899'
ht-degree: 2%

---

# Sicherheitsanforderungen für FTP- und SFTP-Server

Auf dieser Seite werden die Sicherheitsanforderungen für bestehende FTP- und SFTP-Server behandelt, die Daten empfangen, die von Adobe Analytics Daten-Feeds oder Data Warehouse bereitgestellt werden.

* **Bestehende FTP-Server**: Muss für die Verwendung von SFTP aktualisiert werden, wie im folgenden Abschnitt beschrieben: [Aktualisieren von FTP-Servern für die Verwendung von SFTP](#upgrade-ftp-servers-to-use-sftp).

  Ein Upgrade von FTP auf SFTP ist erforderlich, da SFTP die Sicherheit erhöht.

  Alternativ können Sie für ein höheres Sicherheitsniveau zu einem modernen Cloud-Ziel wechseln. (Weitere Informationen finden Sie unter [Konfigurieren von Cloud-Import- und -Exportkonten](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-accounts).)

* **Vorhandene SFTP-Server (und neu aktualisierte SFTP-Server)**: Alte Kennwörter müssen rotiert werden, wie im folgenden Abschnitt beschrieben: &quot;[ des SFTP-Kennworts](#rotate-your-sftp-password).

  Das regelmäßige Rotieren des SFTP-Kennworts ist eine Best Practice für die Sicherheit, die zum Schutz Ihrer Daten beiträgt.

>[!IMPORTANT]
>
>Beachten Sie die folgenden Situationen, bevor Sie die Schritte in diesem Artikel abschließen.
>
>* **Adobe empfiehlt, nach Möglichkeit nicht auf SFTP, sondern auf ein modernes Cloud-Ziel umzustellen.**
>FTP und SFTP sind alte Zieltypen. Anstatt FTP-Konten auf SFTP zu aktualisieren und SFTP-Kennwörter zu drehen, wie in diesem Artikel beschrieben, empfiehlt Adobe, zu einem modernen Cloud-Zieltyp (z. B. Amazon S3, Google Cloud Platform oder Azure) zu wechseln. Diese Cloud-Ziele bieten ein höheres Sicherheitsniveau. Weitere Informationen finden Sie unter [Konfigurieren von Cloud-Import- und -](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-accounts).
>
>* **Wenn FTP- und SFTP-Konten ausschließlich für Klassifizierungen verwendet werden, migrieren Sie zu Klassifizierungssätzen.**
>Wenn Ihr FTP- oder SFTP-Konto ausschließlich für Klassifizierungen verwendet wird, sollten Sie vom **Klassifizierungs-Importer** zu **Klassifizierungssätze** migrieren, anstatt FTP-Konten auf SFTP zu aktualisieren und SFTP-Kennwörter zu rotieren, wie in diesem Artikel beschrieben. Das Classification Importer wird eingestellt und ist nach dem 31. **2026 nicht mehr**. Weitere Informationen finden Sie unter [Übersicht über Klassifizierungssätze](https://experienceleague.adobe.com/en/docs/analytics/components/classifications/sets/overview).

## Voraussetzungen

### Inventarisieren der FTP-Konten

Die auf dieser Seite beschriebenen Prozesse beim Aktualisieren von FTP-Servern auf SFTP müssen für jede FTP-Site abgeschlossen werden, die für Daten-Feeds und Data Warehouse verwendet wird.

Daher müssen Sie alle FTP-Konten identifizieren, die Daten für Daten-Feeds oder Data Warehouse empfangen. Diese Informationen werden in Ihren FTP-Konfigurationseinstellungen angezeigt, wie im Abschnitt [Ältere ](/help/components/locations/configure-import-accounts.md#configure-a-location-account)) des Artikels [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) beschrieben.

Sammeln Sie für jedes Konto die folgenden Informationen:

* **Host**: Der Host-Name des FTP-Servers, mit dem Ihr Konto eine Verbindung herstellt (z. B. `ftp.omniture.com`, `ftp2.omniture.com` usw.).

* **Port**: Bei Verwendung eines von Adobe gehosteten SFTP-Servers stellen SFTP-Clients eine Verbindung über Port 22 her. Nicht sichere FTP-Verbindungen verwenden Port 21.

* **Benutzername**: Der Benutzername, mit dem die Anmeldung beim FTP-Server erfolgt.

* **Geheimnis des Standortkontos**: Das aktuelle Kontogeheimnis für das Konto. Dies ist das Kontogeheimnis (Passwort), das Sie derzeit beim Herunterladen von Daten verwenden, die an Ihren FTP-Speicherort gesendet werden. Diese Informationen sind nicht über die Benutzeroberfläche von Adobe Analytics verfügbar.

### Bestätigen Sie, dass Sie die Anmeldeinformationen in Ihren Tools aktualisieren können

Stellen Sie sicher, dass Sie die SFTP-Kennwörter in jedem Tool oder Skript aktualisieren können, mit dem Sie eine Verbindung zur SFTP-Site herstellen (z. B. SFTP-Client, automatisiertes Skript oder Plattform eines Drittanbieters).

Alle Clients sollten eine Verbindung über SFTP mit einem Passwort als Fallback herstellen.

## Aktualisieren von FTP-Servern auf die Verwendung von SFTP

>[!IMPORTANT]
>
>Wenn Ihre FTP-Daten an einen Drittanbieter geliefert werden (z. B. eine Beratungsfirma oder einen Analytics-Anbieter), stimmen Sie sich mit ihm ab, bevor Sie die Schritte in diesem Artikel befolgen.

### Schritt 1: Generieren der SSH-Schlüssel Ihres Unternehmens zum Herunterladen von Daten

In diesem Abschnitt wird beschrieben, wie Sie die SSH-Schlüssel Ihres Unternehmens (ein Schlüsselpaar aus öffentlichem/privatem Schlüssel) generieren, die zum **(Herunterladen von Daten** vom SFTP-Server verwendet werden.

>[!NOTE]
>
>In einem späteren Schritt laden Sie einen weiteren öffentlichen Schlüssel herunter, der von Adobe bereitgestellt wird. Dies ist Teil eines zweiten Schlüsselpaars aus öffentlichem/privatem Schlüssel, das von Adobe zum **(Hochladen von Daten** auf den SFTP-Server verwendet wird.

So richten Sie eine sichere Übertragung für das Herunterladen von Daten von Ihrem FTP-Server ein:

1. Melden Sie sich bei der Workstation an, von der Sie Daten vom FTP-Server herunterladen.

1. Generieren Sie ein Schlüsselpaar aus öffentlichem/privatem Schlüssel, das für die sichere Übertragung verwendet werden soll.

   Bei Verwendung eines von Adobe gehosteten FTP-Servers unterstützt Adobe RSA- und 25519.

   * **In einer Linux-Umgebung**: Führen Sie den folgenden Befehl aus, um das Schlüsselpaar 25519.

     ```
     ssh-keygen -t ed25519 -C "your-comment-or-email"
     ```

     Wenn Ihre Richtlinie die Verwendung von ed25519-Schlüsseln nicht zulässt, führen Sie den folgenden Befehl aus, um das RSA-Schlüsselpaar zu generieren:

     ```
     ssh-keygen -t rsa -b 4096 -C "your-comment-or-email"
     ```

   * **In einer Windows-Umgebung**: Verwenden Sie PuTTYgen.

1. Datei mit dem Namen [!DNL `authorized_keys`] (ohne Erweiterung) erstellen.

1. Kopieren Sie den Inhalt des öffentlichen Schlüssels in die [!DNL `authorized_keys`].

1. In einem zukünftigen Schritt kehren Sie zu dieser [!DNL `authorized_keys`] zurück, um den öffentlichen Schlüssel von Adobe hinzuzufügen, der von Adobe zum Hochladen von Daten auf den SFTP-Server verwendet wird. Anschließend fügen Sie dem SFTP-Server die [!DNL `authorized_keys`] hinzu.

### Schritt 2: Erstellen eines neuen SFTP-Speicherort-Kontos in Adobe Analytics

Erstellen Sie ein neues SFTP-Speicherort-Konto, um jedes vorhandene FTP-Konto zu ersetzen.

Beim Erstellen eines neuen SFTP-Speicherort-Kontos müssen Sie denselben Host-Namen und Benutzernamen verwenden, die auch in dem vorhandenen FTP-Konto verwendet werden, das es ersetzt.

>[!NOTE]
>
>In einem zukünftigen Schritt konfigurieren Sie dieses neue Speicherort-Konto, das als Ziel für Ihre Daten-Feeds und Data Warehouse-Sendungen verwendet werden soll.

#### SFTP-Konto erstellen

1. Navigieren Sie in Adobe Analytics zu [!UICONTROL **Komponenten**] > [!UICONTROL **Standorte**].

1. Wählen Sie die [!UICONTROL **Speicherort-Konten**] aus.

1. Wählen Sie [!UICONTROL **Konto hinzufügen**] aus.

1. Wählen Sie [!UICONTROL **Dropdown-Feld**] Kontotyp“ die Option [!UICONTROL **SFTP (veraltet)**].

1. Füllen Sie die folgenden Felder aus:

   | Feldname | Funktion |
   |---------|----------|
   | [!UICONTROL **Hostname**] | Ihr SFTP-Host-Name (z. B. `ftp.omniture.com`). |
   | [!UICONTROL **Port**] | Der Firewall-Port, über den Daten gesendet werden. Dies ist Port 22 für von Adobe gehostete SFTP-Verbindungen. |
   | [!UICONTROL **Benutzername**] | Ihr SFTP-Benutzername. Verwenden Sie denselben Benutzernamen wie für Ihr FTP-Konto. |

1. Wählen Sie [!UICONTROL **Speichern**] aus.

1. Laden Sie im Dialogfeld [!UICONTROL **Konto erstellt**] den öffentlichen RSA- oder 25519-Schlüssel herunter und klicken Sie dann auf **[!UICONTROL OK]**. Dies ist der öffentliche SSH-Schlüssel, der von Adobe zum Hochladen von Daten auf den SFTP-Server verwendet wird. (Sie verwenden diesen Schlüssel im folgenden Abschnitt, [Hinzufügen des öffentlichen SSH-Schlüssels von Adobe zum SFTP-Server](#add-adobes-ssh-public-key-to-the-sftp-server).)

1. Wiederholen Sie diesen Vorgang für jedes SFTP-Konto, das Sie erstellen möchten.

1. Fahren Sie mit dem folgenden Abschnitt fort: [Öffentlichen Schlüssel auf den SFTP-Server hochladen](#upload-the-public-key-to-the-sftp-server).

#### Fügen Sie den öffentlichen SSH-Schlüssel von Adobe zur `authorized_keys` hinzu und laden Sie ihn auf Ihren FTP-Server hoch

Der öffentliche Schlüssel, den Sie soeben in Schritt 7 des vorherigen Abschnitts heruntergeladen haben, ist Teil eines Schlüsselpaars aus öffentlichem/privatem Schlüssel, das von Adobe zum Hochladen **Daten** auf den SFTP-Server verwendet wird.

Sie müssen diesen öffentlichen Schlüssel zu derselben `authorized_keys`-Datei hinzufügen, zu der Sie zuvor den Download-Schlüssel Ihres Unternehmens hinzugefügt haben (der Schlüssel, den Sie in [Schritt 1: Generieren des Download-Schlüssels Ihres Unternehmens und Hinzufügen zum FTP-Server](#step-1-generate-your-organizations-download-key-and-add-it-to-your-ftp-server)).

So fügen Sie den öffentlichen SSH-Schlüssel von Adobe zur `authorized_keys` hinzu und laden ihn auf Ihren FTP-Server hoch:

1. Melden Sie sich bei der Workstation an, von der Sie Daten vom FTP-Server herunterladen.

1. Öffnen Sie die [!DNL `authorized_keys`] und fügen Sie den Upload-Schlüssel von Adobe hinzu. Diese Datei sollte bereits den Download-Schlüssel Ihres Unternehmens aus enthalten [Schritt 1: Generieren Sie den Download-Schlüssel Ihres Unternehmens und fügen Sie ihn Ihrem FTP-Server hinzu](#step-1-generate-your-organizations-download-key-and-add-it-to-your-ftp-server).

1. Laden Sie die [!DNL `authorized_keys`]-Datei auf Ihren FTP-Server hoch:

   1. Stellen Sie eine Verbindung zum FTP-Server her und melden Sie sich mit Ihrem Benutzernamen und Kennwort an.\
      Dabei kann es sich um einen von Adobe gehosteten FTP-Server oder einen eigenen FTP-Server handeln.
   1. Das Verzeichnis [!DNL .ssh] erstellen (sofern es noch nicht vorhanden ist).
   1. Die Datei [!DNL `authorized_keys`] in das Verzeichnis [!DNL .ssh] hochladen.

1. Aktualisieren Sie Ihre Firewall-Einstellungen, um eingehende Verbindungen vom SFTP-Server zuzulassen. Wenn Sie einen von Adobe gehosteten SFTP-Server verwenden, lassen Sie eingehende Verbindungen von den IP-Bereichen von Adobe über Port 22 zu.

1. Testen Sie die Verbindung, indem Sie sich mit Ihrem SFTP-Client beim Server anmelden.

1. Wiederholen Sie diesen Vorgang für jedes SFTP-Konto, das Sie im vorherigen Abschnitt (Erstellen [ SFTP-Kontos) erstellt ](#create-the-sftp-account).

1. Fahren Sie mit dem folgenden Abschnitt fort: [Hinzufügen einer Position innerhalb des Kontos](#add-a-location-within-the-account).

#### Einen Speicherort innerhalb des Kontos hinzufügen

1. Wählen Sie auf der **Standorte** die Option **Standort hinzufügen**.

1. Geben Sie einen Namen, eine Beschreibung und an, ob dieser Speicherort mit Daten-Feeds oder Data Warehouse verwendet werden soll.

1. Wählen Sie im Feld [!UICONTROL **Standortkonto**] das soeben erstellte Konto aus.

1. Geben [!UICONTROL **im Feld**] den Pfad zum Verzeichnis auf dem SFTP-Server an. Ordner im Pfad müssen bereits vorhanden sein. Andernfalls tritt ein Fehler auf. Zum Beispiel `/folder_name/folder_name`.

1. Wählen Sie **Speichern** aus.

1. Wiederholen Sie diesen Vorgang für jedes von Ihnen erstellte SFTP-Konto.

Detaillierte Anweisungen finden Sie unter [Konfigurieren von Cloud-Import- und -Exportspeicherorten](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-locations).

### Schritt 3: Bearbeiten von Daten-Feeds und Data Warehouse-Anfragen zur Verwendung des neuen SFTP-Ziels

Aktualisieren Sie alle vorhandenen geplanten Daten-Feeds und Data Warehouse-Anfragen, die derzeit Daten an FTP-Ziele senden, um die von Ihnen erstellten neuen SFTP-Ziele zu verwenden.

#### Daten-Feeds bearbeiten

Bearbeiten Sie jeden geplanten Daten-Feed, der mit dem alten FTP-Ziel konfiguriert ist, um das neue SFTP-Ziel zu verwenden:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**].

1. Suchen Sie den Daten-Feed, den Sie bearbeiten möchten. Um einen Daten-Feed zu finden, können [die Liste der Daten-Feeds filtern und durchsuchen](#filter-and-search-the-list-of-data-feeds).

1. Wählen Sie den Daten-Feed in der Spalte [!UICONTROL **Feed-Name**] aus.

   Die [!UICONTROL **Bearbeiten _feed_name_**] wird angezeigt.

1. Wählen Sie im [!UICONTROL **Ziel**] im Feld [!UICONTROL **Konto**] im Dropdown-Menü das neue von Ihnen erstellte SFTP-Ziel aus.

1. Wählen Sie [!UICONTROL **Feld**] Speicherort“ im Dropdown-Menü den Speicherort im SFTP-Konto aus.

1. Wählen Sie [!UICONTROL **Speichern**] aus.

Weitere Informationen finden Sie unter [Bearbeiten eines Daten-Feeds](/help/export/analytics-data-feed/df-manage-feeds.md#edit-a-data-feed) in [Verwalten von Daten-Feeds](/help/export/analytics-data-feed/df-manage-feeds.md).

#### Data Warehouse-Anfragen bearbeiten

Bearbeiten Sie jede geplante Data Warehouse-Anfrage, die mit dem alten FTP-Ziel konfiguriert ist, um das neue SFTP-Ziel zu verwenden:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Tools**] > [!UICONTROL **Data Warehouse**].

1. Wählen Sie auf der Data Warehouse-Seite die Anfrage aus, die Sie bearbeiten möchten.

   ![Verwalten einer Anfrage](assets/dw-manage-request.png)

1. Wählen Sie [!UICONTROL **Bearbeiten**] aus.

1. Wählen Sie die Registerkarte [!UICONTROL **Berichtsziel**] aus.

1. Wählen Sie im [!UICONTROL **Konto**] im Dropdown-Menü das neue von Ihnen erstellte SFTP-Ziel aus.

1. Wählen Sie [!UICONTROL **Feld**] Speicherort“ im Dropdown-Menü den Speicherort im SFTP-Konto aus.

1. Wählen [!UICONTROL **Änderungen speichern**].

Weitere Informationen finden Sie unter [Anfragen bearbeiten](/help/export/data-warehouse/data-warehouse-requests-manage.md#edit-requests) in [Data Warehouse-Anfragen verwalten](/help/export/data-warehouse/data-warehouse-requests-manage.md).

### Schritt 4: Firewall-Einstellungen aktualisieren

Falls noch nicht geschehen, müssen Sie Ihre Firewall-Einstellungen wie folgt aktualisieren:

* **Bei Verwendung der Adobe-FTP** Server: Aktualisieren Sie Ihre Firewall-Einstellungen, um **ausgehende** Verbindungen an Port 22 zuzulassen.

* **Bei Verwendung eines eigenen FTP-Servers**: Sie müssen Ihre Firewall-Einstellungen aktualisieren, um eine **eingehende** Verbindung an dem Port zuzulassen, an dem Sie den Dienst hosten, normalerweise Port 22.

Sie sollten auch alte FTP-spezifische Regeln entfernen, z. B. eingehende Verbindungen auf Port 21 zulassen. (FTP verwendet Port 21 sowie eine Reihe zusätzlicher Ports für die Datenübertragung. Als Best Practice für die Sicherheit sollten Sie diesen unnötigen Zugriff letztendlich über Ihre Firewall entfernen.)

### Schritt 5: Sicherstellen, dass geplante Daten-Feeds und Data Warehouse-Anfragen korrekt bereitgestellt werden

Warten Sie nach der Aktualisierung aller vorhandenen Daten-Feeds und Data Warehouse-Anfragen auf die Verwendung des neuen SFTP-Kontos und -Speicherorts auf den nächsten geplanten Versand. Stellen Sie sicher, dass die Daten erwartungsgemäß am neuen Ziel eintreffen.

### Schritt 6: Drehen des Kennworts auf dem aktualisierten SFTP-Server

Nach dem Upgrade eines FTP-Servers auf SFTP müssen Sie auch das SFTP-Kennwort rotieren lassen, wie im folgenden Abschnitt &quot;[ des SFTP-Kennworts](#rotate-your-sftp-password) beschrieben.

## Drehen des SFTP-Kennworts

Ein SFTP-Kennwort dient als Fallback-Authentifizierungsmethode, wenn die schlüsselbasierte Authentifizierung fehlschlägt.

Drehen Sie das SFTP-Kennwort kurz nach der Aktualisierung von FTP auf SFTP. Es sollte weiterhin regelmäßig rotiert werden, gemäß Ihren festgelegten Richtlinien.

1. Wenden Sie sich an die Adobe-Kundenunterstützung und fordern Sie ein neues Kennwort an.

1. Geben Sie für jedes SFTP-Konto den **Hostnamen** und **Benutzernamen** an.

   Die Kundenunterstützung generiert für jedes FTP-Konto ein neues Kennwort.

1. Aktualisieren Sie das Kennwort in dem Client, den Sie für die Verbindung mit dem SFTP-Server verwenden.


<!--
< **_Ignore everything after this_** >

-------

## Set up a new SFTP server or upgrade your existing FTP server

## Upgrade your FTP server to use SFTP where files are delivered or FTP account to use SFTP

Set up an SFTP server where Data Feed and Data Warehouse files can be delivered. This could beYou first need to upgrade your FTP server to use SFTP To upgrade an FTP account to use SFTP, follow the steps in [Connect to an FTP account with SFTP](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md).

## Create an SFTP account

## Rotate the passphrase on SFTP accounts


 
Adobe recommends that you periodically rotate the account secrets (passwords) on your FTP accounts that are associated with Data Feeds and Data Warehouse. 
 
Regular rotation of account secrets is a security best practice that helps protect your data. 
 
To ensure uninterrupted reception of data, follow the steps in [Prepare to rotate account secrets](#prepare-to-rotate-account-secrets) prior to changing any account secrets.  
 
>[!IMPORTANT] 
> 
>If your FTP data is delivered to a third-party partner (for example, a consulting firm or Adobe Analytics vendor), coordinate with them before rotating account secrets. The third-party partner will need to update their own tools and scripts with the new account secrets immediately after the new account secrets are provided by your FTP host provider (either Adobe or another provider).

## When rotating account secrets is not necessary 
 
### Transition from FTP to a cloud destination 
 
FTP and SFTP are legacy destination types. Rather than rotating FTP account secrets, Adobe recommends moving to a modern cloud destination type (such as Amazon S3, Google Cloud Platform, or Azure), which provide a higher level of security. For more information, see [Configure cloud import and export accounts](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts). 
 
### Transition from the Classifications importer to Classification sets 
 
If your FTP account is used exclusively for Classifications, you should migrate from the **Classifications importer** to **Classification sets**, rather than rotating your FTP account secrets. The Classification importer will be deprecated and no longer accessible after **August 31, 2026**. For more information, see [Classification sets overview](https://experienceleague.adobe.com/en/docs/analytics/components/classifications/sets/overview). 

## Prepare to rotate account secrets 
 
Complete the following steps before attempting to rotate FTP account secrets: 
 
### Step 1: Inventory your FTP accounts 
 
Identify all FTP accounts that are receiving data for Data Feeds or Data Warehouse. This information is shown in your FTP configuration settings, as described in the [Legacy account types](/help/components/locations/configure-import-accounts.md#configure-a-location-account) section of the article [Configure cloud import and export accounts](/help/components/locations/configure-import-accounts.md). 
 
For each account, gather the following information: 
 
* **Host**: The FTP destination of the host your account connects to (for example, `ftp.omniture.com`, `ftp2.omniture.com`, and so forth). 
 
* **Port**: SFTP clients connect on port 22. FTP connections that are non-secure use port 21. 
 
* **Username**: The username used to log in to the FTP site. 
 
* **location account secret**: The current account secret for the account. This is the account secret (password) that you use currently when downloading data delivered to your FTP location. This information is not available from the Adobe Analytics interface. 
 
 
### Step 2: Confirm that you can update credentials in your tools 
 
Make sure you can update the FTP account secret in whatever tool or script you use to connect to the FTP site (for example, an FTP client, automated script, or third-party platform). 
 
### Step 3: Create FTP cloud location accounts with your current credentials 
 
Create new FTP cloud location accounts to replace your existing FTP location accounts. These new accounts will be used as the destination for your Data Feeds and Data Warehouse deliveries.  
 
When creating the new FTP accounts, you must use the same hostname, username, and account secret that are used in your existing FTP accounts. 
 
#### Create each FTP account 
 
1. In Adobe Analytics, go to **Components** > **Locations**. 
 
1. Select the **Location accounts** tab. 
 
1. Select **Add account**. 
 
1. In the **Account type** drop-down field, select **FTP (legacy)**. 
 
1. Complete the following fields: 

   | Field name | Function |
   |---------|----------|
   | **Hostname** |  Your Adobe FTP hostname (for example, `ftp.omniture.com`). | 
   | **Port** | SFTP clients connect on port 22. FTP connections that are non-secure use port 21. | 
   | **Username** | Your current FTP username. |
   | **Location account secret** | Your current FTP account secrets (password).  |
 
1. Select **Save**. 
 
Repeat this process for each FTP account. 
 
For detailed instructions, see [Configure cloud import and export accounts](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts). 
 
#### Add a location within the account 
 
1. On the **Locations** tab, select **Add location**. 
 
1. Specify a name, description, and whether this location will be used with Data Feeds or Data Warehouse. 
 
1. In the [!UICONTROL **Location account**] field, select the account you just created. 
 
1. In the [!UICONTROL **Directory path**] field, specify the path to the directory on the FTP server. Folders must already exist; feeds throw an error if the specified path does not exist. For example, `/folder_name/folder_name`. 
 
1. Select **Save**. 
 
Repeat this process for each location. 
 
For detailed instructions, see [Configure cloud import and export locations](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-locations). 
 
### Step 4: Reference the new FTP cloud accounts from any scheduled Data Feeds and Data Warehouse requests 
 
Update any existing scheduled Data Feeds and Data Warehouse requests to use the FTP cloud accounts you created.  
 
* **Data Feeds**: Go to **Admin** > **Data Feeds**, edit each scheduled  Data Feed that uses an FTP account, then change the destination to the newly created FTP cloud account. 
 
  For detailed instructions, see [Edit a data feed](/help/export/analytics-data-feed/df-manage-feeds.md#edit-a-data-feed) in [Manage data feeds](/help/export/analytics-data-feed/df-manage-feeds.md). 
 
* **Data Warehouse**: Go to **Tools** > **Data Warehouse**, edit each scheduled Data Warehouse request that uses an FTP account, then change the report destination to the newly created FTP cloud account. 
 
  For detailed instructions, see [Edit requests](/help/export/data-warehouse/data-warehouse-requests-manage.md#edit-requests) in [Manage Data Warehouse requests](/help/export/data-warehouse/data-warehouse-requests-manage.md). 
 
### Step 5: Ensure that scheduled Data Feeds and Data Warehouse requests are being delivered correctly. 
 
After updating each existing Data Feed and Data Warehouse request to use the new FTP account and location, wait for the next scheduled delivery. Verify that data arrives at the new destination as expected. 

## Request a new account secret 
 
>[!IMPORTANT] 
>
>Before requesting a new account secret, consider the following:
>
>* The steps in this section apply only if you are using an Adobe-provided FTP account. For example, the FTP hostname is `ftp.omniture.com`, `ftp2.omniture.com` or similar.   If your FTP hostname is not provided by Adobe, please contact your FTP host provider for details on changing the account secret.
> 
>* Request a new account secret only after you complete all the preparation steps described in [Prepare to rotate account secrets](#prepare-to-rotate-account-secrets). 
>
>* After Adobe Customer Care or your third-party FTP host provider provides a new account secret, the old account secret is immediately invalidated. There is no way to revert to the previous account secret. 
>
 
To request a new account secret from Adobe: 
 
1. Contact Adobe Customer Care. 
 
1. For each FTP account, provide the **Hostname** and **Username** for each account that needs a new account secret. 
 
   Customer Care will generate a new account secret for each FTP account. 

1. Continue immediately with the following section, [After you receive the new account secret](#after-you-receive-the-new-account-secret).
 
## After you receive the new account secret 
 
Act immediately after receiving the new credentials. Any delay results in failed deliveries for active Data Feeds and Data Warehouse requests. 
 
### Step 1: Update your tools and scripts 
 
Update the FTP account secret in any tool, script, or automated process that connects to the FTP account. Make sure all team members and third-party partners who access the account are notified. 
 
### Step 2: Update your cloud location accounts 
 
1. In Adobe Analytics, go to **Components** > **Locations**. 

1. Select the **Location accounts** tab. 

1. Find the FTP account that you created in Step 3 of section, [Prepare to rotate account secrets](#prepare-to-rotate-account-secrets).

1. Select **Edit details**. 

1. Enter the new account secret and confirm it. 

1. Select **Save**. 
 
Repeat this process for each account that was reset. 

For more detailed information about this process, see [Configure cloud import and export accounts](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts).
 
### Step 3: Test your connections 
 
Verify that your Data Feeds or Data Warehouse requests that use the FTP account are working correctly with the new account secret. 
 
>[!TIP] 
> 
>If your current tools use SFTP with SSH keys that haven't been recently rotated, consider rotating those keys as well.

 
## Troubleshooting 
 
If something goes wrong after the account secret is rotated and you cannot restore connectivity, you can create a new FTP account. After the new account is set up, point your Data Feed or Data Warehouse request to the new account and update your cloud location accordingly. 

For information about how to create an FTP account, see [Configure cloud import and export accounts](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts).

To set up secure transfer with your FTP server: 

1. Generate a public/private key pair to use for secure transfer.

   This process differs depending on whether your FTP server is Adobe-hosted or self-hosted:

   +++ For an Adobe-hosted FTP server:

   Generate a public/private key pair: 
   
      * **In a Linux environment**: Run the following command to generate the ed25519 key pair: 

        ```
        ssh-keygen -t ed25519 -C "your-comment-or-email"
        ```

        If your policy does not allow you to use ed25519 keys, run the following command to generate the RSA key pair (**Note:** The RSA key typically applies to customers who operate under FIPS 186-4, as ed25519 is first supported in the newer FIPS 186-5):

        ```
        ssh-keygen -t rsa -b 4096 -C "your-comment-or-email"
        ```

      * **In a Windows environment**: Use PuTTYgen.

   +++

   +++ For a self-hosted FTP server: 
   
   If you want to set up secure transfer with your own FTP server, you must have an SFTP hostname, username, and SFTP account within Adobe Analytics that contains a valid RSA or ed25519 public key from Adobe. This key must be installed on your SFTP server. You download this public key as part of the process of [creating the SFTP account](#create-the-sftp-account).

   +++

1. Create a file named [!DNL `authorized_keys`] (no extension).



3 basic steps: Set up SFTP on customer side, then on Adobe side, then change passphrase. 

1. FTP site: ftp.omniture.com - Using username/password to connect. Adobe uses the same username/password to connect to the site.

2. user can then upload their public key to that server, then start connecting to that server with their private key using SFTP. (They also need to open Port 22 in the firewall and they would close the other ports they don't need.)

3. In Locations, create a new location, use the same username. 

4. After they create that location, we give them our public key, and they have to install it on their SFTP server.

5. Then they switch all their data feeds to use the new Location. And then we'll use SFTP to send the data. 

6. Then they call Customer Care to get new passphrase (rotate passphrase), and then they change the passphrase on their side. Passphrase is only used if SSH fails (they have the wrong keys--a bad actor could use bad keys and then use the password. But they don't have to coordinate the switching of the passphrase with installation of SFTP. )


If they're using a third-party to do this, the third-party would need to set up SFTP - This is the same as we have documented right now. It doesn't have to be immediate, though, like we were assuming before. 


If it's they're own FTP site, it would be the same. They would need to start using SFTP with their FTP server, then get our public key and install it on their server. Shouldn't matter if the FTP site is hosted by Adobe or not. 

-->

