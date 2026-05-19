---
description: Aktives FTP und passives FTP regeln unterschiedlich, wie die Port-Verbindungen hergestellt werden, was gewisse Auswirkungen auf die Firewall hat.
keywords: ftp;sftp
title: Passiven FTP-Modus verwenden
feature: FTP Export
exl-id: 92f39569-ee41-4c1d-b7de-7a0fff42896c
TQID: https://experienceleague.adobe.com/R0fWu2Ik2OQB7VtF9ZVEEX1iLJfTl9A1YvlBm2p3nyU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 48%

---

# Passiven FTP-Modus verwenden

Aktives FTP und passives FTP regeln unterschiedlich, wie die Port-Verbindungen hergestellt werden, was gewisse Auswirkungen auf die Firewall hat.

Adobe verwendet passives FTP, eine sicherere Form der Datenübertragung, bei der der Datenfluss vom FTP-Client (File Transfer Program) und nicht vom FTP-Serverprogramm eingerichtet und initiiert wird. Wenn Sie Schwierigkeiten haben, eine Verbindung zu Adobe FTP herzustellen, stellen Sie sicher, dass Sie den passiven Modus verwenden.
