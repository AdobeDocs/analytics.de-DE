---
title: Bedienfeld „Zielgruppendurchschnitt pro Minute“
description: Verwenden und Interpretieren des Bedienfelds „Medien-Zielgruppendurchschnitt pro Minute“ in Analysis Workspace.
feature: Panels
role: User, Admin
exl-id: be8371ee-8bc6-4a99-8527-dd94eab8a7f9
source-git-commit: 4633225cc35658a7de39a40cd77df00137a54461
workflow-type: tm+mt
source-wordcount: '1656'
ht-degree: 32%

---


# Bedienfeld „Zielgruppendurchschnitt pro Minute“

>[!NOTE]
>
>Das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“ ist nur für Kunden verfügbar, die das Add-on „Streaming-Mediensammlung“ erworben haben.
>
>Wenden Sie sich an Ihren Adobe-Kundenbetreuer oder Ihr Adobe-Account-Team, um das Add-on für Streaming Media Collection zu erwerben.

In Analysis Workspace bezeichnet der Zielgruppendurchschnitt pro Minute die Zeit, die mit der Ansicht Ihres Medien-Streams verbracht wurde, geteilt durch die Inhaltsdauer oder die Gesamtauswahl des Zeitraums mit der ausgewählten Granularität.

Das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“ ermöglicht es Ihnen, die durchschnittliche Nutzung Ihrer Inhalte besser zu verstehen, indem Sie Programme beliebiger Länge oder Genres vergleichen. Sie können beispielsweise den durchschnittlichen Verbrauch verstehen, wenn Sie eine 30-minütige Sitcom mit einem 3-stündigen Sportereignis vergleichen.

Darüber hinaus können Sie das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“ verwenden, um diesen digitalen Zielgruppendurchschnitt pro Minute mit linearen Metriken zum TV-Durchschnitt pro Minute zu vergleichen oder anzuhängen.

Das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“ bietet gegenüber der Metrik „Zielgruppendurchschnitt pro Minute“ die folgenden Vorteile:

* Unterstützt benutzerdefinierte Zeiträume

* Ermöglicht die Aktualisierung der Dauer, nachdem die Classification-Ansichten verarbeitet wurden (falls sie nicht vorhanden waren oder korrigiert werden müssen)

  Wenn Sie dies bei der Verwendung der Metrik getan haben, ist sie entweder nicht vorhanden (wenn die Klassifizierung nicht vorhanden war) oder veraltet (wenn die Klassifizierung vorhanden, aber falsch war).

## Zugriff auf das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“

1. Wechseln Sie in Analysis Workspace zu einer Report Suite, in der Streaming-Medienkomponenten aktiviert sind.

1. Wählen Sie in der linken Navigationsleiste das Symbol **Bedienfelder** aus.

   ![Bereichssymbol in der linken Navigationsleiste](assets/panels-icon.png)

1. Ziehen Sie das Bedienfeld [!UICONTROL **Medien-Zielgruppendurchschnitt pro Minute**] auf die Arbeitsfläche in Analysis Workspace.

