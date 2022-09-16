---
title: Verwalten von Anmerkungen
description: Verwalten von Anmerkungen in Workspace.
role: User, Admin
feature: Annotations
exl-id: 37a538cc-9ea7-4cb1-8ee8-e8e474ad5b08
source-git-commit: 20ab0e9728969c4cc11227a1255e41e3d1a1540f
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 100%

---

# Verwalten von Anmerkungen

Die Anmerkungsverwaltung ([!UICONTROL Komponenten] > [!UICONTROL Anmerkungen]) bietet viele Möglichkeiten zum Verwalten von Anmerkungen, z. B. Freigeben, Filtern, Markieren, Genehmigen, Kopieren, Löschen und Markieren als Favorit.

Die [!UICONTROL Anmerkungsverwaltung] zeigt Ihnen alle Anmerkungen an, die Ihnen gehören und für alle Ihre Projekte gelten und die für Sie freigegeben wurden.

>[!NOTE]
>
>[!UICONTROL Anmerkungen], die Sie nur für ein bestimmtes Projekt erstellt haben, werden nicht in der Anmerkungsverwaltung angezeigt.

## Benutzeroberfläche der Anmerkungsverwaltung

![](assets/annotation-mgr.png)

| UI-Element | Beschreibung |
| --- | --- | 
| [!UICONTROL Titel und Beschreibung] | Werden durch den Anmerkungsgenerator bereitgestellt. Klicken Sie auf den Titel-Link, um den Titel und die Beschreibung zu bearbeiten. Dadurch gelangen Sie zurück zum Anmerkungsgenerator. |
| [!UICONTROL Report Suite] | Die Report Suite(s), für die diese Anmerkung gilt. |
| [!UICONTROL Inhaber] | Zeigt an, wer Inhaber der Anmerkung ist. Wenn Sie kein Administrator sind, können Sie nur Anmerkungen sehen, deren Inhaber Sie sind, sowie Anmerkungen, die für Sie freigegeben wurden. |
| [!UICONTROL Angewendeter Datumsbereich] | Das Datum oder der Datumsbereich, für das bzw. den diese Anmerkung gilt. |
| [!UICONTROL Freigegeben für] | Listet auf, für wie viele Einzelpersonen oder Gruppen Sie die Anmerkung freigegeben haben. Klicken Sie hier, um weitere Details anzuzeigen. |
| [!UICONTROL Änderungsdatum] | Zeigt das Datum und die Uhrzeit der letzten Änderung der Anmerkung an. |

{style=&quot;table-layout:auto&quot;}

## Bearbeiten von Anmerkungen

Sie können eine Anmerkung bearbeiten, indem Sie Datumsbereiche, Farben oder den Umfang anpassen. Sie können ebenfalls festlegen, ob die Anmerkung für alle Report Suites oder Projekte gilt oder nicht. Anmerkungen können auf zwei Arten bearbeitet werden:

* Bewegen Sie in einem Liniendiagramm den Mauszeiger über die Anmerkung und klicken Sie im Popover auf das Stiftsymbol.

* Klicken Sie in der [!UICONTROL Anmerkungsverwaltung] auf den Titel der Anmerkung.

Beide Optionen führen Sie zurück in den [!UICONTROL Anmerkungsgenerator]. Dort können Sie die erforderlichen Anpassungen vornehmen und die neue Version speichern.

## Freigeben von Anmerkungen

Beachten Sie Folgendes beim Freigeben von Anmerkungen oder Arbeiten mit Anmerkungen, die für Sie freigegeben wurden:

* Angenommen, Sie erstellen ein Projekt mit nur projektbezogenen Anmerkungen und geben das Projekt dann für einen anderen Benutzer frei. Diese Anmerkungen werden angezeigt, können jedoch von niemandem bearbeitet oder gelöscht werden, für den Sie das Projekt freigeben.

* Wenn Sie eine Anmerkung speichern und direkt für einen Benutzer freigeben, kann dieser die Anmerkung nur bearbeiten/löschen, wenn er über Administratorrechte verfügt.

* Also: Wenn das Projekt für Sie freigegeben wurde, wird es nur in diesem Projekt angezeigt. Wenn die Anmerkung direkt für Sie freigegeben wird, wird sie in allen Projekten angezeigt, in denen diese Anmerkung angezeigt werden kann.

## Anmerkungen und Zeitzonen

Alle Anmerkungen werden mit einem Zeitstempel erstellt, jedoch ohne Stunden- oder Zeitzoneninformationen. Zum Zeitpunkt des Berichts wird immer die Zeitzone der Report Suite des Bedienfelds angewendet. Daher wird am 25. Dezember eine für Weihnachten erstellte Anmerkung erstellt - unabhängig davon, in welcher Report Suite-Zeitzone Sie sich befinden.

Ein weiteres Beispiel ist der Neujahrstag. Zu Beginn des neuen Jahres werden jede Stunde von einer anderen Zeitzone Feuerwerke ausgelöst. Um 22:00 Uhr US Mountain Time werden an der US-Ostküste Feuerwerke ausgelöst, weil es dort bereits 24:00 Uhr Eastern Time ist.

## Sonstige Aktionen mit Anmerkungen

Mit der Anmerkungsverwaltung können Administratoren Anmerkungen bearbeiten, hinzufügen, taggen, löschen, umbenennen, genehmigen, kopieren, exportieren und filtern. Dies ist für Nicht-Admin-Benutzer nicht sichtbar.

Wählen Sie einfach eine oder mehrere der Anmerkungen aus, und die Task-Leiste wird angezeigt.

| Aufgabe | Beschreibung |
| --- | --- |
| [!UICONTROL Hinzufügen] | Sie gelangen zum Anmerkungsgenerator, in dem Sie neue Anmerkungen erstellen können. |
| [!UICONTROL Tag] | Alle Benutzer können Tags für Anmerkungen erstellen und ein oder mehrere Tags auf eine Anmerkung anwenden. Sie sehen Tags jedoch nur für die Anmerkungen, deren Inhaber Sie sind. Welche Arten von Tags sollten Sie erstellen? Hier finden Sie einige Vorschläge für nützliche Tags:<ul><li>Auf Teamnamen basierende Tags wie Social Marketing, Mobile Marketing</li><li>Projekt-Tags (Analyse-Tags) wie Entrypage-Analyse</li><li>Kategorie-Tags: Männer, Region</li><li>Workflow-Tags: Kuratiert für (einen bestimmten Geschäftsbereich), Genehmigt</li></ul> |
| [!UICONTROL Löschen] | Durch das Löschen einer Anmerkung wird sie aus jedem Projekt in Ihrer Organisation entfernt. |
| [!UICONTROL Umbenennen] | Beim Umbenennen einer Anmerkung wird sie in allen Projekten umbenannt, auf die sie angewendet wurde. |
| [!UICONTROL Kopieren] | Erstellt eine eigenständige Kopie mit einer eigenen neuen Anmerkungs-ID, jedoch mit demselben Namen und derselben Definition. |
| [!UICONTROL In CSV exportieren] | Exportiert die Anmerkungsdefinition in eine CSV-Datei. |
| [!UICONTROL Filter] (linke Leiste) | Filtern Sie nach Tags, Report Suite, Inhabern und anderen Filtern („Meine“, „Genehmigt“, „Favoriten“, „Für mich freigegeben“ und „Alle anzeigen“). |

{style=&quot;table-layout:auto&quot;}
