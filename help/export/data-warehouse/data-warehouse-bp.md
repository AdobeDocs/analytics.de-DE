---
description: Lernen Sie die Richtlinien kennen, die Ihnen helfen, die Zeit für das Abrufen von Daten aus Data Warehouse zu reduzieren.
keywords: Best Practices;Fehler;Zeitüberschreitung;Fehlerbehebung
title: Best Practices für Data Warehouse
feature: Data Warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
exl-id: 7e21534b-a7ec-4231-89f1-0ad5013e70cf
TQID: 'https://experienceleague.adobe.com/fWshdRnbrh11kLLT3DiW0a-qMJ13o8v4EMH-t-ceWC8'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: f47edbe0-f963-46ff-a667-71011396f5f3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 27%

---

# Best Practices für Data Warehouse

Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Verwenden Sie die folgenden Richtlinien, um die Zeit für das Abrufen von Daten zu reduzieren:

| Richtlinie | Beschreibung |
|--- |--- |
| Die angeforderte Datenmenge verstehen | Ein mehrjähriger Bericht für eine große Report Suite kann Dutzende von Milliarden von Datenzeilen enthalten. Die Verarbeitung und Auswertung dieser Daten kann Tage oder gar Wochen dauern. Evaluieren Sie, wie der Bericht verwendet wird, um festzustellen, ob einige der mehrjährigen Daten verfügbar sind oder ob Sie den Bericht in mehrere Anfragen aufteilen können. |
| Berichtszeitraum an die Granularität anpassen | Die Berichtsgranularität erfordert eine zusätzliche Verarbeitungszeit. Wenn Sie monatliche Granularität über ein ganzes Jahr hinweg melden, werden Ihre Berichte viel schneller verarbeitet, wenn Sie für jeden Monat eine Berichtsanfrage senden. |
| Bericht zu abgeschlossenen Datenbereichen | Die Data Warehouse-Berichte werden erst dann erzeugt, wenn der angeforderte Datumsbereich abgeschlossen ist. Wenn Sie beispielsweise am Mittwoch einen Bericht über die laufende Woche anfordern, so wird der Bericht erst am darauffolgenden Sonntag erzeugt. |
| Erzeugen von Pfadberichten in Data Warehouse | Pfadmetriken (Einstiege, Ausstiege, Bounces usw.) sind in Data Warehouse nicht verfügbar. |
| Virtual Report Suites | Data Warehouse-Berichte zu Virtual Report Suites unterstützen die alternative Zeitzone, die in der Virtual Report Suite konfiguriert ist. |

