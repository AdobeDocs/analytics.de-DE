---
description: Erfahren Sie, wie Sie einer Anfrage Metriken und Dimensionen hinzufügen.
title: Hinzufügen von Metriken und Dimensionen
uuid: 588ce96b-3a2d-42b7-8a8e-7e6f448a0115
feature: Report Builder
role: User, Admin
exl-id: d4e36b69-b5aa-43e5-b394-3b6d93143f15
TQID: https://experienceleague.adobe.com/nKf59WLxvtYrcyR-mQ8oM41rUDLl3qpkwbujRDBV27A
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 585
ht-degree: 12%

---

# Metriken und Dimensionen hinzufügen

{{legacy-arb}}

Schritte zum Hinzufügen von Metriken und Dimensionen zu einer Anforderung.

1. Verwenden Sie das Formular [!UICONTROL Anforderungs-Assistent: Schritt 1], um [Datenanforderung erstellen](/help/analyze/legacy-report-builder/data-requests/data-requests.md) und klicken Sie dann auf **[!UICONTROL Weiter]**.
1. Doppelklicken Sie im [!UICONTROL Anforderungs-Assistenten: Schritt 2] auf Metriken oder ziehen Sie sie an die gewünschte Position.

   ![Screenshot mit dem Anforderungs-Assistenten: Schritt 2 mit einem Pfeil, der von der Metrikliste zum gewünschten Seitenansichtsabschnitt zeigt.](assets/adding_metrics.png)

   Wenn Sie Metriken hinzufügen, werden diese nicht aus der Registerkarte [!UICONTROL Metriken] entfernt, da Sie Metriken innerhalb einer Anfrage mehrmals anzeigen können. Beispielsweise kann die Zwischensumme einer Metrik neben jedem Wert angezeigt werden. Die Liste der verfügbaren Metriken ändert sich jedoch jedes Mal, wenn Sie eine Dimension hinzufügen oder entfernen.

   Metriken können nur im Abschnitt [!UICONTROL Metriken] des Layoutbereichs hinzugefügt werden. Metriken werden dem Layout [!UICONTROL Spaltenbeschriftung] als [!UICONTROL Metrikkopfzeile] hinzugefügt. Wenn Sie eine [!UICONTROL Metrik-Kopfzeile] von [!UICONTROL Spalten-Layout] in [!UICONTROL Zeilen-Layout] verschieben, wird sie dort angezeigt und als Metrik für die Aufschlüsselung verwendet.

   Beachten Sie, dass auf der Registerkarte Metriken direkt über der Metrikliste eine Suchleiste angezeigt wird.

   ![Screenshot mit der Suchleiste für Metriken.](assets/search_bar_metric.png)

## Richtlinien

Beachten Sie beim Hinzufügen von Metriken und Dimensionen die folgenden Richtlinien.

* Wenn Sie einen Suchbegriff eingeben, wird die Liste automatisch aktualisiert und zeigt Metriken an, deren Kennzeichnungen mit dem Suchbegriff übereinstimmen.
* Bei der Übereinstimmung wird nicht zwischen Groß- und Kleinschreibung unterschieden und sie entspricht einer *contains*-Suche.
* Vollwortsuchen und andere spezielle Suchkennzeichnungen (beginnt mit, endet mit, UND, ODER usw.) werden nicht unterstützt.

Der Suchbegriff wird gelöscht, wenn Sie den Anforderungs-Assistenten beenden, wenn Sie auf [!UICONTROL Beenden] oder [!UICONTROL Abbrechen] klicken, oder zurück zum Anforderungs-Assistenten zu Schritt 1 wechseln oder die Metrikkategorie ändern.

Der Suchbegriff wird nicht gelöscht:

* Wenn Sie ein Metrik-Element per Drag-and-Drop aus der Liste ziehen (oder darauf doppelklicken), wird es zum Bedienfeld „Pivot-Layout/Benutzerdefinierte Layout-Metriken“ hinzugefügt.
* Wenn Sie ein oder mehrere Metrikelemente aus dem Metrikbedienfeld Pivot-Layout/Benutzerdefiniertes Layout entfernen.
* Wenn Sie auf die Registerkarte Dimension klicken, kehren Sie dann zur Registerkarte Metrik zurück.
* Wenn Sie andere Teilformulare (modal oder moduslos) aufrufen, die beim Beenden zum Anforderungs-Assistenten von Schritt 2 zurückkehren. Beispiele für diese Formulare sind

   * Dimension Filter Forms
   * Datumsbereich-Formatierung Forms
   * Formulare für Formatoptionen
   * Textformular mit vorangestellten und aufgeschobenen Elementen
   * Formular für den Speicherort des Ausgabebereichs

## Sortieren einer Anfrage nach Metrik

Optional können Sie eine Anfrage nach Metrik sortieren.

So sortieren Sie eine Anfrage nach Metrik

1. Klicken Sie auf die Metrikbeschriftung.
1. Dimensionen hinzufügen. Fügen Sie Dimensionen auf die gleiche Weise hinzu wie Metriken. Siehe Schritte 1 und 2 oben.

   Auf der Registerkarte [!UICONTROL Dimensionen] zeigt das System Dimensionen an, die aufgeschlüsselt sind oder eine Klassifizierung eines Basisberichts darstellen, den Sie unter [!UICONTROL Anforderungs-Assistent: Schritt 1] und über die Konfiguration der Report Suite auswählen. Wenn Sie eine Dimension in die Layout-Raster ablegen, wird sie aus der Strukturansicht entfernt und berechnet die Liste der verbleibenden verfügbaren Dimensionen neu.

   Die Dimension [!UICONTROL Datum] wird automatisch hinzugefügt. Die verfügbaren Datumsdimensionen ändern sich je nach der ausgewählten Granularität im [!UICONTROL Anforderungs-Assistenten: Schritt 1]. Gültige Werte sind:

   * Stunde
   * Tag
   * Woche
   * Monat
   * Jahr
   * Datumsbereich (wenn keine Granularität angegeben ist)

1. Ändern Sie Metriken und Dimensionen, indem Sie [Formatoptionen](/help/analyze/legacy-report-builder/layout/t-format-display-headers.md) und Filter konfigurieren.
1. Klicken Sie auf **[!UICONTROL Fertigstellen]**.
Im folgenden Beispiel gehören die Dimensionen zur Metrik [!UICONTROL Seite]. Die Dimension [!UICONTROL Verweisende Domain] erstellt einen Aufschlüsselungsbericht zwischen [!UICONTROL Seite] und [!UICONTROL Verweisende Domain]. Die Registerkarte [!UICONTROL Dimension] wird nur mit Dimensionen aktualisiert, die Sie einem Aufschlüsselungsbericht hinzufügen können.

   ![Screenshot mit den Dimensionen, die sich auf die Metrik beziehen.](assets/page_pageview_02.png)
