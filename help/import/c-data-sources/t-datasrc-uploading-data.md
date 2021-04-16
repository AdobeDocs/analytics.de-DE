---
description: Diese Schritte beschreiben, wie Sie eine Datenquellen-Datei hochladen.
subtopic: Data sources
title: Data Sources-Datei hochladen
topic-fix: Developer and implementation
uuid: 5a9dde91-1297-47e5-9393-611b40413c17
exl-id: 8b7fa32c-01f2-452b-bf8e-8a81da266926
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 87%

---

# Data Sources-Datei hochladen

Nachdem Sie eine Data Sources-Datendatei vorbereitet haben, geben Sie sie zur Verarbeitung an Data Sources weiter. Adobe unterhält mehrere Data Sources-FTP-Server, auf die Sie Data Sources-Dateien hochladen können. Beachten Sie Folgendes über die Data Sources-FTP-Server:

* Wählen Sie auf der Registerkarte [!UICONTROL Data Sources-Manager] neben dem Datenquelleneintrag die Option „FTP-Info“ aus, um den FTP-Host sowie Anmelde- und Kennwortinformationen für das FTP-Konto der Datenquelle anzuzeigen. Jeder mit Zugriff auf diese Informationen kann Daten in Ihre Report Suite hochladen.
* Aus Sicherheitsgründen werden FTP-Konten nach 30 Tagen Inaktivität geschlossen.
* FTP-Konten sind Datenquellen-spezifisch. Sie können nicht ein FTP-Konto zum Hochladen von Data Sources-Dateien in mehrere Datenquellen verwenden.

**So laden Sie eine Datenquellen-Datei hoch**

1. Verwenden Sie einen FTP-Client, um die Daten an Ihre Data Sources-FTP-Site zu senden.

   (Verfügbar im Data Sources-Manager unter dem Link „FTP-Info“).

1. Laden Sie eine [!DNL .fin]-Datei hoch, um Adobe darüber zu informieren, dass der Data Sources-Datei-Upload abgeschlossen ist.

   Die [!DNL .fin]-Datei muss genau den gleichen Namen aufweisen wie die Data Sources-Datei, mit Ausnahme der Dateierweiterung. Adobe stellt die Data Sources-Datei nicht für die Verarbeitung in eine Warteschlange, bis Sie die [!DNL .fin]-Datei hochgeladen haben.

   Laden Sie die Datei erst hoch, wenn alle Data Sources-Dateien vollständig hochgeladen wurden. Anderenfalls könnte Data Sources versuchen, eine unvollständige Datei zu verarbeiten.
1. Nachdem die .fin-Datei hochgeladen wurde, müssen Sie sich unbedingt von der Data Sources-FTP-Site abmelden. Analytics verwendet daher Abmeldedateien als Trigger, um anzugeben, dass die Ereignisse zur Verarbeitung bereit sind.
1. Achten Sie darauf, ob bei der Verarbeitung der Data Sources-Datei Meldungen ausgegeben werden.

   Im Data Sources-Manager werden Fehler angezeigt, die u. U. während der Dateiverarbeitung auftreten.
