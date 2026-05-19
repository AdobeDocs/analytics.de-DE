---
title: Fehlerbehebung bei Data Warehouse-Anfragenlieferzeiten
description: Ermitteln Sie potenzielle Probleme mit einer Data Warehouse-Anforderung, die die Versandzeiten verlängern können.
feature: Data Warehouse
exl-id: eed4d172-fffd-453f-ab5b-0fc2a79d5bd0
TQID: https://experienceleague.adobe.com/oWkM-wTuJ75sR6AzkjD8WfY9DYLUdtToSGyu8hJIXVk
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 358
ht-degree: 59%

---

# Fehlerbehebung bei Versandzeiten von Data Warehouse-Anforderungen

Eine bestimmte Data Warehouse-Anforderung kann zwischen einer Stunde und mehreren Tagen dauern. Aufgrund der folgenden Faktoren ist es schwierig, den genauen Zeitaufwand für die Bearbeitung einer Anforderung abzuschätzen:

* Datumsbereich der Anforderung,
* Traffic-Aufkommen, das Ihre Report Suite während des angeforderten Zeitraums erhalten hat,
* Die Anzahl der Regeln innerhalb eines Segments und welche Variablen innerhalb eines Segments verwendet werden,
* Die Datenmenge innerhalb eines Segments,
* Die Anzahl der verwendeten Aufschlüsselungen und die Anzahl der eindeutigen Werte in jeder Aufschlüsselung,
* Die Anzahl der verwendeten Metriken,
* Die Anzahl der gleichzeitig verarbeiteten Anforderungen,
* VISTA-Regeln, falls für die Anwendung auf Data Warehouse-Anforderungen konfiguriert.

## Anforderungen ändern, um den Versand zu beschleunigen

Wenn Data Warehouse-Anfragen durchgängig lange dauern, sollten Sie Ihre Anfragen ändern. Die einzige Möglichkeit, die Bereitstellung einer Data Warehouse-Anfrage zu beschleunigen, besteht darin, eine Anfrage zu ändern.

Um die Bereitstellung einer Data Warehouse-Anfrage zu beschleunigen, können Sie sie wie folgt ändern:

* **Verwenden Sie ein Segment, das eine kleinere Stichprobe von Daten enthält**: Je weniger Daten eine Anforderung enthält, desto schneller wird ein Bericht zurückgegeben.
* **Anfragen in 14-tägigen Intervallen oder weniger ausführen** Kleinere Anfragen werden schneller verarbeitet als große Anfragen.
* **Weniger Aufschlüsselungen verwenden** Viele Aufschlüsselungen in einer Anfrage erhöhen exponentiell die Verarbeitungszeit.

## Verwenden einer alternativen Methode

Wenn Sie diese Art von Berichten schneller benötigen, ziehen Sie die folgenden Alternativen in Betracht:

* **Analysis Workspace**: Obwohl keine unbegrenzten Dimensionselemente verfügbar sind, sind fast alle anderen Anwendungsfälle enthalten, die von Data Warehouse bereitgestellt werden.
* **Daten-Feed**: Alle Rohdaten in einer Report Suite werden täglich abgerufen und an ein Cloud-Ziel gesendet. Anschließend können Sie die Daten in Ihre eigene Datenbank importieren und Abfragen ausführen, um die benötigten Daten abzurufen.
* **Individuelle Engineering Services-Lösung**: Adobe Engineering Services bieten gegen Aufpreis eine individuelle Lösung für Ihr Unternehmen. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.
