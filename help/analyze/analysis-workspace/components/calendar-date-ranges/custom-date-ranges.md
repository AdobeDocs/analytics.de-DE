---
description: Erstellen Sie benutzerdefinierte Datumsbereiche in Analysis Workspace und speichern Sie sie als Zeitkomponenten.
keywords: Analysis Workspace
title: Erstellen von benutzerdefinierten Datumsbereichen
feature: Date Ranges
role: User, Admin
exl-id: 586bb120-3f20-452c-9867-0b93d2e794bc
source-git-commit: 1281bdc569c9ebc5d8daa151b19dc21710633eab
workflow-type: ht
source-wordcount: '438'
ht-degree: 100%

---

# Erstellen von benutzerdefinierten Datumsbereichen

Erstellen Sie benutzerdefinierte Datumsbereiche in Analysis Workspace und speichern Sie sie als Zeitkomponenten.

Informationen zum Hinzufügen vorhandener Datumsbereiche zu einem Projekt finden Sie in der [Übersicht über Kalender und Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md).

So erstellen Sie einen benutzerdefinierten Datumsbereich:

1. Wählen Sie in Adobe Analytics die Option **[!UICONTROL Komponenten]** > **[!UICONTROL Datumsbereiche]** aus.

   ![Seite „Datumsbereich“](assets/date-ranges.png)

1. Wählen Sie [!UICONTROL **Neuen Datumsbereich erstellen**] aus.

1. Geben Sie im Datumsbereichsgenerator die folgenden Informationen an:

   | Option | Beschreibung |
   |---------|----------|
   | [!UICONTROL **Titel**] | Der Titel des Datumsbereichs, wie er angezeigt wird, wenn er von Benutzenden in Analysis Workspace ausgewählt wird. |
   | [!UICONTROL **Beschreibung**] | Eine Beschreibung für den Datumsbereich. |
   | [!UICONTROL **Tags**] | Alle Tags, die auf den Datumsbereich angewendet werden sollen. |
   | [!UICONTROL **Datumsbereich**] | Hier können Sie einen benutzerdefinierten Datumsbereich auswählen. Standardmäßig sind die letzten 30 Tage ausgewählt. |
   | [!UICONTROL **Voreinstellung**] | Sie können aus einer Liste voreingestellter Datumsbereiche auswählen, beispielsweise [!UICONTROL **Gestern**], [!UICONTROL **Letzte 7 Tage**], [!UICONTROL **Letzte 30 Tage**] usw. |
   | [!UICONTROL **Startzeit**] | Die Tageszeit, zu der der Datumsbereich beginnt. |
   | [!UICONTROL **Endzeit**] | Die Tageszeit, zu der der Datumsbereich endet. |
   | [!UICONTROL **Verwenden von rollierenden Daten**] | Mithilfe rollierender Daten können Sie einen dynamischen Bericht generieren, der zum Zeitpunkt seiner Ausführung einen bestimmten Zeitraum voraus oder zurück umfasst. Wenn Sie zum Beispiel einen Bericht zu allen Bestellungen haben möchten, die im letzten Monat aufgegeben wurden (wobei sich „Letzter Monat“ auf das Feld „Erstellungsdatum“ bezieht), und diesen Bericht dann im Dezember ausführen, würden Ihnen alle Bestellungen angezeigt, die im November aufgegeben wurden. Führen Sie den gleichen Bericht im Januar aus, werden Ihnen die Bestellungen aus dem Dezember angezeigt.<ul><li>**[!UICONTROL Datumsvorschau]**: Gibt an, welchen Zeitraum der rollierende Kalender umfasst.</li><li>**[!UICONTROL Start]**: Sie können zwischen den folgenden Optionen wählen: „Aktueller Tag“, „Aktuelle Woche“, „Aktueller Monat“, „Aktuelles Quartal“ und „Aktuelles Jahr“.</li><li>**[!UICONTROL Ende]**: Sie können zwischen den folgenden Optionen wählen: „Aktueller Tag“, „Aktuelle Woche“, „Aktueller Monat“, „Aktuelles Quartal“ und „Aktuelles Jahr“.</li></ul><br>Standardmäßig ausgewählt. |

1. Wählen Sie [!UICONTROL **Speichern**] aus.

## Beispiel: Datumsbereich für „Vor zwei Monaten“ {#section_C4109C57CB444BB2A79CC8082BD67294}

Der folgende benutzerdefinierte Datumsbereich zeigt den Bereich vor zwei Monaten mit einer Visualisierung der Zusammenfassungsänderung, die eine Trend-Entwicklung anzeigt.

![](assets/date-range-two-months-ago.png)

Der benutzerdefinierte Datumsbereich wird in Ihrem Projekt oben auf dem Komponentenbereich für den [!UICONTROL Datumsbereich] angezeigt:

![](assets/date-range-panel-two-months-ago.png)

Sie können diesen benutzerdefinierten Datumsbereich auf eine Spalte neben einem benutzerdefinierten, monatlichen rollierenden Datumsbereich ziehen und die Voreinstellung für den letzten Monat für den Vergleich nutzen. Fügen Sie eine Visualisierung der Sammeländerung hinzu und wählen Sie die Gesamtsummen der einzelnen Spalten aus, um eine Trendentwicklung zu zeigen:

![](assets/date-range-two-months-table.png)

## Beispiel: Verwenden eines rollierenden 7-Tage-Datumsbereichs {#section_7EF63B2E9FF54D2E9144C4F76956A8DD}

Sie können einen Datumsbereich erstellen, der ein rollierendes Zeitfenster von 7 Tagen festlegt, das zurückliegend vor einer Woche in der Vergangenheit endet:

![](assets/create_date_range.png)

Verwenden Sie *`rolling daily`*.

* Die Starteinstellung lautet *`current day minus 6 days`*.

* Die Endeinstellung lautet *`current day minus 7 days`*.

Dieser Datumsbereich kann eine Komponente sein, die Sie auf eine beliebige Freiformtabelle ziehen können.
