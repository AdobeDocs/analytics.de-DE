---
description: Einrichten und Verwenden von durch Adobe gehosteten FTP-Konten.
keywords: ftp;sftp
title: FTP-Konten einrichten – Übersicht
feature: FTP Export
exl-id: 55f942fe-cb06-43e1-bd3c-57d6786278b7
source-git-commit: 6008cd51b86e403668c15bbfb9d50513e46ddf4d
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 17%

---

# Einrichten von FTP- oder SFTP-Konten - Übersicht

Von Adobe gehostete FTP- oder SFTP-Konten einrichten und verwenden.

Adobe verwaltet hochverfügbare Hochleistungs-FTP- oder SFTP-Cluster, die speziell entwickelt wurden, um die Zuverlässigkeit der Dateiübertragung zu verbessern und gleichzeitig eine hohe Leistung sicherzustellen.

Adobe-Kunden erhalten Wartungsbenachrichtigungen über ihren Standardprozess, da Wartungsereignisse geplant sind. Um sicherzustellen, dass die Adobe FTP- oder SFTP-Systeme wie vorgesehen funktionieren und weiterhin eine sichere und zuverlässige Hochleistungs-Datenübertragung bieten, fordert Adobe die Einhaltung der folgenden Richtlinien an:

* Die meisten Adobe-FTP- oder SFTP-Konten (Klassifizierungen, Datenquellen und andere) werden automatisch aktiviert, wenn die jeweilige Funktion eingerichtet wird. Für Daten-Feed- und allgemeine Dateibereitstellungskonten kann die Adobe-Kundenunterstützung ein neues FTP- oder SFTP-Konto für Sie einrichten. Dieser Prozess ist vorhanden, um sowohl Sicherheit als auch Speicherplatz für das FTP- oder SFTP-Konto zu gewährleisten.
* Benutzer sollten von Adobe an das FTP- oder SFTP-Konto gesendete Daten entfernen, nachdem die Daten erfolgreich auf ihre Systeme übertragen wurden.
* Adobe benachrichtigen, wenn FTP- oder SFTP-Konten nicht mehr benötigt werden, damit sie deaktiviert werden können.

Der Name des Adobe FTP-Hosts lautet `ftp://ftp.omniture.com` oder `ftp://ftp2.omniture.com`.

Diese Information wird zusammen mit dem Benutzernamen und dem Kennwort entweder in der [!UICONTROL Experience Cloud] (für Classifications und Data Sources) bereitgestellt oder durch den Adobe-Support-Mitarbeiter, der für das Einrichten des von Ihnen angeforderten Kontos zuständig ist. Wenn Sie nicht wissen, welche FTP- oder SFTP-Adresse verwendet werden soll, wenden Sie sich an Ihr Adobe-Accountteam, das Ihnen die richtige Adresse zur Verfügung stellen kann. Darüber hinaus verfügt Adobe für Classifications- und Datenquellenkonten nicht über eine bestimmte Tageszeit für die Verarbeitung von FTP- oder SFTP-Dateien. Stattdessen verwendet Adobe ein Skript, das ständig FTP- oder SFTP-Konten für neue Prozessdateien abfragt. In diese Konten hochgeladene Dateien werden so schnell wie möglich verarbeitet.
