---
title: Bulk-Dateneinfüge-API
description: Die Bulk Data Insertion-API (BDIA) ist eine Adobe Analytics-Funktion, mit der Sie Server-Aufrufdaten in Datei-Batches hochladen können, anstatt Client-seitige Bibliotheken wie AppMeasurement zu verwenden.
solution: Analytics
feature: API
exl-id: c9d23fae-2800-42bb-8f8d-adf915cadc62
role: Admin
TQID: https://experienceleague.adobe.com/TVa-LtTWKi6lQKGQKhH2bu5UcKsSJ2-KVqlfU5tQROQ
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 85%

---

# Bulk-Dateneinfüge-API

Die Masseneinfügung von Daten ermöglicht verschiedene Anwendungsfälle, z. B.:

* Aufnahme historischer Daten aus einem früheren Analysesystem

* Ein internes System zur Erfassung von Analysen, durch das AppMeasurement nicht verwendet werden kann. Sie können Extract-Transform-Load-Prozesse (ETL) verwenden, um Daten in Batch-Dateien einzufügen, und diese dann mit BDIA in Adobe Analytics hochladen.

* Datenerfassung in Geräten, die nur gelegentlich eine Internetverbindung haben. Diese Geräte speichern die Interaktionen so lange, bis sie eine Verbindung erhalten. Das Gerät kann dann alle Daten gleichzeitig über BDIA hochladen.

Die Dateneinfüge-API und die [Bulk-Dateneinfüge-API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) sind beides Methoden, um Server-seitig erfasste Daten an Adobe Analytics zu senden. Aufrufe der Data Insertion-API erfolgen jeweils für ein Ereignis. Die Bulk Data Insertion-API akzeptiert Dateien mit Ereignisdaten im CSV-Format, wobei ein Ereignis pro Zeile angegeben wird. Wenn Sie an einer neuen Implementierung der Server-seitigen Sammlung arbeiten, empfehlen wir die Verwendung der Bulk Data Insertion-API.
