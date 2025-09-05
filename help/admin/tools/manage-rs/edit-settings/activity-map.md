---
description: Aktivieren Sie Dimensionen, damit Activity Map Daten erfassen kann.
title: Activity Map-Berichterstellung
feature: Admin Tools
exl-id: 9300c12e-3ade-4850-8a22-cba61b35ca67
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 3%

---

# Activity Map-Berichterstellung

Ermöglicht die Aktivierung von Dimensionen zur Verwendung mit [Activity Map](/help/analyze/activity-map/overview.md).

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map-Reporting]**

Dieser Abschnitt der Dokumentation konzentriert sich auf die Aktivierung von Dimensionen, die Activity Map verwendet. Weitere Informationen über die Überlagerung, [ Implementierungsvariablen und Dimensionen finden Sie unter ](/help/analyze/activity-map/overview.md)Übersicht über Activity Map .

Wenn Sie auf die Schaltfläche **[!UICONTROL Activity Map-Berichte aktivieren]** klicken, werden die folgenden Dimensionen erstellt:

* [[!UICONTROL Activity Map-Link]](/help/components/dimensions/activity-map-link.md): Der Link-Name, auf den geklickt wurde.
* [[!UICONTROL Activity Map-Region]](/help/components/dimensions/activity-map-region.md): Der Name der Region, auf die geklickt wurde.
* [[!UICONTROL Activity Map Page]](/help/components/dimensions/activity-map-page.md): Der Seitenname zum Zeitpunkt, an dem auf den Link geklickt wurde.
* [[!UICONTROL Activity Map-Link nach Region]](/help/components/dimensions/activity-map-link-by-region.md): Ein verketteter Wert von Activity Map Link und Activity Map-Region.

Nach der Aktivierung kann Ihre Implementierung mit dem Senden von Daten an diese Dimensionen zur Verwendung in [Analysis Workspace](/help/analyze/analysis-workspace/home.md) und der [Browser-Erweiterungs-Überlagerung](/help/analyze/activity-map/overlay/overview.md) beginnen.

>[!NOTE]
>
>Wenn Sie Activity Map für eine Report Suite aktivieren, wird es dauerhaft aktiviert, ohne dass Sie es später deaktivieren können.
