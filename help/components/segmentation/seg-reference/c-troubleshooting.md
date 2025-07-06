---
description: Erfahren Sie, wie Sie Probleme im Zusammenhang mit Segmenten beheben.
title: Fehlerbehebung
feature: Segmentation
exl-id: ca51110e-1ba7-4182-b5b2-baf9b0c017af
source-git-commit: 35f2812c1a1a4eed090e04d67014fcebf88a80ec
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 42%

---

# Fehlerbehebung

In diesem Artikel werden einige häufige Probleme mit Segmenten und deren Behebung aufgeführt.

<!-- Looks like this is not part anymore of the current UI.

## Error: "Incompatible elements in this segment" {#incompatible}

This error occurs when you try to save a segment in the Data Warehouse folder where the segment contains elements not compatible with Data Warehouse. To resolve this error, do one of two things:

* Save the segment in a different folder 
* Remove or change the incompatible portions of the segment.

-->

## Warum gibt mein Segment überhaupt keine Daten zurück? {#no-data}

Mögliche Gründe:

* Umgekehrte Verschachtelung - z. B. Verschachteln eines ![User](/help/assets/icons/User.svg)**[!UICONTROL Visitor]**-Containers unter einem ![Visit](/help/assets/icons/Visit.svg) **[!UICONTROL Visit]**-Container.
* Der Bericht unterstützt keine Segmentierung.
* Es stimmen keine Daten mit den Segmentierungskriterien überein.

## Warum kann ich das Segment, das ich erstellt habe, nicht im Segment-Manager sehen? {#invisible}

Mögliche Gründe:

* Einige Dimensionen sind nur in Data Warehouse und nicht im Segment-Manager verfügbar.
* Das Segment ist nur für eine bestimmte Report Suite aktiviert.
* Ein freigegebenes Segment wurde möglicherweise von einem anderen Benutzer gelöscht.
* Segmente konnten aufgrund eines Problems mit dem Rechenzentrum oder dem Browser-Cache nicht geladen werden.
* Das Segment wurde nicht gespeichert.
* Die IP-Adresse ist möglicherweise auf Seiten des Benutzers gesperrt.

## Warum sind die Daten, die nach der Anwendung eines Segments angezeigt werden, falsch? {#page-data}

Mögliche Gründe:

* Regeln oder Operatoren sind für das erforderliche Ergebnis falsch.
* Falsche Verwendung von Containern im Segment.
* Traffic-Variablen, die zur Segmentierung verwendet werden, sind nicht richtig eingestellt oder abgelaufen.
