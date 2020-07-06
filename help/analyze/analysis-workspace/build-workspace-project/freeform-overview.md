---
description: 'null'
keywords: Analysis Workspace
title: Projekt erstellen – Übersicht
topic: Reports and analytics
uuid: a68be05d-f31e-4e6d-ad04-c784ecb0eb00
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 100%

---


# Projekt erstellen – Übersicht

**[!UICONTROL Analytics]** > **[!UICONTROL Workspace]**

Sie können ein stabiles Analytics-Projekt aus einer beliebigen Kombination von Visualisierungen, Berichtskomponenten und Datentabellen erstellen. Dadurch sind viele Funktionen des Tabellenerstellers aus der Ad Hoc Analysis auch in Analytics verfügbar.

Analysis Workspace bietet Ihnen komplett neue Möglichkeiten zum Vergleich und zur Aufschlüsselung von Daten. Sie können z. B. Rangberichte konfigurieren, sofortige iterative Änderungen an der Datenabfrage vornehmen und die Werte auf Berichtsebene aufrufen und damit arbeiten.

Die Abfrage erfolgt direkt an die Berichts-Engine. Sie können Änderungen inline durchführen, ohne andere Berichte aufzurufen, um Ihre Analyse zu erstellen. Die Ergebnisse sind sofort sichtbar, ohne Browseraktualisierung.

## Workspace -Seite mit Projektliste {#section_39AA007D7C384F4E869F842F1C7B11F8}

Wenn Sie **[!UICONTROL Analytics]** > **[!UICONTROL Workspace]** erstmalig aufrufen, werden auf der Seite alle Projekte aufgeführt, die Ihnen gehören oder zu denen Ihnen Zugriff gewährt wurde. Sie können diese Seite als Startseite für Adobe Analytics festlegen, indem Sie auf **[!UICONTROL Als Landingpage festlegen]** klicken. (Wenn die Option wie im unten stehenden Screenshot nicht angezeigt wird, ist die Seite bereits Ihre Landingpage.)

![](assets/sample-project.png)

Die Workspace -Seite mit Projektliste umfasst die folgenden Informationen:

| Element | Beschreibung |
|---|---|
| Projekt [Vorlagen](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md) | Sie können diese fertig ausgefüllten Projektvorlagen unverändert übernehmen oder an Ihre spezifischen Anforderungen anpassen (indem Sie beispielsweise Metriken oder Visualisierungen hinzufügen oder austauschen) und dann unter einem neuen Namen speichern. |
| [Neues Projekt erstellen](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md) | Klicken Sie auf diesen Link, um ein neues Projekt von Grund auf zu erstellen. |
| Projekte verwalten | Wenn Sie auf diesen Link klicken, wird der Projektkomponentenmanager aufgerufen (**[!UICONTROL Analytics]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Projekte]**). Dort sind all Ihre Projekte aufgeführt und Sie können Projekte taggen, freigeben, löschen, umbenennen, genehmigen, kopieren und in CSV exportieren. |
| Tutorials anzeigen | Sie gelangen zu den [YouTube-Videos für Analysis Workspace](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS). |
| Name | Name des Workspace-Projekts. |
| Erstellt von | Die Person, die dieses Projekt erstellt hat (entweder Sie oder eine Person, die das Projekt für Sie freigegeben hat). |
| Tags | Auf das Projekt angewendete Tags, entweder im Projektkomponentenmanager oder unter **[!UICONTROL Arbeitsbereich]** > **[!UICONTROL Projekt]** > **[!UICONTROL Projektinfo und Einstellungen]**. |
| Zuletzt geändert | Datum und Zeitpunkt der letzten Änderung des Projekts. |

## Projektinfo und Einstellungen {#section_63773D0B9E4543E88068ECECB9EEB4C6}

**[!UICONTROL Arbeitsbereich]** > **[!UICONTROL Projekt]** > **[!UICONTROL Projektinfo und Einstellungen]**

![](assets/projectinfo.png)

**[!UICONTROL Projektinfo und Einstellungen]** enthält auf der Projektebene befindliche Informationen über das derzeit aktive Projekt.

