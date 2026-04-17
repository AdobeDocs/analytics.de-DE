---
description: Anleitung zum Einrichten einer sicheren Übertragung mit Adobe FTP-Servern.
keywords: ftp;sftp
title: Verbindung zu einem Adobe FTP-Konto mit SFTP herstellen
feature: FTP Export
exl-id: 727d4f7a-d7d1-40cf-bdcd-c783ca47f51c
source-git-commit: 26ae4edacbc3591d4d3358afe009bf7831d45efb
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 39%

---

# Herstellen einer Verbindung zu einem FTP-Konto mit SFTP

So richten Sie eine sichere Übertragung mit FTP ein:

1. (Bedingt) Wenn Sie eine sichere Übertragung mit Adobe FTP-Servern einrichten möchten:

   1. Fordern Sie ein von Adobe gehostetes FTP-Konto an (50 MB Kontingent).

   1. Erstellen Sie öffentliche/private Schlüssel.

      * Führen Sie in einer Linux-Umgebung Folgendes aus:

        ```
        ssh-keygen -t ed25519 -C "your-comment-or-email"
        ```

        Wenn Ihre Richtlinie die Verwendung von ed25519 nicht zulässt, führen Sie Folgendes aus:

        ```
        ssh-keygen -t rsa -b 4096 -C "your-comment-or-email"
        ```

        **Hinweis:** Dies gilt normalerweise für Kunden, die unter FIPS 186-4 arbeiten, da ed25519 zuerst in den neueren FIPS 186-5 unterstützt wird.

      * Verwenden Sie in einer Windows-Umgebung PuttyGen.

1. (Bedingt) Wenn Sie eine sichere Übertragung mit Ihrem eigenen FTP-Speicherort einrichten möchten, müssen Sie über einen SFTP-Host, einen Benutzernamen und die Ziel-Site verfügen, die einen gültigen öffentlichen RSA- oder 25519-Schlüssel enthalten. Sie können den entsprechenden öffentlichen Schlüssel beim Erstellen des Feeds herunterladen.

1. Datei mit dem Namen [!DNL `authorized_keys`] (ohne Erweiterung) erstellen.

1. Den Inhalt des öffentlichen Schlüssels in die Datei [!DNL `authorized_keys`] kopieren.

1. Die Datei [!DNL `authorized_keys`] in ein FTP-Konto hochladen:

   * Mit dem Adobe FTP-Konto verbinden.
   * Das Verzeichnis [!DNL .ssh] erstellen (sofern es noch nicht vorhanden ist).
   * Die Datei [!DNL `authorized_keys`] in das Verzeichnis [!DNL .ssh] hochladen.

1. Die Verbindung testen, indem Sie sich per SFTP bei dem FTP-Konto anmelden.

Weitere Informationen finden Sie unter [Verbindung zu Adobe über SFTP ohne Kennwort herstellen](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md).

