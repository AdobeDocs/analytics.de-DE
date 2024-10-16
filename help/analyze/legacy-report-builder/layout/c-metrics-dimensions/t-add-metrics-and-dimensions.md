---
description: Erfahren Sie mehr über die Schritte zum Hinzufügen von Metriken und Dimensionen zu einer Anforderung.
title: Hinzufügen von Metriken und Dimensionen
uuid: 588ce96b-3a2d-42b7-8a8e-7e6f448a0115
feature: Report Builder
role: User, Admin
exl-id: d4e36b69-b5aa-43e5-b394-3b6d93143f15
source-git-commit: 12d048b42c6a61e03dbbe73acb9d34df3e37693c
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 38%

---

# Metriken und Dimensionen hinzufügen

Schritte zum Hinzufügen von Metriken und Dimensionen zu einer Anforderung.

1. Verwenden Sie das Formular [!UICONTROL Anforderungs-Assistent: Schritt 1] , um die Datenanforderung zu erstellen.](/help/analyze/legacy-report-builder/data-requests/data-requests.md) Klicken Sie dann auf **[!UICONTROL Weiter]**.[
1. Doppelklicken Sie im Formular [!UICONTROL Anforderungs-Assistent: Schritt 2] auf Metriken oder ziehen Sie sie an die gewünschte Position.

   ![Screenshot mit Anforderungs-Assistent: Schritt 2 mit einem Pfeil, der von der Metrikliste zum gewünschten Seitenansichtsabschnitt zeigt.](assets/adding_metrics.png)

   Wenn Sie Metriken hinzufügen, werden sie nicht aus der Registerkarte [!UICONTROL Metriken] entfernt, da Metriken innerhalb einer Anforderung mehrfach verwendet werden können. Beispielsweise kann die Zwischensumme einer Metrik neben jedem Wert angezeigt werden. Allerdings ändert sich die Liste der verfügbaren Metriken jedes Mal, wenn Sie eine Dimension hinzufügen oder entfernen.

   Metriken können nur im Abschnitt [!UICONTROL Metriken] des Layoutbereichs hinzugefügt werden. Metriken werden dem Layout [!UICONTROL Spaltenbezeichnung] als [!UICONTROL Metrik-Überschrift] hinzugefügt. Wenn Sie eine [!UICONTROL Metrik-Überschrift] aus dem [!UICONTROL Spalten-Layout] in das [!UICONTROL Zeilen-Layout] verschieben, wird sie dort angezeigt und die zugehörige Metrik wird für die Aufschlüsselung verwendet.

   Beachten Sie, dass auf der Registerkarte „Metriken“ direkt über der Metrikenliste eine Suchleiste angezeigt wird.

   ![ Screenshot mit der Suchleiste &quot;Metriken&quot;.](assets/search_bar_metric.png)

## Richtlinien

Beachten Sie beim Hinzufügen von Metriken und Dimensionen die folgenden Richtlinien.

* Wenn Sie einen Suchbegriff eingeben, wird die Liste automatisch aktualisiert, um Metriken anzuzeigen, deren Titel mit dem Suchbegriff übereinstimmen.
* Die Übereinstimmung unterscheidet nicht zwischen Groß- und Kleinschreibung und entspricht einer *contains* -Suche.
* Suchen nach vollständigen Wörtern und anderen speziellen Suchmarkierungen (beginnt mit, endet mit, AND, OR usw.) werden nicht unterstützt.

Der Suchbegriff wird gelöscht, wenn Sie den Anforderungs-Assistenten beenden, wenn Sie auf [!UICONTROL Beenden] oder [!UICONTROL Abbrechen] klicken, oder zu Anforderungs-Assistent: Schritt 1 zurückkehren oder die Metrikkategorie ändern.

Der Suchbegriff wird nicht gelöscht:

* Wenn Sie ein Metrikelement per Drag-and-Drop aus der Liste ziehen (oder doppelklicken), wird es zum Metrikbereich Pivot-Layout/Benutzerdefiniertes Layout hinzugefügt.
* Wenn Sie ein oder mehrere Metrikelemente aus dem Metrikbereich Pivot-Layout/Benutzerdefiniertes Layout entfernen.
* Wenn Sie auf die Registerkarte Dimension klicken, kehren Sie zur Registerkarte Metrik zurück.
* Wenn Sie andere Unterformulare (modale oder modelle) aufrufen, kehrt dieser beim Beenden zum Anforderungs-Assistenten Schritt 2 zurück. Beispiele für diese Formulare:

   * Formulare für Dimensionsfilter
   * Formulare für die Datumsbereichformatierung
   * Formulare für Formatoptionen
   * Formulare für das Voranstellen/Anhängen von Text
   * Formulare für das Festlegen des Ausgabebereichs

## Anforderung nach Metrik sortieren

Sie können eine Anforderung optional nach Metrik sortieren.

So sortieren Sie eine Anforderung nach Metrik

1. Klicken Sie auf die Metrikbezeichnung.
1. Dimensionen hinzufügen. Dimensionen werden auf die gleiche Weise wie Metriken hinzugefügt. Siehe Schritte 1 und 2 oben.

   Auf der Registerkarte [!UICONTROL Dimensionen] zeigt das System Dimensionen an, die aufgeschlüsselt sind oder die eine Classification des Basisberichts darstellen, den Sie unter [!UICONTROL Anforderungs-Assistent: Schritt 1] auswählen, sowie die Konfiguration der Report Suite. Wenn Sie eine Dimension in das Layout-Raster ziehen, wird sie aus der Strukturansicht entfernt und die Liste der verfügbaren Dimensionen neu berechnet.

   Die Dimension [!UICONTROL Datum] wird automatisch hinzugefügt. Die verfügbaren Datumsdimensionen hängen von der im Dialogfeld [!UICONTROL Anforderungs-Assistent: Schritt 1] gewählten Granularität ab. Gültige Werte sind:

   * Stunde
   * Tag
   * Woche
   * Monat
   * Jahr
   * Datumsbereich (wenn keine Granularität angegeben ist)

1. Ändern Sie Metriken und Dimensionen, indem Sie [Formatoptionen](/help/analyze/legacy-report-builder/layout/t-format-display-headers.md) und Filter konfigurieren.
1. Klicken Sie auf **[!UICONTROL Fertigstellen]**. 
Im folgenden Beispiel gehören die Dimensionen zur Metrik [!UICONTROL Seite]. Die Dimension [!UICONTROL Referrerdomäne] erstellt einen Detailbericht zwischen [!UICONTROL Seite] und [!UICONTROL Referrerdomäne]. Die Registerkarte [!UICONTROL Dimension] wird nur mit Dimensionen aktualisiert, die für einen Detailbericht verwenden können.

   ![ Screenshot mit den Dimensionen, die sich auf die Metrik beziehen.](assets/page_pageview_02.png)
