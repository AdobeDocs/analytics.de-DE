---
product: analytics
audience: end-user
user-guide-title: Exportleitfaden für Analytics
breadcrumb-title: Exportleitfaden
user-guide-description: Erfahren Sie mehr über die Verwendung von Daten-Feeds zum Exportieren von Rohdaten und Data Warehouse zum Abrufen einer Tabellenausgabe von Daten. Erfahren Sie, wie Sie FTP und SFTP zur Übertragung von Dateien einsetzen können.
source-git-commit: f68cf0de5e7689d8245572b060a3d81c3bf85072
workflow-type: ht
source-wordcount: '284'
ht-degree: 100%

---


# Exportleitfaden für Adobe Analytics {#export}

+ [Exportleitfaden für Analytics](home.md)
+ [Versionshinweise zu Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=de)
+ Analytics-Daten-Feed {#analytics-data-feed}
   + [Daten-Feed-Übersicht](analytics-data-feed/data-feed-overview.md)
   + [Erstellen oder Bearbeiten eines Daten-Feeds](analytics-data-feed/create-feed.md)
   + [Verwalten von Daten-Feeds](analytics-data-feed/df-manage-feeds.md)
   + [Verwalten von Daten-Feed-Aufträgen](analytics-data-feed/df-manage-jobs.md)
   + Daten-Feed-Inhalte {#data-feed-contents}
      + [Daten-Feed-Inhalte – Übersicht](analytics-data-feed/c-df-contents/datafeeds-contents.md)
      + [Metriken berechnen](analytics-data-feed/c-df-contents/datafeeds-calculate.md)
      + [Datenspaltenreferenz](analytics-data-feed/c-df-contents/datafeeds-reference.md)
      + [Seitenereignissuche](analytics-data-feed/c-df-contents/datafeeds-page-event.md)
      + [Dynamische Suchen](analytics-data-feed/c-df-contents/dynamic-lookups.md)
      + [Merchandising-eVar-Suche](analytics-data-feed/c-df-contents/merchandising-evar-lookup.md)
      + [Sonderzeichen](analytics-data-feed/c-df-contents/datafeeds-spec-chars.md)
      + [Verspätete Treffer](analytics-data-feed/c-df-contents/late-arriving-hits.md)
   + [Häufig gestellte Fragen zu Daten-Feeds](analytics-data-feed/df-faq.md)
   + [Best Practices für Daten-Feeds](analytics-data-feed/data-feeds-best-practices.md)
   + [Fehlerbehebung bei Daten-Feeds](analytics-data-feed/troubleshooting.md)
+ Data Warehouse {#data-warehouse}
   + [Data Warehouse-Übersicht](data-warehouse/data-warehouse.md)
   + [Hinzufügen einer Data Warehouse-Benutzergruppe](data-warehouse/t-dw-group.md)
   + Erstellen einer Data Warehouse-Anfrage {#dw-create-request}
      + [Erstellen einer Data Warehouse-Anforderung](/help/export/data-warehouse/create-request/t-dw-create-request.md)
      + [Allgemeine Einstellungen](/help/export/data-warehouse/create-request/dw-general-settings.md)
      + [Erstellen Ihres Berichts](/help/export/data-warehouse/create-request/dw-request-build-report.md)
      + [Berichtsziel](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
      + [Berichtsoptionen](/help/export/data-warehouse/create-request/dw-request-report-options.md)
      + [Planungsoptionen](/help/export/data-warehouse/create-request/dw-request-scheduling.md)
      + [Benachrichtigungs-E-Mail](/help/export/data-warehouse/create-request/dw-request-email.md)
   + [Versandzeit von Anforderungen](data-warehouse/delivery-time.md)
   + [Datei mit Tableau-Daten](data-warehouse/t-tableau.md)
   + [Nach Metrik sortieren](data-warehouse/sorting-by-metric.md)
   + [Verwalten von Data Warehouse-Anforderungen](data-warehouse/data-warehouse-requests-manage.md)
   + [In Data Warehouse unterstützte Komponenten](data-warehouse/component-support.md)
   + [Häufig gestellte Fragen zu Data Warehouse](data-warehouse/faq.md)
   + [Best Practices für Data Warehouse](data-warehouse/data-warehouse-bp.md)
+ FTP und SFTP {#ftp-and-sftp}
   + [FTP und SFTP mit der Adobe Experience Cloud verwenden](ftp-and-sftp/ftp-overview.md)
   + Von Adobe gehostete FTP-Konten einrichten {#set-up-ftp-accounts}
      + [FTP-Konten einrichten – Übersicht](ftp-and-sftp/c-set-up-ftp-accounts/ftp-accounts.md)
      + [Klassifizierungen](ftp-and-sftp/c-set-up-ftp-accounts/ftp-saint.md)
      + [Datenquellen](ftp-and-sftp/c-set-up-ftp-accounts/ftp-datasources.md)
      + [Daten-Feeds](ftp-and-sftp/c-set-up-ftp-accounts/ftp-datafeeds.md)
      + [Von Data Warehouse bereitgestellte Berichte](ftp-and-sftp/c-set-up-ftp-accounts/ftp-dw-reports.md)
      + [Von Report Builder bereitgestellte Berichte](ftp-and-sftp/c-set-up-ftp-accounts/ftp-arb-reports.md)
      + [Engineering Services-Interaktionen mit FTP](ftp-and-sftp/c-set-up-ftp-accounts/ftp-eng-services.md)
   + [FTP-Beschränkungen und Datenaufbewahrung](ftp-and-sftp/ftp-limits.md)
   + [FTP-Daten und FTP-Konten löschen](ftp-and-sftp/ftp-delete.md)
   + [Gelöschte FTP-Daten und FTP-Konten wiederherstellen](ftp-and-sftp/ftp-restore.md)
   + [Adobe FTP-Server aktualisieren](ftp-and-sftp/ftp-upgrade.md)
   + [Passiven FTP-Modus verwenden](ftp-and-sftp/ftp-passive.md)
   + [FTP-Verarbeitungszeiten](ftp-and-sftp/ftp-processing.md)
   + Secure File Transfer Protocol {#secure-file-transfer-protocol}
      + [Aktualisierung der SFTP-Services – Häufig gestellte Fragen](ftp-and-sftp/c-sftp/sftp-upgrade.md)
      + [Secure File Transfer Protocol – Übersicht](ftp-and-sftp/c-sftp/ftp-sftp.md)
      + [Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen](ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
      + [Adobe-Daten an ein externes FTP-Konto mit SFTP senden](ftp-and-sftp/c-sftp/ftp-sftp-transfer.md)
      + [Data Warehouse-Anforderungen an SFTP-Server senden](ftp-and-sftp/c-sftp/ftp-sftp-dw.md)
      + [Verbindung zu Adobe über SFTP ohne Kennwort herstellen](ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
+ [Analysis Workspace-Downloads](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/download-send.html?lang=de)
+ [Adobe Analytics API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)
+ [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/home.html?lang=de)
