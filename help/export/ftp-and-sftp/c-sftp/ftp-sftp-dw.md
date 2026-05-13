---
description: Adobe unterstützt den Export von Data Warehouse-Anforderungen an SFTP-Server.
keywords: ftp;sftp
title: Data Warehouse-Anforderungen an SFTP-Server senden
feature: FTP Export
exl-id: 45694647-69ec-45e3-b614-4a936909a338
TQID: https://experienceleague.adobe.com/nBerOKEbILwAK5OyayVgdBPN8vq24kk-DXY6XMT50wg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 35%

---

# Data Warehouse-Anforderungen an SFTP-Server senden

Adobe unterstützt den Export von Data Warehouse-Anfragen an SFTP-Server, wie unter [SFTP](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp) im Artikel „Konfigurieren [ Berichtsziels für eine Data Warehouse-Anfrage“ ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md).

Folgende Aufgaben müssen abgeschlossen sein:

* Bei der Anforderung eines Data Warehouse-Berichts wird nur Port 22 verwendet.
* Die `authorized_keys`-Datei von Adobe befindet sich im `.ssh`-Ordner im Stammverzeichnis des Benutzers, mit dem Sie sich anmelden.
* Das Ziel darf nicht `ftp.omniture.com` sein. Das SFTP-Protokoll wird zwischen den internen Servern von Adobe nicht unterstützt.
* Das -Ziel unterstützt die One-Factor-Authentifizierung (PKI). Wenn es eine zweistufige Herausforderung gibt, schlägt die Bereitstellung des Berichts fehl. Stellen Sie sicher, dass der Server nicht so konfiguriert ist, dass er versucht, eine Zwei-Faktor-Authentifizierung durchzuführen. Adobe Analytics erfordert, dass nur der -Schlüssel und nichts anderes zum Anmelden verwendet wird.
* Adobe unterstützt SSHv2-Verschlüsselung und greift auf SSHv1 zurück (nur RSA-Schlüssel).

So senden Sie eine Data Warehouse-Anfrage erfolgreich über SFTP:

1. Führen Sie die Schritte aus[ die im Artikel [Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp) beschrieben sind, ](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) das Herunterladen des öffentlichen Schlüssels.
1. Melden Sie sich bei der SFTP-Site mit den Anmeldedaten an, die für die Data Warehouse-Anfrage verwendet werden.
1. Navigieren Sie im Stammverzeichnis zu dem Ordner `.ssh` (erstellen Sie diesen, falls er nicht vorhanden ist) und legen Sie dort die Datei `authorized_keys` ab.

1. Schließen Sie die Data Warehouse-Anfrage ab, falls noch nicht geschehen, wie unter [Konfigurieren eines Berichtsziels für eine Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) beschrieben.
