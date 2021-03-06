---
title: Von Adobe Analytics verwendete IPs und Domains
description: Wenn die Firewall Ihres Unternehmens IP-Adressen blockiert, die von Adobe stammen, verwenden Sie diese Liste, um Ihre Firewall-Einstellungen zu aktualisieren.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: 6788b904295fd92642d27ade65a31d61897069a3
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 85%

---

# Von Adobe Analytics verwendete IPs und Domains

Einige Firewall-Konfigurationen blockieren IP-Adressen, die von den Adobe-Datenerfassungs-Servern oder -Servern stammen, die für den Datenzugriff zuständig sind. Sie können diese Liste von Bereichen verwenden, um die Firewall-Einstellungen Ihres Unternehmens so zu ändern, dass der Zugriff und das Senden von Daten aus Ihrem Unternehmen heraus möglich ist. Diese Seite enthält sowohl eingehende Systeme (z. B. die Datenerfassung) als auch ausgehende Systeme (z. B. Daten-Feeds), die von Adobe verwendet werden.

>[!IMPORTANT]
>
>Adobe versucht zwar nach besten Kräften, dieses Dokument aktuell zu halten, kann aber nicht garantieren, dass die Liste der IP-Bereiche unverändert bleibt. Zu den möglichen Änderungen gehören Wachstum und Erweiterung des Unternehmens, eine Internet-Registrierung erfordert Änderungen am IP-Adressraum von Adobe, oder ein Internet-Dienstleister funktioniert nicht mehr.

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

## Alle Adobe Analytics-IP-Adressblöcke für Datenerfassung

Die folgende Tabelle enthält alle standardmäßigen Datenerfassungs-Server und regionalen Datenerfassungs-Server für Adobe Analytics. Sie enthält keine einzelnen AWS-Hosts.

| IP-Block (CIDR-Notation) |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `172.82.192.0/18` |
| `185.34.188.0/22` |
| `192.243.224.0/19` |
| `205.219.231.0/24` |
| `208.67.40.0/22` |
| `208.77.136.0/22` |

## Datenerfassungs- und FTP-IP-Adressblöcke

Wenn Ihr Unternehmen es vorzieht, bestimmte IP-Adressbereiche zuzulassen, können Sie die folgende Tabelle verwenden. Alle Bereiche in diesem Abschnitt sind in der obigen Tabelle enthalten. FTP-Verbindungen für Data Warehouse- und Daten-Feeds stammen nur von den Standorten London, Oregon und Singapur.

| Standort | IP-Bereich (CIDR-Notation) |
| --- | --- |
| Amsterdam | `66.117.28.0/23` |
| Dallas | `205.219.231.0/24` |
| Dallas | `66.235.152.0/22` |
| Dallas | `66.235.140.0/22` |
| Dallas | `63.140.32.0/21` |
| Dallas | `172.82.208.0/22` |
| Sonderverwaltungsregion Hongkong der Volksrepublik China | `66.117.24.0/22` |
| London | `66.235.156.0/24` |
| London | `66.235.148.0/23` |
| London | `63.140.40.0/22` |
| London | `208.67.41.0/24` |
| London | `192.243.254.0/23` |
| London | `192.243.244.0/22` |
| London | `185.34.188.0/23` |
| London | `130.248.152.0/21` |
| London | `172.82.224.0/21` |
| London | `172.82.232.0/21` |
| Oregon | `192.243.240.0/22` |
| Oregon | `192.243.232.0/21` |
| Oregon | `192.243.224.0/21` |
| Oregon | `130.248.160.0/21` |
| Oregon | `130.248.148.0/22` |
| Oregon | `172.82.192.0/21` |
| Oregon | `172.82.216.0/21` |
| Paris | `208.67.40.0/24` |
| Singapur | `66.235.150.0/24` |
| Singapur | `66.235.130.0/23` |
| Singapur | `63.140.44.0/22` |
| Singapur | `208.67.43.0/24` |
| Singapur | `172.82.240.0/22` |
| Singapur | `172.82.246.0/23` |
| Singapur | `172.82.248.0/21` |
| San Jose | `66.117.20.0/24` |
| San Jose | `66.235.132.0/22` |
| San Jose | `130.248.128.0/22` |
| San Jose | `192.243.248.0/23` |
| San Jose | `172.82.200.0/22` |
| San Jose | `66.235.136.0/22` |
| San Jose | `208.91.175.0/24` |
| San Jose | `208.91.174.0/24` |
| San Jose | `208.91.169.0/24` |
| Sydney | `216.104.216.0/23` |
| Tokio | `66.235.159.0/24` |
| Tokio | `66.117.21.0/24` |
| Tokio | `63.140.52.0/24` |
| Tokio | `63.140.50.0/23` |
| Virginia | `66.235.144.0/22` |
| Virginia | `208.77.138.0/23` |
| Virginia | `208.77.136.0/23` |
| Virginia | `192.243.250.0/23` |
| Virginia | `130.248.144.0/22` |
| Virginia | `172.82.204.0/22` |
| Virginia | `172.82.212.0/22` |

## AWS-Hosts

Adobe Analytics verwendet Amazon Web Services als Teil des Datenerfassungsprozesses. Die folgende Tabelle enthält AWS-Hosts, die für Adobe reserviert sind. Diese Hosts sind **nicht** im obigen aggregierten Blockbereich enthalten.

| Standort | Host |
| --- | --- |
| China | `140.179.89.228` |
| China | `140.179.125.98` |
| Frankreich | `13.36.218.177` |
| Frankreich | `15.188.95.229` |
| Frankreich | `15.236.176.210` |
| Irland | `54.74.170.177` |
| Irland | `54.195.254.128` |
| Irland | `54.220.133.225` |
| Oregon | `52.10.149.115` |
| Oregon | `52.40.172.46` |
| Oregon | `54.212.155.93` |
| Virginia | `3.216.131.23` |
| Virginia | `34.204.237.47` |
| Virginia | `54.163.234.74` |
