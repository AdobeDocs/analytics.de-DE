---
description: Eine Verbindung zu FTP-Konten kann nur dann ohne Kennwort hergestellt werden, wenn sowohl eine SFTP-Verbindung als auch ein alternatives Authentifizierungsverfahren genutzt werden. Hierzu sind zwei Dateien erforderlich (eine im FTP-Konto und die andere auf Ihrem Computer), die eine Kombination aus öffentlichem und privatem Schlüssel bilden.
keywords: ftp;sftp
title: Verbindung zu Adobe über SFTP ohne Kennwort herstellen
feature: FTP Export
exl-id: 7ff9511c-50a2-466f-b5af-6bbd59941ce5
TQID: 'https://experienceleague.adobe.com/5XpefTP6xLr007yTQjLDVoj-j-EcPLvBDda-NNIg6xA'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2: id: a8bf2e97-0add-4437-b976-1fc5154911a8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 609
ht-degree: 40%

---

# Verbindung zu Adobe über SFTP ohne Kennwort herstellen

Eine Verbindung zu FTP-Konten kann nur dann ohne Kennwort hergestellt werden, wenn sowohl eine SFTP-Verbindung als auch ein alternatives Authentifizierungsverfahren genutzt werden. Hierzu sind zwei Dateien erforderlich (eine im FTP-Konto und die andere auf Ihrem Computer), die eine Kombination aus öffentlichem und privatem Schlüssel bilden.

Dies ist nicht weniger sicher als die Passwortauthentifizierung. Dies ist eine andere Form der Authentifizierung, bei der der Benutzer nicht jedes Mal ein Kennwort eingeben muss. Bei richtiger Verwendung können sich diese Dateien mit diesem bestimmten Computer anmelden, ohne ein Kennwort angeben zu müssen. Dies muss Computer für Computer eingerichtet werden. Alle anderen Verbindungen, die diese Schlüsseldateien nicht verwenden, müssen weiterhin ein Kennwort angeben.

Manche Clients benötigen SFTP (Secure File Transfer Protocol), um sensible Daten zu übertragen. Eine SFTP-Verbindung ist sicherer als eine normale FTP-Verbindung, da die Datenkommunikation verschlüsselt erfolgen kann. Alle Adobe FTP-Konten sind standardmäßig SFTP-fähig. Eine SFTP-Verbindung kann mit einem gültigen Benutzernamen und einem Kennwort über einen SFTP-Client hergestellt werden, der eine Verbindung über Port 22 herstellt (normale FTP-Verbindungen, die nicht sicher sind, nutzen Port 21).

Bei Verwendung von SFTP ist es unter bestimmten Bedingungen möglich, private Schlüssel zu verwenden, um ohne Kennwort eine Verbindung zu einem Konto herzustellen. Mit dieser Methode kann Ihr Computer Schlüsseldateien für die Authentifizierung anstelle der üblichen Passwortauthentifizierung verwenden. Dies bedeutet, dass nur der Computer, der den privaten Schlüssel enthält, eine Verbindung ohne Kennwort herstellen kann. Alle anderen Computer/Benutzer müssen weiterhin die Passwortauthentifizierung verwenden (es sei denn, auf diesen anderen Computern wurden auch private Schlüssel eingerichtet).

**Einrichten und Verwenden privater Schlüssel für die Authentifizierung ohne Passwort**

1. FTP-Konto erstellen (Adobe).

   Ein Adobe-Mitarbeiter kann ein FTP-Konto erstellen, falls noch kein solches Konto vorhanden ist. Wenden Sie sich an Ihr Adobe-Accountteam oder die Adobe-Kundenunterstützung, um ein Konto erstellen zu lassen.
1. Öffentlichen/privaten Schlüssel erstellen (Kunde).

   Erstellen Sie eine öffentliche und eine private Schlüsselkombination. Der private Schlüssel ist eine Datei, die privat auf Ihrem Computer/Server ist und sich dort befindet. Die Datei mit dem öffentlichen Schlüssel muss in das Adobe-Konto hochgeladen werden. Bei dieser Verwendung können Sie eine Verbindung ohne Passwortauthentifizierung herstellen. Die Datei mit dem öffentlichen Schlüssel bei Adobe entspricht der Datei mit dem privaten Schlüssel auf Ihrem Computer/Server und authentifiziert sich auf diese Weise.

   Wenden Sie sich zur Erstellung dieser Dateien an Ihre interne Netzwerk-Supportgruppe, um einen Schlüsselsatz zu erstellen, der für Ihre Umgebung geeignet ist. Es gibt viele Tools und Programme, mit denen diese beiden Dateien erstellt werden können.

   Ein Beispiel dafür, wie dies in einer UNIX-Shell-Umgebung möglich ist, finden Sie unten. Dies ist nur ein Beispiel dafür, wie dies möglich ist, und dient als hilfreicher Bezugspunkt für die Kommunikation der Anforderungen an Ihr Team oder Ihre interne Netzwerkgruppe.

   ```
   // Linux/Unix (bash shell)
   
   // First make sure the ".ssh" directory exists
   
   $ mkdir ~/.ssh
   
   $ cd ~/.ssh
   
   // Now actually generate the key pair
   
   // Usually we will want to create an empty passphrase (just hit "Enter" for both password prompts)
   
   $ ssh-keygen -q -t dsa
   
   Enter file in which to save the key (/home/user/.ssh/id_dsa):
   
   Enter passphrase (empty for no passphrase): ...
   
   Enter same passphrase again: ...
   
   // Rename or copy the public key file to "authorized_keys"
   
   // This "authorized_keys" file is the one that we will upload to the Adobe FTP server in step 3
   
   $ cp id_dsa.pub authorized_keys 
   ```

1. Öffentlichen Schlüssel in das FTP-Konto hochladen (Kunde).

   Laden Sie den öffentlichen Schlüssel hoch und testen Sie ihn. Stellen Sie eine Verbindung zum Adobe FTP-Konto her und erstellen Sie das Verzeichnis [!DNL .ssh], sofern es noch nicht vorhanden ist. Laden Sie die Datei [!DNL authorized_keys] in das Verzeichnis [!DNL .ssh] hoch. Dies kann auf viele verschiedene Arten erfolgen (Befehlszeile, grafischer FTP-Client usw.). Es ist lediglich die Möglichkeit erforderlich, ein Verzeichnis zu erstellen und eine Datei hochzuladen.

   Auch hier ist ein Beispiel dafür, wie dies mit einer UNIX-Shell gemacht wird.

   ```
   $ ftp ftp.Adobe.com
   
   OR (depending on hostname provided by Adobe)
   
   $ ftp ftp2.Adobe.com
   
   // Enter username and password for account as prompted
   
   ftp> mkdir .ssh
   
   ftp> cd .ssh
   
   ftp> put authorized_keys
   
   ftp> exit
   
   // Now test the connection by logging in to the server using "sftp" command:
   
   $ sftp username@ftp.omniture.com
   
   OR (depending on hostname provided by Adobe)
   
   $ sftp username@ftp2.omniture.com
   
   // You should immediately receive an sftp prompt without having to enter the password:
   
   sftp>
   ```
