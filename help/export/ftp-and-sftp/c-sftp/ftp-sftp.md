---
description: SFTP ist ein sicheres Protokoll für die Übertragung von Daten, mit dem sichergestellt wird, dass außer Ihnen niemand Ihre Daten sehen kann. Für Adobe Engineering Services kann ein SFTP-Konto eingerichtet werden, in dem Ihre Daten sicher sind.
keywords: ftp;sftp
title: Secure File Transfer Protocol – Übersicht
feature: FTP Export
exl-id: ea0448f9-1685-4a8f-b2f9-49d315c6ab71
TQID: https://experienceleague.adobe.com/kJYtQSuxz-2NMUYqZb01wsr6ltQQbD5itpPYYzsmlCM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 80%

---

# Secure File Transfer Protocol – Übersicht

SFTP ist ein sicheres Protokoll für die Datenübertragung, das sicherstellt, dass niemand außer Ihnen Ihre Daten sehen kann. Für Adobe Engineering Services kann ein SFTP-Konto eingerichtet werden, in dem Ihre Daten sicher sind.

## Push-Auslieferung {#section_A47831BB1DCA490BB57F0940617AA506}

Das bedeutet, dass die Server von Adobe die Datei an Ihre Server „pushen“. Im Wesentlichen liefern wir sie an Ihren Endpunkt.

[Data Warehouse](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) - und [Analytics-Daten-Feed](/help/export/analytics-data-feed/data-feed-overview.md) können Daten per SFTP übertragen.

Report Builder **kann** Daten per SFTP übertragen.

## Pull-Auslieferung {#section_FA29FAEF02FE40B8B32452146A036F48}

Hierbei wird die Datei über normales FTP an einen der Server von Adobe gesendet. Wenn Sie die Datei auf Ihrem Server haben möchten, müssen Sie sie über Ihren Server per SFTP vom Adobe FTP-Server abrufen. Hierzu sind drei Methoden verfügbar:

* [Verbindung zu Adobe über SFTP ohne Kennwort herstellen.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* Sie können beliebige Berichte per Push an FTP-basierte Adobe Daten-Feeds/Reports &amp; Analytics/Ad Hoc usw. übertragen und dann abrufen. Adobe kann diese Berichte nicht an den von Ihnen eingerichteten SFTP-Server ausliefern.
