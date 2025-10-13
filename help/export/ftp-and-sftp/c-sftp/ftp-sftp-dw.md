---
description: Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server.
keywords: ftp;sftp
title: Data Warehouse-Anforderungen an SFTP-Server senden
feature: FTP Export
exl-id: 45694647-69ec-45e3-b614-4a936909a338
source-git-commit: d8bfad5d388f906c7c7301a9126813f5c2a5dbaa
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 52%

---

# Data Warehouse-Anforderungen an SFTP-Server senden

Adobe unterstützt den Export von Data Warehouse-Anfragen an SFTP-Server, wie unter [SFTP](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp) im Artikel „Konfigurieren [ Berichtsziels für eine Data Warehouse-Anfrage“ ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md).

Folgende Aufgaben müssen abgeschlossen sein:

* Bei der Anforderung eines Data Warehouse-Berichts wird nur Port 22 verwendet.
* Die `authorized_keys`-Datei von Adobe befindet sich im `.ssh`-Ordner im Stammverzeichnis des Benutzers, mit dem Sie sich anmelden.
* Das Ziel darf nicht `ftp.omniture.com` sein. Das SFTP-Protokoll wird zwischen den internen Servern von Adobe nicht unterstützt.
* Das Ziel unterstützt eine Ein-Faktor-Authentifizierung (PKI). Falls eine Zwei-Faktor-Authentifizierung erforderlich ist, schlägt die Bereitstellung des Berichts fehl. Stellen Sie sicher, dass der Server nicht so konfiguriert ist, dass er versucht, eine Zwei-Faktor-Authentifizierung durchzuführen. Für Adobe Analytics ist es erforderlich, dass ausschließlich der Schlüssel für die Anmeldung verwendet wird.
* Adobe unterstützt eine SSHv2-Verschlüsselung und führt ein Fallback auf SSHv1 aus (nur RSA-Schlüssel).

So senden Sie eine Data Warehouse-Anfrage erfolgreich über SFTP:

1. Führen Sie die Schritte aus[ die im Artikel ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp)Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage[ beschrieben sind, ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) das Herunterladen des öffentlichen Schlüssels.
1. Melden Sie sich bei der SFTP-Site mit den Anmeldedaten an, die für die Data Warehouse-Anfrage verwendet werden.
1. Navigieren Sie im Stammverzeichnis zu dem Ordner `.ssh` (erstellen Sie diesen, falls er nicht vorhanden ist) und legen Sie dort die Datei `authorized_keys` ab.

1. Schließen Sie die Data Warehouse-Anfrage ab, falls noch nicht geschehen, wie unter [Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) beschrieben.
