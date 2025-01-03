---
title: Panel „Verbrachte Zeit bei der Medienwiedergabe“
description: Verwendung und Interpretation des Panels „verbrachten Zeit bei der Medienwiedergabe“ in Analysis Workspace.
feature: Panels
role: User, Admin
exl-id: 9268baf7-b50b-4c09-a722-7bfcd4172f15
source-git-commit: 4633225cc35658a7de39a40cd77df00137a54461
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 73%

---

# Panel „Verbrachte Zeit bei der Medienwiedergabe“

In Analysis Workspace bezeichnet die Wiedergabedauer die Zeit, die mit der Anzeige Ihrer Medien-Streams zu einem bestimmten Zeitpunkt verbracht wurde. Dazu gehören Pausen, Pufferung und die Zeit bis zum Start.

Das Bedienfeld „Bei Medienwiedergabe verbrachte Zeit“ ermöglicht die Analyse der Medienwiedergabe im Zeitverlauf mit Details zu Spitzenzeiten, in denen besonders viele gleichzeitige Aufrufe stattfanden, und der Möglichkeit, diese aufzuschlüsseln und zu vergleichen.

Kunden, die das Add-on zur Streaming-Mediensammlung erworben haben, können die Wiedergabedauer analysieren, um wertvolle Einblicke in die Qualität von Inhalten und die Interaktion mit Betrachtern zu erhalten und bei der Fehlerbehebung oder Planung von Volumen oder Skalierung zu helfen.

Die Wiedergabedauer kann Ihnen dabei helfen, Folgendes zu verstehen:

* Wo Spitzenzeiten bei gleichzeitigen Ansichten auftraten

* Wo es zu Abbrüchen kam

Im Folgenden finden Sie eine Videoübersicht zu diesem Bedienfeld:

