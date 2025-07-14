---
title: Was ist der Report Builder-Hub in Adobe Analytics?
description: Beschreibt die Report Builder-Hub-Komponenten
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: e18381ea-b7d4-4d7a-9ded-23b2d06fa204
source-git-commit: d3d74042f6c282db490483393f4b58cddd6b1525
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 54%

---

# Report Builder-Hub

Verwenden Sie den Report Builder-Hub, um Datenblöcke zu erstellen, zu aktualisieren, zu löschen und zu verwalten.

Der Report Builder-Hub enthält die Schaltflächen „Erstellen“, „Verwalten“ und „Planen“, das Bedienfeld „Befehle“ und das Bedienfeld „Schnellbearbeitung“.

<img src="./assets/hub51.png" alt="Report Builder-Hub"/>


## Erstellen, Verwalten und Planen von Schaltflächen

Verwenden Sie die Schaltflächen Erstellen, Verwalten und Planen , um neue Datenblöcke zu erstellen, vorhandene Datenblöcke zu verwalten oder Datenblöcke zu planen.

## Bedienfeld „Befehle“

Verwenden Sie das Bedienfeld „Befehle“, um auf Befehle zuzugreifen, die mit den ausgewählten Zellen oder einer vorherigen Aktion kompatibel sind.

### Befehle

| Angezeigte Befehle | Verfügbar wenn… | Zweck |
|------|------------------|--------|
| Datenblock bearbeiten | Die ausgewählte Zelle bzw. der ausgewählte Zellenbereich ist nur Teil eines Datenblocks. | Dient zum Bearbeiten eines Datenblocks |
| Datenblock aktualisieren | Die Auswahl enthält mindestens einen Datenblock. Der Befehl aktualisiert nur die Datenblöcke in der Auswahl. | Wird zum Aktualisieren eines oder mehrerer Datenblöcke verwendet |
| Alle Datenblöcke aktualisieren | Die Arbeitsmappe enthält einen oder mehrere Datenblöcke. | Wird zum Aktualisieren aller Datenblöcke in der Arbeitsmappe verwendet |
| Arbeitsmappe senden |   | Eine Arbeitsmappe nach einem Zeitplan senden. |
| Datenblock kopieren | Die ausgewählte Zelle oder der ausgewählte Zellbereich ist Teil eines oder mehrerer Datenblöcke. | Dient zum Kopieren eines Datenblocks |
| Datenblock ausschneiden |   | Wird zum Ausschneiden eines Datenblocks verwendet |
| Datenblock löschen | Die ausgewählte Zelle bzw. der ausgewählte Zellenbereich ist nur Teil eines Datenblocks. | Dient zum Löschen eines Datenblocks |

## Bedienfeld „Schnellbearbeitung“

Wenn Sie einen oder mehrere Datenblöcke in einem Arbeitsblatt auswählen, zeigt Report Builder das Bedienfeld „Schnellbearbeitung“ an. Sie können das Bedienfeld „Schnellbearbeitung“ verwenden, um Parameter in einem Datenblock zu ändern oder Parameter in mehreren Datenblöcken gleichzeitig zu ändern.

![Das Bedienfeld „Schnellbearbeitung“ in Report Builder](./assets/hub2.png)

Die mithilfe der Schnellbearbeitungs-Bereiche vorgenommenen Änderungen gelten für alle ausgewählten Datenblöcke.

### Report Suites

Datenblöcke rufen Daten aus einer ausgewählten Report Suite ab. Wenn mehrere Datenblöcke in einem Arbeitsblatt ausgewählt sind und sie keine Daten aus derselben Report Suite abrufen, wird der **Report Suites**-Link *Mehrere* angezeigt.

Wenn Sie die Report Suite ändern, übernehmen alle Datenblöcke in der Auswahl die neue Report Suite. Komponenten im Datenblock werden mit der neuen Report Suite abgeglichen, die beispielsweise auf einer ID basiert, die mit ```evars``` übereinstimmt). Wenn eine Komponente nicht in einem Datenblock gefunden wird, wird eine Warnmeldung angezeigt und die Komponente wird aus dem Datenblock entfernt.

Um die Report Suite zu ändern, wählen Sie eine neue Report Suite aus dem Dropdown-Menü aus.

![Der Report Builder Hub mit dem Dropdown-Menü für die Report Suite.](./assets/image16.png)

### Datumsbereich

**[!UICONTROL Datumsbereich]** zeigt den Datumsbereich für die ausgewählten Datenblöcke an. Wenn mehrere Datenblöcke mit mehreren Datumsbereichen ausgewählt sind, zeigt der Link **[!UICONTROL Datumsbereich]** &quot;*&quot;*. [Weitere Informationen](/help/analyze/report-builder/select-date-range.md)

### Segmente

Der **Segmente**-Link zeigt eine zusammenfassende Liste der Segmente an, die von den ausgewählten Datenblöcken verwendet werden. Wenn mehrere Datenblöcke mit mehreren angewendeten Segmenten ausgewählt sind, wird der Link **Segmente** angezeigt *Mehrere*. [Weitere Informationen](/help/analyze/report-builder/work-with-segments.md)
