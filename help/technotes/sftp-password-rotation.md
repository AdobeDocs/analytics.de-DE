---
title: Sicherheitsanforderungen für FTP- und SFTP-Server
description: Erfahren Sie mehr über die Sicherheitsanforderungen für FTP- und SFTP-Server.
feature: Data Configuration and Collection
role: Admin
TQID: 'https://experienceleague.adobe.com/qbBCeUihfvRTQm7LvR8jylRWf8rRlzFoZfs62l0fito'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 301a0341e725ca15f1700046528ea5f42969add4
workflow-type: tm+mt
source-wordcount: 1933
ht-degree: 100%

---

# Sicherheitsanforderungen für FTP- und SFTP-Server

Auf dieser Seite werden die Sicherheitsanforderungen für bestehende FTP- und SFTP-Server behandelt, die Daten empfangen, die von Adobe Analytics Daten-Feeds oder Data Warehouse bereitgestellt werden.

* **Bestehende FTP-Server:** Müssen für die Verwendung von SFTP aktualisiert werden, wie unten im Abschnitt [Aktualisieren von FTP-Servern für die Verwendung von SFTP](#upgrade-ftp-servers-to-use-sftp) beschrieben.

  Ein Upgrade von FTP auf SFTP ist erforderlich, da SFTP die Sicherheit erhöht.

  Alternativ können Sie für ein höheres Sicherheitsniveau zu einem modernen Cloud-Ziel wechseln. (Weitere Informationen finden Sie unter [Konfigurieren von Cloud-Import- und Exportkonten](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-accounts).)

* **Bestehende SFTP-Server (und kürzlich aktualisierte SFTP-Server):** Alte Kennwörter müssen rotiert werden, wie unten im Abschnitt [Rotieren des SFTP-Kennworts](#rotate-your-sftp-password) beschrieben.

  Das regelmäßige Rotieren des SFTP-Kennworts ist eine Best Practice für die Sicherheit, die zum Schutz Ihrer Daten beiträgt.

>[!IMPORTANT]
>
>Bedenken Sie folgende Situationen, bevor Sie die Schritte in diesem Artikel abschließen.
>
>* **Adobe empfiehlt, nach Möglichkeit zu einem modernen Cloud-Ziel zu wechseln, anstatt ein Upgrade auf SFTP durchzuführen.**
>FTP und SFTP sind veralte Zieltypen. Anstatt FTP-Konten auf SFTP zu aktualisieren und SFTP-Kennwörter zu rotieren, wie in diesem Artikel beschrieben, empfiehlt Adobe, zu einem modernen Cloud-Zieltyp zu wechseln (z. B. Amazon S3, Google Cloud Platform oder Azure). Diese Cloud-Ziele bieten ein höheres Sicherheitsniveau. Weitere Informationen finden Sie unter [Konfigurieren von Cloud-Import- und Exportkonten](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-accounts).
>
>* **Wenn FTP- und SFTP-Konten ausschließlich für Klassifizierungen verwendet werden, migrieren Sie zu Klassifizierungssätzen.**
>Wenn Ihr FTP- oder SFTP-Konto ausschließlich für Klassifizierungen verwendet wird, sollten Sie vom **Classification Importer** zu **Klassifizierungssätzen** migrieren, anstatt FTP-Konten auf SFTP zu aktualisieren und SFTP-Kennwörter zu rotieren, wie in diesem Artikel beschrieben. Der Classification Importer wird eingestellt und ist nach dem **31. August 2026** nicht mehr verfügbar. Weitere Informationen finden Sie unter [Klassifizierungssätze – Überblick](https://experienceleague.adobe.com/de/docs/analytics/components/classifications/sets/overview).

## Voraussetzungen

### Inventarisieren der FTP-Konten

Sie müssen die SFTP-Upgrade-Schritte auf dieser Seite für jede FTP-Site ausführen, die mit Daten-Feeds oder Data Warehouse verwendet wird.

Daher müssen Sie alle FTP-Konten identifizieren, die Daten für Daten-Feeds oder Data Warehouse empfangen. Diese Informationen werden in Ihren FTP-Konfigurationseinstellungen angezeigt, wie im Abschnitt [Alte Kontotypen](/help/components/locations/configure-import-accounts.md#configure-a-location-account) im Artikel [Konfigurieren von Cloud-Import- und -Exportkonten](/help/components/locations/configure-import-accounts.md) beschrieben.

Erfassen Sie für jedes Konto die folgenden Informationen:

* **Host:** Der Host-Name des FTP-Servers, mit dem Ihr Konto eine Verbindung herstellt (z. B. `ftp.omniture.com`, `ftp2.omniture.com` usw.).

* **Port:** Bei Verwendung eines von Adobe gehosteten SFTP-Servers stellen SFTP-Clients eine Verbindung über Port 22 her. Nicht sichere FTP-Verbindungen verwenden Port 21.

* **Benutzername:** Der für die Anmeldung bei der FTP-Site verwendete Benutzername.

* **Geheimnis des Standortkontos**: Das aktuelle Kontogeheimnis für das Konto. Dies ist das Kontogeheimnis (Kennwort), das Sie derzeit beim Herunterladen von Daten verwenden, die an Ihren FTP-Speicherort gesendet werden. Diese Informationen sind nicht über die Benutzeroberfläche von Adobe Analytics verfügbar.

### Bestätigen, dass Sie die Anmeldeinformationen in Ihren Tools aktualisieren können

Stellen Sie sicher, dass Sie die SFTP-Kennwörter in jedem Tool oder Skript aktualisieren können, mit dem Sie eine Verbindung zur SFTP-Site herstellen (z. B. SFTP-Client, automatisches Skript oder Plattform eines Drittanbieters).

Alle Clients sollten eine Verbindung über SFTP mit einem Kennwort als Fallback-Option herstellen.

## Aktualisieren von FTP-Servern auf die Verwendung von SFTP

>[!IMPORTANT]
>
>Wenn Ihre FTP-Daten an einen Drittanbieter geliefert werden (z. B. eine Beratungsfirma oder einen Analytics-Anbieter), stimmen Sie sich mit ihm ab, bevor Sie die Schritte in diesem Artikel befolgen.

### Schritt 1: Generieren der SSH-Schlüssel Ihres Unternehmens zum Herunterladen von Daten

In diesem Abschnitt wird beschrieben, wie Sie die SSH-Schlüssel Ihres Unternehmens (ein Schlüsselpaar aus öffentlichem/privatem Schlüssel) generieren, die zum **Herunterladen von Daten** vom SFTP-Server verwendet werden.

>[!NOTE]
>
>In einem späteren Schritt laden Sie einen weiteren öffentlichen Schlüssel herunter, der von Adobe bereitgestellt wird. Dies ist Teil eines zweiten Schlüsselpaars aus öffentlichem/privatem Schlüssel, das von Adobe zum **Hochladen von Daten** auf den SFTP-Server verwendet wird.

So richten Sie eine sichere Übertragung für das Herunterladen von Daten von Ihrem FTP-Server ein:

1. Melden Sie sich bei der Workstation an, von der Sie Daten vom FTP-Server herunterladen.

1. Generieren Sie ein Schlüsselpaar aus öffentlichem/privatem Schlüssel, das für die sichere Übertragung verwendet werden soll.

   Bei Verwendung eines von Adobe gehosteten SFTP-Servers unterstützt Adobe RSA- und ed25519-Schlüssel.

   * **In einer Linux-Umgebung:** Führen Sie den folgenden Befehl aus, um das ed25519-Schlüsselpaar zu generieren:

     ```
     ssh-keygen -t ed25519 -C "your-comment-or-email"
     ```

     Wenn Ihre Richtlinie die Verwendung von ed25519-Schlüsseln nicht zulässt, führen Sie den folgenden Befehl aus, um das RSA-Schlüsselpaar zu generieren:

     ```
     ssh-keygen -t rsa -b 4096 -C "your-comment-or-email"
     ```

   * **In einer Windows-Umgebung:** Verwenden Sie PuTTYgen.

1. Datei mit dem Namen [!DNL `authorized_keys`] (ohne Erweiterung) erstellen.

1. Kopieren Sie den Inhalt des öffentlichen Schlüssels in die Datei [!DNL `authorized_keys`].

1. In einem zukünftigen Schritt kehren Sie zu dieser Datei [!DNL `authorized_keys`] zurück, um den öffentlichen Schlüssel von Adobe hinzuzufügen, der von Adobe zum Hochladen von Daten auf den SFTP-Server verwendet wird. Anschließend fügen Sie dem SFTP-Server die Datei [!DNL `authorized_keys`] hinzu.

### Schritt 2: Erstellen eines neuen SFTP-Speicherort-Kontos in Adobe Analytics

Erstellen Sie ein neues SFTP-Speicherort-Konto, um jedes vorhandene FTP-Konto zu ersetzen.

Beim Erstellen eines neuen SFTP-Speicherort-Kontos müssen Sie denselben Host-Namen und Benutzernamen verwenden, die auch im vorhandenen FTP-Konto verwendet werden, das ersetzt wird.

>[!NOTE]
>
>In einem zukünftigen Schritt konfigurieren Sie dieses neue Speicherort-Konto, das als Ziel für Ihre Daten-Feeds und den Data Warehouse-Versand verwendet werden soll.

#### Erstellen des SFTP-Kontos

1. Navigieren Sie in Adobe Analytics zu [!UICONTROL **Komponenten**] > [!UICONTROL **Speicherorte**].

1. Wählen Sie die Registerkarte [!UICONTROL **Speicherort-Konten**] aus.

1. Wählen Sie [!UICONTROL **Konto hinzufügen**] aus.

1. Wählen Sie im Dropdown-Menü [!UICONTROL **Kontotyp**] die Option [!UICONTROL **SFTP (veraltet)**] aus.

1. Füllen Sie die folgenden Felder aus:

   | Feldname | Funktion |
   |---------|----------|
   | [!UICONTROL **Host-Name**] | Ihr SFTP-Host-Name (z. B. `ftp.omniture.com`). |
   | [!UICONTROL **Port**] | Der Firewall-Port, über den Daten gesendet werden. Dies ist Port 22 für von Adobe gehostete SFTP-Verbindungen. |
   | [!UICONTROL **Benutzername**] | Ihr SFTP-Benutzername. Verwenden Sie denselben Benutzernamen wie für Ihr FTP-Konto. |

1. Wählen Sie [!UICONTROL **Speichern**] aus.

1. Laden Sie im Dialogfeld [!UICONTROL **Konto erstellt**] den öffentlichen RSA- oder ed25519-Schlüssel herunter und klicken Sie dann auf [!UICONTROL **OK**]. Dies ist der öffentliche SSH-Schlüssel, der von Adobe zum Hochladen von Daten auf den SFTP-Server verwendet wird. (Sie verwenden diesen Schlüssel im folgenden Abschnitt, [Hinzufügen des öffentlichen SSH-Schlüssels von Adobe zum SFTP-Server](#add-adobes-ssh-public-key-to-the-sftp-server).)

1. Wiederholen Sie diesen Vorgang für jedes SFTP-Konto, das Sie erstellen möchten.

1. Fahren Sie mit dem folgenden Abschnitt [Hochladen des öffentlichen Schlüssels auf den SFTP-Server](#upload-the-public-key-to-the-sftp-server) fort.

#### Hinzufügen des öffentlichen SSH-Schlüssels von Adobe zur Datei [!DNL `authorized_keys`] und Hochladen auf Ihren FTP-Server

Der öffentliche Schlüssel, den Sie soeben in Schritt 7 des vorherigen Abschnitts heruntergeladen haben, ist Teil eines Schlüsselpaars aus öffentlichem/privatem Schlüssel, das von Adobe zum **Hochladen von Daten** auf den SFTP-Server verwendet wird.

Sie müssen diesen öffentlichen Schlüssel in dieselbe Datei [!DNL `authorized_keys`] hinzufügen, in die Sie zuvor den Download-Schlüssel Ihres Unternehmens eingefügt haben (den Schlüssel, den Sie in [Schritt 1: Generieren der SSH-Schlüssel Ihres Unternehmens zum Herunterladen von Daten](#step-1-generate-your-organizations-ssh-keys-for-downloading-data) generiert haben).

So fügen Sie den öffentlichen SSH-Schlüssel von Adobe zur Datei [!DNL `authorized_keys`] hinzu und laden sie auf Ihren FTP-Server hoch:

1. Melden Sie sich bei der Workstation an, von der Sie Daten vom FTP-Server herunterladen.

1. Öffnen Sie die Datei [!DNL `authorized_keys`] und fügen Sie den Upload-Schlüssel von Adobe hinzu. Diese Datei sollte bereits den Download-Schlüssel Ihres Unternehmens aus [Schritt 1: Generieren der SSH-Schlüssel Ihres Unternehmens zum Herunterladen von Daten](#step-1-generate-your-organizations-ssh-keys-for-downloading-data) enthalten.

1. Laden Sie die Datei [!DNL `authorized_keys`] auf den FTP-Server hoch:

   1. Stellen Sie eine Verbindung zum FTP-Server her und melden Sie sich mit Ihrem Benutzernamen und Kennwort an.
Dabei kann es sich um einen von Adobe gehosteten FTP-Server oder einen eigenen FTP-Server handeln.
   1. Das Verzeichnis [!DNL .ssh] erstellen (sofern es noch nicht vorhanden ist).
   1. Die Datei [!DNL `authorized_keys`] in das Verzeichnis [!DNL .ssh] hochladen.

1. Aktualisieren Sie Ihre Firewall-Einstellungen, um eingehende Verbindungen vom SFTP-Server zuzulassen. Wenn Sie einen von Adobe gehosteten SFTP-Server verwenden, lassen Sie eingehende Verbindungen von den IP-Bereichen von Adobe über Port 22 zu.

1. Testen Sie die Verbindung, indem Sie sich mit Ihrem SFTP-Client beim Server anmelden.

1. Wiederholen Sie diesen Vorgang für jedes SFTP-Konto, das Sie im vorherigen Abschnitt [Erstellen SFTP-Kontos](#create-the-sftp-account) erstellt haben.

1. Fahren Sie mit dem folgenden Abschnitt [Hinzufügen eines Speicherorts innerhalb des Kontos](#add-a-location-within-the-account) fort.

#### Hinzufügen eines Speicherorts innerhalb des Kontos

1. Wählen Sie auf der Registerkarte [!UICONTROL **Speicherorte**] die Option [!UICONTROL **Speicherort hinzufügen**] aus.

1. Geben Sie einen Namen und eine Beschreibung an und legen Sie fest, ob dieser Speicherort mit Daten-Feeds oder Data Warehouse verwendet werden soll.

1. Wählen Sie im Feld [!UICONTROL **Speicherort-Konto**] das soeben erstellte Konto aus.

1. Geben Sie im Feld [!UICONTROL **Verzeichnispfad**] den Pfad zum Verzeichnis auf dem SFTP-Server an. Die Ordner im Pfad müssen bereits vorhanden sein. Anderenfalls tritt ein Fehler auf. Zum Beispiel `/folder_name/folder_name`.

1. Wählen Sie [!UICONTROL **Speichern**] aus.

1. Wiederholen Sie diesen Vorgang für jedes von Ihnen erstellte SFTP-Konto.

Ausführliche Anleitungen finden Sie unter [Konfigurieren von Cloud-Import- und -Exportspeicherorten](https://experienceleague.adobe.com/de/docs/analytics/components/locations/configure-import-locations).

### Schritt 3: Bearbeiten von Daten-Feeds und Data Warehouse-Anfragen zur Verwendung des neuen SFTP-Ziels

Aktualisieren Sie alle vorhandenen geplanten Daten-Feeds und Data Warehouse-Anfragen, die derzeit Daten an FTP-Ziele senden, um die von Ihnen erstellten neuen SFTP-Ziele zu verwenden.

#### Bearbeiten von Daten-Feeds

Bearbeiten Sie jeden mit dem alten FTP-Ziel konfigurierten geplanten Daten-Feed so, dass er das neue SFTP-Ziel verwendet:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Admin**] > [!UICONTROL **Daten-Feeds**] aus.

1. Suchen Sie den Daten-Feed, den Sie bearbeiten möchten. Um einen Daten-Feed zu finden, können Sie [die Liste der Daten-Feeds filtern und durchsuchen](#filter-and-search-the-list-of-data-feeds).

1. Wählen Sie den Daten-Feed in der Spalte [!UICONTROL **Feed-Name**] aus.

   Die Seite [!UICONTROL **feed-name bearbeiten __**] wird angezeigt.

1. Wählen Sie im Abschnitt [!UICONTROL **Ziel**] im Feld [!UICONTROL **Konto**] mit dem Dropdown-Menü das neue von Ihnen erstellte SFTP-Ziel aus.

1. Wählen Sie mit dem Dropdown-Menü im Feld [!UICONTROL **Speicherort**] den Speicherort im SFTP-Konto aus.

1. Wählen Sie [!UICONTROL **Speichern**] aus.

Weitere Informationen finden Sie unter [Bearbeiten eines Daten-Feeds](/help/export/analytics-data-feed/df-manage-feeds.md#edit-a-data-feed) in [Verwalten von Daten-Feeds](/help/export/analytics-data-feed/df-manage-feeds.md).

#### Bearbeiten von Data Warehouse-Anfragen

Bearbeiten Sie jede mit dem alten FTP-Ziel konfigurierte geplante Data Warehouse-Anfrage so, dass sie das neue SFTP-Ziel verwendet:

1. Wählen Sie in Adobe Analytics [!UICONTROL **Tools**] > [!UICONTROL **Data Warehouse**] aus.

1. Wählen Sie auf der Seite „Data Warehouse“ die Anfrage aus, die Sie bearbeiten möchten.

   ![Verwalten einer Anfrage](assets/dw-manage-request.png)

1. Wählen Sie [!UICONTROL **Bearbeiten**] aus.

1. Wählen Sie die Registerkarte [!UICONTROL **Berichtsziel**] aus.

1. Wählen Sie im Feld [!UICONTROL **Konto**] mit dem Dropdown-Menü das neue von Ihnen erstellte SFTP-Ziel aus.

1. Wählen Sie mit dem Dropdown-Menü im Feld [!UICONTROL **Speicherort**] den Speicherort im SFTP-Konto aus.

1. Wählen Sie [!UICONTROL **Änderungen speichern**] aus.

Weitere Informationen finden Sie unter [Bearbeiten von Anfragen](/help/export/data-warehouse/data-warehouse-requests-manage.md#edit-requests) in [Verwalten von Data Warehouse-Anfragen](/help/export/data-warehouse/data-warehouse-requests-manage.md).

### Schritt 4: Aktualisieren der Firewall-Einstellungen

Falls noch nicht geschehen, müssen Sie Ihre Firewall-Einstellungen wie folgt aktualisieren:

* **Bei Verwendung der FTP-Server von Adobe:** Aktualisieren Sie Ihre Firewall-Einstellungen, um **ausgehende** Verbindungen an Port 22 zuzulassen.

* **Bei Verwendung eines eigenen FTP-Servers:** Sie müssen Ihre Firewall-Einstellungen aktualisieren, um **eingehende** Verbindungen an dem Port zuzulassen, an dem Sie den Dienst hosten, normalerweise Port 22.

Sie sollten auch alte FTP-spezifische Regeln entfernen, z. B. das Zulassen eingehender Verbindungen auf Port 21. (FTP verwendet Port 21 sowie eine Reihe zusätzlicher Ports für die Datenübertragung. Als Best Practice für die Sicherheit sollten Sie diesen unnötigen Zugriff letztendlich über Ihre Firewall entfernen.)

### Schritt 5: Sicherstellen, dass geplante Daten-Feeds und Data Warehouse-Anfragen korrekt bereitgestellt werden

Warten Sie nach der Aktualisierung aller vorhandenen Daten-Feeds und Data Warehouse-Anfragen für die Verwendung des neuen SFTP-Kontos und -Speicherorts auf den nächsten geplanten Versand. Stellen Sie sicher, dass die Daten wie erwartet am neuen Ziel eintreffen.

### Schritt 6: Rotieren des Kennworts auf dem aktualisierten SFTP-Server

Nach dem Upgrade eines FTP-Servers auf SFTP müssen Sie auch das SFTP-Kennwort rotieren, wie im folgenden Abschnitt [Rotieren des SFTP-Kennworts](#rotate-your-sftp-password) beschrieben.

## Rotieren des SFTP-Kennworts

Ein SFTP-Kennwort dient als Fallback-Authentifizierungsmethode, wenn die schlüsselbasierte Authentifizierung fehlschlägt.

Rotieren Sie das SFTP-Kennwort kurz nach der Aktualisierung von FTP auf SFTP. Es sollte auch künftig entsprechend Ihren etablierten Richtlinien regelmäßig rotiert werden.

1. Wenden Sie sich an die Adobe-Kundenunterstützung und fordern Sie ein neues Kennwort an.

1. Geben Sie für jedes SFTP-Konto den **Host-Namen** und **Benutzernamen** an.

   Die Kundenunterstützung generiert für jedes FTP-Konto ein neues Kennwort.

1. Aktualisieren Sie das Kennwort in dem Client, den Sie für die Verbindung mit dem SFTP-Server verwenden.


