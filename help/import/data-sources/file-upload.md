---
title: Datenquellendatei in Adobe hochladen
description: Der Prozess zum Hochladen einer Datenquellendatei zur Aufnahme in Adobe Analytics.
exl-id: 64e3cd70-b511-4c4e-abd0-94eb36bc3519
feature: Data Sources
role: Admin
TQID: 'https://experienceleague.adobe.com/vKIGKArWqdtTSAGhU9kLtonCGyyQtC60UnNle4b5E6A'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2: id: f46a60da-b0b2-4ca3-bd91-271173f4123d
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 1%

---

# Datenquellendatei in Adobe hochladen

Das Senden einer Datenquellendatei an Adobe umfasst einen typischen authentifizierten FTP-Workflow. Sie können Windows Explorer, Finder oder einen dedizierten FTP-Client verwenden, um die gewünschten Dateien in den FTP-Speicherort von Adobe hochzuladen.

Suchen Sie die FTP-Anmeldeinformationen im [Datenquellen-Manager](manage.md). Jede Datenquelle verfügt über einen Link zu ihrer **[!UICONTROL FTP-]**. Jeder FTP-Speicherort ist für diese spezifische Datenquelle bestimmt. Sie können nicht denselben FTP-Speicherort für mehrere Datenquellen verwenden.

Aus Sicherheitsgründen sind FTP-Speicherorte deaktiviert, die seit mehr als 30 Tagen keine Aktivität aufweisen.

## Die `.fin`

Ein wichtiger Bestandteil für die erfolgreiche Aufnahme einer Datenquellendatei ist das Einfügen einer `.fin`. Diese Datei zeigt Adobe an, dass die Datendatei zur Verarbeitung bereit ist. Wenn Sie eine Datenquellendatei ohne entsprechende `.fin` hochladen, verarbeitet Adobe diese Daten nie.

Die `.fin`-Datei weist die folgenden Eigenschaften auf:

* Die Datei hat eine `.fin`. Stellen Sie sicher, dass Sie mit Ihrem Betriebssystem Dateitypen anzeigen und bearbeiten können.
* Die Datei ist leer. Speichern Sie keine Daten in der `.fin`.
* Die Datei hat denselben Namen wie die Datenquellendatei. Wenn Sie beispielsweise eine Datenquellendatei mit dem Namen &quot;`example.txt`&quot; hochladen, **die `.fin` Datei** den Namen &quot;`example.fin`&quot;. Wenn sie nicht identisch benannt sind, verarbeitet Adobe die Datenquellendatei nie.

Nachdem sowohl die Datenquellendatei als auch `.fin` Datei auf die FTP-Site hochgeladen wurden, verarbeitet Adobe die Datei. Laden Sie die `.fin` erst hoch, wenn die Datenquellendatei vollständig hochgeladen wurde. Wenn die `.fin`-Datei vorzeitig hochgeladen wird, ruft Adobe die teilweise hochgeladene Datei ab und nimmt sie auf, was zu möglichen Fehlern führt.

## Verarbeitungsreihenfolge

Wenn Sie mehrere Dateien gleichzeitig auf die FTP-Site hochladen, nimmt Adobe sie in alphanumerischer Reihenfolge auf. Wenn Ihr Unternehmen die Aufnahme von Dateien in einer bestimmten Reihenfolge erfordert, stellen Sie sicher, dass ihre Dateinamen alphanumerisch benannt sind.

## Verarbeitungszeit

Um eine schnellste Verarbeitung der Dateien zu gewährleisten, empfiehlt Adobe, Metrikdaten pro Datum in einer einzigen Zeile zu aggregieren. Diese Datenquellendatei ist zwar gültig, wird aber langsamer verarbeitet:

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