>[!VIDEO](https://video.tv.adobe.com/v/338699)

## Verwenden des Panels „Bei Medienwiedergabe verbrachte Zeit“

1. Navigieren Sie zu einer Report Suite mit aktivierten Streaming-Medienkomponenten.
1. Wählen Sie ganz links das Bedienfeldsymbol aus und ziehen Sie das Bedienfeld dann in Ihr Analysis Workspace-Projekt.
1. Fahren Sie mit den folgenden Abschnitten fort, um das Bedienfeld „Bei Medienwiedergabe verbrachte Zeit“ anzupassen

   * [Panel-Eingaben](#panel-inputs)
   * [Panel-Ausgabe](#panel-output)

## Panel-Eingaben {#Input}

Sie können das Panel „Verbrachte Zeit bei der Medienwiedergabe“ mithilfe der folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
|---|---|
| Datumsbereich der Bedienfelder | Der Datumsbereich des Panels ist standardmäßig „Heute“. Sie können ihn so verändern, dass Sie einen einzelnen Tag oder viele Monate auf einmal betrachten können.<br>Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch reduziert, um den vollständigen Datumsbereich zu erlauben. |
| Granularität | Die Standardeinstellung für die Granularität ist „Minute“.<br>Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn eine Kombination aus Datumsbereich und Granularität zu mehr als 1440 Zeilen führt, wird die Granularität automatisch reduziert, um den vollständigen Datumsbereich zu erlauben. |
| Zusammenfassende Zahlen der Bedienfelder | Um Details zu Datum und Uhrzeit für die verbrachte Zeit bei der Medienwiedergabe anzuzeigen, steht eine zusammenfassende Zahl zur Verfügung. Das Maximum zeigt Details zu Spitzenzeiten von gleichzeitigen Aufrufen an. Das Minimum zeigt Details zum Tiefpunkt an. In der Summe wird die gesamte Wiedergabezeit für diese Auswahl dargestellt. Im Panel wird standardmäßig nur der maximale Wert angezeigt. Sie können dies jedoch ändern, sodass das Minimum, die Summe oder eine beliebige Kombination der drei Werte angegeben wird.<br>Wenn Sie Aufschlüsselungen verwenden, wird jeweils eine Zusammenfassungsnummer angezeigt. |
| Serienaufschlüsselung | Optional können Sie Ihre Visualisierung nach Segmenten, Dimensionen, Dimensionselementen oder Datumsbereichen unterteilen.<p>– Sie können bis zu 10 Zeilen auf einmal ansehen. Aufschlüsselungen sind auf eine einzelne Ebene beschränkt.</p><p>– Beim Ziehen einer Dimension werden die oberen Dimensionselemente automatisch anhand des im Panels ausgewählten Datumsbereichs ausgewählt.</p>– Ziehen Sie zum Vergleichen von Datumsbereichen zwei oder mehr Datumsbereiche in den Filter für die Aufschlüsselung der Serie. |
| Zeitformat | Sie können die Wiedergabedauer entweder in `Hours:Minutes:Seconds` (Standard) oder in `Minutes` anzeigen (in Ganzzahlen, auf 0,5 aufgerundet). |
| Anzeige der Datumsreihe | Wenn Sie mindestens zwei Datumsbereichssegmente als Serienaufschlüsselungen platziert haben, sehen Sie die Option, entweder Überlagerung (Standard) oder Sequenziell auszuwählen. Bei der Überlagerung werden die Linien mit einem gemeinsamen X-Achsen-Beginn gezeigt, sodass sie parallel laufen, während bei der Sequenz die Linien mit ihrem jeweiligen X-Achsen-Beginn dargestellt werden. Wenn die Daten aufeinanderfolgend sind (z. B. Segment 1 endet um 20:44 Uhr und Segment 2 startet um 20:45 Uhr), werden die Zeilen nacheinander dargestellt. |

## Standardansicht

![Standardansicht](assets/mpts_default_view.png)

## Panel-Ausgabe {#Output}

Das Panel „Verbrachte Zeit bei der Medienwiedergabe“ gibt ein Liniendiagramm und zusammenfassende Zahlen zurück, die Details zur maximalen Wiedergabedauer, minimalen Wiedergabedauer und/oder der Summe der Wiedergabedauer enthalten. Oben im Bedienfeld wird eine Zusammenfassungszeile angezeigt, die Sie an die ausgewählten Bedienfeldeinstellungen erinnert.

Sie können das Bedienfeld jederzeit bearbeiten oder erneut erstellen, indem Sie oben rechts auf den Stift zum Bearbeiten klicken.

Wenn Sie Serienaufschlüsselung ausgewählt haben, wird für jeden der folgenden Punkte eine Zeile im Liniendiagramm und eine Zusammenfassungsnummer angezeigt:

![Ausgabe der verbrachten Zeit bei der Medienwiedergabe](assets/mpts_outputs1.png)

### Datenquelle

Die einzige Metrik, die in diesem Panel verwendet werden kann, ist „Wiedergabedauer“.

| Metrik | Beschreibung |
|---|---|
| Wiedergabedauer | `hours:minutes:seconds` (oder `minutes`) des Inhalts, der während der ausgewählten Granularität betrachtet wurde, einschließlich Pausen, Pufferung und der Zeit bis zum Start. |

## Häufig gestellte Fragen (FAQ)

| Frage | Antwort |
|---|---|
| Wo ist die Freiformtabelle? Wie kann ich die Datenquelle anzeigen? | Die Freiformtabelle ist in dieser Ansicht nicht verfügbar. Sie können die Datenquelle herunterladen, indem Sie mit der rechten Maustaste auf das Liniendiagramm klicken und die CSV-Datei herunterladen. |
| Warum hat sich meine Granularität verändert? | Diese Visualisierung ist auf 1440 Datenzeilen beschränkt (z. B. 24 Stunden bei einer Granularität auf Minutenebene). Wenn die Kombination aus Datumsbereich und Granularität mehr als 1440 Zeilen ergibt, wird die Granularität automatisch aktualisiert, um den vollständigen Datumsbereich zu erfassen. <p>Wenn Sie von einem größeren auf einen kleineren Datumsbereich wechseln, wird die Granularität auf das niedrigste zulässige Detail aktualisiert, sobald der Datumsbereich geändert wird. Um eine höhere Granularität zu sehen, bearbeiten Sie das Bedienfeld und erstellen Sie es erneut.</p> |
| Wie vergleiche ich Videonamen, Segmente, Inhaltstypen usw.? | Um diese in einer einzigen Visualisierung zu vergleichen, ziehen Sie Segmente, Dimensionen oder bestimmte Dimensionselemente in den Filter für die Aufschlüsselung von Serien. Die Ansicht ist auf 10 Aufschlüsselungen beschränkt. Um mehr als 10 ansehen zu können, müssen Sie mehrere Bedienfelder verwenden. |
| Wie vergleiche ich Datumsbereiche? | Um Datumsbereiche in einer einzigen Visualisierung zu vergleichen, verwenden Sie die Serienaufschlüsselungen, indem Sie zwei oder mehr Datumsbereiche in das Panel ziehen. Diese Datumsbereiche setzen den Datumsbereich des Bedienfelds außer Kraft. |
| Wie ändere ich den Visualisierungstyp? | Dieses Bedienfeld ermöglicht nur die Linienvisualisierung für die Zeitreihen. |
| Kann ich die Anomalieerkennung ausführen? | Nein. Die Anomalieerkennung ist für dieses Panel nicht verfügbar. |
