---
description: Erfahren Sie, wie Sie mit Daten-Feeds Rohdaten aus Adobe Analytics abrufen können. Erfahren Sie mehr über die Voraussetzungen für die Verwendung von Daten-Feeds und darüber, was Sie als Nächstes tun können.
keywords: Clickstream;Daten-Feed;Daten-Feed;Data Feed
title: Analytics-Daten-Feed - Übersicht
feature: Data Feeds
exl-id: 2cfff9ad-cdb5-4ae9-a266-4f3d3d046f0c
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 79%

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
* [Daten-Feed-Inhalte](c-df-contents/datafeeds-contents.md): Verstehen Sie, was sich in der komprimierten Datei befindet<!-- Is this still the output users can download from the destination? I aske Jun. -->
* [Definitionen der Datenspalten](c-df-contents/datafeeds-reference.md): Eine vollständige Liste aller verfügbaren Spalten.

>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Navigieren in der Daten-Feed-](https://video.tv.adobe.com/v/3428560?quality=12&learn=on&captions=ger){target="_blank"}) für ein Demovideo.

>[!ENDSHADEBOX]



>[!BEGINSHADEBOX]

Siehe ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Ermitteln der Daten-Feed-](https://video.tv.adobe.com/v/335747?quality=12&learn=on){target="_blank"}) für ein Demovideo.

>[!ENDSHADEBOX]
