---
description: Im Standardmodus exportiert Analytics Daten aus der Activity Map in eine Datei mit durch Komma getrennten Werten (CSV).
title: Exportieren in CSV-Datei
uuid: dc6c50c0-57f7-45b8-a4cb-2092a21da529
feature: Activity Map
role: User, Admin
exl-id: b385abaf-6994-4a60-a78d-efa09f17b15f
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 100%

---

# Exportieren in CSV-Datei

Im Standardmodus exportiert Analytics Daten aus der Activity Map in eine Datei mit durch Komma getrennten Werten (CSV).

Als Benutzer müssen Sie eventuell Daten für Link-Klicks mit anderen Datenquellen zusammenführen oder andere Analysen (z. B. in Excel) durchführen. Durch den Export als CSV-Datei stehen Ihnen alle Activity Map-Daten für eine gegebene Seite in einem einfach zu verwendenden Format zur Verfügung. Sie können die für eine Seite generierten Analysedaten in einer CSV-Flatfile speichern. Dies ermöglicht Ihnen den Export des  Seitenberichts, [Seitenflussberichts](/help/analyze/activity-map/activitymap-page-flow.md) und der Daten zu den [Links auf der Seite](/help/analyze/activity-map/activitymap-links-report.md). Anschließend können Sie die Daten als Tabelle oder Textdatei anzeigen oder in ein anderes System importieren.

Klicken Sie auf das Exportsymbol in der Activity Map-Symbolleiste.

Activity Map generiert den Dateinamen anhand des Adobe Analytics-Seitennamens und fügt ein Datum sowie einen Zeitstempel an: Seitenname_DatumUhrzeit.csv. Diese Datei wird im standardmäßigen Downloadverzeichnis des entsprechenden Browsers gespeichert.

| Exportinformationen | Beschreibung |
|---|---|
| Seitenmetrikbericht | Seitenmetrikdaten aus Analytics, einschließlich der auf einer Seite verbrachten Zeit, Klicks auf die Seite und Seitenansichten insgesamt. |
| Seitendetailbericht | Informationen zum Seiteneinstieg und Seitenausstieg, wobei die vorherige Seite bei internem Einstieg oder externe Verweise angegeben werden, sowie Ausstiegsdaten. |
| Bericht zu Links auf Seite | Linkinformationen für eine bestimmte Seite im Standard- oder Livemodus. |
