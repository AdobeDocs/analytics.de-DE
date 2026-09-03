---
description: Aktivieren Sie Dimensionen, damit Activity Map Daten erfassen kann.
title: Activity Map – Berichterstattung
feature: Admin Tools
exl-id: 9300c12e-3ade-4850-8a22-cba61b35ca67
TQID: https://experienceleague.adobe.com/GiBhdUMAX5P9zxxDAVUZPcaeKpnezKvDn3MB0g95DH0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: c153fd90-23e1-4614-81d3-3cc7571227f7id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: ef60b66e-5984-4336-ba72-6d978b1b6f87
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 31%

---

# Activity Map – Berichterstattung

Ermöglicht die Aktivierung von Dimensionen zur Verwendung mit [Activity Map](/help/analyze/activity-map/overview.md).

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Report Suite auswählen > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Activity Map]** > **[!UICONTROL Activity Map-Reporting]**

Dieser Abschnitt der Dokumentation konzentriert sich auf die Aktivierung von Dimensionen, die Activity Map verwendet. Weitere Informationen über die Überlagerung, ](/help/analyze/activity-map/overview.md) Implementierungsvariablen und Dimensionen finden Sie unter [Übersicht über Activity Map .

Wenn Sie auf die Schaltfläche **[!UICONTROL Activity Map-Berichte aktivieren]** klicken, werden die folgenden Dimensionen erstellt:

* [[!UICONTROL Activity Map-Link]](/help/components/dimensions/activity-map-link.md): Der Link-Name, auf den geklickt wurde.
* [[!UICONTROL Activity Map-Region]](/help/components/dimensions/activity-map-region.md): Der Name der Region, auf die geklickt wurde.
* [[!UICONTROL Activity Map-Seite]](/help/components/dimensions/activity-map-page.md): Der Name der Seite zum Zeitpunkt des Klickens auf den Link.
* [[!UICONTROL Activity Map-Link nach Region]](/help/components/dimensions/activity-map-link-by-region.md): Ein verketteter Wert aus Activity Map-Link und Activity Map-Region.

Nach der Aktivierung kann Ihre Implementierung mit dem Senden von Daten an diese Dimensionen zur Verwendung in [Analysis Workspace](/help/analyze/analysis-workspace/home.md) und der [Browser-Erweiterungs-Überlagerung](/help/analyze/activity-map/overlay/overview.md) beginnen.

>[!NOTE]
>
>Wenn Sie Activity Map für eine Report Suite aktivieren, wird es dauerhaft aktiviert, ohne dass Sie es später deaktivieren können.
