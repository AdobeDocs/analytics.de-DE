---
title: Transaktions-ID-Datenquellen
description: Erfahren Sie mehr über den allgemeinen Workflow bei der Verwendung der Transaktions-ID-Datenquellen.
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
source-git-commit: 1ee6a1e69a277f0d3c0ffd1defca0d4cb098cc6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 92%

---

# Transaktions-ID-Datenquellen

Mit den Transaktions-ID-Datenquellen können Sie nicht nur Online- und Offline-Daten nebeneinander anzeigen, sondern die Daten auch miteinander verknüpfen. Dazu müssen Sie die [`transactionID`](/help/implement/vars/page-vars/transactionid.md)-Variablen in Ihrer Analytics-Implementierung verwenden.

Wenn Sie einen Online-Treffer senden, der einen `transactionID`-Wert enthält, erstellt Adobe einen „Schnappschuss“ aller zu diesem Zeitpunkt festgelegten oder beibehaltenen Variablen. Wenn eine übereinstimmende Transaktions-ID gefunden wird, die über Data Sources hochgeladen wurde, werden die Offline- und Online-Daten miteinander verknüpft. Dabei ist es nicht wichtig, welche Datenquelle zuerst abgerufen wird.

## Allgemeiner Workflow Transaktions-ID-Datenquellen

Verwenden Sie den folgenden generischen Workflow, um mit der Verwendung von Transaktions-ID-Datenquellen zu beginnen:

1. Erstellen Sie eine Datenquelle (Kategorie „Generische“ und Typ „Generische Datenquelle (Transaktions-ID)“).
1. Führen Sie den Einrichtungsassistenten für die Datenquelle aus, um einen FTP-Speicherort zum Hochladen von Daten und Herunterladen einer Vorlagendatei für Datenquellen abzurufen.
1. Aktualisieren Sie Ihre Implementierung, um die `transactionID`-Variable einzuschließen.
1. Laden Sie eine Datenquellendatei mit einer `.fin`-Datei auf die FTP-Site hoch.

## Beispiel für eine Upload-Datei und den Implementierungscode

Wenn Sie die folgende Datenquellendatei hochgeladen und den folgenden Code auf Ihrer Site implementiert haben, werden die Daten in der Berichterstellung verknüpft. Die Datenquellendatei verwendet eVar1 und event1, während die Online-Implementierung eVar2 und event2 verwendet. Da die Transaktions-ID übereinstimmt, können Sie event2-Daten für eVar1 und event1-Daten für eVar2 anzeigen.

### Beispieldatei

Laden Sie die Vorlage herunter, aktualisieren Sie die Werte und laden Sie sie dann auf den FTP-Speicherort der Datenquellen hoch:

| `#` | `Example eVar1 name` | `Example event 1 name` | `1` |
|---|---|---|---|
| `Date` | `Evar 1` | `Event 1` | `transactionID` |
| `01/01/2020/12/00/00` | `Example eVar1 value` | `1` | `1234` |

### Beispiel für den Implementierungscode

Weitere Informationen zur Transaktions-ID finden Sie unter [`transactionID`](/help/implement/vars/page-vars/transactionid.md) im Benutzerhandbuch für die Implementierung.

```js
var s = s_gi("examplersid");
s.eVar2 = "Example eVar2 value";
s.events = "event2";
s.transactionID = "1234";
s.t();
```