| Einstellung | Beschreibung |
|---|---|
| Projekt  Name | Der Name des Projekts. Sie können auf den Namen doppelklicken, um ihn zu bearbeiten. |
| Erstellt von | Name des Projektinhabers. |
| Zuletzt geändert | Das Datum, an dem die letzte Änderung an dem Projekt vorgenommen wurde. |
| Tags | Zeigt eine Liste aller Tags an, die auf ein Projekt angewendet wurden, um die Kategorisierung zu vereinfachen. Sie können Projekte beim Speichern auch taggen. Die Tags eines Projekts können Sie auf der Workspace-Landingpage in der Spalte [!UICONTROL Tags] einsehen. |
| Beschreibung | Eine Beschreibung hilft, den Zweck eines Projekts anzugeben. Sie können auf die Beschreibung doppelklicken, um sie zu bearbeiten. |
| Wiederholte Instanzen in Projekt zählen | Diese Einstellung legt fest, ob wiederholte Instanzen in Berichten gezählt werden sollen. Wenn mehrere sequentielle Werte für dieselbe Variable vorhanden sind, können Sie sie entweder als eine oder mehrere Instanzen der Variablen zählen. |
| Visualisierungsfarbschema | Sie können das in Workspace verwendete Farbschema ändern, indem Sie eine Farbe aus einer anderen Farbpalette auswählen oder Ihre eigene Palette festlegen. Diese Funktion betrifft vieles in Workspace, einschließlich der meisten Visualisierungen. |
| Dichte anzeigen | So können Sie mehr Daten auf dem Bildschirm anzeigen, indem Sie den vertikalen Abstand der linken Schiene, Freiformtabellen und Kohortentabellen reduzieren. |

## Menü „Projekte“ {#section_850CDFCB86A64EB0A0AD5B9E0FCB7013}

Die oberste Ebene des Menüs „Projekte“ sieht wie folgt aus:

![](assets/new-project-menus.png)

Die Untermenüs enthalten die folgenden Optionen.

>[!NOTE]
>
>Mit einem Sternchen (*) markierte Optionen werden nur bei **gespeicherten** Projekten angezeigt.

| Projekt | Vorlage | Einfügen | Komponenten | Freigabe | Hilfe |
|---|---|---|---|---|---|
| Neu | Rückgängig | Neues Bedienfeld | Neues Segment | Projekt freigeben | Videos |
| Öffnen | Leeren | Neues Freiformfeld | Neue Metrik | Projektverknüpfung abrufen* | Tastaturbefehle |
| Speichern | Alle löschen | Neues Bedienfeld für Segmentvergleich | Neuer Datumsbereich | Datei jetzt senden* | Hilfeforum |
| Speichern unter* |  | Neue Freiformtabelle | Neuer Warnhinweis | Datei planmäßig senden* |  |
| Als Landingpage festlegen* |  | Neue Zeile | Komponenten aktualisieren | Projekt kuratieren |  |
| Projekt aktualisieren |  | Neuer Balken |  |  |  |
| CSV herunterladen |  |  |  |  |  |
| PDF herunterladen* |  |  |  |  |  |
| Projektinfo und Einstellungen |  |  |  |  |  |

## Linke Leiste {#section_271295C26EC840ABB2A8E7EC0498B60E}

Die linke Leiste enthält 3 Symbole, über die Sie mit einem Klick auf Bedienfelder, [Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) und [Komponenten](/help/analyze/analysis-workspace/components/analysis-workspace-components.md) (Dimensionen, Metriken, Segmente, Datenbereiche) zugreifen können:

![](assets/panels.png) ![](assets/visualizations.png) ![](assets/components.png)

Zur Liste der in der linken Leiste verfügbaren Bedienfelder wurde ein **[!UICONTROL leeres Bedienfeld]** hinzugefügt. Um ein **neues Kohortenbedienfeld** zu erstellen, ziehen Sie eine Kohortentabellen-Visualisierung auf ein leeres Bedienfeld.
