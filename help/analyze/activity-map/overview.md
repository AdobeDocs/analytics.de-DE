---
description: Weisen Sie der Link-Aktivität mithilfe von visuellen Überlagerungen einen Rang zu, um die Interaktion der Zielgruppe mit Ihren Web-Seiten zu überwachen.
title: Activity Map – Überblick
feature: Activity Map
role: User, Admin
exl-id: 30a800f7-e2c8-443e-b5d4-36834ef0ba20
source-git-commit: a7670fcda3e8e6af0c036c8b263746e142278255
workflow-type: ht
source-wordcount: '623'
ht-degree: 100%

---

# Activity Map – Überblick

Adobe Analytics Activity Map ist eine Funktion in Adobe Analytics, die eine visuelle Darstellung der Benutzerinteraktion auf Web-Seiten und in Mobile Apps bietet. Sie ermöglicht es Marketing-Fachleuten sowie Analystinnen und Analysten, Benutzerinteraktionen wie Klicks und das Scroll-Verhalten nachzuverfolgen und zu analysieren. Activity Map erstellt Heatmaps und Überlagerungsberichte, die die beliebtesten Elemente auf einer Web-Seite anzeigen und Ihnen bei der Optimierung Ihrer digitalen Erlebnisse helfen.

Das Konzept der Activity Map besteht aus mehreren wichtigen Komponenten:

* **Report Suite-Einstellung**: Activity Map muss vor der Verwendung in der Report Suite aktiviert sein. Siehe [Activity Map-Reporting](/help/admin/tools/manage-rs/edit-settings/activity-map.md) in den Report Suite-Einstellungen.
* **Implementierung**: Die meisten Activity Map-Berichte sind vorkonfiguriert verfügbar. Einige Websites benötigen jedoch möglicherweise eine zusätzliche Implementierung, um das Linktracking optimal zu nutzen. Die folgenden Implementierungsvariablen sind verfügbar:
   * [`ActivityMap.linkExclusions`](/help/implement/vars/config-vars/activitymap-linkexclusions.md): Filtern von Klickdaten nach Link-Name.
   * [`ActivityMap.regionExclusions`](/help/implement/vars/config-vars/activitymap-regionexclusions.md): Filtern von Klickdaten nach Regionsname.
   * [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md): Ändern des Attributs, das die Dimension „Activity Map-Region“ ausfüllt.
   * [`ActivityMap.link`](/help/implement/vars/functions/activitymap-link.md): Anpassen der Logik, die Activity Map zum Ausfüllen der Dimension „Activity Map-Link“ verwendet.
   * [`ActivityMap.region`](/help/implement/vars/functions/activitymap-region.md): Anpassen der Logik, die Activity Map zum Ausfüllen der Dimension „Activity Map-Region“ verwendet.
* **Überlagerung**: Eine Browser-Erweiterung, mit der Sie Klickdaten auf Ihrer Website als Überlagerung anzeigen können. Weitere Informationen finden Sie unter [Schnittstelle für Activity Map-Erweiterung](overlay/overview.md). Diese Funktion ist nicht für Web SDK-Implementierungen verfügbar.
* **Dimensionen**: Zusätzlich zur Überlagerungserweiterung stellt Activity Map mehrere Dimensionen bereit, die Sie in Analysis Workspace verwenden können.
   * [Activity Map-Link](/help/components/dimensions/activity-map-link.md): Der Link-Name, auf den geklickt wurde.
   * [Activity Map-Region](/help/components/dimensions/activity-map-region.md): Der Name der Region, auf die geklickt wurde.
   * [Activity Map-Seite](/help/components/dimensions/activity-map-page.md): Der Name der Seite zum Zeitpunkt des Klickens auf den Link.
   * [Activity Map-Link nach Region](/help/components/dimensions/activity-map-link-by-region.md): Ein verketteter Wert aus Activity Map-Link und Activity Map-Region.

## Funktionen und Verbesserungen

* **Visualisierung der Benutzerinteraktion**: Activity Map bietet eine dynamische visuelle Darstellung des Benutzerverhaltens, und ermöglicht es Ihnen, genau zu sehen, wohin die Benutzenden klicken. Diese visuellen Daten erleichtern die Identifizierung von Mustern, Trends und Interessenbereichen. Auf dieser Grundlage können Sie fundierte Entscheidungen über das Design, die Platzierung von Inhalten und den Benutzerfluss treffen.

* **Heatmaps**: Activity Map erstellt Heatmaps, die Bereiche einer Web-Seite anzeigen, die am häufigsten angeklickt wurden oder mit denen am häufigsten interagiert wurde. Bei Heatmaps wird die Interaktionsstufe mit Farbcodierung dargestellt, sodass Sie Hotspots identifizieren und die Aufmerksamkeit auf Bereiche mit hoher Auswirkung richten können. Diese Informationen können für die Optimierung von Aktionsaufruf-Schaltflächen, Links, Formularen oder anderen interaktiven Elementen von unschätzbarem Wert sein.

* **Überlagerungsberichte**: Überlagerungsberichte in Activity Map bieten detaillierte Klickmetriken für bestimmte Elemente auf einer Web-Seite. Durch Kenntnis der Clickthrough-Raten und Interaktionsstufen einzelner Elemente können Sie ihre Design- und Inhaltsstrategien optimieren, um Benutzererlebnisse zu verbessern. Diese Funktion ist nicht für Web SDK-Implementierungen verfügbar.

* **Segmentanalyse**: Sie können das Benutzerverhalten basierend auf verschiedenen Segmenten analysieren, z. B. Traffic-Quellen, demografische Daten oder Personas. Durch die Segmentierung der Daten können Sie wertvolle Erkenntnisse zu bestimmten Benutzergruppen gewinnen, wodurch personalisierte Erlebnisse und zielgerichtete Marketing-Strategien ermöglicht werden.

## Praktische Anwendungen

* **Website-Optimierung**: Activity Map hilft Ihnen, Ihre Websites zu optimieren, indem leistungsschwache Elemente identifiziert, die Navigation verbessert und das Benutzererlebnis insgesamt verbessert werden. Durch die Analyse von Benutzerinteraktionen können Sie datengesteuerte Entscheidungen treffen, um Benutzerflüsse zu optimieren, Formulare zu vereinfachen oder die Inhaltsplatzierung so anzupassen, dass eine maximale Wirkung erzielt wird.

* **Optimierung der Konversionsrate**: Mit der Visualisierung von Benutzerinteraktionen und Analyse der Clickthrough-Raten spielt Activity Map eine entscheidende Rolle bei den CRO-Bemühungen. Sie können Hindernisse für die Konversion erkennen und mit verschiedenen Design-Varianten experimentieren, um Konversionstrichter, Landingpages und Checkout-Prozesse zu optimieren.

* **A/B-Tests**: Activity Map kann mit A/B-Tests kombiniert werden, um die Auswirkungen von Design- oder Inhaltsänderungen zu messen. Durch den Vergleich von Interaktionsmetriken zwischen verschiedenen Versionen einer Web-Seite können Sie ermitteln, welche Varianten zu höheren Benutzerinteraktionen, Konversionsraten oder Umsatz führen.

