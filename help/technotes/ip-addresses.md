---
title: Von Adobe Analytics verwendete IPs und Domains
description: Wenn die Firewall Ihres Unternehmens IP-Adressen blockiert, die von Adobe stammen, verwenden Sie diese Liste, um Ihre Firewall-Einstellungen zu aktualisieren.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: ea859717c6a40b4eeeb9eca54b95718859af9c7b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 32%

---

# Von Adobe Analytics verwendete IPs und Domains

Einige Firewall-Konfigurationen blockieren Domänen, auf die Adobe Analytics für seine Produktoberfläche angewiesen ist. Sie können diese Liste von Domänen verwenden, um die Netzwerkeinstellungen Ihres Unternehmens zu ändern und den Produktzugriff innerhalb Ihres Unternehmens zuzulassen.

## Abhängige Technologiedomänen zulassen

Adobe Analytics verwendet die folgenden Hosts, um die Leistung und das Produkterlebnis zu verbessern. Adobe empfiehlt, diese Domänen über die Firewall Ihres Unternehmens zuzulassen, damit eine optimale Nutzung von Adobe Analytics gewährleistet ist.

| Technologie | Domain |
| --- | --- |
| Adobe Analytics-Domains | `adobe.com`, `adobe.net`, `adobe.io` |
| Veraltete Adobe Analytics-Domäne | `omniture.com` |
| Amazon AWS | `aaui-879784980514.s3.us-east-2.amazonaws.com` |
| Amazon CloudFront | `d30ln29764hddd.cloudfront.net` |
| Gainsight | `esp.aptrinsic.com`, `esp-m.aptrinsic.com` |
| LaunchDarkly | `app.launchdarkly.com` |
| Microsoft Azure Blob Storage | `awaascicdprodva7.blob.core.windows.net` |
| Microsoft Azure CDN | `aauicdnva7.azureedge.net` |

{style="table-layout:auto"}

## IP-Adressblöcke von Adobe Experience Cloud

Zusätzlich zu den oben genannten Domänen benötigt Adobe Analytics für die Datenerfassung und den Export von Berichten verschiedene IP-Adressblöcke.

Eine vollständige Liste der IP-Bereiche finden Sie unter Adobe Experience Cloud-IP-Adressen .

## IP-Adressen zur Optimierung der chinesischen Leistung

Das Add-On-Paket zur Leistungsoptimierung von China ist ein zusätzlicher zahlungspflichtiger Dienst, der die AppMeasurement-Datenerfassungsleistung für Besucher in China verbessert. Wenden Sie sich an Ihr Adobe-Account-Team, um mehr über die Verwendung dieser Funktion zu erfahren.

>[!IMPORTANT]
>
>China RDC ist nicht für die Web SDK-Datenerfassung verfügbar. Diese Server gelten nur für AppMeasurement-Bibliotheken.

Regionale Datenerfassungsserver in China verwenden die folgenden IP-Adressen:

| Standort | Host |
| --- | --- |
| China | `52.80.168.159` |
| China | `52.80.199.104` |
| China | `54.223.199.8` |

{style="table-layout:auto"}
