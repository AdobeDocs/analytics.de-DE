---
description: Erfahren Sie mehr über Richtlinien, die Ihnen helfen, die Zeit für das Abrufen von Daten vom Data Warehouse zu reduzieren.
keywords: Best Practices;Fehler;Zeitüberschreitung;Fehlerbehebung
title: Best Practices für Data Warehouse
feature: Data Warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
exl-id: 7e21534b-a7ec-4231-89f1-0ad5013e70cf
source-git-commit: d929e97a9d9623a8255f16729177d812d59cec05
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 79%

---

# Best Practices für Data Warehouse

Data Warehouse bietet eine flexible Oberfläche zum Ausführen benutzerdefinierter Berichte. Verwenden Sie die folgenden Richtlinien, um die Zeit für das Abrufen von Daten zu reduzieren:

| Richtlinie | Beschreibung |
|--- |--- |
| Einschätzen der angeforderten Datenmenge | Bei einem mehrere Jahre umspannenden Bericht für eine umfangreiche Report Suite kann die Anzahl der Datenzeilen durchaus im zweistelligen Milliardenbereich liegen. Die Verarbeitung und Auswertung dieser Daten kann Tage oder gar Wochen dauern. Stellen Sie fest, wie der Bericht genutzt werden soll, und ermitteln Sie anhand dieser Informationen, ob ein Teil der Mehrjahresdaten verfügbar ist oder ob der Bericht in mehrere Anforderungen unterteilt werden kann. |
| Anpassen des Berichtszeitraums an die Granularität | Die Berichtgranularität verlängert die Verarbeitungszeit. Wenn Sie die monatliche Granularität über ein ganzes Jahr in einem Bericht darstellen, so wird der Bericht erheblich schneller verarbeitet, wenn Sie je eine Berichtanforderung für jeden Monat senden. |
| Bericht über abgeschlossene Datumsbereiche | Die Data Warehouse-Berichte werden erst dann erzeugt, wenn der angeforderte Datumsbereich abgeschlossen ist. Wenn Sie beispielsweise am Mittwoch einen Bericht über die laufende Woche anfordern, so wird der Bericht erst am darauffolgenden Sonntag erzeugt. |
| Erstellen von Pfadberichten in Data Warehouse | Pfadmetriken (Einstiege, Ausstiege, Bounces usw.) sind in Data Warehouse nicht verfügbar. |
| Virtual Report Suites | Data Warehouse-Berichte zu Virtual Report Suites unterstützen die alternative Zeitzone, die in der Virtual Report Suite konfiguriert wurde. |

