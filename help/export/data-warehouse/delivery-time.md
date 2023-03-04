---
title: Fehlerbehebung bei Versandzeiten von Data Warehouse-Anforderungen
description: Ermitteln Sie potenzielle Probleme mit einer Data Warehouse-Anforderung, die die Versandzeiten verlängern können.
feature: Data Warehouse
exl-id: eed4d172-fffd-453f-ab5b-0fc2a79d5bd0
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 97%

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

Wenn Sie feststellen, dass Data Warehouse-Anforderungen durchweg lange dauern, sollten Sie Ihre Anforderungen ändern, um Folgendes zu berücksichtigen:

* **Verwenden Sie ein Segment, das eine kleinere Stichprobe von Daten enthält**: Je weniger Daten eine Anforderung enthält, desto schneller wird ein Bericht zurückgegeben.
* **Anforderungen in Schritten von 14 Tagen oder weniger ausführen**: Kleinere Anforderungen werden schneller verarbeitet als große Anforderungen.
* **Weniger Aufschlüsselungen verwenden:** Viele Aufschlüsselungen in einer Data Warehouse-Anforderung erhöhen die Verarbeitungszeit exponentiell.

>[!IMPORTANT]
>
> *Es gibt keine Möglichkeit, den Versand einer Data Warehouse-Anforderung zu beschleunigen.*

Wenn Sie diese Art von Berichten schneller benötigen, ziehen Sie die folgenden Alternativen in Betracht:

* **Analysis Workspace**: Obwohl keine unbegrenzten Dimensionselemente verfügbar sind, sind fast alle anderen Anwendungsfälle enthalten, die von Data Warehouse bereitgestellt werden.
* **Daten-Feed**: Nimmt täglich alle Rohdaten in einer Report Suite auf und sendet sie an eine FTP-Site. Sie können diese Daten dann in Ihre eigene Datenbank importieren und Abfragen ausführen, um die gewünschten Daten abzurufen.
* **Individuelle Engineering Services-Lösung**: Adobe Engineering Services bieten gegen Aufpreis eine individuelle Lösung für Ihr Unternehmen. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.
