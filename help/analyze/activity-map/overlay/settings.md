---
description: Ändern Sie die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen in Activity Map.
title: Konfigurieren von Einstellungen für Activity Map
uuid: 42a0309e-3efc-4506-989b-09b6fe419423
feature: Activity Map
role: User, Admin
exl-id: 65c9c690-81e0-4f0f-989d-586d247ed380
TQID: 'https://experienceleague.adobe.com/A83iKOXks62-m-PoHZpFuGIAJQEQ1HS1B-Mvqit3zVc'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
    internal-label: Dashboards
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: dcae653e-62c6-4cc8-84e6-ee110b848296
    internal-label: Visualizations
  - id: d40ce8ba-a8b5-4daa-9c46-16a4e57a022b
    internal-label: Activity Map
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 9a50beeb0aa51cf9f4baf212566947c14029ce8e
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 2%
---
# Activity Map-Einstellungen konfigurieren

Im Einstellungsbedienfeld von Activity Map können Sie die Einstellungen und Eigenschaften für alle Arten von Überlagerungsvisualisierungen ändern.

**[!UICONTROL Activity Map-Überlagerung]** > **Einstellungen anzeigen (Zahnradsymbol)** > **[!UICONTROL Einstellungen]**

## Allgemeine Einstellungen

Ändern Sie allgemeine Einstellungen für die Erweiterung und Überlagerungen.

* **[!UICONTROL Unternehmen]**: Zeigt die aktuelle Analytics-Organisation an, bei der Sie angemeldet sind.
* **[!UICONTROL Seitenname:]** den Namen der aktuellen Seite an.
* **[!UICONTROL Language]**: Ändert die Sprache für Activity Map-Erweiterungsbeschriftungen. Diese Einstellung ändert weder den Inhalt Ihrer Website noch die Link-Namen in Berichten. Zu den unterstützten Sprachen gehören Englisch, Französisch, Chinesisch (vereinfacht), Chinesisch (traditionell), Deutsch, Japanisch, Koreanisch, Spanisch und Portugiesisch.
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
* **[!UICONTROL Unterste ausschließen (%)]**: Filtern Sie den untersten Prozentsatz der Link-Änderungen heraus, um nur die Links mit ausreichend Daten anzuzeigen, um relevante Gewinne oder Verluste anzuzeigen. Der Prozentsatz wird anhand der Anzahl der Links auf dieser Seite berechnet. Wenn Sie beispielsweise die unteren 10 % einer Liste mit 200 Links herausfiltern, werden die unteren 20 Links herausgefiltert.
* **[!UICONTROL Daten automatisch aktualisieren]**: Bestimmt, ob die in der Überlagerung angezeigten Analytics-Daten automatisch aktualisiert werden, wenn ein neuer Zeitraum berechnet wird.
* **[!UICONTROL Zeitraum für automatische Aktualisierung]**: Wenn diese Option aktiviert ist, wird die Seite bei jedem neuen Datenabruf aktualisiert, damit die Links auf der Seite enger mit den erfassten Daten synchronisiert werden.
