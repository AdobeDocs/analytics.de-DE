---
description: Beschreibt, wie Report Builder Pfade- und Fallout-Berichte unterstützt und wie sich die Implementierung von Reports & Analytics unterscheidet.
title: Pfad- und Pfad-Fallout-Berichte in Report Builder
feature: Report Builder
role: User, Admin
exl-id: 211b0e76-2895-401d-a5a5-73e459a486e2
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 83%

---

# Pfad- und Pfad-Fallout-Berichte in Report Builder

{{legacy-arb}}

Beschreibt, wie Report Builder Pfade- und Fallout-Berichte unterstützt und wie sich die Implementierung von Reports &amp; Analytics (jetzt eingestellt) unterscheidet.

| Pfadberichtname in Reports &amp; Analytics (Pfade > Dimension >) | Unterstützt in Report Builder? |
|--- |--- |
| Fluss der nächsten/vorherigen Dimension | Ist nicht als eigenständiger Bericht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Nächste/Vorherige Dimension | Ist nicht als eigenständiger Bericht verfügbar. Kann mit einem Pfadbericht und mithilfe eines Filters reproduziert werden. |
| Fallout | Als eigenständiger Bericht unterstützt und bereitgestellt (Pfade > Dimension > Dimension Fallout). |
| Vollständige Pfade | Nicht unterstützt. |
| PathFinder | Ist nicht als eigenständiger Bericht verfügbar. Kann als Pfadbericht mithilfe eines Filters reproduziert werden. |
| Pfadlänge | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse > Dimensionszusammenfassung | Ist nicht als eigenständiger Bericht verfügbar. Kann mit mehreren Anforderungen bei der Pfaddimension und mithilfe eines Filters reproduziert werden. |
| Seitenanalyse > Neuladungen | Ist nicht als eigenständiger Bericht verfügbar. Kann mit einem Dimensionsbericht mithilfe der Metrik „Neuladungen“ reproduziert werden. |
| Seitenanalyse > Dimension „Tiefe“ | Wird nur für die Seitendimension unterstützt. |
| Seitenanalyse > Besuchszeit für Dimension | Nicht unterstützt. |
| Einstiege und Ausstiege > Entrypages | Ist nicht als eigenständiger Bericht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters „Einstiegs-Site“ reproduziert werden. |
| Einstiege und Ausstiege > Ursprüngliche Entrypages | Wird nur für die Seitendimension unterstützt. |
| Einstiege und Ausstiege > Einzelseitenbesuche | Ist nicht als eigenständiger Bericht verfügbar. Kann als Pfadbericht mithilfe eines vordefinierten Filters reproduziert werden. |
| Einstiege und Ausstiege > Dimension „Ausstieg“ | Ist nicht als eigenständiger Bericht verfügbar. Kann als Pfadbericht mithilfe des vordefinierten Filters „Ausstiegs-Site“ reproduziert werden. |
