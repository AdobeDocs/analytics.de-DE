---
title: Regionale Datenerfassung
description: Informationen zur regionalen Datenerfassung
translation-type: tm+mt
source-git-commit: 09b453c1b4cd8555c5d1718759003945f5c230c5
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 77%

---


# Regionale Datenerfassung

Adobe Experience Cloud verwendet regionale Datenerfassung (Regional Data Collection, RDC), damit die Interaktionen zwischen Ihren Endanwendern und Adobe Experience Cloud so nahe wie möglich an den Anwendern stattfinden. Dies verbessert die Leistung Ihrer Site/App und stellt sicher, dass die Daten so schnell wie möglich erfasst werden, um das Endanwendererlebnis zu optimieren. Sobald Daten aus Ihren digitalen Assets regional in einem Data Collection Center (DCC) erfasst wurden, werden sie über eine sichere Verbindung an ein DPC weitergeleitet, wo sie verarbeitet und für Produkte in Adobe Experience Cloud bereitgestellt werden.

>[!IMPORTANT]
>
>Das China RDC (China Performance Optimization) Hinzufügen-On-Paket ist ein kostenpflichtiges Add-On für Adobe Analytics. Die Leistungsoptimierung der Adobe auf dem chinesischen Festland ermöglicht es Kunden in China, Daten direkt an den China Edge-Knoten zu senden, anstatt an andere Standorte weltweit. Dadurch werden die Seitenladezeit und die Datengenauigkeit verbessert, da die Daten an Knoten außerhalb Chinas gesendet werden. Wenden Sie sich für weitere Informationen an Ihren Vertriebsmitarbeiter für Adobe.

RDC enthält derzeit die folgenden Speicherorte (kann geändert werden):

## Drittanbieter- und HTTP-Datenerfassung

| RDC-Typ | Data Collection Centers |
|---------------------|-------------------|
| Standard | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |

Note: If your Analytics image request is sent to the `adobedc`, `2o7.net` or `omtrdc.net` endpoints, then you have third-party data collection. Sie können dies festlegen, wenn Sie einen der beiden Endpunkte in der URL Ihrer Anfragen sehen.

## Erstanbieter-HTTPS-Datenerfassung

| RDC-Typ | Data Collection Centers |
|---------------------|-------------------|
| Global (Standard) | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |
| Nur Amerika | Oregon, Virginia |
| Nur Europa | Irland, Paris |
| Nur Asien | Mumbai, Singapur, Tokio, Sydney |

Hinweis: Experience-Edge „Global“ bietet die beste Leistung für Ihre Endanwender.  Wenn Sie einen alternativen RDC-Typ verwenden möchten, wenden Sie sich zur Unterstützung an die Adobe-Kundenunterstützung.

## Funktionsweise von RDC

In der folgenden Liste wird der von Adobe verwendete Datenerfassungsprozess beschrieben:

1. DNS löst den Hostnamen der Datenerfassung automatisch in die IP-Adresse des Data Collection Centers auf, das dem Besucher am nächsten ist.
1. Der Besucher sendet die Daten an diesen Ort.
1. Die Daten werden über eine sichere Verbindung sofort an das Data Processing Center weitergeleitet, wo sie verarbeitet und den Produkten in Adobe Experience Cloud bereitgestellt werden.
