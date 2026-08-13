---
description: Die Adobe-FTP-Richtlinie deaktiviert automatisch den Zugriff auf FTP-Konten, die an 90 aufeinanderfolgenden Tagen ungenutzt bleiben.
keywords: ftp;sftp
title: Löschen von FTP- und SFTP-Konten und -Daten
feature: FTP Export
exl-id: accf2f8d-c22c-4684-ba85-73a286325d0c
TQID: 'https://experienceleague.adobe.com/i2jpzTOx-CJzWjHMXT14EE761uGvNjcoW3f1dyF0ZlA'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: a8bf2e97-0add-4437-b976-1fc5154911a8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 237
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
