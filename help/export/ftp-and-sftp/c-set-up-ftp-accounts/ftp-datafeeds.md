---
description: Daten-Feeds sind Exporte von durch Adobe empfangene Clickstream-Daten. Verfügbar sind sowohl standardmäßige als auch benutzerdefinierte Daten-Feeds.
keywords: ftp;sftp
title: Daten-Feeds
feature: FTP Export
exl-id: 286050fa-e197-4b70-b167-da6921615c1b
TQID: 'https://experienceleague.adobe.com/JYiAXR-SbFNV3xQQ5Y1Qv10kVWpFJRWmuOvERcQ-zP4'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2: id: a8bf2e97-0add-4437-b976-1fc5154911a8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 27%

---

# Daten-Feeds

>[!NOTE]
>
>Die folgenden Informationen beziehen sich auf FTP- und SFTP-Zieltypen. FTP und SFTP sind veralte Zieltypen. Beim Konfigurieren eines Daten-Feeds sollten Sie einen Cloud-Zieltyp verwenden, der sicherer ist. Weitere Informationen zum Konfigurieren von Cloud-Zieltypen für einen Daten-Feed finden Sie unter [Erstellen eines Daten-Feeds](/help/export/analytics-data-feed/create-feed.md).

Data Feeds sind Exporte von durch Adobe empfangene Clickstream-Daten. Verfügbar sind sowohl standardmäßige als auch benutzerdefinierte [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md).

Wenn Sie Adobe Data Warehouse und [!UICONTROL Standard Data Feeds] erworben haben, können Sie eigene Analytics-Daten-Feeds einrichten. Sie können an jedes FTP-Konto gesendet werden (entweder an ein von Adobe eingerichtetes oder an ein externes FTP-Konto). Adobe Engineering Services bietet benutzerdefinierte [!UICONTROL Daten-Feeds] die auf praktisch jede Weise gesendet werden können.

[!UICONTROL Daten-Feed] FTP-Konten erlauben 10 GB (standardmäßig). Alle anderen Standard-FTP-Konten haben standardmäßig eine Größe von 50 MB. Wenn Kunden das FTP-Konto für den bestimmungsgemäßen Gebrauch verwenden, können einige Benutzer mit hohem Traffic-Volumen diese Konten schnell füllen. Wenn ein FTP-Konto voll ist, können keine zusätzlichen Dateien an sie gesendet werden. An dieses FTP-Konto gelieferte Dateien ([!UICONTROL Daten-Feeds]-, Data Warehouse-Anforderungen usw.) werden daher nicht ausgeliefert. Dies ist einer der Gründe, warum es wichtig ist, Ihr Adobe FTP-Konto zu verwalten, indem Sie erhaltene und heruntergeladene Dateien entfernen.

Wenn ein FTP-Konto voll ist, sollten Sie die aktuellen Dateien herunterladen und entfernen und Adobe mitteilen, dass der Speicherplatz frei wurde. Adobe kann dann noch einmal Dateien senden, die noch nicht zugestellt wurden. Einige Tools, wie Data Warehouse, ermöglichen es Benutzern, diese Dateien erneut zu senden. Das erneute Senden erfordert möglicherweise keine Beteiligung von Adobe. Wenn Ihr FTP-Konto häufig ausgelastet zu sein scheint, wenden Sie sich an die Adobe-Kundenunterstützung, die Ihnen Versandalternativen vorschlagen kann, darunter die Erhöhung des FTP-Speicherplatzes und des Dateinamenkontingents für das Konto.
