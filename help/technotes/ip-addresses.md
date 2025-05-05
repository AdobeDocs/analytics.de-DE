---
title: Von Adobe Analytics verwendete IP-Adressen
description: Wenn die Firewall Ihres Unternehmens IP-Adressen blockiert, die von Adobe stammen, verwenden Sie diese Liste, um Ihre Firewall-Einstellungen zu aktualisieren.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: 5ac6da2eb53d2748e8838ef2c6334a771abc26c9
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 35%

---

# Von Adobe Analytics verwendete IP-Adressen

Einige Firewall-Konfigurationen blockieren IP-Adressen, die von den Adobe-Datenerfassungs-Servern oder -Servern stammen, die für den Datenzugriff zuständig sind. Sie können diese Liste von Bereichen verwenden, um die Firewall-Einstellungen Ihres Unternehmens so zu ändern, dass der Zugriff und das Senden von Daten aus Ihrem Unternehmen heraus möglich ist.

Alle von Adobe Analytics verwendeten IP-Adressen sind Teil von [vom Adobe Experience Cloud verwendeten IP-Adressen](https://experienceleague.adobe.com/de/docs/core-services/interface/data-collection/ip-addresses) mit Ausnahme des Add-on-Pakets „China Performance Optimization“.

## IP-Adressen zur Leistungsoptimierung in China

Das Add-on-Paket zur Leistungsoptimierung für China ist ein zusätzlicher gebührenpflichtiger Service, der die Leistung der AppMeasurement-Datenerfassung für Besucher innerhalb Chinas verbessert. Wenden Sie sich an Ihr Adobe-Account-Team, um mehr über die Verwendung dieser Funktion zu erfahren.

>[!IMPORTANT]
>
>Die regionale Datenerfassung für China ist nicht für die Web SDK-Datenerfassung verfügbar. Diese Server gelten nur für AppMeasurement-Bibliotheken.

Regionale Datenerfassungs-Server in China verwenden die folgenden IP-Adressen:

| Standort | Host |
| --- | --- |
| China | `52.80.168.159` |
| China | `52.80.199.104` |
| China | `54.223.199.8` |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>[Von der Adobe Experience Cloud verwendete IP-Adressen](https://experienceleague.adobe.com/de/docs/core-services/interface/data-collection/ip-addresses)
>
>[Von Adobe Analytics verwendete Domains](domains.md)
