---
description: Erläuterung der drei Produktkompatibilitätsoptionen.
title: Metrikkompatibilität
feature: Calculated Metrics
exl-id: 936d8139-7bbc-4de4-9e30-60ef5e12be08
source-git-commit: d9f95b12a43305cecff1190e6544334f3b48835d
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 50%

---

# Metrikkompatibilität {#metrics-compatibility}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_productcompatibility"
>title="Produktkompatibilität"
>abstract="„Einige wenige verfügbare Metrikkriterien sind nicht mit allen Adobe Analytics-Tools kompatibel. Tools, die mit der Metrik kompatibel sind, sind in dieser Liste aufgeführt. Um eine Metrik mit allen Adobe Analytics-Tools kompatibel zu machen, müssen Sie Ihre Kriterien bearbeiten."

In diesem Artikel werden die drei Produktkompatibilitätsoptionen erläutert.

Wenn Sie berechnete Metriken im Generator für berechnete Metriken erstellen, wird Ihre Metrik als mit mindestens einem Tool in Adobe Analytics kompatibel angezeigt. Beispiel: Analysis Workspace, Reports &amp; Analytics, Data Warehouse.


| Kompatibel mit | Beschreibung |
| --- | --- |
| Aktuelle Daten | Mit der Option [!UICONTROL Aktuelle Daten einschließen] in Adobe Analytics können Sie die jüngsten Analytics-Daten abrufen, und das häufig noch bevor die Daten vollständig verarbeitet und abgeschlossen sind. [!UICONTROL Aktuelle Daten] zeigt die meisten Metriken in Minutenschnelle an und liefert so verwertbare Daten für die rasche Entscheidungsfindung. [!UICONTROL Aktuelle Daten] unterstützt nur berechnete Metriken (mit Multiplikation, Division, Addition und Subtraktion). [!UICONTROL Aktuelle Daten] unterstützt keine erweiterten berechneten Metriken (mit Segmenten oder Funktionen). |
| Vollständig verarbeitete Daten | Daten, die vollständig verarbeitet wurden und Segmente und Classifications enthalten. Wenn Sie alle Metriken lieber erst dann anzeigen möchten, wenn die Daten vollständig verarbeitet sind, können Sie [!UICONTROL Aktuelle Daten] deaktivieren, indem Sie Benutzer aus der Gruppe „Benutzer der aktuellen Daten“ entfernen. |
| Marketing-Kanalberichte | Metriken mit Erstkontaktzuordnung sind nur mit Marketingkanalberichten kompatibel. |
