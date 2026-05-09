---
description: Erläuterung der drei Produktkompatibilitätsoptionen.
title: Metrikkompatibilität
feature: Calculated Metrics
exl-id: 936d8139-7bbc-4de4-9e30-60ef5e12be08
source-git-commit: 035723a8a1dcdee96c9be9a2ee7a0b2e98a8f56e
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 57%

---

# Metrikkompatibilität {#metrics-compatibility}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_productcompatibility"
>title="Produktkompatibilität"
>abstract="Einige wenige verfügbare Metrikkriterien sind nicht mit allen Adobe Analytics-Tools kompatibel. Tools, die mit der Metrik kompatibel sind, sind in dieser Liste aufgeführt. Versuchen Sie Ihre Kriterien zu bearbeiten, damit die Metrik mit allen Adobe Analytics-Tools kompatibel ist."

In diesem Artikel werden die drei Produktkompatibilitätsoptionen erläutert.

Wenn Sie berechnete Metriken im Generator für berechnete Metriken erstellen, wird Ihre Metrik als mit einem oder mehreren Tools in Adobe Analytics kompatibel angezeigt.


| Kompatibel mit | Beschreibung |
| --- | --- |
| **[!UICONTROL Aktuelle Daten]** | Mit der Option [!UICONTROL Aktuelle Daten einschließen] in Adobe Analytics können Sie die jüngsten Analytics-Daten abrufen, und das häufig noch bevor die Daten vollständig verarbeitet und abgeschlossen sind. [!UICONTROL Aktuelle Daten] zeigt die meisten Metriken in Minutenschnelle an und liefert so verwertbare Daten für die rasche Entscheidungsfindung. [!UICONTROL Aktuelle Daten] unterstützt nur berechnete Metriken (mit Multiplikation, Division, Addition und Subtraktion). [!UICONTROL Aktuelle Daten] unterstützt keine erweiterten berechneten Metriken (mit Segmenten oder Funktionen). |
| **[!UICONTROL Vollständig verarbeitete]** | Daten, die vollständig verarbeitet sind und Segmente und Klassifizierungen enthalten. Wenn Sie alle Metriken lieber erst dann anzeigen möchten, wenn die Daten vollständig verarbeitet sind, können Sie [!UICONTROL Aktuelle Daten] deaktivieren, indem Sie Benutzer aus der Gruppe „Benutzer der aktuellen Daten“ entfernen. |
| **[!UICONTROL Berichte zu Marketing-Kanälen]** | Metriken mit Erstkontakt-Zuordnung sind nur mit Marketing-Kanal-Berichten kompatibel. |
