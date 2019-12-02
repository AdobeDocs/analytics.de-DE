---
description: Data Feeds sind ein Export von durch Adobe empfangenen Clickstream-Daten, der sowohl standardmäßige als auch benutzerdefinierte Data Feeds bietet.
keywords: ftp;sftp
solution: Analytics
title: Data Feeds
uuid: 3c70eea3-ca59-4aa5-9b11-64e1bb677bfa
translation-type: tm+mt
source-git-commit: a52516c7746db399ff54a1a4880eeb7ee0ca66e1

---


# Data Feeds

Data Feeds sind ein Export von durch Adobe empfangenen Clickstream-Daten, der sowohl standardmäßige als auch benutzerdefinierte [Data Feeds](/help/export/analytics-data-feed/data-feed-overview.md) bietet.

Wenn Sie Adobe Data Warehouse und [!UICONTROL Standard Data Feeds] erworben haben, können Sie eigene Analytics-Data Feeds einrichten. Diese können an ein beliebiges FTP-Konto gesendet werden (entweder ein durch Adobe eingerichtetes oder ein externes FTP-Konto). Adobe Engineering Services bieten benutzerdefinierte [!UICONTROL Data Feeds], die auf nahezu jede Art gesendet werden können.

[!UICONTROL Data Feed]-FTP-Konten sind auf 2 GB oder 63 Dateien beschränkt (standardmäßig). Für alle anderen Standard-FTP-Konten gilt eine Obergrenze von 50 MB. In Fällen, in denen Kunden das FTP-Konto bestimmungsgemäß verwenden, kann es bei Benutzern mit hohem Traffic-Aufkommen schnell passieren, dass die Konten voll sind. Wenn ein FTP-Konto voll ist, können keine weiteren Dateien in das Konto übertragen werden. An dieses FTP-Konto gelieferte Dateien ([!UICONTROL Data Feeds]-, Data Warehouse-Anforderungen usw.) werden daher nicht ausgeliefert. Dies ist einer Gründe, aus denen es wichtig ist, dass Sie Ihr Adobe FTP-Konto verwalten und empfangene Dateien nach dem Herunterladen entfernen.

Wenn ein FTP-Konto voll ist, müssen Sie die vorhandenen Dateien herunterladen und entfernen und Adobe mitteilen, dass der Speicher wieder frei ist. Adobe kann dann nicht ausgelieferte Dateien erneut senden. Einige Werkzeuge, z. B. Data Warehouse, erlauben dem Benutzer das erneute Senden der betroffenen Dateien. Hier ist für das erneute Senden kein Eingreifen von Adobe erforderlich. Falls Ihr FTP-Konto häufig voll ist, wenden Sie sich an die Adobe-Kundenunterstützung, um sich über Zustellungsalternativen zu informieren, wozu die Vergrößerung des FTP-Speichers und die Erhöhung der Dateigrenze für das Konto gehören.
