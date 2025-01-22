---
description: Ändern Sie die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen in Activity Map.
title: Activity Map-Einstellungen konfigurieren
uuid: 42a0309e-3efc-4506-989b-09b6fe419423
feature: Activity Map
role: User, Admin
exl-id: 65c9c690-81e0-4f0f-989d-586d247ed380
source-git-commit: 13ad9d40ad74a8dffe05d899db54f4d77cbcc34c
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 4%

---

# Activity Map-Einstellungen konfigurieren

Im Bedienfeld Activity Map-Einstellung können Sie die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen ändern.

**[!UICONTROL Activity Map-Überlagerung]** > **Einstellungen anzeigen (Zahnradsymbol)** > **[!UICONTROL Einstellungen]**

## Allgemeine Einstellungen

Ändern Sie allgemeine Einstellungen für die Erweiterung und Überlagerungen.

* **[!UICONTROL Unternehmen]**: Zeigt die aktuelle Analytics-Organisation an, bei der Sie angemeldet sind.
* **[!UICONTROL Seitenname:]** den Namen der aktuellen Seite an.
* **[!UICONTROL Language]**: Ändert die Sprache für das Activity Map von Erweiterungsbeschriftungen. Diese Einstellung ändert weder den Inhalt Ihrer Website noch die Link-Namen in Berichten. Zu den unterstützten Sprachen gehören Englisch, Französisch, Chinesisch (vereinfacht), Chinesisch (traditionell), Deutsch, Japanisch, Koreanisch, Spanisch und Portugiesisch.
* **[!UICONTROL Überlagerungen beschriften mit]**: Bestimmt, was der Blasen- oder Verlaufstext ist. Die Standardeinstellung ist [!UICONTROL Rang]. Zu den Optionen zählen: 
   * **[!UICONTROL Keine Beschriftung]**: Kein Text innerhalb der Beschriftungen, wodurch sie zu farbigen Feldern werden
   * **[!UICONTROL Wert]**: Zeigt die Anzahl der Link-Klicks ([Vorfälle](/help/components/metrics/occurrences.md))
   * **[!UICONTROL Prozent]**: Zeigt den Anteil der Link-Klicks im Vergleich zur Gesamtzahl der Link-Klicks auf der Seite an
   * **[!UICONTROL Rank]**: Der numerische Rang des Links nach der Anzahl der Link-Klicks.
* **[!UICONTROL Schriftgröße der Beschriftung]**: Bestimmt die Größe des Textes innerhalb der Blase oder des Verlaufs.
* **[!UICONTROL Verlaufsfarbe]**: Ermöglicht das Ändern der Verlaufsfarbe, wenn der Visualisierungstyp &quot;[!UICONTROL &quot; ].
* **[!UICONTROL Sprechblasenfarbe]**: Ermöglicht das Ändern der Sprechblasenfarbe, wenn der Visualisierungstyp &quot;[!UICONTROL &quot; ].
* **[!UICONTROL Farbverlauf basierend auf]**: Bestimmt, auf welcher Metrik die Farbintensität einer Relation basiert, wenn der Visualisierungstyp &quot;[!UICONTROL &quot; ].
   * **[!UICONTROL Top 30-Rangfolgen]**: Die Farbintensität für die 30 wichtigsten Links wird normalisiert.
   * **[!UICONTROL Absoluter Metrikwert]**: Die Farbintensität ist eine Funktion des absoluten Metrikwerts.
* **[!UICONTROL Verlaufstransparenz]**: Bestimmt die Transparenz von Verlaufsüberlagerungen, wenn der Visualisierungstyp &quot;[!UICONTROL &quot; ]. Mit diesem Schieberegler können Sie die Farbüberlagerung vollständig transparent, vollständig deckend oder irgendwo dazwischen machen.

## Standardeinstellungen

Einstellungen für die Standardansicht anpassen.

* **[!UICONTROL Dynamische Datenfilterung]**: Ermöglicht es Ihnen zu ändern, welche Links angezeigt werden.
   * **[!UICONTROL Top]**: Zeigt die beliebtesten Links an. Verwenden Sie die numerische Dropdown-Liste auf der rechten Seite, um die Anzahl der anzuzeigenden Top-Links zu bestimmen. Die Optionen umfassen 1, 10, 50 und 100.
   * **[!UICONTROL Unten]**: Zeigt die am wenigsten beliebten Links basierend auf der Dropdown-Liste Zahl an. Verwenden Sie die numerische Dropdown-Liste auf der rechten Seite, um die Anzahl der anzuzeigenden untersten Links zu bestimmen. Die Optionen umfassen 1, 10, 50 und 100.
   * **[!UICONTROL Alle Links]**: Wendet keine dynamische Datenfilterung an. Die numerische Dropdown-Liste gilt nicht, wenn diese Option ausgewählt ist.
* **[!UICONTROL Überlagerungen für Links ausblenden, die keine Treffer erhalten haben]**: Links auf der Seite mit null Link-Klicks zeigen keine Überlagerung an. Diese Links sind von der dynamischen Datenfilterung ausgeschlossen.

## Live-Einstellungen

* **[!UICONTROL Oben anzeigen]**: Zeigt die höchste Anzahl von Gewinnern oder Verlierern basierend auf der numerischen Dropdown-Liste auf der linken Seite an.
* **[!UICONTROL Unterste ausschließen (%)]**: Filtern Sie den untersten Prozentsatz der Link-Änderungen heraus, um nur die Links mit ausreichend Daten anzuzeigen, um relevante Gewinne oder Verluste anzuzeigen. Der Prozentsatz wird anhand der Anzahl der Links auf der Seite berechnet. Wenn Sie beispielsweise die unteren 10 % einer Liste mit 200 Links herausfiltern, werden die unteren 20 Links herausgefiltert.
* **[!UICONTROL Daten automatisch aktualisieren]**: Bestimmt, ob die in der Überlagerung angezeigten Analytics-Daten automatisch aktualisiert werden, wenn ein neuer Zeitraum berechnet wird.
* **[!UICONTROL Zeitraum für automatische Aktualisierung]**: Wenn diese Option aktiviert ist, wird die Seite bei jedem neuen Datenabruf aktualisiert, damit die Links auf der Seite enger mit den erfassten Daten synchronisiert werden.
