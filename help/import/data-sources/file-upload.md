---
title: Hochladen der Datenquellendatei auf Adobe
description: Der Prozess zum Hochladen einer Datenquellendatei in Adobe Analytics zur Erfassung.
exl-id: 64e3cd70-b511-4c4e-abd0-94eb36bc3519
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 1%

---

# Hochladen der Datenquellendatei auf Adobe

Das Senden einer Datenquellendatei an Adobe umfasst einen typischen authentifizierten FTP-Workflow. Sie können Windows Explorer, Finder oder einen dedizierten FTP-Client verwenden, um die gewünschten Dateien zum Speicherort auf Adobe FTP hochzuladen.

Suchen Sie die FTP-Anmeldeinformationen im [Datenquellen-Manager](manage.md). Jede Datenquelle verfügt über einen Link zu ihrer **[!UICONTROL FTP-Info]**. Jeder FTP-Speicherort ist für diese Datenquelle vorgesehen. Sie können nicht denselben FTP-Speicherort für mehrere Datenquellen verwenden.

Aus Sicherheitsgründen sind FTP-Standorte ohne Aktivität für mehr als 30 Tage deaktiviert.

## Die Datei `.fin`

Ein wichtiger Teil der erfolgreichen Aufnahme einer Datenquellendatei ist die Einbeziehung einer `.fin` -Datei. Diese Datei zeigt dem Adobe an, dass die Datendatei zur Verarbeitung bereit ist. Wenn Sie eine Datenquellendatei ohne entsprechende `.fin` -Datei hochladen, verarbeitet Adobe diese Daten nie.

Die Datei `.fin` verfügt über die folgenden Eigenschaften:

* Die Datei weist die Erweiterung `.fin` auf. Stellen Sie sicher, dass Ihr Betriebssystem es Ihnen ermöglicht, Dateitypen anzuzeigen und zu bearbeiten.
* Die Datei ist leer. Speichern Sie keine Daten in der Datei &quot;`.fin`&quot;.
* Die Datei hat genau den gleichen Namen wie die Datenquellendatei. Wenn Sie beispielsweise eine Datenquellendatei mit dem Namen `example.txt` hochladen, muss die `.fin` Datei **** den Namen `example.fin` haben. Wenn sie nicht identisch benannt sind, verarbeitet Adobe nie die Datenquellendatei.

Sobald sowohl die Datenquellendatei als auch die `.fin`-Datei auf die FTP-Site hochgeladen wurden, verarbeitet Adobe die Datei. Laden Sie die Datei &quot;`.fin`&quot;erst hoch, nachdem die Datenquellendatei vollständig hochgeladen wurde. Wenn die `.fin` -Datei vorzeitig hochgeladen wird, ruft Adobe die teilweise hochgeladene Datei ab und erfasst sie, was zu Fehlern führt.

## Verarbeitungsreihenfolge

Wenn Sie mehrere Dateien gleichzeitig auf die FTP-Site hochladen, erfasst Adobe sie in alphanumerischer Reihenfolge. Wenn Ihre Organisation erfordert, dass Dateien in einer bestimmten Reihenfolge erfasst werden, stellen Sie sicher, dass ihre Dateinamen alphanumerisch benannt sind.

## Verarbeitungszeit

Um eine schnellste Dateiverarbeitung zu gewährleisten, empfiehlt Adobe, metrische Daten in einer einzigen Zeile pro Datum zu aggregieren. Diese Datenquellendatei wäre zwar gültig, würde jedoch langsamer verarbeitet:

| `date` | `eVar1` | `event1` | `event2` | `event3` |
| --- | --- | --- | --- | --- |
| `07/24/YYYY` | `red` | `1` | | |
| `07/24/YYYY` | `red` | `1` | | |
| `07/24/YYYY` | `red` | | `1` | |
| `07/24/YYYY` | `red` | | | `1` |

Diese Datei würde schneller verarbeitet werden, da sie dieselben Daten enthält:

| `date` | `eVar1` | `event1` | `event2` | `event3` |
| --- | --- | --- | --- | --- |
| `07/24/YYYY` | `red` | `2` | `1` | `1` |
