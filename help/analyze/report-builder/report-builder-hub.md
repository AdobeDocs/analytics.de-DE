---
title: Was ist der Report Builder-Hub in Adobe Analytics?
description: Beschreibt die Report Builder-Hub-Komponenten
role: User
feature: Report Builder
type: Documentation
solution: Analytics
source-git-commit: eedabc6295f9b918e1e00b93993680e676c216c3
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 61%

---

# Report Builder-Hub

Verwenden Sie den Report Builder-Hub, um Datenblöcke zu erstellen, zu aktualisieren, zu löschen und zu verwalten.

Der Report Builder-Hub enthält die Schaltflächen Erstellen und Verwalten , die Liste BEFEHLE und die Bedienfelder SCHNELLE BEARBEITUNG .

<img src="./assets/hub51.png" alt="Report Builder-Hub"/>


## Schaltflächen zum Erstellen, Verwalten und Planen

Verwenden Sie die Schaltflächen Erstellen, Verwalten und Planen , um neue Datenblöcke zu erstellen, vorhandene Datenblöcke zu verwalten oder Datenbanksperren zu planen.

## Bedienfeld „Befehle“

Verwenden Sie das Bedienfeld „Befehle“, um auf Befehle zuzugreifen, die mit den ausgewählten Zellen oder einer vorherigen Aktion kompatibel sind.

### Befehle

| Angezeigte Befehle | Verfügbar wenn… | Zweck |
|------|------------------|--------|
| Datenblock erstellen | Eine oder mehrere Zellen sind in der Arbeitsmappe ausgewählt. | Dient zum Erstellen eines Datenblocks |
| Datenblock bearbeiten | Die ausgewählte Zelle bzw. der ausgewählte Zellenbereich ist nur Teil eines Datenblocks. | Dient zum Bearbeiten eines Datenblocks |
| Datenblock aktualisieren | Die Auswahl enthält mindestens einen Datenblock. Mit dem Befehl werden nur die Datenblöcke in der Auswahl aktualisiert. | Wird zum Aktualisieren eines oder mehrerer Datenblöcke verwendet |
| Alle Datenblöcke aktualisieren | Die Arbeitsmappe enthält einen oder mehrere Datenblöcke. | Wird zum Aktualisieren aller Datenblöcke in der Arbeitsmappe verwendet |
| Arbeitsmappe senden |   | Arbeitsmappe planmäßig versenden |
| Datenblock kopieren | Die ausgewählte Zelle oder der ausgewählte Zellbereich ist Teil eines oder mehrerer Datenblöcke. | Dient zum Kopieren eines Datenblocks |
| Datenblock löschen | Die ausgewählte Zelle bzw. der ausgewählte Zellenbereich ist nur Teil eines Datenblocks. | Dient zum Löschen eines Datenblocks |

## Bedienfeld „Schnellbearbeitung“

Wenn Sie einen oder mehrere Datenblöcke in einem Arbeitsblatt auswählen, zeigt Report Builder das Bedienfeld „Schnellbearbeitung“ an. Sie können das Bedienfeld „Schnellbearbeitung“ verwenden, um Parameter in einem Datenblock zu ändern oder Parameter in mehreren Datenblöcken gleichzeitig zu ändern.

![Das Bedienfeld &quot;Schnellbearbeitung&quot;in Report Builder](./assets/hub2.png)

Die mithilfe der Schnellbearbeitungs-Bereiche vorgenommenen Änderungen gelten für alle ausgewählten Datenblöcke.

### Report Suites

Datenblöcke rufen Daten aus einer ausgewählten Report Suite ab. Wenn mehrere Datenblöcke in einem Arbeitsblatt ausgewählt sind und sie keine Daten aus derselben Report Suite abrufen, zeigt der Link **Report Suites** den Wert *Mehrere* an.

Wenn Sie die Report Suite ändern, übernehmen alle Datenblöcke in der Auswahl die neue Report Suite. Komponenten im Datenblock werden basierend auf der ID (beispielsweise Übereinstimmung mit ```evars```) mit der neuen Report Suite abgeglichen. Wenn eine Komponente nicht in einem Datenblock gefunden wird, wird eine Warnmeldung angezeigt und die Komponente wird aus dem Datenblock entfernt.

Um die Report Suite zu ändern, wählen Sie eine neue Report Suite aus dem Dropdownmenü aus.

![Der Report Builder-Hub, der das Dropdown-Menü der Report Suite anzeigt.](./assets/image16.png)

### Datumsbereich

**[!UICONTROL Datumsbereich]** zeigt den Datumsbereich für die ausgewählten Datenblöcke an. Wenn mehrere Datenblöcke mit mehreren Datumsbereichen ausgewählt sind, zeigt der Link **[!UICONTROL Datumsbereich]** den Wert *Mehrere* an.

### Filter

Der Link für **Filter** zeigt eine zusammenfassende Liste der Filter an, die von den ausgewählten Datenblöcken verwendet werden. Wenn mehrere Datenblöcke mit mehreren angewendeten Filtern ausgewählt sind, zeigt der Link **Filter** den Wert *Mehrere* an.
