---
title: Protokolldatei
description: Rufen Sie eine Protokolldatei zur Fehlerbehebung ab.
translation-type: tm+mt
source-git-commit: aea3b4448b61e8b1b217b4f74b0b80c9fbedd070
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 3%

---


# Protokolldatei

Bei der Fehlerbehebung von Problemen mit Ad Hoc Analysis ist es manchmal erforderlich, die Protokolldatei abzurufen. Adobe kann die Protokolldatei verwenden, um die Ursache des Problems zu ermitteln und eine Lösung bereitzustellen. Die `discover.log` Datei enthält alle Benutzerinteraktionen, Informationen zum Laden von Berichten und Java-Fehlermeldungen für alle Sitzungen. Es werden alle geschützten Informationen, z. B. das Kennwort des Benutzers, zwischengespeichert. Große Protokolldateien werden in 10-MB-Schritten aufgeteilt. Achten Sie bei der Bereitstellung der Adobe mit den Protokolldateien darauf, dass alle Dateien ausgewählt sind.

## Windows

Rufen Sie die `discover.log` Datei für Windows ab:

1. Klicken Sie auf das Menü &quot;Beginn&quot;und wählen Sie &quot; **Ausführen**&quot;oder drücken Sie `[Win]` + `[R]`.
2. Fügen Sie Folgendes in das Textfeld ein und klicken Sie auf **OK**:

   ```text
   %appdata%/../Local/Adobe/Discover/log
   ```

3. Markieren Sie alle Dateien im Ordner, klicken Sie mit der rechten Maustaste und wählen Sie &quot; **Senden an&quot;> &quot;Komprimierter (komprimierter) Ordner**&quot;.
4. Stellen Sie dem Vertreter der Adobe die ZIP-Datei zur Verfügung.

## Mac

Gehen Sie wie folgt vor, um die `discover.log` Datei für Mac OS abzurufen:

1. Öffnen Sie den Finder und navigieren Sie zu `/Users/your-user/.adobe/Discover/log`
2. Markieren Sie alle Dateien im Ordner, klicken Sie mit der rechten Maustaste und wählen Sie **Komprimieren**.
3. Stellen Sie dem Vertreter der Adobe die ZIP-Datei zur Verfügung.

Wenn die Gesamtgröße für komprimierte Dateien 10 MB überschreitet, kann ein Vertreter der Adobe einen temporären FTP-Speicherort angeben.
