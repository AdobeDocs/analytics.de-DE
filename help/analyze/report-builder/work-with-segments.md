---
title: Verwenden von Segmenten in Report Builder in Adobe Analytics
description: Beschreibt die Verwendung von Segmenten in Report Builder für Adobe Analytics
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 2691fde0-59c6-45a7-80a5-8e5e221adce2
source-git-commit: 2cb8f72a37699aa45135c9d26686f93ee20f20d7
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 4%

---

# Arbeiten mit Segmenten in Report Builder

Segmente können angewendet werden, wenn Sie einen neuen Datenblock erstellen oder wenn Sie die Option **Datenblock bearbeiten** im Bedienfeld „Befehle“ auswählen.

## Anwenden von Segmenten auf einen Datenblock

Um ein Segment auf den gesamten Datenblock anzuwenden, doppelklicken Sie auf ein Segment oder ziehen Sie Filter aus der Komponentenliste in den Abschnitt Segmente der Tabelle.

## Segmente auf einzelne Metriken anwenden

Um Segmente auf einzelne Metriken anzuwenden, ziehen Sie ein Segment auf eine Metrik in der Tabelle. Sie können auch auf das Symbol **…** rechts neben einer Metrik im Tabellenbereich klicken und dann **[!UICONTROL Segmentmetrik]** auswählen. Um angewendete Segmente anzuzeigen, bewegen Sie den Mauszeiger über eine Metrik im Tabellenbereich oder wählen Sie sie aus. Metriken mit angewendeten Segmenten zeigen ein Filtersymbol an.

![Registerkarte „Segmente“ mit Metriken.](./assets/filter_by.png)

## Schnellbearbeitungssegmente

Sie können das Bedienfeld „Schnellbearbeitung“ verwenden, um Segmente für vorhandene Datenblöcke hinzuzufügen, zu entfernen oder zu ersetzen.

Wenn Sie einen Zellenbereich im Arbeitsblatt auswählen, wird der Link **[!UICONTROL Segmente]** im Bereich „Schnellbearbeitung“ eine zusammenfassende Liste der Segmente anzeigen, die von den in dieser Auswahl enthaltenen Datenblöcken verwendet werden.

So bearbeiten Sie Segmente über das Bedienfeld „Schnellbearbeitung“

1. Wählen Sie einen Zellenbereich aus einem oder mehreren Datenblöcken aus.

   ![Bedienfeld „Schnellbearbeitung“ für Segmente mit Segmentoptionen für Report Suites, Datumsbereich und Segmente.](./assets/select_multiple_dbs.png)

1. Klicken Sie auf den Link unter **[!UICONTROL Segmente]**, um das Bedienfeld „Schnellbearbeitung - Filter“ zu starten.

   ![Bedienfeld Segmente , das das Feld Segmente hinzufügen und die Listen Angewandte Segmente anzeigt.](./assets/quick_edit_filters.png)

### Segment hinzufügen oder entfernen

Mithilfe der Optionen „Hinzufügen“/„Entfernen“ können Sie Segmente hinzufügen oder entfernen.

1. Wählen Sie die **[!UICONTROL Hinzufügen/Entfernen]** im Bedienfeld „Schnellbearbeitungssegmente“ aus.

   Alle Segmente, die auf die ausgewählten Datenblöcke angewendet werden, werden im Bedienfeld „Schnellbearbeitungssegmente“ aufgeführt. Segmente, die auf alle Datenblöcke in der Auswahl angewendet werden, werden unter der Überschrift **[!UICONTROL Auf alle ausgewählten Datenblöcke angewendet]** aufgeführt. Segmente, die auf einige, aber nicht alle Datenblöcke angewendet werden, werden unter der Überschrift **[!UICONTROL Auf einen oder mehrere ausgewählte Datenblöcke angewendet]** aufgeführt.

   Wenn in den ausgewählten Datenblöcken mehrere Segmente vorhanden sind, können Sie mithilfe des Suchfelds **[!UICONTROL Filter hinzufügen]** nach bestimmten Segmenten suchen.

   ![Das Feld Segmente hinzufügen.](./assets/add_filter.png)

1. Fügen Sie Segmente hinzu, indem Sie Segmente aus dem Dropdown-Menü **[!UICONTROL Segment hinzufügen]** auswählen.

   Die Liste durchsuchbarer Segmente enthält alle Segmente, auf die die Report Suites zugreifen können, die in einem oder mehreren der ausgewählten Datenblöcke vorhanden sind, sowie alle Segmente, die in der Organisation global verfügbar sind.

   Beim Hinzufügen eines Segments wird das Segment auf alle Datenblöcke in der Auswahl angewendet.

