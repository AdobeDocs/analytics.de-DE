---
description: Die Adobe-FTP-Richtlinie deaktiviert automatisch den Zugriff auf FTP-Konten, die an 90 aufeinanderfolgenden Tagen ungenutzt bleiben.
keywords: ftp;sftp
title: Löschen von FTP- und SFTP-Konten und -Daten
feature: FTP Export
exl-id: accf2f8d-c22c-4684-ba85-73a286325d0c
source-git-commit: 6008cd51b86e403668c15bbfb9d50513e46ddf4d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 8%

---

# Löschen von FTP- und SFTP-Konten und -Daten

Die Adobe-FTP- und -SFTP-Richtlinie kann den Zugriff auf FTP- und SFTP-Konten deaktivieren, die an 90 aufeinander folgenden Tagen inaktiv bleiben.

Adobe kann dann nach einer zusätzlichen 90-tägigen Übergangsphase deaktivierte FTP- und SFTP-Konten entfernen (und alle in diesen Konten gespeicherten Daten dauerhaft entfernen). Beispielsweise wird ein SFTP-Konto, das 90 Tage lang inaktiv bleibt (vom 5. Juli 2025 bis zum 2. Oktober 2025), am 3. Oktober 2025 deaktiviert. Am 2. Januar 2026 wird sie dann vollständig entfernt.

Vor dem 5. Oktober 2025 wurden keine Konten deaktiviert und vor dem 2. Januar 2026 wurden keine Konten entfernt.

Adobe kann alte Daten in aktiven Konten auch dauerhaft entfernen, wenn auf diese Daten seit 90 Tagen nicht zugegriffen wurde.

Um uns bei diesem Prozess zu unterstützen und sicherzustellen, dass die FTP- oder SFTP-Umgebung weiterhin eine sichere und zuverlässige Datenübertragung für unsere Kunden bietet, bitten wir unsere Kunden, Folgendes zu tun:

* Entfernen Sie ausgehende Daten aus FTP- und SFTP-Systemen, nachdem diese Daten erfolgreich in Ihre interne Umgebung übertragen wurden. Adobe kann alle im System verbleibenden Dateien nach 90 Tagen identifizieren und entfernen.
* Adobe benachrichtigen, wenn FTP- und SFTP-Konten nicht mehr benötigt werden, damit sie deaktiviert und entfernt werden können.
