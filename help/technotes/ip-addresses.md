---
title: Von Adobe Analytics verwendete IP-Adressen
description: Wenn die Firewall Ihres Unternehmens IP-Adressen blockiert, die von Adobe stammen, verwenden Sie diese Liste, um Ihre Firewall-Einstellungen zu aktualisieren.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
TQID: https://experienceleague.adobe.com/-4XZdprTBXpIaFnHeXBQsAr5YoZMW4ocnZRY50bHGUs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 208
ht-degree: 31%

---

# Von Adobe Analytics verwendete IP-Adressen

Einige Firewall-Konfigurationen blockieren IP-Adressen, die von den Adobe-Datenerfassungs-Servern oder -Servern stammen, die für den Datenzugriff zuständig sind. Sie können diese Liste von Bereichen verwenden, um die Firewall-Einstellungen Ihres Unternehmens so zu ändern, dass der Zugriff und das Senden von Daten aus Ihrem Unternehmen heraus möglich ist.

Alle von Adobe Analytics verwendeten IP-Adressen sind Teil von [vom Adobe Experience Cloud verwendeten IP-Adressen](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/ip-addresses) mit Ausnahme des Add-on-Pakets „China Performance Optimization“.

## IP-Adressen zur Leistungsoptimierung in China

Das Add-on-Paket zur Leistungsoptimierung für China ist ein zusätzlicher gebührenpflichtiger Service, der die Datenerfassungsleistung von AppMeasurement für Besucher innerhalb Chinas verbessert. Wenden Sie sich an Ihr Adobe-Accountteam , um mehr über die Verwendung dieser Funktion zu erfahren.

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
>[Von der Adobe Experience Cloud verwendete IP-Adressen](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/ip-addresses)
>
>[Von Adobe Analytics verwendete Domains](domains.md)
