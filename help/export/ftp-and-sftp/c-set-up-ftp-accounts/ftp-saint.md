---
description: Die FTP-Option für Klassifizierungen (SAINT) bietet mehr Flexibilität beim Hochladen großer Klassifizierungs-Datensätze. So können u. a. auch Daten in mehrere Report Suites und Datensätze mit mehr als 50.000 Zeilen hochgeladen werden.
keywords: ftp;sftp
title: Klassifizierungen
feature: FTP Export
exl-id: fc783328-a70b-4af3-b3d3-c59ab79d6b8f
TQID: https://experienceleague.adobe.com/JdxiVF-HzQPiFzC6CH0yeIIPEulsacjl11-X8wLMrl4
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 157cc2bde1047063014aff39319d5cfaa1de9b5c
workflow-type: tm+mt
source-wordcount: 449
ht-degree: 72%

---

# Klassifizierungen

Die FTP-Option für Classifications bietet mehr Flexibilität beim Hochladen großer Classification-Datensätze. So können u. a. auch Daten in mehrere Report Suites und Datensätze mit mehr als 50.000 Zeilen hochgeladen werden.

Die Zeit, die das System zum Importieren dieser Dateien benötigt, hängt von einer Reihe von Faktoren ab. Wenn eine hochgeladene Datei länger als drei Tage auf dem FTP-Server vorhanden ist, wenden Sie sich an einen unterstützten Benutzer Ihrer Organisation, damit er Kontakt mit der Adobe-Kundenunterstützung aufnimmt.

Bei einem erfolgreichen Import erscheinen die entsprechenden Änderungen sofort in einem Export, während die Datenänderungen in Analytics bei einem Browser-Import bis zu 4 Stunden und bei einem FTP-Import bis zu 24 Stunden später erscheinen können.

Informationen zu FTP-Beschränkungen und zur Datenaufbewahrung finden Sie unter [FTP-Beschränkungen und Datenaufbewahrung](/help/export/ftp-and-sftp/ftp-limits.md).

## Informationen zur `.fin`-Datei für Uploads von Klassifizierungen und Datenquellen {#section_1484719F8A134EAE91212DBD8F15174F}

Beim Hochladen einer Klassifizierungs- oder Source-Datendatei (`.tab` oder `.txt`) müssen Sie auch eine leere Datei mit exakt demselben Namen wie die importierte Datendatei hochladen, jedoch mit .`.fin` Erweiterung. Diese `.fin`-Datei ist eine Finish-Datei. Sie dient dazu, dem System mitzuteilen, dass die Datendatei vollständig in das FTP-Konto hochgeladen wurde. Über die `.fin`-Datei erkennt Adobe, dass Sie mit Ihrem Import fertig sind.

Nachdem Sie sowohl die Quelldatei als auch die `.fin`-Datei übermittelt haben, müssen Sie sich unbedingt von der FTP-Site abmelden. Adobe Analytics verwendet Abmeldeereignisse nämlich als Trigger dafür, dass Dateien zur Verarbeitung bereit sind. Nach Abschluss des Imports entfernt Adobe beide Dateien aus dem FTP-Verzeichnis.

Finish-Datei: [!DNL Classifications.fin]

Wenn Sie Ihre Datenquell- oder Klassifizierungs-Datei ohne zugehörige `.fin`-Datei hochladen, fügt Adobe Ihre Datei nicht zur Verarbeitungswarteschlange hinzu. Die Datei verbleibt auf dem FTP-Server und wird nicht auf Ihre Daten in CX Enterprise angewendet. Sie werden nur benachrichtigt, wenn Sie Ihre E-Mail-Adresse als [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] von Analytics eingegeben haben. Wenn keine E-Mail-Adresse in dieses Feld eingegeben wird, wird keine Benachrichtigung gesendet.

Wenn Sie Ihre Datei zusammen mit einer `.fin`-Datei hochgeladen haben, die Datei jedoch fehlerhaft ist, wird sie zur Verarbeitung gesendet. Der Fehler sorgt dann dafür, dass die Verarbeitung abgebrochen und die Datei an einen Fehlerordner gesendet wird. In diesem Fall wird eine Benachrichtigung an die im Feld [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] angegebene E-Mail-Adresse gesendet. Wenn keine E-Mail-Adresse angegeben wurde, wird keine Benachrichtigung gesendet.
