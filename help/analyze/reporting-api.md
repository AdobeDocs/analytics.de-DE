---
description: Ressourcen und Links für die Reporting-API.
title: Analytics-Reporting-API
uuid: 68ec3490-6e47-4606-860d-dd5e89c574a1
feature: API
role: Developer
exl-id: 003a8b83-6ef0-4313-903a-b76078558d55
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 90%

---

# Analytics-Reporting-API

Die Dokumentation zu den Adobe Analytics-APIs finden Sie unter [Adobe Developer](https://developer.adobe.com/analytics-apis/docs/2.0/).

## Vergleich der Analytics-APIs

| **API-Typ** | **Vollständig verarbeitet** | **Echtzeit** | **Livestream** | **Data Warehouse** |
| --- | --- | --- | --- | --- |
| **Beschreibung** | Vollständig verarbeitete, finale Daten, die für alle Analytics-Schnittstellen zur Verfügung stehen. | Teilweise verarbeitete, beschränkte Metriken, die innerhalb von Sekunden nach der Erfassung verfügbar sind. | Teilweise verarbeitete Trefferdaten, die innerhalb von Sekunden nach der Erfassung verfügbar sind. | Vollständig verarbeitete, finale Daten, die als Grundlage für umfangreiche Datenexporte dienen. |
| [**Latenz**](/help/technotes/latency.md) | 30–90 Minuten | Sekunden – 10 Minuten | Sekunden – 10 Minuten | 90 Minuten oder mehr |
| **Abschluss der Verarbeitung** | „Voll“ | Teilweise | Teilweise | „Voll“ |
| **Berichtsschnittstellen** | Analysis Workspace, Report Builder, API | Echtzeitbericht in Report Builder, 1.4-API | Nur API | Data Warehouse-API |
| **Datengranularität** | Zusammenfassung | Zusammenfassung | Trefferebene | Zusammenfassung |
| **Verarbeitung von Besucherprofilen** | Ja | Nein | Nein | Ja |
| **Segmentunterstützung** | Ja | Nein | Nein | Teilweise |