1. Um Segmente zu entfernen, klicken Sie auf das Löschsymbol **x** rechts neben den Segmenten in der Liste **[!UICONTROL Angewendete Segmente]**.

1. Klicken Sie auf **[!UICONTROL Anwenden]**, um Änderungen zu speichern und zum Hub-Bedienfeld zurückzukehren.

   Report Builder zeigt eine Meldung zur Bestätigung der angewendeten Segmentänderungen an.

### Segment ersetzen

Sie können ein vorhandenes Segment durch ein anderes Segment ersetzen, um die Segmentierung der Daten zu ändern.

1. Wählen Sie die **[!UICONTROL Ersetzen]** im Bedienfeld „Schnellbearbeitungssegment“ aus.

   ![Wählen Sie die Registerkarte Ersetzen aus.](./assets/replace_filter.png)

1. Suchen Sie mithilfe **[!UICONTROL Suchfelds]** Suchliste“ nach bestimmten Segmenten.

1. Wählen Sie ein oder mehrere Segmente aus, die Sie ersetzen möchten.

1. Suchen Sie im Feld Ersetzen durch nach einem oder mehreren Segmenten.

   Wenn Sie einen Filter auswählen, wird dieser der Liste **[!UICONTROL Ersetzen durch]**... hinzugefügt.

1. Klicken Sie auf **[!UICONTROL Anwenden]**.

   Report Builder aktualisiert die Segmentliste entsprechend der Ersetzung.

### Definieren von Datenblocksegmenten aus einer Zelle

Datenblöcke können auf Segmente aus einer Zelle verweisen. Mehrere Datenblöcke können dieselbe Zelle für Segmente referenzieren, sodass Sie mühelos Segmente für mehrere Datenblöcke gleichzeitig wechseln können.

So wenden Sie Segmente aus einer Zelle an

1. Navigieren Sie entweder beim Erstellen oder Bearbeiten von Datenblöcken zu Schritt 2. Siehe [Erstellen eines Datenblocks](./create-a-data-block.md).
1. Klicken Sie auf **[!UICONTROL Segmente]**, um Filter zu definieren.
1. Klicken Sie **[!UICONTROL Segment aus Zelle erstellen]**.

   ![Segment aus Zellensymbol erstellen.](./assets/create-filter-from-cell.png)

1. Wählen Sie die Zelle aus, aus der die Datenblöcke auf ein Segment verweisen sollen.

1. Fügen Sie die Segmentauswahl hinzu, die Sie der Zelle hinzufügen möchten, indem Sie entweder auf das Segment doppelklicken oder es per Drag-and-Drop in den Abschnitt **[!UICONTROL Segmente enthalten]** ziehen.

   Hinweis: Für die jeweilige Zelle kann jeweils nur eine Auswahl ausgewählt werden.

   ![Das Fenster Segment aus Zelle hinzufügen , das die eingeschlossenen Filter anzeigt.](./assets/select-filters.png)

1. Klicken Sie auf **[!UICONTROL Anwenden]**, um die Referenzzelle zu erstellen.

1. Fügen Sie auf **[!UICONTROL Registerkarte]** die neu erstellten Referenzzellensegmente zu Ihrem Datenblock hinzu.

   ![Registerkarte „Segmente“ mit dem der Tabelle hinzugefügten Segment Sheet1!J1(All Data).](./assets/reference-cell-filter.png)

1. Klicken Sie auf **[!UICONTROL Fertig stellen]**.

   Jetzt kann diese Zelle von anderen Datenblöcken in ihren Segmenten referenziert werden. Um die Referenzzelle als Segment auf andere Datenblöcke anzuwenden, fügen Sie einfach den Zellenverweis auf der Registerkarte Segmente zu ihren Segmenten hinzu.

#### Verwenden der Referenzzelle zum Ändern von Datenblocksegmenten

1. Wählen Sie die Referenzzelle im Arbeitsblatt aus.

1. Klicken Sie auf den Link unter **[!UICONTROL Segmente aus Zelle]** im Menü Schnellbearbeitung.

   ![Segmente aus Zellenlink zeigen Blatt1!J1 (Alle Daten)](./assets/filters-from-cell-link.png)

1. Wählen Sie Ihr Segment aus dem Dropdown-Menü aus.

   ![Dropdown-Menü „Segmente“](./assets/filter-drop-down.png)

1. Klicken Sie auf **[!UICONTROL Anwenden]**.
