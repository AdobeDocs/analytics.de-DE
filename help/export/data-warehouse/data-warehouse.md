---
description: Erfahren Sie mehr über Data Warehouse und das Filtern der Daten, sodass Sie benutzerdefinierte Berichte erstellen und ausführen können.
title: Data Warehouse-Übersicht
feature: Data Warehouse
uuid: 768557dd-1644-4ce6-bfc2-8c46dd6e1cd1
exl-id: 6a051d53-397b-4a55-9cca-1c83b31c9448
source-git-commit: d929e97a9d9623a8255f16729177d812d59cec05
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 79%

---

# Data Warehouse-Übersicht

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

Data Warehouse ZIP-komprimiert automatisch Dateien, die größer als 1 MB sind. Die Maximalgröße für E-Mail-Anhänge beträgt 10 MB.

## Zugriff

Adobe aktiviert Data Warehouse nur für Benutzende auf Administratorebene und nur für bestimmte Report Suites. (Sie kann für globale und untergeordnete Report Suites, jedoch nicht für Datenaggregations-Report Suites aktiviert werden.) Der Administrator kann eine Gruppe erstellen, die Zugriff auf Data Warehouse hat, und anschließend Benutzer, die sich nicht auf Administratorebene befinden, dieser Gruppe zuweisen.

Siehe [Verwalten von Data Warehouse-Berechtigungen](/help/export/data-warehouse/t-dw-group.md).

## Erstellen einer Data Warehouse-Anfrage

Informationen zum Erstellen einer Data Warehouse-Anfrage finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

## Verwalten von Data Warehouse-Anfragen

Informationen zum Verwalten von Data Warehouse-Anfragen finden Sie unter [Verwalten von Data Warehouse-Anfragen](/help/export/data-warehouse/data-warehouse-requests-manage.md).

