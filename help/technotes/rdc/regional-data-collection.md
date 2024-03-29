---
title: Regionale Datenerfassung
description: Informationen zur regionalen Datenerfassung
feature: Regional Data Collection
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
source-git-commit: a4dd138f0f2198da66caa272dd62b46f24b578b2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 35%

---

# Regionale Datenerfassung

Die Adobe Experience Cloud verwendet die regionale Datenerfassung (Regional Data Collection, RDC), damit Interaktionen zwischen Ihren Besuchern und der Adobe so nahe wie möglich an Ihren Besuchern stattfinden. Sobald Daten regional in einem Datenerfassungscenter (DCC, auch Edge-Site genannt) erfasst werden, werden sie über eine sichere Verbindung an ein Datenverarbeitungszentrum (DPC, auch als Core-Site bezeichnet) weitergeleitet. Nach der Verarbeitung sind die Daten für Produkte in der Adobe Experience Cloud verfügbar. Wenden Sie sich zur Änderung Ihres RDC-Typs an die Kundenunterstützung von Adobe.

Der regionale Datenerfassungsprozess umfasst die folgenden Schritte:

1. DNS löst automatisch den Hostnamen der Sammlung auf die IP-Adresse des Datenerfassungszentrums auf, das dem Besucher am nächsten ist.
1. Der Besucher sendet die Daten an diesen Ort.
1. Die Daten werden über eine sichere Verbindung sofort an das Data Processing Center weitergeleitet, wo sie verarbeitet und den Produkten in Adobe Experience Cloud bereitgestellt werden.

Die Verwendung der regionalen Datenerfassung bietet verschiedene Vorteile:

* **Leistung**: Mit RDC stellen Ihre Besucher eine Verbindung zum nächstgelegenen DCC her. Diese Optimierung bietet die schnellste Reaktionszeit, was zu genauerer Verfolgung und schnelleren Ladezeiten führt.
* **Redundanz**: Wenn die Kommunikation zwischen dem DCC und Ihrem DPC unterbrochen wird, speichert die RDC-Infrastruktur der Adobe Daten lokal und leitet sie bei der Wiederherstellung der Kommunikation an das DPC weiter.

RDC enthält derzeit die folgenden Speicherorte (kann sich ändern):

## Datenerfassung durch Dritte

| RDC-Typ | Data Collection Centers |
| --- | --- |
| Standard | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney, China* |

{style="table-layout:auto"}

*Die regionale Datenerfassung für China benötigt das Add-on-Paket für China. Siehe [Leistungsoptimierung für China](#china-performance-optimization) unten.

>[!NOTE]
>
>Wenn Ihre Analytics-Bildanfrage an die Endpunkte `adobedc.net`, `2o7.net` oder `omtrdc.net` gesendet wird, erfolgt die Datenerfassung durch Dritte. Sie können dies festlegen, wenn Sie einen der beiden Endpunkte in der URL Ihrer Anfragen sehen.

## First-Party-Datenerfassung

| RDC-Typ | Data Collection Centers |
| --- | --- |
| Global (Standard) | Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |
| Global + China* | China*, Oregon, Virginia, Irland, Paris, Mumbai, Singapur, Tokio, Sydney |
| Nur Amerika | Oregon, Virginia |
| Nur Europa | Irland, Paris |
| Nur Asien | Mumbai, Singapur, Tokio, Sydney |
| Nur China* | Peking |

{style="table-layout:auto"}

*Die RDC-Typen „Nur China“ und „Global + China“ erfordern das China-Zusatzpaket. Global + China leitet Daten aus China an die China RDC der Adobe weiter, während Daten aus China an die nächstgelegene RDC außerhalb Chinas weitergeleitet werden. Siehe [Leistungsoptimierung für China](#china-performance-optimization) unten.

## Leistungsoptimierung für China

Das Add-On-Paket China RDC (China Performance Optimization) ist ein kostenpflichtiges Add-on zu Adobe Analytics. Durch die Leistungsoptimierung der Adobe in Festlandchina können Kunden mit Nutzern in China diese Daten direkt an Adobe-Datenerfassungsserver und nicht an andere Standorte weltweit senden lassen. Diese Optimierung verbessert die Seitenladezeiten und die Datengenauigkeit im Vergleich zum Senden der Daten an Orte außerhalb Chinas. Die Daten werden schließlich an eines der Datenverarbeitungszentren (Data Processing Center, DPC) der Adobe außerhalb Chinas übermittelt. Wenden Sie sich für weitere Informationen an Ihren Adobe-Vertriebsmitarbeiter.

>[!NOTE]
>
>Das China RDC Add-On-Paket wird für die [Web SDK](/help/implement/aep-edge/overview.md).

