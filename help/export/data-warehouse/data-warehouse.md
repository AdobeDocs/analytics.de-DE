---
description: Erfahren Sie mehr über Data Warehouse und wie Sie Daten filtern, um benutzerdefinierte Berichte zu erstellen und auszuführen.
title: Überblick über Data Warehouse
feature: Data Warehouse
uuid: 768557dd-1644-4ce6-bfc2-8c46dd6e1cd1
exl-id: 6a051d53-397b-4a55-9cca-1c83b31c9448
TQID: https://experienceleague.adobe.com/Vkn9mWvBzaiIBf1KYIEUK8cRwTuzw41MT-v-thMBg38
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2:
  - id: e3e906cf-5493-4e0a-9a33-bf0ac37393d6
  - id: ef60b66e-5984-4336-ba72-6d978b1b6f87
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 86%

---

# Überblick über Data Warehouse

Mit Data Warehouse können Sie Adobe Analytics-Daten für das Speichern und Erstellen benutzerdefinierter Berichte kopieren, die Sie durch Filtern der Daten ausführen können.

## Berichtübersicht

Data Warehouse-Berichte können erweiterte Datenbeziehungen aus Rohdaten basierend auf den für Sie relevanten Fragen anzeigen. Sie können eine unbegrenzte Anzahl an Zeilen in einer einzigen Anfrage enthalten (für einzelne, terminierte und heruntergeladene Berichte).

>[!NOTE]
>
>Data Warehouse gibt in Berichten den ersten aufgefundenen Wert innerhalb des Berichtszeitraums aus.

>[!IMPORTANT]
>
>Bei der Segmentierung nach klassifizierten Werten behandeln Analysis Workspace und Data Warehouse „nicht spezifizierte“ Werte unterschiedlich. „Nicht spezifiziert“ in Workspace bezieht sich auf Werte, die nicht klassifiziert sind, während „nicht spezifiziert“ in Data Warehouse auf Werte verweist, die Sie als „nicht spezifiziert“ klassifiziert haben.

## Überblick über die Bereitstellung

Data Warehouse-Berichte werden per E-Mail an einen Cloud-Speicherplatzanbieter verschickt oder gesendet. Die Verarbeitung kann bis zu 72 Stunden dauern. Die Verarbeitungsdauer ist abhängig von der Komplexität der Abfrage und der Menge der angeforderten Daten.

Data Warehouse komprimiert automatisch alle Dateien, die eine Größe von 1 MB überschreiten. Die maximale Größe für E-Mail-Anhänge beträgt 10 MB.

## Zugriff

Adobe aktiviert Data Warehouse nur für Benutzende auf Administratorebene und nur für bestimmte Report Suites. (Sie kann für globale und untergeordnete Report Suites aktiviert werden, jedoch nicht für Datenaggregations-Report Suites.) Der Administrator kann eine Gruppe erstellen, die Zugriff auf Data Warehouse hat, und dann Benutzer, die keine Administratoren sind, mit dieser Gruppe verknüpfen.

Siehe [Verwalten von Data Warehouse-Berechtigungen](/help/export/data-warehouse/t-dw-group.md).

## Erstellen einer Data Warehouse-Anfrage

Informationen zum Erstellen einer Data Warehouse-Anfrage finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

## Verwalten von Data Warehouse-Anfragen

Informationen zum Verwalten von Data Warehouse-Anfragen finden Sie unter [Verwalten von Data Warehouse-Anfragen](/help/export/data-warehouse/data-warehouse-requests-manage.md).

