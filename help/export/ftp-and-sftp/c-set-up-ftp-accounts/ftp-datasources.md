---
description: Sie können Analytics verwenden, um FTP-basierte Datenquellen zu erstellen und zu verwalten, wodurch die FTP-Dateiübertragung genutzt werden kann, um Offline- oder historische Daten in CX Enterprise zu importieren.
keywords: ftp;sftp
title: Datenquellen – Übersicht
feature: FTP Export
exl-id: 777917bd-bd11-4360-a149-e4fd0bb2f99e
TQID: https://experienceleague.adobe.com/Mq4r5p1872tIxfjts7HOq50XWky12Oy4fTi9ajzbAsc
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 157cc2bde1047063014aff39319d5cfaa1de9b5c
workflow-type: tm+mt
source-wordcount: 453
ht-degree: 35%

---

# FTP-basierte Datenquellen

Sie können Analytics verwenden, um FTP-basierte Datenquellen zu erstellen und zu verwalten, wodurch die FTP-Dateiübertragung genutzt werden kann, um Offline- oder historische Daten in CX Enterprise zu importieren.

Nachdem Sie eine Data Sources-Instanz erstellt haben, stellt das Tool einen FTP-Speicherort bereit, mit dem Sie Data Sources-Dateien hochladen können. Nach dem Hochladen werden sie von Data Sources automatisch gefunden und verarbeitet. Nachdem die Dateien verarbeitet wurden, stehen die Daten für das Analytics-Reporting zur Verfügung.

Auf [!UICONTROL &#x200B; Registerkarte &#x200B;]Erstellen“ im Datenquellen-Manager können Sie eine neue Datenquelleninstanz für die ausgewählte Report Suite konfigurieren. Der Assistent für Datenquellen führt Sie durch den Prozess der Erstellung einer Datenquellenvorlage und erstellt einen FTP-Speicherort für das Hochladen von Daten.

Suchen Sie im Fenster [!UICONTROL Datenquellen verwalten] Ihre Datenquelle und klicken Sie auf den Link FTP-Informationen . Ihre FTP-Anmeldeinformationen werden im Fenster [!UICONTROL Aktivieren einer Data Source] im Abschnitt [!UICONTROL Hochladen/FTP-Informationen] angezeigt.

Informationen zu FTP-Beschränkungen und zur Datenaufbewahrung finden Sie unter [FTP-Beschränkungen und Datenaufbewahrung](/help/export/ftp-and-sftp/ftp-limits.md).

## Informationen zur FIN-Datei für Uploads für Klassifizierungen und Datenquellen {#section_1484719F8A134EAE91212DBD8F15174F}

Beim Hochladen einer Klassifizierungs- oder einer Datenquellendatei (`.tab` oder `.txt`) müssen Sie auch eine leere Datei mit exakt demselben Namen wie die importierte Datei, jedoch mit einer `.fin` Erweiterung, hochladen. Diese `.fin`-Datei ist eine Finish-Datei. Sie dient dazu, dem System mitzuteilen, dass die Datendatei vollständig in das FTP-Konto hochgeladen wurde. Über die `.fin`-Datei erkennt Adobe, dass Sie mit Ihrem Import fertig sind. Nachdem Sie diese Datei übermittelt haben, entfernt Adobe beide Dateien aus dem FTP-Konto und startet den Importprozess.

Importdatei: `Classifications.tab`

Finish-Datei: `Classifications.fin`

Wenn Sie Ihre Datenquellen- oder SAINT-Datei ohne zugehörige `.fin`-Datei hochladen, fügt Adobe Ihre Datei nicht zur Verarbeitungswarteschlange hinzu. Die Datei verbleibt auf dem FTP-Server und wird nicht auf Ihre Daten in CX Enterprise angewendet. Sie werden nur benachrichtigt, wenn Sie Ihre E-Mail-Adresse als [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] des Berichts eingegeben haben. Wenn keine E-Mail-Adresse in dieses Feld eingegeben wird, wird keine Benachrichtigung gesendet.

Wenn Sie Ihre Datei zusammen mit einer `.fin`-Datei hochgeladen haben, die Datei jedoch fehlerhaft ist, wird sie zur Verarbeitung gesendet. Der Fehler sorgt dann dafür, dass die Verarbeitung abgebrochen und die Datei an einen Fehlerordner gesendet wird. In diesem Fall wird eine Benachrichtigung an die im Feld [!UICONTROL Benachrichtigungsempfänger] im Fenster [!UICONTROL FTP-Konto erstellen] angegebene E-Mail-Adresse gesendet. Wenn keine E-Mail-Adresse eingegeben wird, wird keine Benachrichtigung gesendet.