1. Fahren Sie zum Konfigurieren des Bereichs mit &quot;[&quot; ](#panel-inputs).

## Panel-Eingaben {#Input}

Verwenden Sie die in diesem Abschnitt beschriebenen Eingabeeinstellungen, um das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“ zu konfigurieren.

1. Beginnen Sie mit der Erstellung eines Bedienfelds „Medien-Zielgruppendurchschnitt pro Minute“, wie [ unter „Zugriff auf das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“](#access-the-media-average-minute-audience-panel) beschrieben.

1. Konfigurieren Sie die folgenden Eingabeeinstellungen:

   | Einstellung | Beschreibung |
   |---------|------------|
   | **Datumsbereich des Bedienfelds** | Der Datumsbereich des Bedienfelds ist standardmäßig [!UICONTROL **Diesen Monat**]. Sie können ihn so verändern, dass Sie einen einzelnen Tag oder viele Monate auf einmal betrachten können. <br></br> Diese Visualisierung ist auf 1.440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn eine Kombination aus Datumsbereich und Granularität mehr als 1.440 Zeilen zur Folge hat, wird die Granularität automatisch aktualisiert, um den vollständigen Datumsbereich anzuzeigen. |
   | [!UICONTROL **Legen Sie hier ein Segment (oder eine beliebige andere Komponente) ab**] | Wie andere Bedienfelder filtert diese Einstellung Ihre Auswahl anhand von Segmenten, die Sie erstellt haben. Dies ist eine hervorragende Möglichkeit, bestimmte Plattformen, Live-Streams oder andere gängige Mediensegmente anzusehen. |
   | [!UICONTROL **Metrik berechnen für**] | Wählen Sie aus, ob Sie den Zielgruppendurchschnitt pro Minute für einen bestimmten Inhalt anzeigen möchten oder ob Sie den Zielgruppendurchschnitt pro Minute für einen benutzerdefinierten Zeitraum anzeigen möchten:<ul><li>**Spezifischer Inhalt:** ist nur verfügbar, wenn die Dauer mithilfe von Klassifizierungen aktualisiert wurde. Wenn die Dauer nicht verfügbar ist oder Sie den Zielgruppendurchschnitt pro Minute für eine Zeitreihe mit mehreren Inhalten oder Inhalten ohne bestimmte Dauer anzeigen möchten (z. B. während eines Live-Streams oder -Ereignisses), sollten Sie [!UICONTROL **Benutzerdefinierter Zeitraum**] auswählen. (Die Dauer kann mithilfe von Klassifizierungen entweder vor oder nach der Verarbeitungszeit festgelegt werden.)</li><li>**Benutzerdefinierter Zeitraum:** Dieser ist unabhängig davon verfügbar, ob die Dauer mithilfe von Klassifizierungen zur Verfügung gestellt wird.</li></ul> <p>Diese Einstellung ändert den Workflow und die Berichtsausgabe.</p> |

1. Fahren Sie mit [Bestimmter Inhalt](#specific-content) oder [Benutzerdefinierter Zeitraum](#custom-time-period) fort, je nach der Option, die Sie im Dropdown-Menü [!UICONTROL **Metrik berechnen für**] ausgewählt haben.

### Bestimmter Inhalt

1. Wenn Sie [!UICONTROL **Spezifischer Inhalt**] im Dropdown-Menü [!UICONTROL **Metrik berechnen für**] beim [Konfigurieren von Bedienfeldeingaben](#panel-inputs) ausgewählt haben, geben Sie die folgenden Konfigurationsoptionen an:

   | Einstellung | Beschreibung |
   |---------|------------|
   | [!UICONTROL **Reporting-Dimension**] | Wenn Sie einen bestimmten Inhalt auswählen, können Sie für die Berichtsausgabe entweder das Feld für den Videonamen oder die Inhalts-ID verwenden, um den Inhalt und den zugehörigen Zielgruppendurchschnitt pro Minute für den ausgewählten Zeitraum anzuzeigen. |
   | [!UICONTROL **Inhalt filtern nach (optional)**] | Wählen Sie aus, wie der spezifische Inhalt gefiltert werden soll, je nach der gewünschten Ansicht oder der Art und Weise, wie Ihre Daten strukturiert sind. <ul>[!UICONTROL **Sendung, Staffel, Folge**]: Zeigt Ihre verfügbaren Sendungen in der Dropdown-Liste an, die Sie mithilfe einer Suche filtern können (oder indem Sie den Sendungsnamen aus der linken Spalte ziehen und ablegen). Sie können Ihre Auswahl hier beenden, um alle Staffeln Ihrer Sendung zu sehen, oder Sie können nach einzelnen Staffeln und dann nach einzelnen Folgen filtern. Diese Einstellung zeigt die Daten für diese Sendungen, Staffeln oder Folgen für den ausgewählten Zeitraum an.</li><li>[!UICONTROL **Benutzerdefinierte Dimension**]: Wenn sich der Name der Sendung unter einer benutzerdefinierten Dimension befindet, können Sie ihn entweder über die Suche im Dropdown-Menü der Dimension (optional) oder über die Suche in der linken Spalte finden. Das Dimensionselement wird basierend auf dieser Auswahl automatisch ausgefüllt und als Folge behandelt.</li><li>[!UICONTROL **None**] Zeigt alle Videonamen an, für die Daten über den Zielgruppendurchschnitt pro Minute für die von Ihnen ausgewählte Auswahl vorliegen. (Diese Option ist standardmäßig ausgewählt.)</li></ul> |

1. Fahren Sie mit [Erweiterte Einstellungen für spezifischen Inhalt](#specific-content-advanced-settings) fort, um erweiterte Einstellungen zu konfigurieren.

### Erweiterte Einstellungen für spezifischen Inhalt

1. Wenn [!UICONTROL **Spezifischer Inhalt**] im Dropdown-Menü [!UICONTROL **Metrik berechnen für**] ausgewählt ist, wählen Sie [!UICONTROL **Erweiterte Einstellungen anzeigen**] und geben Sie dann die folgenden Konfigurationsoptionen an:

   | Einstellung | Beschreibung |
   |---------|------------|
   | Tabelleneinstellungen | Die Standardeinstellung zeigt die Berechnungswerte in der Tabelle an, wobei Zähler und Nenner des Zielgruppendurchschnitts pro Minute als die vorangehenden Spalten in der Tabelle angezeigt werden. Wenn Sie diese Option deaktivieren, werden diese beiden Spalten entfernt, sodass nur der Zielgruppendurchschnitt pro Minute neben dem Videonamen oder der Inhalts-ID verbleibt. |
   | Besuchszeit-Kennzahl | Sie können die standardmäßige mit dem Inhalt verbrachte Zeit auswählen, die nur die Inhaltsdauer enthält, oder die mit der Medienwiedergabe verbrachte Zeit verwenden, die die mit dem Inhalt und den Werbeanzeigen verbrachte Zeit als Zählerberechnung für den Zielgruppendurchschnitt pro Minute enthält. |

1. Wählen Sie [!UICONTROL **Erstellen**], um das Erstellen des Bedienfelds „Medien-Zielgruppendurchschnitt pro Minute“ abzuschließen.

1. Fahren Sie mit [Bedienfeldausgabe](#panel-output) fort, um Informationen zur Verwendung des Bedienfelds „Medien-Zielgruppendurchschnitt pro Minute“ zu erhalten.

### Benutzerdefinierter Zeitraum

1. Wenn Sie [!UICONTROL **Benutzerdefinierter Zeitraum**] im Dropdown-Menü [!UICONTROL **Metrik berechnen für**] beim [Konfigurieren von Bedienfeldeingaben](#panel-inputs) ausgewählt haben, geben Sie die folgenden Konfigurationsoptionen an:

   | Einstellung | Beschreibung |
   |---------|------------|
   | Granularität | Die Standardgranularität beträgt [!UICONTROL **5 Minuten**], Sie können jedoch eine beliebige Granularität auswählen, die als Nenner für die Zeitreihe innerhalb Ihrer gesamten Zeitraumauswahl in der Kalenderauswahl verwendet wird. Wenn Sie beispielsweise 12:00 Uhr bis 12:30 Uhr mit einer Granularität von 5 Minuten auswählen, werden der Zielgruppendurchschnitt pro Minute über die gesamte halbe Stunde sowie sechs Zeilen mit dem Zielgruppendurchschnitt pro Minute für jeden 5-minütigen Zeitraum zurückgegeben. Diese Zeilen werden als Datenpunkte für das Zeitreihendiagramm verwendet. |
   | [!UICONTROL **Inhalt filtern nach (optional)**] | Wählen Sie aus, wie der spezifische Inhalt gefiltert werden soll, je nach der gewünschten Ansicht oder der Art und Weise, wie Ihre Daten strukturiert sind. <ul>[!UICONTROL **Sendung, Staffel, Folge**]: Zeigt Ihre verfügbaren Sendungen in der Dropdown-Liste an, die Sie mithilfe einer Suche filtern können (oder indem Sie den Sendungsnamen aus der linken Spalte ziehen und ablegen). Sie können Ihre Auswahl hier beenden, um alle Staffeln Ihrer Sendung zu sehen, oder Sie können nach einzelnen Staffeln und dann nach einzelnen Folgen filtern. Diese Einstellung zeigt die Daten für diese Sendungen, Staffeln oder Folgen für den ausgewählten Zeitraum an.</li><li>[!UICONTROL **Benutzerdefinierte Dimension**]: Wenn sich der Name der Sendung unter einer benutzerdefinierten Dimension befindet, können Sie ihn entweder über die Suche im Dropdown-Menü der Dimension (optional) oder über die Suche in der linken Spalte finden. Das Dimensionselement wird basierend auf dieser Auswahl automatisch ausgefüllt und als Folge behandelt.</li><li>[!UICONTROL **None**] Zeigt alle Videonamen an, für die Daten über den Zielgruppendurchschnitt pro Minute für die von Ihnen ausgewählte Auswahl vorliegen. (Diese Option ist standardmäßig ausgewählt.)</li></ul> |

1. Fahren Sie mit [Erweiterte Einstellungen für benutzerdefinierte Zeiträume](#custom-time-period-advanced-settings) fort, um die erweiterten Einstellungen zu konfigurieren.

### Erweiterte Einstellungen für benutzerdefinierte Zeiträume

1. Wenn [!UICONTROL **Benutzerdefinierter Zeitraum**] im Dropdown-Menü [!UICONTROL **Metrik berechnen für**] ausgewählt ist, wählen Sie [!UICONTROL **Erweiterte Einstellungen anzeigen**] und geben Sie dann die folgende Konfigurationsoption an:

   | Einstellung | Beschreibung |
   |---------|------------|
   | Tabelleneinstellungen | Die Standardeinstellung zeigt die Berechnungswerte in der Tabelle an, die den Zähler und Nenner des Zielgruppendurchschnitts pro Minute als die vorangehenden Spalten in der Tabelle anzeigt. Wenn Sie diese Option deaktivieren, werden die beiden Spalten entfernt, sodass neben dem Zeitraum nur der Zielgruppendurchschnitt pro Minute verbleibt. |

1. Wählen Sie [!UICONTROL **Erstellen**], um das Erstellen des Bedienfelds „Medien-Zielgruppendurchschnitt pro Minute“ abzuschließen.

1. Fahren Sie mit [Bedienfeldausgabe](#panel-output) fort, um Informationen zur Verwendung des Bedienfelds „Medien-Zielgruppendurchschnitt pro Minute“ zu erhalten.

## Bedienfeldausgabe

Die Bedienfeldausgabe unterscheidet sich je nachdem, ob Sie [!UICONTROL **Bestimmter Inhalt**] oder [!UICONTROL **Benutzerdefinierter**] im [!UICONTROL **Metrik berechnen für**] Dropdown-Menü beim [Konfigurieren von Bedienfeldeingaben](#panel-inputs) haben.

### Bestimmter Inhalt

Das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“ gibt Folgendes zurück:

* Gesamtwert des Zielgruppendurchschnitts pro Minute für Ihre gesamte Auswahl
* Filter und Zielgruppendurchschnitt pro Minute für die einzelnen Videos, die in einer Tabelle angezeigt werden
* Mit dem Inhalt verbrachte Zeit und Videolänge (Dauer), wenn diese erweiterte Einstellung ausgewählt wurde

Um das Bedienfeld jederzeit zu bearbeiten und neu zu erstellen, klicken Sie oben rechts auf das Symbol Bearbeiten (Stift) .

![Standardansicht](assets/specific-content-panel-output.png)

### Spezifische Inhaltsdatenquelle

Das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“ verwendet nur die Metrik „Zielgruppendurchschnitt pro Minute“ zum Erfassen von Daten. Aufschlüsselungen oder andere Metriken können im Bedienfeld nicht verwendet werden.

| Metrik | Beschreibung |
|--------|-------------|
| Zielgruppendurchschnitt pro Minute | Die Zeit, die mit der Ansicht Ihres Medien-Streams verbracht wurde, dividiert durch die Videolänge (Dauer), die über Classifications bereitgestellt wird. |

### Benutzerdefinierter Zeitraum {#custom-time-period-output}

Das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“ gibt Folgendes zurück:

* Der Zielgruppendurchschnitt pro Minute für die gesamte Auswahl

* Der maximale und minimale Zielgruppendurchschnitt pro Minute

* Das Liniendiagramm, das den Zielgruppendurchschnitt pro Minute für die gesamte Auswahl anzeigt.

* Eine Tabelle, die die Filter und den Zielgruppendurchschnitt pro Minute für die Granularitäten sowie die mit dem Inhalt verbrachte Zeit und die Granularität für jeden Zeitraum anzeigt

  Diese Tabelle wird nur angezeigt, wenn die Option unter Erweiterte Einstellungen [!UICONTROL **Berechnungswerte in Tabelle anzeigen**] ausgewählt ist.

Um das Bedienfeld jederzeit zu bearbeiten und neu zu erstellen, klicken Sie oben rechts auf das Symbol Bearbeiten (Stift) .

![Output von gleichzeitigen Betrachtern](assets/custom-time-period-panel-output.png)

### Datenquelle für benutzerdefinierten Zeitraum

Das Bedienfeld „Medien-Zielgruppendurchschnitt pro Minute“ verwendet nur die Metrik „Zielgruppendurchschnitt pro Minute“ zum Erfassen von Daten. Aufschlüsselungen oder andere Metriken können im Bedienfeld nicht verwendet werden.

| Metrik | Beschreibung |
|---|---|
| Zielgruppendurchschnitt pro Minute | Die mit der Ansicht Ihres Medien-Streams verbrachte Zeit dividiert durch die Gesamtauswahl oder die ausgewählte Granularität in Minuten. |
