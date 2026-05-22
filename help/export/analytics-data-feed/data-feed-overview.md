---
description: Erfahren Sie, wie Sie mit Daten-Feeds Rohdaten aus Adobe Analytics abrufen können. Erfahren Sie mehr über die Voraussetzungen für die Verwendung von Daten-Feeds und die nächsten Schritte.
keywords: Clickstream;Daten-Feed;Daten-Feed;Data Feed
title: Überblick über Analytics-Daten-Feed
feature: Data Feeds
exl-id: 2cfff9ad-cdb5-4ae9-a266-4f3d3d046f0c
TQID: 'https://experienceleague.adobe.com/XVFQdMEfIM7lQlnU3b-zRbQ9-RliqtaBjr-7ptxkI1o'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: ede9f3ba-4ee4-4497-9d8e-e9da5848bda0
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 335
ht-degree: 95%

---

# Analytics-Daten-Feed-Dokumentation

Daten-Feeds sind eine leistungsstarke Methode, Rohdaten aus Adobe Analytics abzurufen. Diese Rohdaten können nach Ermessen Ihrer Organisation auf anderen Plattformen außerhalb von Adobe verwendet werden. Die Daten werden in stündlichen Stapeln am Ende jeder Stunde oder in täglichen Stapeln am Ende jedes Tages bereitgestellt.

## Voraussetzungen

Bevor Sie Daten-Feeds verwenden, müssen Sie alle folgenden Anforderungen erfüllen.

* Eine funktionierende Implementierung, die Daten an Adobe-Datenerfassungs-Server sendet. Siehe [Überprüfen und Veröffentlichen einer Implementierung](/help/implement/launch/validate-publish-prod.md) im Implementierungshandbuch.
* Ihr Konto ist eine Analytics-Produktadministratorin bzw. ein Analytics-Produktadministrator, oder Ihr Konto gehört zu einem Produktprofil mit Zugriff auf Daten-Feeds.
* Ein Bucket, der für Amazon S3, Google Cloud Platform, Azure RBAC oder Azure SAS konfiguriert wurde.
* (Veraltet: Nur für veraltete FTP- und SFTP-Zieltypen erforderlich) Verwenden Sie eine FTP-Site und Ihre Anmeldeinformationen (FTP-Anmeldeinformationen, die von Ihrem Unternehmen bereitgestellt werden).

## Nächste Schritte

Die folgenden Ressourcen helfen Ihnen dabei, den grundlegenden Workflow beim Abrufen von Daten-Feeds zu verstehen. Sobald Sie den grundlegenden Workflow kennen, können Sie mit Teams in Ihrer Organisation zusammenarbeiten, um Rohdaten in einer Datenbank zu speichern oder in sie aufzunehmen.

* [Best Practices für Daten-Feeds](/help/export/analytics-data-feed/data-feeds-best-practices.md): Best Practices zum Erstellen und Verwalten von Daten-Feeds.
* [Erstellen von Daten-Feeds](create-feed.md): Technische Details zum Erstellen eines Daten-Feed, detaillierte Erläuterungen einzelner Felder
* [Verwalten von Daten-Feeds](df-manage-feeds.md): Weitere Informationen zum Navigieren in der Daten-Feed-Benutzeroberfläche
* [Daten-Feed-Inhalte](c-df-contents/datafeeds-contents.md): Erfahren Sie mehr über den Inhalt der komprimierten Datei <!-- Is this still the output users can download from the destination? I aske Jun. -->
* [Definitionen der Datenspalten](c-df-contents/datafeeds-reference.md): Eine vollständige Liste aller verfügbaren Spalten.

>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Navigieren in der Daten-Feed-Oberfläche](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/exporting/data-feeds/data-feeds-management-ui){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]



>[!BEGINSHADEBOX]

Unter ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Ermitteln Ihrer Daten-Feed-ID](https://experienceleague.adobe.com/de/docs/analytics-learn/tutorials/exporting/data-feeds/find-your-data-feed-id){target="_blank"} finden Sie ein Demovideo.

>[!ENDSHADEBOX]
